# Website chat widgets

**Route:** `/chat-widgets` · [Open Veluro](https://veluro.ai/chat-widgets)

**When:** Use to answer website questions and capture eligible leads.

**Prerequisites:** Approved bot identity, business knowledge, privacy process, embed access and CRM routing.

## Agent procedure

1. Create a widget with name, welcome, color, goal and tone.
2. Supply business/services/FAQ and optional website/files.
3. Inspect knowledge ingestion; test common questions and unsafe/unknown cases in simulation.
4. Review appearance, lead fields and booking destination.
5. Embed only on the approved site, then verify real capture and CRM routing.

## Success and recovery

Completion proof: The actual embedded widget answers accurately and records leads in the correct account.

Simulation may use AI credits. Widget creation, toggle, duplicate and embed are separate actions.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

2 captured screen states; 18 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| New Widget | data-testid=create-widget-btn | BUTTON |  | False |
| Input / icon | data-testid=widget-bot-name | INPUT | e.g. Sales Assistant | False |
| Answer Questions / Qualify Leads / Book Calls / Collect Leads | Use observed accessible label/placeholder | SELECT | ; options: Answer Questions, Qualify Leads, Book Calls, Collect Leads | False |
| Professional | data-testid=create-tone-professional | button |  | False |
| Friendly | data-testid=create-tone-friendly | button |  | False |
| Casual | data-testid=create-tone-casual | button |  | False |
| Witty | data-testid=create-tone-witty | button |  | False |
| Funny & playful | data-testid=create-tone-funny | button |  | False |
| Edgy & bold | data-testid=create-tone-edgy | button |  | False |
| Empathetic | data-testid=create-tone-empathetic | button |  | False |
| Enthusiastic | data-testid=create-tone-enthusiastic | button |  | False |
| Luxury / premium | data-testid=create-tone-luxury | button |  | False |
| Formal | data-testid=create-tone-formal | button |  | False |
| Input / icon | Use observed accessible label/placeholder | TEXTAREA | What does your business do? | False |
| Input / icon | Use observed accessible label/placeholder | TEXTAREA | List your services or products | False |
| Input / icon | Use observed accessible label/placeholder | TEXTAREA | Common questions and answers... | False |
| Input / icon | data-testid=widget-website-url | INPUT | https://yourcompany.com | False |
| Create Widget | data-testid=create-widget-submit | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/widgets` | read candidate; inspect endpoint side effects | api-0650 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/widgets` | create / edit / configuration; inspect before execution | api-0651 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/widgets/{parameter_1}` | delete / remove | api-0652 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/widgets/{parameter_1}` | create / edit / configuration; inspect before execution | api-0653 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/widgets/{parameter_1}/duplicate` | create / edit / configuration; inspect before execution | api-0654 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/widgets/{parameter_1}/embed` | read candidate; inspect endpoint side effects | api-0655 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/widgets/{parameter_1}/knowledge` | read candidate; inspect endpoint side effects | api-0656 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/widgets/{parameter_1}/knowledge/document` | create / edit / configuration; inspect before execution | api-0657 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/widgets/{parameter_1}/knowledge/text` | create / edit / configuration; inspect before execution | api-0658 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/widgets/{parameter_1}/knowledge/website` | create / edit / configuration; inspect before execution | api-0659 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/widgets/{parameter_1}/knowledge/{parameter_2}` | delete / remove | api-0660 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/widgets/{parameter_1}/simulate` | generation / analysis; may consume credits or store output | api-0661 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/widgets/{parameter_1}/toggle` | create / edit / configuration; inspect before execution | api-0662 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-05.json` — /chat-widgets · 2026-09-08T17:04:09.439Z
- `dialogs-01.json` — New Widget · 2026-09-08T17:12:44.535Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
