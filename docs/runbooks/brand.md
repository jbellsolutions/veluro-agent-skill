# Brand Kit

**Route:** `/settings?tab=brand-kit` · [Open Veluro](https://veluro.ai/settings?tab=brand-kit)

**When:** Use before generating visual assets or after an approved rebrand.

**Prerequisites:** Approved logo, colors, font and style direction.

## Agent procedure

1. Open Brand Kit; select the approved logo from the asset library.
2. Set primary, secondary and accent/background colors.
3. Select the brand font and describe visual style, desired subjects and exclusions.
4. Save Brand Kit, reload and confirm the values.
5. Check the next generated asset actually follows the brand.

## Success and recovery

Completion proof: Saved brand settings and inspected output match the approved identity.

Applying a brand does not verify facts or rights in generated assets.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 20 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Profile | data-testid=settings-tab-profile | button |  | False |
| Integrations | data-testid=settings-tab-integrations | button |  | False |
| Notifications | data-testid=settings-tab-notifications | button |  | False |
| Billing | data-testid=settings-tab-billing | button |  | False |
| Brand Kit | data-testid=settings-tab-brand-kit | button |  | False |
| Choose from Library | data-testid=brand-pick-logo | BUTTON |  | False |
| Input / icon | data-testid=brand-primary_color | color |  | False |
| Input / icon | data-testid=brand-secondary_color | color |  | False |
| Input / icon | data-testid=brand-accent_color | color |  | False |
| Outfit | data-testid=brand-font-outfit | BUTTON |  | False |
| Inter | data-testid=brand-font-inter | BUTTON |  | False |
| DM Sans | data-testid=brand-font-dm-sans | BUTTON |  | False |
| Manrope | data-testid=brand-font-manrope | BUTTON |  | False |
| Poppins | data-testid=brand-font-poppins | BUTTON |  | False |
| Playfair Display | data-testid=brand-font-playfair-display | BUTTON |  | False |
| Instrument Serif | data-testid=brand-font-instrument-serif | BUTTON |  | False |
| Roboto | data-testid=brand-font-roboto | BUTTON |  | False |
| Input / icon | data-testid=brand-creative-style | TEXTAREA | e.g. "Bright, warm lifestyle photos with real people — never stocky corporate shots. Navy + gold tones. Show homes and families, not offices. No cartoons, no neon." | False |
| Save Brand Kit | data-testid=brand-save | BUTTON |  | False |
| Save Changes | data-testid=save-settings-btn | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/brand-kit` | read candidate; inspect endpoint side effects | api-0128 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/brand-kit` | create / edit / configuration; inspect before execution | api-0129 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `dialogs-02.json` — Brand Kit · 2026-09-08T17:13:46.990Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
