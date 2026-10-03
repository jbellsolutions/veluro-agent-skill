# Marketing Library and Starter Kit

**Route:** `/marketing-materials` · [Open Veluro](https://veluro.ai/marketing-materials)

**When:** Use to prepare Veluro promotional materials with the correct referral attribution.

**Prerequisites:** Approved offer, actual commission terms and permission for any publication/advertising.

## Agent procedure

1. Choose the Veluro asset group and inspect the material’s intended channel.
2. Check the referral URL and any per-asset attribution parameters.
3. Adapt text and fact-check statistics, trial claims and feature promises.
4. Download/copy a reviewed asset or prepare a campaign draft.
5. Launch/share only within the approved promotional scope and inspect performance attribution.

## Success and recovery

Completion proof: The material contains accurate claims and the correct tracked link; actual publishing is independently verified.

Prebuilt launch buttons can create ads. Investment-related asset groups were outside this Veluro documentation scope.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 2 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Veluro /  / 46+ ASSETS /  / Everything to promote Veluro with your referral link — proven ad copies, display & video creatives, Google Ads campaigns, scripts and emails. | data-testid=folder-veluro | BUTTON |  | False |
| SixthShock /  / INVESTMENT STRUCTURE CAMPAIGN /  / Approved done-for-you campaign for SixthShock — SEC-compliant, asset-backed capital raises ($2M–$75M). FB ads, LinkedIn & email sequences, image creatives. | data-testid=folder-sixthshock | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/partner/display-ads` | read candidate; inspect endpoint side effects | api-0456 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/partner/display-ads/launch` | delivery / publishing / provider or workflow change | api-0457 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/partner/marketing-materials` | read candidate; inspect endpoint side effects | api-0460 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/partner/promo-ads` | read candidate; inspect endpoint side effects | api-0461 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/partner/promo-ads/launch` | delivery / publishing / provider or workflow change | api-0462 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/partner/video-ads` | read candidate; inspect endpoint side effects | api-0472 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/partner/video-ads/launch` | delivery / publishing / provider or workflow change | api-0473 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/referrals/partner/starter-kit` | create / edit / configuration; inspect before execution | api-0506 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-08.json` — /marketing-materials · 2026-09-08T17:17:56.488Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
