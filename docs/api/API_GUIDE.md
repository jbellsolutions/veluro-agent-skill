# Veluro API operating guide

Evidence date: September 8, 2026. Base URL: `https://veluro.ai/api`.

The authenticated browser application uses an internal JSON API. Login and local campaign draft operations work in this account. No published, versioned developer specification, service-account authentication, official SDK, stable rate limit, webhook contract or API support policy was located. The material below documents observed behavior; it is not a vendor-issued contract. The account's terms and any approved agency/API arrangement still govern production use.

## Choose the right reference

| File | Purpose | Confidence |
|---|---|---|
| [Observed OpenAPI subset](observed-openapi.json) | Machine-readable paths and inferred sample schemas for checked reads, login and campaign drafts | Specific operations observed; schemas are inferred, not exhaustive |
| [Endpoint catalog](ENDPOINT_CATALOG.md) / [JSON](endpoint-catalog.json) | All 662 normalized method/path templates found across 833 browser call sites | Source observed; not 662 tested endpoints |
| [Draft request](draft-example.json) | Complete body captured from the UI's Save & finish later action | Tested local-draft creation shape |
| [Model catalog](MODEL_CATALOG.md) / [JSON](model-catalog.json) | 66 image/video model entries, slugs and displayed credit costs | Catalog GET tested; generation untested |
| [Service catalog](../runbooks/SERVICE_CATALOG.md) / [JSON](service-catalog.json) | Nine industry groups and 43 service presets | Catalog GET tested |
| [Feature runbooks](../runbooks/INDEX.md) | The relevant UI procedure, prerequisites and verification for each API family | Per-operation evidence varies |

The catalog's `{parameter_1}` names represent dynamic expressions in the application. They do not establish the meaning, accepted type or encoding of a parameter. Some entries combine path and query templates; do not add these literally to an OpenAPI server. `request_expression` is a research annotation, not executable JSON. A value such as `e`, `a` or `void 0` means the payload must be resolved from the current UI flow. For GET calls, the expression can be an HTTP-client configuration object (`params`, `responseType`), not a request body. Duplicate expressions were consolidated, so template counts do not imply a count of independent backend capabilities.

## Authentication and identity

1. Sign in at `https://veluro.ai/login` using the authorized account's securely supplied credentials. Partner users enter the partner portal; Back to App opens the client application without another login.
2. The login request observed in the app is `POST /auth/login` with JSON `email` and `password`. The browser stores its session token under `auth_token` and sends `Authorization: Bearer <session token>`. This is a session bearer token, not a separately issued developer API key.
3. Use `GET /auth/me` to verify the user and plan context before doing work. A successful login alone does not establish the correct client's workspace or provider account.
4. Keep credentials and tokens in the execution environment's secret store. Do not write them in prompts, knowledge entries, screenshots, URLs, request logs or this documentation. When using computer use, preserve the authenticated session without exposing storage values.
5. Token expiry, refresh, revoke behavior, service-account support and per-token scopes are unverified. On 401, stop the dependent operation, reauthenticate through the supported flow and verify identity again. Do not repeatedly replay a write after a login redirect.

An isolated browser-context read can use the current token without returning it to the agent:

```javascript
const identity = await page.evaluate(async () => {
  const token = localStorage.getItem("auth_token");
  if (!token) throw new Error("No authenticated Veluro session");
  const response = await fetch("/api/auth/me", {
    headers: { Authorization: `Bearer ${token}` }
  });
  if (!response.ok) throw new Error(`Identity check failed: ${response.status}`);
  const user = await response.json();
  return { user_id: user.user_id, plan_level: user.plan_level };
});
```

That example is an implementation pattern for an authorized browser session. It does not establish vendor support for unattended API access.

## Preflight reads

All paths below use GET and returned HTTP 200 during this review unless stated otherwise. Save the read time and account ID with every operational decision.

| Paths | What the agent should establish |
|---|---|
| `/auth/me`, `/billing/plan` | Account identity, plan entitlement, billing and trial state separately |
| `/credits`, `/usage/quota` | General AI balance, plan caps and legacy feature counters |
| `/omnirogue/usage`, `/sales-coach/usage` | Studio and coaching allowance; do not substitute the general AI balance |
| `/platform/flags` | Current provider/service issue flags |
| `/ads/connections`, `/ads/readiness-summary`, `/ads/stats` | Provider availability, account readiness and campaign/spend totals |
| `/integrations`, `/outreach/connection`, `/outreach/mailboxes` | Actual CRM/sending integrations, mailbox capacity and sender state |
| `/intent/status`, `/intent/provider-status`, `/intent/quota` | Provider state and intent allocation/renewal; `audience_count` alone is not a verified client-owned audience count |
| `/landing/quota` | Existing landing page count and cap |
| `/service-brain/catalog` | Current service presets |
| `/omnirogue/models` | Exact available model variants and costs |
| `/sales-coach/playbooks` | Current selectable coaching playbooks |
| `/health-score`, `/health-insights`, `/health-actions` | Response availability only; this account's values have unresolved provenance and cannot authorize actions |

Two lookup calls were checked: `/intent/topics/search?q=roofing&scope=b2c` and `/intent/city-search?q=Austin`. Topic responses contain separate B2B/B2C arrays and identifiers; `match_score` is not a person's probability of buying. A null person count means unknown. City search returned several cities named Austin in different states; use the complete intended city/state. Encode actual search values with `URLSearchParams`.

`GET /ads/optimizer/settings` returned 405. That proves GET is unsupported there; it does not mean an optimizer is absent. Do not try a different write method merely to see whether it succeeds.

## Tested campaign lifecycle

The checked lifecycle is a local Veluro draft. It did not create an ad in Meta, Google, LinkedIn or TikTok.

| Step | Request | Observed result |
|---|---|---|
| Create through UI | `POST /ads/campaigns` with [draft-example.json](draft-example.json) | 200; returned a `campaign_id`, `status: draft`, zero metrics |
| Read | `GET /ads/campaigns/{campaign_id}` | 200; persisted campaign returned |
| Full-body update | `PUT /ads/campaigns/{campaign_id}` using the create body with a changed name | 200; name persisted, but the `ad_copy` representation changed |
| Minimal update | `PUT /ads/campaigns/{campaign_id}` with only `campaign_name` | Separate test returned 200; existing structured `ad_copy` was preserved |
| Delete own QA draft | `DELETE /ads/campaigns/{campaign_id}` | 200; `message: Campaign deleted` |
| Verify cleanup | GET the deleted ID; GET stats and credits | 404 for deleted draft; total campaigns 0, spend 0, general AI usage 0 |

Both test drafts were removed. Their historic IDs in evidence are not reusable examples. The minimal update test also created its own local draft directly through the API with nonempty test copy before updating and cleaning it up.

### Creation fields

The draft example is deliberately incomplete for live advertising. A permissive draft save does not prove that a provider will accept its values.

| Field | Observed request shape and operating rule |
|---|---|
| `platform` | `meta` in the test; the UI also offers Google, LinkedIn and TikTok. Validate each provider's actual supported workflow. |
| `campaign_name` | String; use a unique client/job name and clearly label test drafts. |
| `campaign_type` | `leads` tested; UI offers traffic, conversions and brand awareness as well. Do not infer provider enums from display labels. |
| `lead_method` | `lead_form` tested; the UI also offers destination URL. |
| `page_id`, `ad_account_id` | Null accepted for a local draft; live work needs verified provider identifiers. |
| `destination_url` | Null accepted for this lead-form draft. Validate the actual landing destination for a website/search campaign even if a wizard marks it optional. |
| `audience` | Object with `mode`, `selected`, `names`, `geo_locations`, `region`; empty values saved in the test. Their presence does not prove targeting or audience activation. |
| `budget_monthly`, `budget_daily` | Numeric 30 and 1 in the test. These were draft settings, not spend. The monthly-to-daily UI conversion should be inspected for every chosen budget. |
| `optimization_rules`, `auto_optimize` | `{auto:false}` and `false` in the test. Keep disabled until the client authorizes explicit limits and the optimization path is validated. |
| `ad_copy` | String in the creation request. Read/update behavior differs; see the warning below. |
| `ad_copy_details` | Object containing `primary_text`, `headline`, `description`, `cta` and plural variation arrays. `LEARN_MORE` was accepted in the draft. |
| `creative_assets`, `creative_urls` | Empty arrays accepted in the test. Finished assets and provider requirements must be checked before launch. |
| `pixel_id`, `nurture_sequence_id` | Null accepted; only attach the intended client's tested conversion/nurture object. |
| `keywords_exact`, `keywords_phrase`, `negative_keywords` | Arrays, empty in the Meta test. Google UI exposes all three match types. No keyword upload/launch was tested. |
| `lead_form` | Nested name, intro, privacy, thank-you fields and questions. `FULL_NAME` and `EMAIL` were stored. Empty privacy content is draft-only. |
| `status` | Explicitly `draft` in both tests. Never use a guessed status value to launch, pause or terminate provider ads. |

### Update behavior that needs special handling

Creation normalized `ad_copy` into an object containing the structured copy. Replaying the complete create request in a PUT changed `ad_copy` back to a string and stored `ad_copy_details` separately. The GET afterward retained that changed representation. A second controlled test established that a name-only PUT preserved the existing copy object and its contents.

For a name-only edit, send only the changed name:

```json
{ "campaign_name": "Approved client campaign name" }
```

Read back the entire campaign and compare the intended fields plus copy, budget, status and account IDs. This tested partial-update behavior applies to the campaign-name case. It does not prove all fields merge safely or that every PUT endpoint accepts partial bodies. Changing copy or nested objects needs a dedicated draft test first; prefer the current UI until that path is verified. Do not take a GET response and blindly submit it as a create or update body.

### Operational request pattern

For each write, save the client/job ID, intended changes, previous values, returned object ID and completion check. Set a timeout; a timeout does not establish that the write failed. Read the existing object before any retry. Server idempotency-key support was not found, so do not invent an `Idempotency-Key` guarantee. Avoid simultaneous edits to the same campaign; version/ETag conflict handling is unverified.

Draft deletion was tested only on the task's own identified drafts. It does not prove that deleting an active Veluro record stops a provider campaign. For live ads, verify an authorized pause at the provider before considering record deletion.

## API families and their operating relationships

| Family | Typical sequence | Evidence boundary |
|---|---|---|
| `/service-brain/*` | Read catalog → create engine → read engine → review/edit blueprint → launch selected components | Catalog read tested; create/launch may consume credits or publish |
| `/ads/*`, `/google-ads/*`, `/linkedin-marketing/*`, TikTok ads | Read readiness → prepare draft → validate targets/copy/creative/tracking → use the correct provider action → read provider status/performance | Local draft tested; provider launch/pause/optimization untested |
| `/intent/*` | Check quota/provider → resolve topics/geography → build audience → inspect records → review drafts → activate the authorized channel → read activation status | Lookups/quota tested; audience build, export and activation untested |
| Landing/funnels/pixels | Prepare site/form/event → preview → validate destination/integration → publish/install → test actual conversion | Entry UI and source observed; deployment and tracking not exercised |
| Leads/CRM/integrations | Read destination and mappings → import controlled authorized records → verify deduplication/sync → bulk operation | Current connection reads tested; import and sync untested |
| `/outreach/*`, nurture, email, replies | Connect sender → verify sender health → prepare list/sequence → review routing/schedule → launch only within scope → inspect delivery/replies/suppression | Sender-state reads tested; downstream UI gated by missing sender |
| `/omnirogue/*`, storyboard, media/editors | Read model/usage → submit one approved job → record job ID → poll existing job → inspect asset → reconcile credits | Catalog/usage reads tested; generation/rendering untested |
| Social | Connect exact profile → create/review post → schedule/publish → inspect provider result | UI/source observed; publishing untested and Meta gated |
| Scheduling/proposals/coaching/widgets | Prepare accurate content/config → verify appropriate destination/recipient → execute scoped action → read resulting object/event | Entry UI observed; consequential actions not performed |
| Health/analytics/reports | Read data → establish provenance and consistent window → calculate/report → review proposed action | Reads tested; current health data fails provenance check |
| Partner/referrals/team/billing | Read relationship/terms → prepare exact authorized change → save → verify attribution/member/billing record | Partner UI observed; no invitation, payout or billing change tested |

Launch, activate, approve, connect, sync, send and publish endpoints are distinct actions with different consequences. A source expression containing `override_readiness` is not authority to bypass readiness checks. Even a GET can initiate an OAuth redirect or export data; inspect purpose as well as HTTP method.

## Asynchronous jobs, pagination, files and webhooks

The UI and source expose long-running generation, engine creation and audience activation states. Exact global job statuses, polling intervals, retry ceilings and retention periods are not established. An agent should record the returned job/object ID, use that feature's observed status route, apply bounded backoff with jitter and stop at its job deadline while preserving the pending ID. “Queued” or an HTTP 200 acceptance response is not proof of a finished video, delivered message or active campaign.

There is no verified universal pagination contract. Use only the current route's observed query parameters and response cursor/page fields; test completeness and deduplication. Do not append guessed `page`, `limit` or `cursor` parameters and assume they worked.

Exports can return blobs rather than JSON; one source-observed example is `/intent/audiences/{id}/export-csv`. Uploads can use multipart data; a minified body variable does not describe the supported file fields. Inspect the current UI request and allowed types/size before implementing uploads. Keep exported contact data within the intended client's storage and retention scope.

Webhook signing, event schemas, retry policy and delivery guarantees were not established. Do not invent a webhook integration. Poll validated read endpoints or use supported UI notifications until a real contract is available.

## Errors and recovery

| Condition | Agent response |
|---|---|
| 401 / login redirect | Stop dependent work; reauthenticate; verify identity and reconcile any in-flight write. |
| 402 / quota message | Preserve draft/job state; check each relevant meter. Do not buy credits or change plans without existing authority. |
| 403 | Inspect account role, provider scope and availability. Do not bypass access restrictions. |
| 404 | Verify route and object/account identity. A deleted QA draft correctly returned 404; `/leads/statuses` also returned 404 and remains a feature gap. |
| 405 | Method unsupported; inspect the actual UI's method and purpose before considering a different request. |
| 409 / validation error | Read the response details and current object; repair the specific issue. Exact error envelopes are not standardized here. |
| 429 | Honor a provided `Retry-After`; back off and reduce concurrency. Published rate limits are unverified. |
| 5xx / timeout | Retry safe reads with bounded backoff. For writes, first find the existing object/job/provider state to avoid duplicate spending or delivery. |
| 200 with unexpected data | Verify schema, identity and provenance; do not treat transport success as business success. |

Some rows above are operator recovery policy, not error codes actually reproduced. The review directly observed transient 5xx, missing/forbidden documentation URLs, the unsupported GET, and the deleted-draft 404. See [verification](../VERIFICATION.md) for exact observed gaps and the [maintenance protocol](../MAINTENANCE.md) for change detection.

## Evidence and production boundary

The evidence files preserve checked responses and controlled draft operations: `api-read-verification.json`, `catalogue-api-reads.json`, `draft-ui-create-test.json`, `draft-api-update-test.json`, `draft-minimal-update-test.json` and `draft-cleanup-test.json`. The generated subset schema intentionally leaves empty-array element types and unseen/null value types open rather than inventing validators.

Before relying on a new write operation, prepare the intended result, establish authorization and prerequisites, perform a small appropriate test, verify its actual effect and update the runbook. Maintain the vendor/API support, multi-client isolation, live delivery and data-provenance items in the central verification register. This documentation supports that work; it does not erase those gaps.
