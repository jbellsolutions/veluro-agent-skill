# SEO Blog Engine

**Route:** `/blog` · [Open Veluro](https://veluro.ai/blog)

**When:** Use for source-backed organic content and an approved business blog.

**Prerequisites:** Approved topic, sources, brand voice and publishing destination.

## Agent procedure

1. Choose a primary topic/keyword or request topic suggestions.
2. Generate one article and record the post ID.
3. Review claims, links, metadata, FAQ schema and quotations; edit to match client evidence.
4. Preview and publish only the approved version to the intended blog.
5. Verify served URL and content; use unpublish when an authorized rollback is needed.

## Success and recovery

Completion proof: The published article is accurate, correctly branded and reachable at the expected URL.

AI readiness and SEO scores are heuristics. Publishing and unpublishing are external actions.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 7 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| veluro.ai/b/justin | data-testid=public-blog-link | A |  | — |
| Generate | data-testid=blog-tab-generate | BUTTON |  | False |
| Library (0) | data-testid=blog-tab-library | BUTTON |  | False |
| Input / icon | data-testid=blog-keyword-input | INPUT | e.g. best CRM for roofing contractors | False |
| Generate SEO article | data-testid=blog-generate-btn | BUTTON |  | False |
| Input / icon | data-testid=blog-topic-input | INPUT | optional seed e.g. lead generation | False |
| Suggest | data-testid=blog-ideas-btn | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| POST | `/blog/generate` | generation / analysis; may consume credits or store output | api-0116 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/blog/ideas` | create / edit / configuration; inspect before execution | api-0117 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/blog/posts` | read candidate; inspect endpoint side effects | api-0118 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/blog/posts/{parameter_1}` | delete / remove | api-0119 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/blog/posts/{parameter_1}` | read candidate; inspect endpoint side effects | api-0120 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/blog/posts/{parameter_1}` | create / edit / configuration; inspect before execution | api-0121 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/blog/posts/{parameter_1}/publish` | delivery / publishing / provider or workflow change | api-0122 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/blog/posts/{parameter_1}/rescore` | create / edit / configuration; inspect before execution | api-0123 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/blog/posts/{parameter_1}/unpublish` | delivery / publishing / provider or workflow change | api-0124 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/blog/settings` | read candidate; inspect endpoint side effects | api-0125 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-07.json` — /blog · 2026-09-08T17:06:50.926Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
