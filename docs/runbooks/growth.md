# Growth Engine

**Route:** `/service-brain` · [Open Veluro](https://veluro.ai/service-brain)

**When:** Use to assemble an integrated campaign package around a service and market.

**Prerequisites:** Approved industry/service, offer, market, goal, business knowledge, quotas and delivery plan.

## Agent procedure

1. Choose New Growth Engine and select or describe the industry.
2. Choose the service or services; multiple selections can create multiple engines.
3. Set market, goal and notes; complete business training inputs.
4. Create once and record every returned engine ID; poll existing engines rather than restart.
5. Inspect ads, landing content, outreach, booking and scoring; edit each component.
6. Before launch, inspect generate-images and publish-landing choices, account routing and authorization.

## Success and recovery

Completion proof: Each component has the expected content and state; live components are independently checked.

Creation can consume AI resources; launch can publish a page and create media. Live launch was not tested.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

2 captured screen states; 13 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| New Growth Engine | data-testid=brain-new-engine-btn | BUTTON |  | False |
| Back | Use observed accessible label/placeholder | BUTTON |  | False |
| Roofing & Exteriors | data-testid=brain-industry-roofing---exteriors | BUTTON |  | False |
| Med Spa & Aesthetics | data-testid=brain-industry-med-spa---aesthetics | BUTTON |  | False |
| B2B & Professional Services | data-testid=brain-industry-b-b---professional-services | BUTTON |  | False |
| E-commerce & Retail | data-testid=brain-industry-e-commerce---retail | BUTTON |  | False |
| Home Services | data-testid=brain-industry-home-services | BUTTON |  | False |
| Health & Wellness | data-testid=brain-industry-health---wellness | BUTTON |  | False |
| Legal & Financial | data-testid=brain-industry-legal---financial | BUTTON |  | False |
| Real Estate | data-testid=brain-industry-real-estate | BUTTON |  | False |
| Automotive | data-testid=brain-industry-automotive | BUTTON |  | False |
| Input / icon | data-testid=brain-custom-industry | INPUT | Or type your own industry… | False |
| Next | data-testid=brain-step1-next | BUTTON |  | True |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/service-brain/catalog` | read candidate; inspect endpoint side effects | api-0545 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/service-brain/engines` | read candidate; inspect endpoint side effects | api-0546 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/service-brain/engines` | create / edit / configuration; inspect before execution | api-0547 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/service-brain/engines/{parameter_1}` | delete / remove | api-0548 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/service-brain/engines/{parameter_1}` | read candidate; inspect endpoint side effects | api-0549 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PATCH | `/service-brain/engines/{parameter_1}` | create / edit / configuration; inspect before execution | api-0550 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/service-brain/engines/{parameter_1}/creatives/edit` | create / edit / configuration; inspect before execution | api-0551 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/service-brain/engines/{parameter_1}/creatives/overlay` | create / edit / configuration; inspect before execution | api-0552 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/service-brain/engines/{parameter_1}/creatives/revert` | create / edit / configuration; inspect before execution | api-0553 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/service-brain/engines/{parameter_1}/launch` | delivery / publishing / provider or workflow change | api-0554 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-02.json` — /service-brain · 2026-09-08T17:01:12.698Z
- `dialogs-01.json` — New Growth Engine · 2026-09-08T17:12:29.664Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
