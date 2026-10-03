# SEO audit and rank tracking

**Route:** `/seo` · [Open Veluro](https://veluro.ai/seo)

**When:** Use to diagnose site issues and track approved keywords.

**Prerequisites:** Correct website, site editing authority and relevant keywords/competitors.

## Agent procedure

1. Run a site audit against the intended URL.
2. Inspect findings and proposed fixes; verify issues on the actual pages.
3. Set keywords, competitor and scan preferences deliberately.
4. Apply approved changes in the website system and rerun relevant checks.
5. Compare rank history using the same terms, location and time window.

## Success and recovery

Completion proof: Actual site changes and tracked observations support the reported improvement.

An audit score or generated fix is not proof of ranking improvement. Repeated scans may consume resources.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 4 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Site Audit & Rankings | data-testid=seo-tab-audit | BUTTON |  | False |
| Blog Engine | data-testid=seo-tab-blog | BUTTON |  | False |
| Input / icon | data-testid=seo-url-input | INPUT | https://yourwebsite.com | False |
| Run SEO audit | data-testid=seo-run-audit-btn | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| POST | `/seo/audit` | create / edit / configuration; inspect before execution | api-0537 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/seo/competitor` | create / edit / configuration; inspect before execution | api-0538 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/seo/keywords` | create / edit / configuration; inspect before execution | api-0539 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/seo/latest` | read candidate; inspect endpoint side effects | api-0540 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/seo/ranks` | read candidate; inspect endpoint side effects | api-0541 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/seo/ranks/check` | create / edit / configuration; inspect before execution | api-0542 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/seo/ranks/history` | read candidate; inspect endpoint side effects | api-0543 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/seo/settings` | create / edit / configuration; inspect before execution | api-0544 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-02.json` — /seo · 2026-09-08T17:01:23.152Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
