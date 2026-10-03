# Flyers and PDF output

**Route:** `/flyers` · [Open Veluro](https://veluro.ai/flyers)

**When:** Use for an approved printable promotional artifact.

**Prerequisites:** Approved business/offer/contact details, branding and image rights.

## Agent procedure

1. Fill name, headline, subheadline, offer, CTA, phone, website and QR URL.
2. Choose a design and approved image; review AI-generated copy if used.
3. Save the flyer and inspect the preview.
4. Download PDF and verify text fit, page layout and QR/phone/link accuracy.
5. Preserve the final approved PDF with the client record.

## Success and recovery

Completion proof: The printable artifact is accurate, readable and has working destinations.

Save and generation differ from PDF export. Do not use unverified performance claims in the offer.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 25 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| New | data-testid=flyer-new-btn | BUTTON |  | False |
| Save | data-testid=flyer-save-btn | BUTTON |  | False |
| Download PDF | data-testid=flyer-download-btn | BUTTON |  | False |
| Input / icon | data-testid=flyer-topic-input | INPUT | What's this flyer for? e.g. Spring cleaning special | False |
| AI Fill | data-testid=flyer-ai-fill-btn | BUTTON |  | False |
| Input / icon | data-testid=flyer-name-input | INPUT |  | False |
| Input / icon | data-testid=flyer-business-input | INPUT |  | False |
| Input / icon | data-testid=flyer-headline-input | INPUT |  | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | Benefit 1 | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | Benefit 2 | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | Benefit 3 | False |
| Input / icon | data-testid=flyer-qr-input | INPUT | https://yourbusiness.com/book | False |
| Bold Impact | data-testid=flyer-template-bold | BUTTON |  | False |
| Promo Offer | data-testid=flyer-template-promo | BUTTON |  | False |
| Photo Split | data-testid=flyer-template-split | BUTTON |  | False |
| Minimal | data-testid=flyer-template-minimal | BUTTON |  | False |
| Input / icon | data-testid=flyer-palette-violet | BUTTON |  | False |
| Input / icon | data-testid=flyer-palette-ocean | BUTTON |  | False |
| Input / icon | data-testid=flyer-palette-sunset | BUTTON |  | False |
| Input / icon | data-testid=flyer-palette-forest | BUTTON |  | False |
| Input / icon | data-testid=flyer-palette-clean | BUTTON |  | False |
| Input / icon | data-testid=flyer-image-prompt | INPUT | Describe the flyer image… | False |
| Generate | data-testid=flyer-gen-image-btn | BUTTON |  | False |
| Input / icon | data-testid=flyer-upload-input | file |  | False |
| Upload your own flyer | data-testid=flyer-upload-btn | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/flyers` | read candidate; inspect endpoint side effects | api-0181 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/flyers` | create / edit / configuration; inspect before execution | api-0182 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/flyers/ai-fill` | generation / analysis; may consume credits or store output | api-0183 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/flyers/generate-image` | generation / analysis; may consume credits or store output | api-0184 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/flyers/upload-image` | create / edit / configuration; inspect before execution | api-0185 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/flyers/{parameter_1}` | delete / remove | api-0186 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/flyers/{parameter_1}` | read candidate; inspect endpoint side effects | api-0187 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-06.json` — /flyers · 2026-09-08T17:04:59.201Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
