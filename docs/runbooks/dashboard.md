# Dashboard, analytics and reports

**Route:** `/dashboard` · [Open Veluro](https://veluro.ai/dashboard)

**When:** Use to review actual operations and produce evidence-backed reporting.

**Prerequisites:** Correct data sources, dates, timezone, attribution and currency.

## Agent procedure

1. Choose Overview, Analytics, Command Center or Reports.
2. Read empty/disconnected states explicitly and verify underlying sources.
3. Inspect consistent date windows before comparing metrics.
4. Generate insights/report only when its inputs are understood.
5. Review numbers, forecasts and recommendations; export/share only the verified report.

## Success and recovery

Completion proof: Reported results reconcile to source events and the stated window.

A Live label, chart, generated insight or PDF is not proof of real underlying business activity.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

4 captured screen states; 13 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Overview | data-testid=dashboard-tab-overview | BUTTON |  | False |
| Analytics | data-testid=dashboard-tab-analytics | BUTTON |  | False |
| Command Center | data-testid=dashboard-tab-command-center | BUTTON |  | False |
| Reports | data-testid=dashboard-tab-reports | BUTTON |  | False |
| 7D | data-testid=period-7d | BUTTON |  | False |
| 30D | data-testid=period-30d | BUTTON |  | False |
| 90D | data-testid=period-90d | BUTTON |  | False |
| Generate Report | data-testid=generate-report-btn | BUTTON |  | False |
| Generate Insights | data-testid=generate-insights-btn | BUTTON |  | False |
| Get Today's Briefing | data-testid=copilot-activate-btn | BUTTON |  | False |
| Generate ICP Brief | data-testid=open-icp-brief-btn | BUTTON |  | False |
| Input / icon | data-testid=command-input | text | e.g. Create a social post, optimize my Meta Ads budget... | False |
| Ask Veluro | data-testid=command-submit | submit |  | True |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/analytics/insights` | read candidate; inspect endpoint side effects | api-0070 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/analytics/insights` | generation / analysis; may consume credits or store output | api-0071 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/analytics/performance?period={parameter_1}` | read candidate; inspect endpoint side effects | api-0072 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/analytics/summary` | read candidate; inspect endpoint side effects | api-0073 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/analytics/unified` | read candidate; inspect endpoint side effects | api-0074 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/copilot-briefing` | read candidate; inspect endpoint side effects | api-0143 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/dashboard/charts` | read candidate; inspect endpoint side effects | api-0156 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/dashboard/copilot` | create / edit / configuration; inspect before execution | api-0157 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/dashboard/metrics` | read candidate; inspect endpoint side effects | api-0158 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/icp/auto-discover` | create / edit / configuration; inspect before execution | api-0252 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/icp/brief` | read candidate; inspect endpoint side effects | api-0253 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/reports` | read candidate; inspect endpoint side effects | api-0517 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/reports/generate` | generation / analysis; may consume credits or store output | api-0518 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-08.json` — /dashboard?tab=analytics · 2026-09-08T17:17:59.848Z
- `ui-batch-08.json` — /dashboard?tab=command-center · 2026-09-08T17:18:08.639Z
- `ui-batch-08.json` — /dashboard?tab=reports · 2026-09-08T17:18:10.360Z
- `ui-batch-06.json` — /dashboard · 2026-09-08T17:05:00.935Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
