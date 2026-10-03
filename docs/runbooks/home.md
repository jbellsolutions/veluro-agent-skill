# Home and AI operator

**Route:** `/home` · [Open Veluro](https://veluro.ai/home)

**When:** Use for planning, explaining the account and initiating a clearly scoped task.

**Prerequisites:** Verified client identity and approved business facts.

## Agent procedure

1. Open Home and inspect the current next-action suggestion.
2. Use a new chat for a distinct job or reopen the relevant chat history.
3. Describe the desired output, client, audience, facts, constraints and whether the result should remain a draft.
4. Review the proposed action and any attached assets; distinguish explanation from an executable action.
5. Check resulting objects in their owning module and record their IDs.

## Success and recovery

Completion proof: The requested artifact exists and its actual state matches the request.

Chat and recommendation output is fallible; do not let a chat instruction silently authorize spending or delivery.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 47 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Start a campaign | data-testid=next-action-cta | BUTTON |  | False |
| Copy | data-testid=copy-msg-0 | BUTTON |  | False |
| Listen | data-testid=speak-msg-0 | BUTTON |  | False |
| Turn into an ad | data-testid=quick-action-turn-into-an-ad | BUTTON |  | False |
| Write social posts | data-testid=quick-action-write-social-posts | BUTTON |  | False |
| Find buyers | data-testid=quick-action-find-buyers | BUTTON |  | False |
| Draft a follow-up email | data-testid=quick-action-draft-a-follow-up-email | BUTTON |  | False |
| Input / icon | data-testid=concierge-file-input | file |  | False |
| Input / icon | data-testid=concierge-attach-btn | button |  | False |
| Input / icon | data-testid=concierge-input | INPUT | Reply to Veluro… | False |
| Ask | data-testid=concierge-send | button |  | True |
| Start a new chat | data-testid=concierge-new-chat | BUTTON |  | False |
| Chat history | data-testid=concierge-chat-history-btn | BUTTON |  | False |
| Copy conversation | data-testid=copy-conversation-btn | BUTTON |  | False |
| 🚀 Build my Veluro reseller campaign | data-testid=starter-chat | BUTTON |  | False |
| ⚡Launch my pre-built campaigns | data-testid=starter-launch_prebuilt | BUTTON |  | False |
| Help me reply to an email | data-testid=starter-chat | BUTTON |  | False |
| Find me high-intent buyers | data-testid=starter-chat | BUTTON |  | False |
| Draft a LinkedIn campaign for SaaS founders | data-testid=starter-chat | BUTTON |  | False |
| What is my business health score this week? | data-testid=starter-chat | BUTTON |  | False |
| Write 3 Instagram posts for our launch | data-testid=starter-chat | BUTTON |  | False |
| Set up a follow-up sequence for new leads | data-testid=starter-chat | BUTTON |  | False |
| High-Intent Buyers /  / Find people actively looking for what you sell — right now | data-testid=feature-intent | button |  | False |
| LinkedIn /  / AI ICPs, prospects, campaigns, inbox & outreach copy | data-testid=feature-linkedin | button |  | False |
| Outreach (CSV) /  / Upload a list → AI builds a 3-step email sequence | data-testid=feature-outreach | button |  | False |
| Ad Campaigns /  / Launch Meta / Google / LinkedIn ads from one place | data-testid=feature-ads | button |  | False |
| Funnel Builder /  / Multi-page sales funnels that convert | data-testid=feature-funnels | button |  | False |
| Landing Pages /  / AI-built landing pages with A/B testing | data-testid=feature-landing-pages | button |  | False |
| Website Chatbot /  / Capture leads from your site, 24/7 | data-testid=feature-chat-widgets | button |  | False |
| Social Media /  / Plan, schedule, and analyze posts across channels | data-testid=feature-social | button |  | False |
| Messenger & Nurture /  / Conversations that warm leads into customers | data-testid=feature-messenger-nurture | button |  | False |
| AI Reply Drafter /  / Paste an email → I write the perfect reply for you | data-testid=feature-reply-drafter | button |  | False |
| LinkedIn Compose /  / Paste-ready DMs & InMails (never auto-sent) | data-testid=feature-linkedin?tab=compose | button |  | False |
| Email Triage /  / AI sorts your inbox, drafts replies | data-testid=feature-email | button |  | False |
| Creative Library /  / AI-generated images, videos, and ad creative | data-testid=feature-studio | button |  | False |
| Business Health /  / A single score for your marketing momentum | data-testid=feature-health | button |  | False |
| Command Center /  / All channels in one unified view | data-testid=feature-dashboard?tab=command-center | button |  | False |
| Analytics /  / Deep performance and attribution data | data-testid=feature-dashboard?tab=analytics | button |  | False |
| Competitors /  / Track competitor ads, posts, and offers | data-testid=feature-competitors | button |  | False |
| Demand Map /  / Where the buying signals are coming from | data-testid=feature-demand-map | button |  | False |
| Pixels /  / Track visitors, conversions, retargeting | data-testid=feature-pixels | button |  | False |
| Scheduling /  / Bookings + calendar in one place | data-testid=feature-scheduling | button |  | False |
| Leads CRM /  / Your pipeline, organized | data-testid=feature-leads | button |  | False |
| Campaigns /  / Every active campaign at a glance | data-testid=feature-campaigns | button |  | False |
| Sales Coach /  / AI prep + call coaching | data-testid=feature-sales-coach | button |  | False |
| Reports /  / Auto-generated weekly recaps | data-testid=feature-dashboard?tab=reports | button |  | False |
| Switch to the classic metrics dashboard | Use observed accessible label/placeholder | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| POST | `/ai/chat` | generation / analysis; may consume credits or store output | api-0069 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/briefing/dismiss` | create / edit / configuration; inspect before execution | api-0130 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/briefing/today` | read candidate; inspect endpoint side effects | api-0131 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/next-action` | read candidate; inspect endpoint side effects | api-0397 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/veluro-chat/attach` | generation / analysis; may consume credits or store output | api-0629 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/veluro-chat/capture-email` | generation / analysis; may consume credits or store output | api-0630 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/veluro-chat/claim-session` | generation / analysis; may consume credits or store output | api-0631 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/veluro-chat/memory` | account / access / configuration change | api-0632 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/veluro-chat/memory` | read candidate; inspect endpoint side effects | api-0633 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/veluro-chat/memory` | account / access / configuration change | api-0634 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/veluro-chat/my-sessions` | read candidate; inspect endpoint side effects | api-0635 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/veluro-chat/practice` | generation / analysis; may consume credits or store output | api-0636 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/veluro-chat/proactive` | read candidate; inspect endpoint side effects | api-0637 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/veluro-chat/session/{parameter_1}` | delete / remove | api-0638 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/veluro-chat/session/{parameter_1}` | read candidate; inspect endpoint side effects | api-0639 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/veluro-chat/welcome` | read candidate; inspect endpoint side effects | api-0640 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `home.json` — /home · 2026-09-08T17:38:23.075Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
