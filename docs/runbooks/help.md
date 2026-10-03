# Help, guides and support

**Route:** `/help` · [Open Veluro](https://veluro.ai/help)

**When:** Use to learn setup or resolve a discrepancy.

**Prerequisites:** Current live UI and dated evidence.

## Agent procedure

1. Search Help or choose its category.
2. Open the relevant guide and compare labels/limits with the live page.
3. Follow verified current controls rather than stale illustrations.
4. Record any discrepancy in the verification register and continue independent work.
5. Prepare a precise support question with sanitized evidence if needed; do not send without messaging authority.

## Success and recovery

Completion proof: Instructions match the current usable interface and unresolved gaps are explicit.

The built-in guides have some stale labels and topic limits; vendor descriptions are not execution proof.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 14 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Input / icon | data-testid=help-search-input | INPUT | Search guides… e.g. landing pages, commissions, reviews | False |
| Getting Started | data-testid=help-cat-getting-started | BUTTON |  | False |
| Platform Setup | data-testid=help-cat-platform-setup | BUTTON |  | False |
| Acquire Customers | data-testid=help-cat-acquire | BUTTON |  | False |
| Create & Publish | data-testid=help-cat-create | BUTTON |  | False |
| Convert & Nurture | data-testid=help-cat-convert | BUTTON |  | False |
| Operate & Grow | data-testid=help-cat-operate | BUTTON |  | False |
| Partner Program | data-testid=help-cat-partner | BUTTON |  | False |
| Account Setup & Onboarding | data-testid=help-guide-onboarding | BUTTON |  | False |
| Brand Kit (Logo & Colors) | data-testid=help-guide-brand-kit | BUTTON |  | False |
| Dashboard & Home | data-testid=help-guide-dashboard | BUTTON |  | False |
| Business Health Score | data-testid=help-guide-business-health | BUTTON |  | False |
| AI Chat (Your CMO + CFO) | data-testid=help-guide-ai-chat | BUTTON |  | False |
| support@veluro.ai | data-testid=help-support-email | A |  | — |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/integrations/setup-guide/{parameter_1}` | read candidate; inspect endpoint side effects | api-0259 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-01.json` — /help · 2026-09-08T17:00:47.900Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
