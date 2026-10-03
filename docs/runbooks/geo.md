# GEO and AI visibility

**Route:** `/geo` · [Open Veluro](https://veluro.ai/geo)

**When:** Use for testing brand visibility in AI answers and preparing structured content.

**Prerequisites:** Correct brand, website, competitors and representative buyer prompts.

## Agent procedure

1. Set brand/website/competitors and review the generated buyer prompts.
2. Run the scan and poll its ID to completion.
3. Inspect the tested prompts, returned answers and scoring rather than rely only on a score.
4. Run the site audit; generate llms.txt or FAQ JSON-LD as drafts.
5. Review facts and schema; deploy only through approved site access, then verify served content.

## Success and recovery

Completion proof: The report clearly distinguishes observed answers from predicted future visibility.

GEO settings can save during editing. Files and scores do not guarantee mentions or ranking.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 9 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Input / icon | data-testid=geo-brand-input | INPUT | e.g. Veluro | False |
| Input / icon | data-testid=geo-website-input | INPUT | https://yourbusiness.com | False |
| Input / icon | data-testid=geo-competitor-input | INPUT | Add competitor + Enter | False |
| Generate buyer prompts | data-testid=geo-gen-prompts-btn | BUTTON |  | False |
| Run AI Visibility Scan | data-testid=geo-scan-btn | BUTTON |  | True |
| Input / icon | data-testid=geo-audit-url | INPUT | https://yourbusiness.com | False |
| Audit | data-testid=geo-audit-btn | BUTTON |  | False |
| Generate llms.txt /  / The AI-readable summary file every site should host at /llms.txt | data-testid=geo-llmstxt-btn | BUTTON |  | False |
| Generate FAQ schema (JSON-LD) /  / Paste into your site's <head> so AI engines can quote your answers | data-testid=geo-schema-btn | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| POST | `/geo/audit` | create / edit / configuration; inspect before execution | api-0228 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/geo/config` | read candidate; inspect endpoint side effects | api-0229 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/geo/config` | create / edit / configuration; inspect before execution | api-0230 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/geo/fix` | create / edit / configuration; inspect before execution | api-0231 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/geo/prompts/generate` | generation / analysis; may consume credits or store output | api-0232 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/geo/scan` | generation / analysis; may consume credits or store output | api-0233 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/geo/scans` | read candidate; inspect endpoint side effects | api-0234 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/geo/scans/{parameter_1}` | read candidate; inspect endpoint side effects | api-0235 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/geo/{parameter_1}` | create / edit / configuration; inspect before execution | api-0236 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-02.json` — /geo · 2026-09-08T17:01:25.208Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
