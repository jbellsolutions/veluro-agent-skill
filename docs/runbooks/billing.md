# Plans, quotas and billing

**Route:** `/settings?tab=billing` · [Open Veluro](https://veluro.ai/settings?tab=billing)

**When:** Use before batching work or evaluating service capacity.

**Prerequisites:** Read-only account access; separate explicit authority for financial changes.

## Agent procedure

1. Read plan level and billing status separately.
2. Check AI credits, Studio usage, intent quota, active campaigns, landing pages, social pages and coaching caps.
3. Store each reset date; do not combine unlike meters.
4. Estimate planned usage against the relevant allowance and approved spending ceiling.
5. Preserve drafts on exhaustion; use a top-up or plan switch only if authorized.

## Success and recovery

Completion proof: The resource plan fits current entitlements and authorized costs.

Checkout, top-up, cancel, resume and plan-switch operations have financial effects. Partner and customer pricing differ.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 15 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Profile | data-testid=settings-tab-profile | button |  | False |
| Integrations | data-testid=settings-tab-integrations | button |  | False |
| Notifications | data-testid=settings-tab-notifications | button |  | False |
| Billing | data-testid=settings-tab-billing | button |  | False |
| Brand Kit | data-testid=settings-tab-brand-kit | button |  | False |
| 500 /  / $19 | data-testid=llm-pack-pack500 | BUTTON |  | False |
| 1,500 /  / $49 | data-testid=llm-pack-pack1500 | BUTTON |  | False |
| 5,000 /  / $129 | data-testid=llm-pack-pack5000 | BUTTON |  | False |
| 15,000 /  / $299 | data-testid=llm-pack-pack15000 | BUTTON |  | False |
| Switch to Free — $0/mo | data-testid=upgrade-free | BUTTON |  | False |
| Switch to Starter — $297/mo | data-testid=upgrade-starter | BUTTON |  | False |
| Switch to Command — $997/mo | data-testid=upgrade-command | BUTTON |  | False |
| Switch to Scale — $2,497/mo | data-testid=upgrade-scale | BUTTON |  | False |
| Switch to Enterprise — $6,497/mo | data-testid=upgrade-enterprise | BUTTON |  | False |
| Save Changes | data-testid=save-settings-btn | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| POST | `/billing/checkout` | billing / financial change | api-0113 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/billing/plan` | read candidate; inspect endpoint side effects | api-0114 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/billing/status/{parameter_1}` | read candidate; inspect endpoint side effects | api-0115 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/credits` | read candidate; inspect endpoint side effects | api-0147 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/credits/topup` | billing / financial change | api-0148 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/credits/topup/confirm` | billing / financial change | api-0149 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/subscriptions/cancel` | billing / financial change | api-0601 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/subscriptions/portal` | billing / financial change | api-0602 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/subscriptions/resume` | billing / financial change | api-0603 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/usage/quota` | read candidate; inspect endpoint side effects | api-0628 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-07.json` — /settings?tab=billing · 2026-09-08T17:06:47.794Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
