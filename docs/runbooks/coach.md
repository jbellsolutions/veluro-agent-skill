# AI Sales Coach

**Route:** `/sales-coach` · [Open Veluro](https://veluro.ai/sales-coach)

**When:** Use before, during and after authorized sales calls.

**Prerequisites:** Approved playbook, accurate prospect context, available seat/call/minute quota and recording process.

## Agent procedure

1. Select the appropriate playbook and prepare prospect/company/pain/goal/objections.
2. Generate prep and check that advice fits the offer.
3. For Live, arm only when the agreed recording process permits; verify microphone capture.
4. For Review, paste transcript or upload authorized audio and inspect analysis.
5. Review drafted follow-up before any send; reconcile usage and maintain session history.

## Success and recovery

Completion proof: Useful coaching is grounded in the actual call, and usage/session records are verified.

UI exposes 10 analyses / 300 minutes in this plan, plus one seat. Live microphone capture and analysis were not run.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

3 captured screen states; 20 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| SaaS / Software · auto | data-testid=playbook-select | button |  | False |
| 1. Prep | data-testid=tab-prep | button |  | False |
| 2. Live | data-testid=tab-live | button |  | False |
| 3. Review | data-testid=tab-post | button |  | False |
| History | data-testid=tab-history | button |  | False |
| Arm Live Coach | data-testid=start-live-btn | BUTTON |  | True |
| Send to Review | Use observed accessible label/placeholder | BUTTON |  | True |
| Refresh now | Use observed accessible label/placeholder | BUTTON |  | True |
| Input / icon | data-testid=audio-upload-input | file |  | False |
| Upload audio | data-testid=upload-audio-btn | BUTTON |  | False |
| Input / icon | data-testid=post-transcript-input | TEXTAREA | Paste transcript here, or upload an audio file (mp3/m4a/wav, ≤25MB)... | False |
| Analyze Call & Build Follow-Ups | data-testid=run-post-analysis-btn | BUTTON |  | True |
| Input / icon | data-testid=playbook-select | button |  | False |
| Input / icon | data-testid=prep-prospect-name | INPUT | Sarah Chen | False |
| Discovery | Use observed accessible label/placeholder | button |  | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | book demo / close deal | False |
| Input / icon | Use observed accessible label/placeholder | TEXTAREA | Too expensive / We already have a tool | False |
| Generate Pre-Call Strategy | data-testid=generate-prep-btn | BUTTON |  | False |
| Input / icon | data-testid=objection-input | INPUT | "This is too expensive right now" | False |
| Decode | Use observed accessible label/placeholder | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/sales-coach/context` | read candidate; inspect endpoint side effects | api-0523 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/sales-coach/live` | create / edit / configuration; inspect before execution | api-0524 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/sales-coach/objection` | generation / analysis; may consume credits or store output | api-0525 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/sales-coach/playbooks` | read candidate; inspect endpoint side effects | api-0526 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/sales-coach/post-analysis` | generation / analysis; may consume credits or store output | api-0527 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/sales-coach/prep` | generation / analysis; may consume credits or store output | api-0528 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/sales-coach/seats` | read candidate; inspect endpoint side effects | api-0529 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/sales-coach/seats/{parameter_1}` | delete / remove | api-0530 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/sales-coach/sessions` | read candidate; inspect endpoint side effects | api-0531 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/sales-coach/sessions/{parameter_1}` | delete / remove | api-0532 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/sales-coach/sessions/{parameter_1}` | read candidate; inspect endpoint side effects | api-0533 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/sales-coach/transcribe` | create / edit / configuration; inspect before execution | api-0534 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/sales-coach/usage` | read candidate; inspect endpoint side effects | api-0535 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/sales-coach/win-rate-report` | read candidate; inspect endpoint side effects | api-0536 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `dialogs-03.json` — tab-live · 2026-09-08T17:17:30.161Z
- `dialogs-03.json` — tab-post · 2026-09-08T17:17:31.865Z
- `ui-batch-05.json` — /sales-coach · 2026-09-08T17:03:57.905Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
