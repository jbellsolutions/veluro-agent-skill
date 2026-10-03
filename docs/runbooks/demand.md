# Demand Map and surge alerts

**Route:** `/demand-map` · [Open Veluro](https://veluro.ai/demand-map)

**When:** Use for market research and geographically focused campaign planning.

**Prerequisites:** Approved operating geography, service categories and an interpretable source of demand.

## Agent procedure

1. Enter a specific city/state/region; remove irrelevant default categories.
2. Optionally select the intended saved audience.
3. Generate the map once and inspect location, segments, estimated volumes and assumptions.
4. Drill into a hotspot before creating a campaign; verify target geography in the campaign itself.
5. Enable email surge alerts only under the client’s notification preference.

## Success and recovery

Completion proof: Map interpretation and resulting campaign geography are reviewed and recorded.

Estimated demand is not a census. The source request supplies descriptive audience context; exact person-level targeting is unverified.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 10 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Input / icon | data-testid=map-location | INPUT | e.g., Texas — or Dallas, TX | False |
| No audience — analyze the whole market | data-testid=map-audience-select | SELECT | ; options: No audience — analyze the whole market | False |
| Input / icon | data-testid=map-add-industry | INPUT | Add a product / service / industry | False |
| + Add | data-testid=map-add-industry-btn | BUTTON |  | False |
| + Home Services | data-testid=suggest-ind-home-services | BUTTON |  | False |
| + Education | data-testid=suggest-ind-education | BUTTON |  | False |
| + Fitness / Wellness | data-testid=suggest-ind-fitness-wellness | BUTTON |  | False |
| Generate Demand Map | data-testid=generate-map-btn | BUTTON |  | False |
| Input / icon | data-testid=alert-location-input | INPUT | Your market, e.g. Dallas, Texas | False |
| Input / icon | data-testid=alert-toggle | button |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/demand-alerts` | read candidate; inspect endpoint side effects | api-0160 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/demand-alerts` | create / edit / configuration; inspect before execution | api-0161 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/demand-map/drilldown` | create / edit / configuration; inspect before execution | api-0162 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/demand-map/generate` | generation / analysis; may consume credits or store output | api-0163 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-02.json` — /demand-map · 2026-09-08T17:01:21.069Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
