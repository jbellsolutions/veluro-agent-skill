# Verification and outstanding production checks

Evidence date: September 8, 2026. This register is the source of truth for what was actually demonstrated.

## Completed checks

| Check | Result | Evidence |
|---|---|---|
| Supplied partner credentials | Login succeeded; entered `/partner` | Authenticated UI and `/auth/me` |
| Partner → client portal | Purple Back to App entered `/home`; no second login | Browser navigation |
| Account identity | Partner Growth; referral partner; `demo_account:false` | `evidence/api-read-verification.json` |
| Demo access | Full transcript obtained from the report's own network response | `evidence/demo-transcript.txt`, 67 turns, approximately 7,075 words |
| Built-in help | 53 guide entries opened; 59 guide objects found including duplicates/imported variants | `evidence/help-guides.json`, `guide-source-data.json` |
| Client feature inventory | Sidebar destinations and additional linked routes visited; entry dialogs and tabs inspected | UI batches and dialog captures |
| Internal API reads | Account, limits, connections, intent topic/city lookup, model/service catalogs and health endpoints returned JSON | API read evidence files |
| Local campaign draft | Created through UI; HTTP 200; stored `status:draft`, `auto_optimize:false` | `evidence/draft-ui-create-test.json` |
| API update | GET and PUT succeeded; renamed draft stayed draft; new name confirmed in UI | `evidence/draft-api-update-test.json` |
| Minimal API update | Separate direct-API draft with nonempty copy; name-only PUT preserved structured copy; own draft deleted; counts and spend returned to 0 | `evidence/draft-minimal-update-test.json` |
| Cleanup | DELETE returned 200; subsequent GET returned 404; campaign total and active count returned to 0 | `evidence/draft-cleanup-test.json` |
| Resource impact of draft test | General AI balance stayed 3,500; used count 0; ad spend 0 | Draft cleanup evidence |
| Outbound/publishing boundary | No live ad launch, email/SMS send, social post, signature request, live page deployment or provider-account connection was performed | Executed-operation record |

The initial test draft was deleted; its historic identifier is retained in the private evidence archive. The second minimal-update test's draft was also deleted. Neither historic ID may be used as a production example ID.

## Material conflicts and gates

| ID | Finding | Implication | Resolution needed |
|---|---|---|---|
| V01 | User's proposed second-tier rate was 10%; account and demo distinguish 10% reseller subscription + 5% reseller client revenue | Commission forecasting needs three revenue bases | Use exact account terms; confirm agreement before public promises |
| V02 | Partner Growth quotas differ from public customer Growth pricing/allowances | Partner pricing is not customer pricing | Read the correct plan before quoting or provisioning |
| V03 | AI credits, Studio credits and legacy media counters coexist | One “unlimited” or “credits” figure is insufficient | Meter all applicable resources; validate how media counters interact |
| V04 | Intent credits reset October 1, while general AI/coaching show October 5 | Counters have different cycles | Store each renewal independently |
| V05 | Meta settings banner says final app review is pending | General launch and auto-posting access is gated | Re-check banner and actual account readiness before live delivery |
| V06 | Google verification banner remains; LinkedIn identity and Ads connections have different capabilities | A generic connected badge is not enough | Verify scope, account ID and provider's available operations |
| V07 | Local Listings says Coming Soon in UI and help | It is not a currently operable service here | Keep unavailable until the real workflow works |
| V08 | LinkedIn Compose explicitly never auto-sends | Drafting and reminders are available; automated DM delivery is not proved | Describe the workflow accurately; verify any future sending feature independently |
| V09 | Demo requested alternate SMTP; current UI and source now expose Gmail/Outlook/SMTP | Demo is not the freshest feature inventory | Retain current UI instructions; validate mailbox setup and delivery when authorized |
| V10 | Outreach lists/campaign tabs are disabled until sender setup | Downstream UI was not accessible with current connections | Use source-observed contract as provisional; verify after a client sender is connected |
| V11 | Consumer free trial reportedly lacked intent access; founder agreed to investigate | “All features for seven days” remains unproven for new customer accounts | Validate a properly scoped customer trial before leading with this claim |
| V12 | Health API returns populated financial/performance figures with no connected source and 0 campaigns; `demo_account:false` | Recommendations cannot safely be treated as actual business intelligence | Establish data provenance and reconcile metrics before any autonomous action |
| V13 | Transient 5xx errors and a temporary login redirect occurred; later reads succeeded | Empty/loading screens are not evidence of absent records/features | Use bounded retry and independent read-back; record failures |
| V14 | `/api/leads/statuses` was observed returning 404 during UI load | Custom-status operation is not fully validated | Test in a controlled client workspace before depending on custom pipelines |
| V15 | Common OpenAPI/docs URLs did not provide a schema: `/api/openapi.json` and `/api/docs` 404; root equivalents 403 | No public versioned API contract located | Establish vendor-approved API/automation access, support and change policy |
| V16 | Growth/partner workspace was inspected; multi-client tenancy was not proved | Partner referral visibility is not proof of isolated managed client workspaces | Validate account model, licensing and cross-client isolation before service scale |
| V17 | Demand map request uses location, industries and descriptive audience context | A saved audience selector alone does not prove person-level geographical targeting | Verify actual provider audience IDs, seed contents and targeting before launch |
| V18 | Some guide labels are stale: “New Audience,” old sidebar group names, and guidance to choose 3–6 topics | Built-in help can disagree with the live interface | Prefer current Track Intent UI and its five-topic limit |
| V19 | Model catalog has repeated display names and multiple prices | Name-only model selection can misprice a job | Use model slug + current cost/variant |
| V20 | Studio Pro exposes avatar/audio categories; current model API returned only image/video categories | Visible category labels are not proof that a usable model exists | Check live availability and validate output |
| V21 | Replaying a campaign create payload in PUT changed `ad_copy` from an object to a string and stored `ad_copy_details` separately | A successful rename can also alter the copy representation | Name-only PUT was independently tested and preserved copy; use minimal verified updates and compare the whole read-back |
| V22 | Google wizard's destination checklist can label its URL optional | Draft checklist completion does not establish a valid search-ad destination | Require and verify the intended destination before a website/search launch |

No support message was sent; no approval was requested from another person. These are specific production validation items preserved for the next authorized operating stage, not instructions for the user to do research.

## Required production certification

Run these in the intended client's connected account and within its existing authorization. Use a designated internal recipient or test conversion where sending is authorized. Complete all preparation before seeking any missing final approval.

1. **Provider connections:** establish precise user/ad account/page/property/calendar scopes; verify reconnect and expiry behavior; verify isolation from other clients.
2. **Ads:** create one reviewed paused campaign on each purchased channel; confirm provider object IDs and settings; then test an authorized live campaign with explicit spend ceilings and a stop condition. Verify pause truly stops provider delivery.
3. **Intent:** build a narrowly scoped tracker; verify allocation, returned count, record quality, recency and geographical mapping; export and compare; verify audience activation/matching; verify deletion's next-cycle accounting. Do not assume 100% identity or buyer accuracy.
4. **Pages/funnels:** build, edit and preview; publish on the approved domain; verify mobile layout, actual form submission, CRM fields, booking, tracking and payment if used; verify unpublish and rollback.
5. **Mailboxes/outreach/nurture:** authenticate the intended sender; verify routing and inbound reply handling; test delivery logs, unsubscribe, bounce suppression, reply stop rules, timezones and duplication protection before enrollment.
6. **SMS:** verify the intended Twilio number and outbound authorization, delivery receipts and suppression before a nurture step goes active.
7. **Creative:** generate one approved sample at the selected model/cost, poll it to completion, verify output, credit delta, saved asset and download; test retries without duplicate charges.
8. **Social:** prepare and approve one scheduled post for the intended profile; verify provider publish result; test rescheduling/canceling without duplicates.
9. **CRM/calendar:** validate import and field mapping, deduplication, sync direction, meeting timezone, conflict handling and public reschedule/cancel.
10. **Coaching:** validate live capture, file upload and review within agreed recording permissions; reconcile seat/call/minute accounting.
11. **Reporting/optimization:** reconcile all metrics to actual source events. Only then enable permitted optimization; verify maximum changes and audit trail. Health provenance is a blocking condition for health-driven actions.
12. **Partner:** test attribution using a controlled properly authorized signup, not an invented referral; reconcile settled commission and a real payout when available. Do not create synthetic business purchases to manufacture a payout test.

## Release position

This is a documented operating baseline and a tested local-draft API integration. It is ready to train an agent to navigate, prepare work, recognize prerequisites and verify operations. It is not yet a certification that an unattended agent can deliver every advertised live service. The distinction should remain visible in both the knowledge base and the future service's operating process.
