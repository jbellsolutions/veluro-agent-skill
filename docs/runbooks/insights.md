# Creative Insights

**Route:** `/creative-insights` · [Open Veluro](https://veluro.ai/creative-insights)

**When:** Use to analyze actual ad creative performance.

**Prerequisites:** Connected correct Meta account and reliable date-window metrics.

## Agent procedure

1. Connect the intended account and select the date range.
2. Inspect ad-level results and underlying provider metrics.
3. Ask a bounded analytical question tied to the selected ads.
4. Compare suggested tests with the actual winning/losing evidence.
5. Prepare revised assets as drafts; execute budget or live creative changes only within authority.

## Success and recovery

Completion proof: Recommendations can be traced to the actual ads and reporting window.

The current account is gated by absent Meta connection. Fatigue and AI scores do not replace observed results.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 3 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Connect in Settings | Use observed accessible label/placeholder | A |  | — |
| Input / icon | data-testid=ci-chat-input | INPUT | Ask anything about your ad performance… | False |
| Input / icon | data-testid=ci-chat-send | BUTTON |  | True |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/creative-insights/ads?date_preset={parameter_1}` | read candidate; inspect endpoint side effects | api-0144 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/creative-insights/analyze` | generation / analysis; may consume credits or store output | api-0145 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/creative-insights/chat` | generation / analysis; may consume credits or store output | api-0146 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-06.json` — /creative-insights · 2026-09-08T17:04:57.631Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
