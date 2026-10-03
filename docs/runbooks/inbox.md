# Replies Inbox

**Route:** `/inbox` · [Open Veluro](https://veluro.ai/inbox)

**When:** Use to triage responses to the client’s campaigns.

**Prerequisites:** Correct client inbox and response authorization.

## Agent procedure

1. Read the relevant replies and originating lead/campaign.
2. Identify intent, requested action, opt-out or delivery issue.
3. Update the lead and stop/suppress further follow-up where appropriate.
4. Prepare a contextual response and send only if the engagement authorizes it.
5. Verify reply/delivery state and record the next step.

## Success and recovery

Completion proof: The reply is handled with accurate context and no conflicting automated follow-up.

Opening a reply may mark it read. Reply generation and sending are different effects.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 1 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Input / icon | data-testid=inbox-refresh | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/inbox/replies` | read candidate; inspect endpoint side effects | api-0254 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/inbox/replies/{parameter_1}/read` | create / edit / configuration; inspect before execution | api-0255 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/inbox/unread-count` | read candidate; inspect endpoint side effects | api-0256 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/leads` | read candidate; inspect endpoint side effects | api-0330 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads` | create / edit / configuration; inspect before execution | api-0331 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/auto-score` | create / edit / configuration; inspect before execution | api-0332 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/bulk-delete` | create / edit / configuration; inspect before execution | api-0333 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/bulk/nurture` | create / edit / configuration; inspect before execution | api-0334 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/import-csv` | create / edit / configuration; inspect before execution | api-0335 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/leads/statuses` | read candidate; inspect endpoint side effects | api-0336 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/statuses` | create / edit / configuration; inspect before execution | api-0337 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/leads/statuses/{parameter_1}` | delete / remove | api-0338 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/leads/statuses/{parameter_1}` | create / edit / configuration; inspect before execution | api-0339 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/leads/{parameter_1}` | read candidate; inspect endpoint side effects | api-0340 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/leads/{parameter_1}` | create / edit / configuration; inspect before execution | api-0341 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/{parameter_1}/coach` | create / edit / configuration; inspect before execution | api-0342 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/{parameter_1}/draft-reply` | generation / analysis; may consume credits or store output | api-0343 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/{parameter_1}/score` | create / edit / configuration; inspect before execution | api-0344 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/{parameter_1}/send-reply` | delivery / publishing / provider or workflow change | api-0345 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/{parameter_1}/send-sms` | delivery / publishing / provider or workflow change | api-0346 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-04.json` — /inbox · 2026-09-08T17:02:42.425Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
