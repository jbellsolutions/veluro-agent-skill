# Sales funnels and funnel editor

**Route:** `/funnels` · [Open Veluro](https://veluro.ai/funnels)

**When:** Use for a multi-step conversion, booking or sales flow.

**Prerequisites:** Approved offer, audience, CTA, brand, tracking and any payment/automation authorization.

## Agent procedure

1. Create Funnel and choose AI or template.
2. For AI, specify goal, product/offer, audience, market, desired outcome and style.
3. Record the funnel ID and wait for generation; inspect each page and step.
4. Edit content, forms, step order and upsell/downsell paths; verify navigation and conversion mapping.
5. Configure only approved pixels, automations, payment connection and webhooks.
6. Preview responsive output; publish only on the approved destination; verify actual submissions.

## Success and recovery

Completion proof: The served flow, routing, forms and authorized downstream actions work end to end.

Template creation can create stored objects. Automation test buttons can send real messages. Payment, publishing and variant promotion were not executed.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

2 captured screen states; 7 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Create Funnel | data-testid=create-funnel-btn | BUTTON |  | False |
| Input / icon | data-testid=funnel-search | INPUT | Search funnels… | False |
| All statuses / Draft / Live / Paused | Use observed accessible label/placeholder | SELECT | ; options: All statuses, Draft, Live, Paused | False |
| Create Funnel | Use observed accessible label/placeholder | BUTTON |  | False |
| Build With AI / RECOMMENDED /  / Answer a few questions — AI designs the steps, writes the copy, and builds the form. | data-testid=build-with-ai-btn | BUTTON |  | False |
| Start From Template /  / 6 polished, proven funnel templates — fully customizable. | data-testid=start-from-template-btn | BUTTON |  | False |
| Cancel | Use observed accessible label/placeholder | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/funnels` | read candidate; inspect endpoint side effects | api-0194 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/funnels` | create / edit / configuration; inspect before execution | api-0195 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/funnels/automations/{parameter_1}` | delete / remove | api-0196 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/funnels/automations/{parameter_1}` | create / edit / configuration; inspect before execution | api-0197 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/funnels/automations/{parameter_1}/test` | create / edit / configuration; inspect before execution | api-0198 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/funnels/from-template` | create / edit / configuration; inspect before execution | api-0199 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/funnels/pages/{parameter_1}` | delete / remove | api-0200 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/funnels/pages/{parameter_1}` | read candidate; inspect endpoint side effects | api-0201 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/funnels/pages/{parameter_1}` | create / edit / configuration; inspect before execution | api-0202 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/funnels/pages/{parameter_1}/ai-edit` | generation / analysis; may consume credits or store output | api-0203 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/funnels/pages/{parameter_1}/duplicate` | create / edit / configuration; inspect before execution | api-0204 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/funnels/pages/{parameter_1}/promote` | create / edit / configuration; inspect before execution | api-0205 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/funnels/pages/{parameter_1}/variant` | create / edit / configuration; inspect before execution | api-0206 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/funnels/pages/{parameter_1}/variant-ai` | create / edit / configuration; inspect before execution | api-0207 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/funnels/stripe/connect` | billing / financial change | api-0208 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/funnels/stripe/status` | read candidate; inspect endpoint side effects | api-0209 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/funnels/templates` | read candidate; inspect endpoint side effects | api-0210 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/funnels/{parameter_1}` | delete / remove | api-0211 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/funnels/{parameter_1}` | read candidate; inspect endpoint side effects | api-0212 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/funnels/{parameter_1}` | create / edit / configuration; inspect before execution | api-0213 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/funnels/{parameter_1}/analytics` | read candidate; inspect endpoint side effects | api-0214 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/funnels/{parameter_1}/automations` | read candidate; inspect endpoint side effects | api-0215 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/funnels/{parameter_1}/automations` | create / edit / configuration; inspect before execution | api-0216 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/funnels/{parameter_1}/duplicate` | create / edit / configuration; inspect before execution | api-0217 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/funnels/{parameter_1}/generate` | generation / analysis; may consume credits or store output | api-0218 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/funnels/{parameter_1}/leads` | read candidate; inspect endpoint side effects | api-0219 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/funnels/{parameter_1}/optimize` | create / edit / configuration; inspect before execution | api-0220 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/funnels/{parameter_1}/orders` | read candidate; inspect endpoint side effects | api-0221 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/funnels/{parameter_1}/steps` | create / edit / configuration; inspect before execution | api-0222 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/funnels/{parameter_1}/steps/reorder` | create / edit / configuration; inspect before execution | api-0223 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/funnels/{parameter_1}/webhooks/test` | create / edit / configuration; inspect before execution | api-0224 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-02.json` — /funnels · 2026-09-08T17:01:16.852Z
- `dialogs-01.json` — Create Funnel · 2026-09-08T17:12:33.287Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
