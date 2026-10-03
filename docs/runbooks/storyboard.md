# Storyboard Video Builder

**Route:** `/studio/storyboard` · [Open Veluro](https://veluro.ai/studio/storyboard)

**When:** Use for a multi-scene video assembled from a script.

**Prerequisites:** Approved script, duration, aspect ratio, scene plan and credit ceiling.

## Agent procedure

1. Supply the script/brief and select 15/30/45/60 seconds and ratio.
2. Build the storyboard; preserve project and scene IDs.
3. Review script and each scene before generation.
4. Generate required clips, poll their existing IDs and check each result.
5. Stitch only complete approved clips; inspect final video/audio and library output.

## Success and recovery

Completion proof: The final stitched video matches the approved scene order and technical specification.

Generating scenes and stitching are distinct jobs; partial completion must not trigger duplicate generation.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 6 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Input / icon | data-testid=storyboard-brief | TEXTAREA | Describe your video or paste a script… / e.g. "A 45-second ad for my mobile detailing business: hook on a dirty car, show the transformation, happy customer, end with a booking CTA" | False |
| 15 seconds / 30 seconds / 45 seconds / 60 seconds | data-testid=storyboard-duration | SELECT | ; options: 15 seconds, 30 seconds, 45 seconds, 60 seconds | False |
| 9:16 Reels | data-testid=storyboard-aspect-9-16 | BUTTON |  | False |
| 16:9 Wide | data-testid=storyboard-aspect-16-9 | BUTTON |  | False |
| 1:1 Square | data-testid=storyboard-aspect-1-1 | BUTTON |  | False |
| Build my storyboard | data-testid=storyboard-create-btn | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/storyboard/projects` | read candidate; inspect endpoint side effects | api-0579 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/storyboard/projects` | create / edit / configuration; inspect before execution | api-0580 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/storyboard/projects/{parameter_1}` | read candidate; inspect endpoint side effects | api-0581 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/storyboard/projects/{parameter_1}` | create / edit / configuration; inspect before execution | api-0582 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/storyboard/projects/{parameter_1}/generate{parameter_2}` | generation / analysis; may consume credits or store output | api-0583 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/storyboard/projects/{parameter_1}/recommendations` | create / edit / configuration; inspect before execution | api-0584 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/storyboard/projects/{parameter_1}/stitch` | create / edit / configuration; inspect before execution | api-0585 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-08.json` — /studio/storyboard · 2026-09-08T17:17:58.296Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
