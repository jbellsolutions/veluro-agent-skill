# Veluro Intelligence and business knowledge

**Route:** `/teach-veluro` · [Open Veluro](https://veluro.ai/teach-veluro)

**When:** Use to prepare or update the AI knowledge used across features.

**Prerequisites:** Approved business references and correct isolated account.

## Agent procedure

1. Add the main website and specific useful pages.
2. Upload appropriate supported files within the 30 MB UI limit.
3. Add structured notes using company, competitor, persona, FAQ, pricing or goal categories.
4. Inspect knowledge entries and resolve conflicting facts or stale offers.
5. Ask a bounded factual question and compare the answer with the reference before depending on it.

## Success and recovery

Completion proof: Knowledge entries exist and output accurately reflects the approved source.

Do not upload passwords, unrelated personal information or another client’s knowledge. Removing an entry changes future AI context.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 13 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Input / icon | data-testid=teach-website-input | INPUT | yourbusiness.com | False |
| Add website | data-testid=teach-website-btn | BUTTON |  | False |
| Input / icon | data-testid=teach-file-input | file |  | False |
| Click to upload | data-testid=teach-upload-btn | BUTTON |  | False |
| Company note | Use observed accessible label/placeholder | BUTTON |  | False |
| Competitor | Use observed accessible label/placeholder | BUTTON |  | False |
| Customer persona | Use observed accessible label/placeholder | BUTTON |  | False |
| FAQ | Use observed accessible label/placeholder | BUTTON |  | False |
| Pricing | Use observed accessible label/placeholder | BUTTON |  | False |
| Goal | Use observed accessible label/placeholder | BUTTON |  | False |
| Input / icon | data-testid=teach-note-title | INPUT | Title (optional) | False |
| Input / icon | data-testid=teach-note-text | TEXTAREA | e.g. "Our main competitor is Acme Corp — they undercut on price but have slow support" | False |
| Teach Veluro | data-testid=teach-note-save | BUTTON |  | True |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/intelligence/knowledge` | read candidate; inspect endpoint side effects | api-0261 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intelligence/knowledge/note` | create / edit / configuration; inspect before execution | api-0262 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intelligence/knowledge/upload` | create / edit / configuration; inspect before execution | api-0263 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intelligence/knowledge/website` | create / edit / configuration; inspect before execution | api-0264 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/intelligence/knowledge/{parameter_1}` | delete / remove | api-0265 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/intelligence/score` | read candidate; inspect endpoint side effects | api-0266 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-01.json` — /teach-veluro · 2026-09-08T17:00:49.424Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
