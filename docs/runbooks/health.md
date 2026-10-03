# Business Health and reputation

**Route:** `/health` · [Open Veluro](https://veluro.ai/health)

**When:** Use only after verifying the origins of the business and financial data.

**Prerequisites:** Reconciled source metrics; approved action scope.

## Agent procedure

1. Inspect health components and their underlying details.
2. Check connected sources and reconcile revenue, spend, conversion, retention and reputation against them.
3. Flag unexplained/sample figures and exclude them from client decisions.
4. Review any recommendation with its actual evidence and expected effect.
5. Execute an action only after provenance and authorization are established; read back actual outcomes.

## Success and recovery

Completion proof: Scores and proposed actions have demonstrated data lineage.

Current account has a material provenance conflict. Do not use its populated metrics to trigger spending, financial actions or messaging.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

3 captured screen states; 0 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|

No usable field snapshot was retained for this route; use the live UI and the related verified guide before acting.

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/health-actions` | read candidate; inspect endpoint side effects | api-0248 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/health-actions/{parameter_1}/{parameter_2}` | create / edit / configuration; inspect before execution | api-0249 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/health-insights` | read candidate; inspect endpoint side effects | api-0250 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/health-score` | read candidate; inspect endpoint side effects | api-0251 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/reputation` | read candidate; inspect endpoint side effects | api-0519 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/reputation/manual` | create / edit / configuration; inspect before execution | api-0520 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/reputation/platform/{parameter_1}` | delete / remove | api-0521 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/reputation/scan` | generation / analysis; may consume credits or store output | api-0522 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-08.json` — /health · 2026-09-08T17:18:19.861Z
- `ui-batch-07.json` — /health · 2026-09-08T17:06:54.376Z
- `ui-batch-06.json` — /health · 2026-09-08T17:05:10.063Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
