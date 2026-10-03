# AI Reply Drafter

**Route:** `/reply-drafter` · [Open Veluro](https://veluro.ai/reply-drafter)

**When:** Use to prepare a response from provided email text.

**Prerequisites:** Relevant email, accurate business context and desired outcome.

## Agent procedure

1. Paste the email into the drafter.
2. Choose the intended outcome and provide needed context.
3. Generate, review and refine for factual accuracy and tone.
4. Copy the result into the authorized sending surface or preserve as a draft.
5. Check history only within the correct client account.

## Success and recovery

Completion proof: A usable reviewed draft is produced; delivery is claimed only if separately verified.

Do not treat reassuring privacy copy in the UI as a verified server retention guarantee.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 3 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| History (0) | data-testid=toggle-history | BUTTON |  | False |
| Input / icon | data-testid=email-input | TEXTAREA | Paste the email you received here… Include the subject line if you can — I'll write the perfect reply based on what they're asking. | False |
| Help me reply | data-testid=analyze-btn | BUTTON |  | True |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| POST | `/reply-drafter/analyze` | generation / analysis; may consume credits or store output | api-0513 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/reply-drafter/draft` | generation / analysis; may consume credits or store output | api-0514 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/reply-drafter/history` | read candidate; inspect endpoint side effects | api-0515 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/reply-drafter/refine` | generation / analysis; may consume credits or store output | api-0516 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-04.json` — /reply-drafter · 2026-09-08T17:03:25.884Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
