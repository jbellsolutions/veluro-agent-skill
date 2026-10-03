# CSV email campaigns and sender setup

**Route:** `/outreach` · [Open Veluro](https://veluro.ai/outreach)

**When:** Use for approved list-based email programs.

**Prerequisites:** Authorized list, verified sender setup, suppression, send window and provider cost allowance.

## Agent procedure

1. Configure the intended mailbox or Resend sender and verify connection/route.
2. Import the CSV and validate list count/mapping and suppression.
3. Create campaign with purpose, value proposition, tone, sequence length and CTA.
4. Inspect all messages and sender routing; set launch timing deliberately.
5. Launch only within approved audience/sending scope; monitor delivery, replies, bounces and opt-outs.
6. Pause and reconcile before retrying any ambiguous send operation.

## Success and recovery

Completion proof: Correct recipients receive the intended messages and suppression/reply behavior is verified.

Current Lists/Campaigns tabs were gated by absent senders. Source exposes mailbox warmup and test-send actions, which can send real messages.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 10 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Setup | data-testid=outreach-tab-setup | BUTTON |  | False |
| Lists | data-testid=outreach-tab-lists | BUTTON |  | True |
| Campaigns | data-testid=outreach-tab-campaigns | BUTTON |  | True |
| Replies | data-testid=outreach-tab-inbox | BUTTON |  | True |
| resend.com/signup | Use observed accessible label/placeholder | A |  | — |
| API Keys | Use observed accessible label/placeholder | A |  | — |
| Open Resend API Keys | data-testid=resend-howto-cta | A |  | — |
| Read the guide | Use observed accessible label/placeholder | A |  | — |
| Input / icon | data-testid=setup-api-key-input | password | re_xxxxxxxxxxxxxxxxxxxxxxxx | False |
| Connect Resend | data-testid=setup-api-key-submit | submit |  | True |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/outreach/campaigns` | read candidate; inspect endpoint side effects | api-0432 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/outreach/campaigns` | create / edit / configuration; inspect before execution | api-0433 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/outreach/campaigns/{parameter_1}` | read candidate; inspect endpoint side effects | api-0434 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/outreach/campaigns/{parameter_1}/launch` | delivery / publishing / provider or workflow change | api-0435 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/outreach/campaigns/{parameter_1}/pause` | delivery / publishing / provider or workflow change | api-0436 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/outreach/connect` | account / access / configuration change | api-0437 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/outreach/connection` | read candidate; inspect endpoint side effects | api-0438 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/outreach/disconnect` | account / access / configuration change | api-0439 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/outreach/from-address` | create / edit / configuration; inspect before execution | api-0440 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/outreach/gmail-oauth/start` | read candidate; inspect endpoint side effects | api-0441 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/outreach/lists` | read candidate; inspect endpoint side effects | api-0442 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/outreach/lists/upload` | create / edit / configuration; inspect before execution | api-0443 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/outreach/lists/{parameter_1}` | delete / remove | api-0444 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/outreach/mailboxes` | read candidate; inspect endpoint side effects | api-0445 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/outreach/mailboxes` | create / edit / configuration; inspect before execution | api-0446 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/outreach/mailboxes/bulk` | create / edit / configuration; inspect before execution | api-0447 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/outreach/mailboxes/{parameter_1}` | delete / remove | api-0448 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/outreach/mailboxes/{parameter_1}/health` | read candidate; inspect endpoint side effects | api-0449 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/outreach/mailboxes/{parameter_1}/test` | create / edit / configuration; inspect before execution | api-0450 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/outreach/mailboxes/{parameter_1}/{parameter_2}` | create / edit / configuration; inspect before execution | api-0451 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/outreach/refresh-domains` | create / edit / configuration; inspect before execution | api-0452 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/outreach/replies` | read candidate; inspect endpoint side effects | api-0453 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/outreach/suppressions` | read candidate; inspect endpoint side effects | api-0454 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/outreach/test-send` | delivery / publishing / provider or workflow change | api-0455 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-03.json` — /outreach · 2026-09-08T17:02:09.965Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
