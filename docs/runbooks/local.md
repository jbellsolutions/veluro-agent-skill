# Local Listings

**Route:** `/local-listings` · [Open Veluro](https://veluro.ai/local-listings)

**When:** Use to check availability of the planned Google Business Profile feature.

**Prerequisites:** Current feature availability.

## Agent procedure

1. Open Local Listings and inspect its state.
2. If it still says Coming Soon, record unavailable and continue other work.
3. When released, verify actual GBP connection, location selection and approved edit/review-reply workflows before use.

## Success and recovery

Completion proof: Availability is reported accurately.

Coming Soon in the inspected account. Do not claim listing management or review response works here.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 0 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|

No usable field snapshot was retained for this route; use the live UI and the related verified guide before acting.

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/gbp/accounts` | read candidate; inspect endpoint side effects | api-0225 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/gbp/locations` | read candidate; inspect endpoint side effects | api-0226 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/gbp/status` | read candidate; inspect endpoint side effects | api-0227 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-02.json` — /local-listings · 2026-09-08T17:01:27.280Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
