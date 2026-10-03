# Email Triage and connected inbox

**Route:** `/email` · [Open Veluro](https://veluro.ai/email)

**When:** Use for authorized inbox management and reply preparation.

**Prerequisites:** The intended email account is connected and in scope.

## Agent procedure

1. Connect the specific mailbox through the supported account flow.
2. Inspect only the requested folders/messages.
3. Run triage when authorized and review classifications and proposed drafts.
4. Approve or send the correct response within engagement scope.
5. Verify message state; distinguish star, archive, delete and send actions.

## Success and recovery

Completion proof: The intended email is handled and its resulting state is checked.

The inspected account had no email connection. This is separate from cold outreach sender setup.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 1 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Connect Email | data-testid=connect-email-btn | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/email/accounts` | read candidate; inspect endpoint side effects | api-0167 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/email/accounts/connect` | account / access / configuration change | api-0168 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/email/accounts/{parameter_1}` | delete / remove | api-0169 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/email/ai-draft` | generation / analysis; may consume credits or store output | api-0170 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/email/compose` | create / edit / configuration; inspect before execution | api-0171 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/email/inbox?folder={parameter_1}` | read candidate; inspect endpoint side effects | api-0172 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/email/resend` | delete / remove | api-0173 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/email/resend` | read candidate; inspect endpoint side effects | api-0174 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/email/resend/connect` | account / access / configuration change | api-0175 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/email/stats` | read candidate; inspect endpoint side effects | api-0176 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/email/triage` | create / edit / configuration; inspect before execution | api-0177 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/email/{parameter_1}` | delete / remove | api-0178 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/email/{parameter_1}` | read candidate; inspect endpoint side effects | api-0179 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/email/{parameter_1}/star` | create / edit / configuration; inspect before execution | api-0180 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-07.json` — /email · 2026-09-08T17:06:52.449Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
