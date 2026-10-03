# LinkedIn prospecting, Compose and queue

**Route:** `/linkedin` · [Open Veluro](https://veluro.ai/linkedin)

**When:** Use for B2B prospect records, manually sent copy and reminder sequences.

**Prerequisites:** Approved prospect context and intended LinkedIn workflow.

## Agent procedure

1. Add the prospect with accurate name/company/profile.
2. Choose Compose and provide role, industry, hook and relevant context.
3. Generate connection request, InMail, follow-up or reply copy.
4. Review and preserve copy; the built-in Compose feature does not send it.
5. Save a sequence to the Outreach Queue when appropriate; mark sent only after actual authorized sending elsewhere.

## Success and recovery

Completion proof: Prospect records, copy and reminders reflect actual work and message history.

Marketing API connection, identity login and Compose are different capabilities. Do not automate DM delivery by inference.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

4 captured screen states; 24 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Prospects | data-testid=li-tab-prospects | BUTTON |  | False |
| Campaigns | data-testid=li-tab-campaigns | BUTTON |  | False |
| Inbox | data-testid=li-tab-inbox | BUTTON |  | False |
| Compose | data-testid=li-tab-compose | BUTTON |  | False |
| Outreach Queue | data-testid=li-tab-queue | BUTTON |  | False |
| Pull a high-intent buyer | data-testid=buyer-picker-open | button |  | False |
| Input / icon | data-testid=li-msg-name | INPUT | Sarah Chen | False |
| Input / icon | data-testid=li-msg-title | INPUT | VP of Marketing | False |
| Input / icon | data-testid=li-msg-company | INPUT | Acme SaaS | False |
| Input / icon | data-testid=li-msg-industry | INPUT | B2B SaaS | False |
| Input / icon | data-testid=li-msg-url | INPUT | https://linkedin.com/in/... | False |
| Input / icon | data-testid=li-msg-intent | INPUT | Marketing automation tools | False |
| Connection request /  / Get accepted, build relationship. /  / Generate | data-testid=li-msg-quickstart-connection_request | BUTTON |  | True |
| Cold InMail /  / Value-first first touch. /  / Generate | data-testid=li-msg-quickstart-cold_inmail | BUTTON |  | True |
| Follow-up sequence /  / 4-step cadence over 14 days. /  / Generate | data-testid=li-msg-quickstart-follow_up_sequence | BUTTON |  | True |
| Reply handler /  / Best next move when they respond. /  / Generate | data-testid=li-msg-quickstart-reply_handler | BUTTON |  | True |
| Refresh | Use observed accessible label/placeholder | BUTTON |  | False |
| Add Prospect | data-testid=add-prospect-btn | BUTTON |  | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | John Smith | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | VP of Marketing | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | Acme Corp | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | SaaS | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | https://linkedin.com/in/... | False |
| Add Prospect | Use observed accessible label/placeholder | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| POST | `/linkedin-marketing/launch-campaign` | delivery / publishing / provider or workflow change | api-0347 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/linkedin-marketing/push-audience` | create / edit / configuration; inspect before execution | api-0348 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/linkedin-messaging/save-sequence` | create / edit / configuration; inspect before execution | api-0349 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/linkedin-messaging/tasks/{parameter_1}/mark-sent` | delivery / publishing / provider or workflow change | api-0350 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/linkedin-messaging/tasks/{parameter_1}/skip` | create / edit / configuration; inspect before execution | api-0351 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/linkedin-messaging/tasks?status=pending&limit=50` | read candidate; inspect endpoint side effects | api-0352 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/linkedin/campaigns` | read candidate; inspect endpoint side effects | api-0353 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/linkedin/campaigns/{parameter_1}` | delete / remove | api-0354 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/linkedin/inbox` | read candidate; inspect endpoint side effects | api-0355 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/linkedin/posting/posts` | read candidate; inspect endpoint side effects | api-0356 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/linkedin/posting/publish` | delivery / publishing / provider or workflow change | api-0357 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/linkedin/posting/status` | read candidate; inspect endpoint side effects | api-0358 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/linkedin/prospects` | read candidate; inspect endpoint side effects | api-0359 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/linkedin/prospects` | create / edit / configuration; inspect before execution | api-0360 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/linkedin/prospects/{parameter_1}` | delete / remove | api-0361 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/linkedin/stats` | read candidate; inspect endpoint side effects | api-0362 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `dialogs-03.json` — li-tab-compose · 2026-09-08T17:17:33.719Z
- `dialogs-03.json` — li-tab-queue · 2026-09-08T17:17:35.390Z
- `dialogs-03.json` — add-prospect-btn · 2026-09-08T17:17:37.245Z
- `ui-batch-04.json` — /linkedin · 2026-09-08T17:03:02.887Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
