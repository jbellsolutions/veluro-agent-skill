# Competitor Tracking

**Route:** `/competitors` · [Open Veluro](https://veluro.ai/competitors)

**When:** Use to track relevant public competitor activity and inform approved tests.

**Prerequisites:** Correct competitors, official sites and a defined comparison question.

## Agent procedure

1. Add a competitor or review AI suggestions.
2. Verify company name and website before saving.
3. Run analysis and inspect cited/current evidence.
4. Separate observation from inference and unsupported positioning claims.
5. Use findings to prepare an approved test and record source date.

## Success and recovery

Completion proof: Competitive claims are supported by the right company/source and date.

Analysis can be incomplete or stale. Do not copy unsupported statistics into outreach.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

2 captured screen states; 7 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Find my competitors | data-testid=find-competitors-btn | BUTTON |  | False |
| Add Competitor | data-testid=add-competitor-btn | BUTTON |  | False |
| Run Analysis | data-testid=run-analysis-btn | BUTTON |  | True |
| Input / icon | data-testid=competitor-name-input | INPUT | e.g. Acme Corp | False |
| Input / icon | data-testid=competitor-website-input | INPUT | https://acmecorp.com | False |
| Input / icon | data-testid=competitor-notes-input | TEXTAREA | Key things to monitor... | False |
| Add Competitor | data-testid=submit-competitor-btn | submit |  | True |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/competitors` | read candidate; inspect endpoint side effects | api-0137 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/competitors` | create / edit / configuration; inspect before execution | api-0138 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/competitors/analyze` | generation / analysis; may consume credits or store output | api-0139 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/competitors/find` | create / edit / configuration; inspect before execution | api-0140 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/competitors/reports` | read candidate; inspect endpoint side effects | api-0141 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/competitors/{parameter_1}` | delete / remove | api-0142 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-06.json` — /competitors · 2026-09-08T17:05:12.079Z
- `dialogs-01.json` — Add Competitor · 2026-09-08T17:13:10.458Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
