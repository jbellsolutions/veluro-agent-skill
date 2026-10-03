# Creative Library and asset editing

**Route:** `/studio` · [Open Veluro](https://veluro.ai/studio)

**When:** Use to organize, upload, reuse and edit approved assets.

**Prerequisites:** Correct client assets, rights and intended output.

## Agent procedure

1. Filter Social, Ads, AI Creatives or Media Library.
2. Import image/video only when needed; record asset IDs and folder.
3. Open the appropriate image/video editor and preserve an original.
4. Apply approved edits, resizing, background removal or video changes; poll render jobs.
5. Inspect exported media and use the correct asset ID in campaigns/posts.

## Success and recovery

Completion proof: The intended asset and edited/exported version are identifiable and usable.

Delete, AI edit, folder assignment and launch-as-ads have different effects. Do not infer that a thumbnail is a finished render.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 11 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Creative Studio | data-testid=library-goto-studio | A |  | — |
| All | data-testid=filter-all | BUTTON |  | False |
| Social | data-testid=filter-social | BUTTON |  | False |
| Ads | data-testid=filter-ad | BUTTON |  | False |
| AI Creatives | data-testid=studio-tab-ai | BUTTON |  | False |
| Media Library | data-testid=studio-tab-library | BUTTON |  | False |
| Video Editor | data-testid=studio-tab-video-editor | BUTTON |  | False |
| Import image | data-testid=import-image-btn | BUTTON |  | False |
| Import video | data-testid=import-video-btn | BUTTON |  | False |
| All | data-testid=folder-chip-all | BUTTON |  | False |
| New folder | data-testid=folder-new-btn | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/folders` | read candidate; inspect endpoint side effects | api-0188 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/folders` | create / edit / configuration; inspect before execution | api-0189 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/folders/assign` | create / edit / configuration; inspect before execution | api-0190 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/folders/suggest` | generation / analysis; may consume credits or store output | api-0191 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/folders/{parameter_1}` | delete / remove | api-0192 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/folders/{parameter_1}` | create / edit / configuration; inspect before execution | api-0193 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/media/assets/{parameter_1}` | delete / remove | api-0363 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/media/assets/{parameter_1}` | read candidate; inspect endpoint side effects | api-0364 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/media/assets/{parameter_1}/ai-edit` | generation / analysis; may consume credits or store output | api-0365 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/media/assets/{parameter_1}/edit-video` | create / edit / configuration; inspect before execution | api-0366 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/media/assets/{parameter_1}/remove-background` | create / edit / configuration; inspect before execution | api-0367 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/media/assets/{parameter_1}/resize-pack` | create / edit / configuration; inspect before execution | api-0368 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/media/assets?kind={parameter_1}` | read candidate; inspect endpoint side effects | api-0369 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/media/slideshow` | create / edit / configuration; inspect before execution | api-0370 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/media/upload` | create / edit / configuration; inspect before execution | api-0371 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/media/video-edit-status/{parameter_1}` | read candidate; inspect endpoint side effects | api-0372 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/studio-wizard/plan` | create / edit / configuration; inspect before execution | api-0586 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/studio-wizard/script` | create / edit / configuration; inspect before execution | api-0587 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/studio-wizard/stitch` | create / edit / configuration; inspect before execution | api-0588 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/studio-wizard/stitches` | read candidate; inspect endpoint side effects | api-0589 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/studio/creatives` | read candidate; inspect endpoint side effects | api-0590 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/studio/creatives/from-media` | create / edit / configuration; inspect before execution | api-0591 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/studio/creatives/launch-as-ads` | delivery / publishing / provider or workflow change | api-0592 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/studio/creatives/{parameter_1}` | delete / remove | api-0593 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/studio/creatives/{parameter_1}` | create / edit / configuration; inspect before execution | api-0594 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/studio/creatives/{parameter_1}/render-image` | generation / analysis; may consume credits or store output | api-0595 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/studio/creatives/{parameter_1}/render-video` | generation / analysis; may consume credits or store output | api-0596 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/studio/from-script` | create / edit / configuration; inspect before execution | api-0597 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/studio/prompt-assist` | create / edit / configuration; inspect before execution | api-0598 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/studio/render-pending` | generation / analysis; may consume credits or store output | api-0599 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/studio/video-status/{parameter_1}` | read candidate; inspect endpoint side effects | api-0600 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/video-editor/music` | read candidate; inspect endpoint side effects | api-0641 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/video-editor/projects` | read candidate; inspect endpoint side effects | api-0642 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/video-editor/projects` | create / edit / configuration; inspect before execution | api-0643 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/video-editor/projects/{parameter_1}` | delete / remove | api-0644 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/video-editor/projects/{parameter_1}` | read candidate; inspect endpoint side effects | api-0645 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/video-editor/projects/{parameter_1}` | create / edit / configuration; inspect before execution | api-0646 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/video-editor/projects/{parameter_1}/render` | generation / analysis; may consume credits or store output | api-0647 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/video-editor/projects/{parameter_1}/status` | read candidate; inspect endpoint side effects | api-0648 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-05.json` — /studio · 2026-09-08T17:04:27.756Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
