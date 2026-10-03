# Landing pages and A/B tests

**Route:** `/landing-pages` · [Open Veluro](https://veluro.ai/landing-pages)

**When:** Use for a single conversion-focused page and controlled variants.

**Prerequisites:** Approved business description, CTA, branding, domain, privacy and page allowance.

## Agent procedure

1. Supply business name, detailed offer and CTA goal.
2. Optionally extract design from an inspiration URL; review design use and write original client copy.
3. Choose look/feel and generate once; preserve page ID.
4. Edit sections, images, form and CTA; preview desktop/mobile output.
5. Publish to the approved slug/domain and verify domain status and served content.
6. For A/B tests, record variant IDs, metric and evaluation window before promoting a winner.

## Success and recovery

Completion proof: The actual page and conversion destination work, and variant decisions use real data.

Generation, saving, publishing, domain verification and autopilot are separate operations. Page creation is quota-limited.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 10 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| New | data-testid=lp-new-btn | button |  | False |
| Input / icon | data-testid=lp-business-name | INPUT | e.g. Veluro | False |
| Input / icon | data-testid=lp-prompt | TEXTAREA | e.g. AI demand engine for SMBs. We replace your CMO. Target: founders & marketing leads at companies 10-200 employees. | False |
| Get leads | data-testid=lp-goal-get-leads | button |  | False |
| Book calls | data-testid=lp-goal-book-calls | button |  | False |
| Sell a product | data-testid=lp-goal-sell-a-product | button |  | False |
| Get signups | data-testid=lp-goal-get-signups | button |  | False |
| Input / icon | data-testid=lp-inspo-url | INPUT | https://stripe.com | False |
| Extract | data-testid=lp-extract-btn | button |  | True |
| Next: look & feel | data-testid=lp-next-1 | button |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/landing` | read candidate; inspect endpoint side effects | api-0305 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/landing/extract-design` | create / edit / configuration; inspect before execution | api-0306 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/landing/generate` | generation / analysis; may consume credits or store output | api-0307 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/landing/quota` | read candidate; inspect endpoint side effects | api-0308 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/landing/suggest-designs` | generation / analysis; may consume credits or store output | api-0309 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/landing/templates` | read candidate; inspect endpoint side effects | api-0310 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/landing/{parameter_1}` | delete / remove | api-0311 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/landing/{parameter_1}` | create / edit / configuration; inspect before execution | api-0312 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/landing/{parameter_1}/ab-variant` | delete / remove | api-0313 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/landing/{parameter_1}/ab-variant` | create / edit / configuration; inspect before execution | api-0314 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/landing/{parameter_1}/ab-variant/promote` | create / edit / configuration; inspect before execution | api-0315 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/landing/{parameter_1}/analytics` | read candidate; inspect endpoint side effects | api-0316 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/landing/{parameter_1}/autopilot` | create / edit / configuration; inspect before execution | api-0317 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/landing/{parameter_1}/chat` | read candidate; inspect endpoint side effects | api-0318 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/landing/{parameter_1}/chat-edit` | generation / analysis; may consume credits or store output | api-0319 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/landing/{parameter_1}/custom-domain` | create / edit / configuration; inspect before execution | api-0320 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/landing/{parameter_1}/generate-ad-creatives` | generation / analysis; may consume credits or store output | api-0321 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/landing/{parameter_1}/generate-image` | generation / analysis; may consume credits or store output | api-0322 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/landing/{parameter_1}/hero-image` | create / edit / configuration; inspect before execution | api-0323 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/landing/{parameter_1}/place-media-ai` | create / edit / configuration; inspect before execution | api-0324 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/landing/{parameter_1}/publish` | delivery / publishing / provider or workflow change | api-0325 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/landing/{parameter_1}/regenerate-section` | generation / analysis; may consume credits or store output | api-0326 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/landing/{parameter_1}/unpublish` | delivery / publishing / provider or workflow change | api-0327 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/landing/{parameter_1}/upload-asset` | create / edit / configuration; inspect before execution | api-0328 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/landing/{parameter_1}/verify-domain` | create / edit / configuration; inspect before execution | api-0329 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-02.json` — /landing-pages · 2026-09-08T17:01:19.005Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
