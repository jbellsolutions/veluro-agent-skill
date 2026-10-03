# Pixels and conversion tracking

**Route:** `/pixels` · [Open Veluro](https://veluro.ai/pixels)

**When:** Use before measuring or optimizing campaign conversion events.

**Prerequisites:** Authorized site/funnel access and correct provider tag/pixel ID.

## Agent procedure

1. Open Add Pixel and choose Meta, Google, LinkedIn, TikTok or Custom Script.
2. Enter the actual provider identifier/script and a descriptive name.
3. Generate and inspect install code; assign it only to the intended page/funnel.
4. Install through the authorized site flow and trigger a controlled test conversion.
5. Verify the event in the provider and ensure events are not double-fired.

## Success and recovery

Completion proof: Actual provider event receipt and intended page placement are verified.

Creating a Veluro pixel record is not proof of installation. Custom scripts execute on client pages.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

2 captured screen states; 7 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Add Pixel | data-testid=create-pixel-btn | BUTTON |  | False |
| Set up my first pixel — takes 2 minutes | data-testid=education-create-btn | BUTTON |  | False |
| Meta Pixel /  / For Facebook advertising (Facebook & Instagram ads) | data-testid=wizard-type-meta | BUTTON |  | False |
| Google Tag /  / For Google Ads or Google Analytics | data-testid=wizard-type-google | BUTTON |  | False |
| LinkedIn Insight /  / For LinkedIn advertising | data-testid=wizard-type-linkedin | BUTTON |  | False |
| TikTok Pixel /  / For TikTok advertising | data-testid=wizard-type-tiktok | BUTTON |  | False |
| Custom Script /  / For any other tracking script | data-testid=wizard-type-custom | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/ads/pixels` | read candidate; inspect endpoint side effects | api-0060 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/pixels` | create / edit / configuration; inspect before execution | api-0061 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/pixels/meta` | read candidate; inspect endpoint side effects | api-0062 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/google-ads/conversion-action` | create / edit / configuration; inspect before execution | api-0240 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/google-ads/conversion-actions` | read candidate; inspect endpoint side effects | api-0241 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/pixels` | read candidate; inspect endpoint side effects | api-0474 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/pixels` | create / edit / configuration; inspect before execution | api-0475 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/pixels/{parameter_1}` | delete / remove | api-0476 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/pixels/{parameter_1}/assign` | create / edit / configuration; inspect before execution | api-0477 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/pixels/{parameter_1}/install-code` | read candidate; inspect endpoint side effects | api-0478 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/pixels/{parameter_1}/toggle` | create / edit / configuration; inspect before execution | api-0479 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-02.json` — /pixels · 2026-09-08T17:01:14.759Z
- `dialogs-01.json` — Add Pixel · 2026-09-08T17:12:31.633Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
