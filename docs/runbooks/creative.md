# Creative Studio

**Route:** `/creative-studio` · [Open Veluro](https://veluro.ai/creative-studio)

**When:** Use to generate image/video assets or assemble creative variants.

**Prerequisites:** Approved creative brief, asset rights, exact model variant, credit allowance and output specs.

## Agent procedure

1. Choose Guided or Pro mode and the intended output type.
2. Read current model slug, price, ratio/duration and reference-image requirements.
3. Write the brief and inspect added text/branding fields.
4. Generate once and store the job/generation ID; poll rather than resubmit.
5. Review finished output and saved library asset, then check credit delta.
6. Use Photos → Video, Ad Lab or storyboard only for the matching need and inspect their separate final actions.

## Success and recovery

Completion proof: The finished asset meets specification, exists in the library and has a verified cost/result.

Model names can repeat with different costs. Avatar/audio labels do not establish available models. Generation was not executed.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

5 captured screen states; 125 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Buy more credits | data-testid=studio-buy-credits-btn | BUTTON |  | False |
| Guided | data-testid=studio-mode-wizard | BUTTON |  | False |
| Pro mode | data-testid=studio-mode-pro | BUTTON |  | False |
| Photos → Video | data-testid=studio-mode-photos | BUTTON |  | False |
| Ad Lab | data-testid=studio-mode-adlab | BUTTON |  | False |
| 🎬 Storyboard Video Builder | data-testid=open-storyboard-builder | A |  | — |
| Model Guide — all models & credits | data-testid=studio-model-guide-btn | BUTTON |  | False |
| A Video /  / Ads, UGC, product clips, talking heads — up to 90s | data-testid=wizard-pick-video | BUTTON |  | False |
| An Image /  / Product shots, promos, flyers, social graphics | data-testid=wizard-pick-image | BUTTON |  | False |
| Input / icon | data-testid=model-guide-close | BUTTON |  | False |
| Use | data-testid=guide-pick-lipsync-sync | BUTTON |  | False |
| Use | data-testid=guide-pick-luma-ray2-flash | BUTTON |  | False |
| Use | data-testid=guide-pick-hailuo-3-max-turbo | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-2-0-mini | BUTTON |  | False |
| Use | data-testid=guide-pick-hailuo-piapi | BUTTON |  | False |
| Use | data-testid=guide-pick-wan-3-0 | BUTTON |  | False |
| Use | data-testid=guide-pick-hailuo-3-max | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-piapi-fast | BUTTON |  | False |
| Use | data-testid=guide-pick-grok-imagine-video | BUTTON |  | False |
| Use | data-testid=guide-pick-ltx-video | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-1-5-pro | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-piapi | BUTTON |  | False |
| Use | data-testid=guide-pick-vertex-veo-lite | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-2-0-mini-720p | BUTTON |  | False |
| Use | data-testid=guide-pick-pixverse-v6 | BUTTON |  | False |
| Use | data-testid=guide-pick-wan-3-0-720p | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-piapi-fast-720p | BUTTON |  | False |
| Use | data-testid=guide-pick-story-video | BUTTON |  | False |
| Use | data-testid=guide-pick-vertex-veo-fast | BUTTON |  | False |
| Use | data-testid=guide-pick-vertex-veo | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-2-5-piapi | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-piapi-720p | BUTTON |  | False |
| Use | data-testid=guide-pick-wan-3-0-1080p | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-2-5-piapi-720p | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-piapi-fast-1440p | BUTTON |  | False |
| Use | data-testid=guide-pick-kling-3 | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-2-5-piapi-1080p | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-piapi-fast-2560p | BUTTON |  | False |
| Use | data-testid=guide-pick-kling-video | BUTTON |  | False |
| Use | data-testid=guide-pick-kling-3-omni | BUTTON |  | False |
| Use | data-testid=guide-pick-deerflow-omnireels | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-piapi-1080p | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-piapi-fast-4k | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-2-5-piapi-1440p | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-piapi-1440p | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-piapi-2560p | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-2-5-piapi-2560p | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-piapi-4k | BUTTON |  | False |
| Use | data-testid=guide-pick-seedance-2-5-piapi-4k | BUTTON |  | False |
| Use | data-testid=guide-pick-flux-schnell | BUTTON |  | False |
| Use | data-testid=guide-pick-flux-dev | BUTTON |  | False |
| Use | data-testid=guide-pick-gpt-image-2-low-1024x1024 | BUTTON |  | False |
| Use | data-testid=guide-pick-gpt-image-2-low-1024x1536 | BUTTON |  | False |
| Use | data-testid=guide-pick-gpt-image-2-low-1024x768 | BUTTON |  | False |
| Use | data-testid=guide-pick-imagen-standard | BUTTON |  | False |
| Use | data-testid=guide-pick-nano-banana | BUTTON |  | False |
| Use | data-testid=guide-pick-nano-banana-2 | BUTTON |  | False |
| Use | data-testid=guide-pick-seedream | BUTTON |  | False |
| Use | data-testid=guide-pick-imagen-ultra | BUTTON |  | False |
| Use | data-testid=guide-pick-gpt-image-2-medium-1024x1536 | BUTTON |  | False |
| Use | data-testid=guide-pick-gpt-image-2-medium-1024x768 | BUTTON |  | False |
| Use | data-testid=guide-pick-gpt-image-2-medium-1920x1080 | BUTTON |  | False |
| Use | data-testid=guide-pick-flux-piapi | BUTTON |  | False |
| Use | data-testid=guide-pick-gpt-image-2-medium-1024x1024 | BUTTON |  | False |
| Use | data-testid=guide-pick-gpt-image-2-medium-2560x1440 | BUTTON |  | False |
| Use | data-testid=guide-pick-vertex-imagen | BUTTON |  | False |
| Use | data-testid=guide-pick-gpt-image-2-medium-3840x2160 | BUTTON |  | False |
| Use | data-testid=guide-pick-grok-imagine-image | BUTTON |  | False |
| Use | data-testid=guide-pick-cinema-asset-sheet | BUTTON |  | False |
| Use | data-testid=guide-pick-mood-board-creator | BUTTON |  | False |
| Use | data-testid=guide-pick-gpt-image-2-high-1024x768 | BUTTON |  | False |
| Use | data-testid=guide-pick-gpt-image-2-high-1920x1080 | BUTTON |  | False |
| Use | data-testid=guide-pick-gpt-image-2 | BUTTON |  | False |
| Use | data-testid=guide-pick-gpt-image-2-high-1024x1536 | BUTTON |  | False |
| Use | data-testid=guide-pick-gpt-image-2-high-2560x1440 | BUTTON |  | False |
| Use | data-testid=guide-pick-gpt-image-2-high-3840x2160 | BUTTON |  | False |
| Video | data-testid=studio-cat-video | BUTTON |  | False |
| Image | data-testid=studio-cat-image | BUTTON |  | False |
| AI Avatar | data-testid=studio-cat-avatar | BUTTON |  | False |
| Voice / Audio | data-testid=studio-cat-audio | BUTTON |  | False |
| Not sure what to write? Describe it in plain English — Veluro will craft the perfect prompt | data-testid=creative-assistant-toggle | BUTTON |  | False |
| Input / icon | data-testid=studio-prompt | TEXTAREA | e.g. 8-second vertical ad for a local coffee shop — cozy morning vibes, latte art close-up, upbeat energy | False |
| Input / icon | data-testid=studio-overlay-text | INPUT | Exact on-screen text (optional) — e.g. "50% Off This Week Only" | False |
| Testimonial | data-testid=studio-template-testimonial | BUTTON |  | False |
| Promo | data-testid=studio-template-promo | BUTTON |  | False |
| Before / After | data-testid=studio-template-before-after | BUTTON |  | False |
| Product Demo | data-testid=studio-template-product-demo | BUTTON |  | False |
| Behind the Scenes | data-testid=studio-template-behind-the-scenes | BUTTON |  | False |
| 9:16 | data-testid=studio-ratio-9x16 | BUTTON |  | False |
| 16:9 | data-testid=studio-ratio-16x9 | BUTTON |  | False |
| 1:1 | data-testid=studio-ratio-1x1 | BUTTON |  | False |
| Input / icon | data-testid=studio-duration | range | ; min: 4; max: 30 | False |
| Reference image (optional) | data-testid=studio-ref-image-open | button |  | False |
| Generate | data-testid=studio-generate-btn | BUTTON |  | True |
| Add image | data-testid=p2v-add-image-open | button |  | False |
| 9:16 | data-testid=p2v-ratio-9x16 | BUTTON |  | False |
| 16:9 | data-testid=p2v-ratio-16x9 | BUTTON |  | False |
| 1:1 | data-testid=p2v-ratio-1x1 | BUTTON |  | False |
| Input / icon | data-testid=p2v-seconds | range | ; min: 1.5; max: 6 | False |
| Create Video (free) | data-testid=p2v-build-btn | BUTTON |  | True |
| Input / icon | data-testid=oneclick-offer | TEXTAREA | Your offer… e.g. 'Mobile detailing service, $149 full detail, we come to you, book online in 60 seconds' | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | Audience (optional) | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | Landing page URL | False |
| Meta / LinkedIn | Use observed accessible label/placeholder | SELECT | ; options: Meta, LinkedIn | False |
| Input / icon | Use observed accessible label/placeholder | number | $/day; min: 5 | False |
| Bold Promo / Spotlight / Hook + Offer | Use observed accessible label/placeholder | SELECT | ; options: Bold Promo, Spotlight, Hook + Offer | False |
| 9:16 Mobile / 16:9 Desktop | Use observed accessible label/placeholder | SELECT | ; options: 9:16 Mobile, 16:9 Desktop | False |
| Product image | Use observed accessible label/placeholder | BUTTON |  | False |
| Create My Ad | data-testid=oneclick-run-btn | BUTTON |  | True |
| Input / icon | data-testid=template-headline | INPUT | Headline — e.g. Stop guessing. Start growing. | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | Supporting line (optional) | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | CTA — e.g. Start Free Trial | False |
| Product image | data-testid=template-image-btn | BUTTON |  | False |
| Logo (optional) | Use observed accessible label/placeholder | BUTTON |  | False |
| 9:16 Mobile | Use observed accessible label/placeholder | BUTTON |  | False |
| 16:9 Desktop | Use observed accessible label/placeholder | BUTTON |  | False |
| No music | Use observed accessible label/placeholder | SELECT | ; options: No music | False |
| Render Video Ad | data-testid=template-render-btn | BUTTON |  | True |
| Upload talking-head footage | data-testid=trimmer-upload-btn | BUTTON |  | False |
| Vertical 9:16 (Reels/TikTok) | Use observed accessible label/placeholder | BUTTON |  | False |
| Keep original size | Use observed accessible label/placeholder | BUTTON |  | False |
| Create Jump-Cut | data-testid=trimmer-run-btn | BUTTON |  | True |
| Input / icon | data-testid=hormozi-offer-input | TEXTAREA | Describe your offer/product… e.g. 'AI marketing platform that finds high-intent buyers and runs campaigns automatically, $497/mo, 7-day free trial' | False |
| Input / icon | data-testid=hormozi-audience-input | INPUT | Target audience (optional) — e.g. med spa owners | False |
| Generate 3-2-2 Set | data-testid=hormozi-generate-btn | BUTTON |  | True |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| POST | `/ad-lab/hormozi-copy` | create / edit / configuration; inspect before execution | api-0001 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ad-lab/jobs/{parameter_1}` | read candidate; inspect endpoint side effects | api-0002 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ad-lab/one-click` | create / edit / configuration; inspect before execution | api-0003 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ad-lab/silence-trim` | create / edit / configuration; inspect before execution | api-0004 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ad-lab/template-render` | generation / analysis; may consume credits or store output | api-0005 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ad-lab/templates` | read candidate; inspect endpoint side effects | api-0006 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/omnirogue/assistant` | create / edit / configuration; inspect before execution | api-0410 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/omnirogue/assistant/{parameter_1}` | read candidate; inspect endpoint side effects | api-0411 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/omnirogue/generate` | generation / analysis; may consume credits or store output | api-0412 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/omnirogue/generations` | read candidate; inspect endpoint side effects | api-0413 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/omnirogue/models` | read candidate; inspect endpoint side effects | api-0414 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/omnirogue/topup` | billing / financial change | api-0415 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/omnirogue/topup/confirm` | billing / financial change | api-0416 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/omnirogue/usage` | read candidate; inspect endpoint side effects | api-0417 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/studio-wizard/plan` | create / edit / configuration; inspect before execution | api-0586 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/studio-wizard/script` | create / edit / configuration; inspect before execution | api-0587 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/studio-wizard/stitch` | create / edit / configuration; inspect before execution | api-0588 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/studio-wizard/stitches` | read candidate; inspect endpoint side effects | api-0589 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `dialogs-03.json` — studio-model-guide-btn · 2026-09-08T17:17:28.461Z
- `dialogs-02.json` — Pro mode · 2026-09-08T17:13:51.076Z
- `dialogs-02.json` — Photos → Video · 2026-09-08T17:13:59.304Z
- `dialogs-02.json` — Ad Lab · 2026-09-08T17:14:03.501Z
- `ui-batch-05.json` — /creative-studio · 2026-09-08T17:04:17.295Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
