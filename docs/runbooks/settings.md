# Profile, settings and notifications

**Route:** `/settings` · [Open Veluro](https://veluro.ai/settings)

**When:** Use during onboarding, contact changes and preference maintenance.

**Prerequisites:** Correct workspace, approved identity/contact facts and permission to change settings.

## Agent procedure

1. Open Settings → Profile; distinguish login email from public contact email.
2. Fill approved name, business and contact fields and save the profile.
3. Review agent memory against business facts; amend only relevant entries.
4. Open Notifications and set only approved push, reply, demand, win-rate and optimization preferences.
5. Read back changed values and confirm no unintended preference changed.

## Success and recovery

Completion proof: Saved values survive reload; client-facing materials use the correct public details.

Language selection may save immediately. Reset memory deletes learned context. Auto-Optimize is an operating permission, not just an email preference.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

6 captured screen states; 78 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

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
| crm-system-name | data-testid=crm-name-input | INPUT | Type your CRM here — e.g. HubSpot, Pipedrive, Salesforce… | False |
| Show me how | data-testid=crm-guide-btn | BUTTON |  | False |
| Input / icon | data-testid=early-access-input | INPUT | Your Facebook profile link or username | False |
| Request early ad access | data-testid=early-access-btn | BUTTON |  | False |
| f / Connect with Facebook | data-testid=connect-meta_ads-oauth | BUTTON |  | False |
| Set up → | data-testid=connect-email_outreach | BUTTON |  | False |
| Connect Google Ads | data-testid=connect-google-ads | BUTTON |  | False |
| Connect Google | data-testid=connect-google | BUTTON |  | False |
| Input / icon | data-testid=google_analytics-measurement_id | text | G-XXXXXXXXXX | False |
| Input / icon | data-testid=google_analytics-api_secret | password | Your API secret | False |
| Connect | data-testid=connect-google_analytics | BUTTON |  | False |
| Setup Guide | data-testid=guide-google_analytics | BUTTON |  | False |
| Docs → | Use observed accessible label/placeholder | A |  | — |
| Sign in with LinkedIn | data-testid=connect-linkedin-oauth | BUTTON |  | False |
| Connect LinkedIn Ads | data-testid=connect-linkedin-marketing | BUTTON |  | False |
| Connect TikTok Ads | data-testid=connect-tiktok | BUTTON |  | False |
| Input / icon | data-testid=sendgrid-api_key | password | SG.xxxxx | False |
| Input / icon | data-testid=sendgrid-sender_email | email | hello@yourdomain.com | False |
| Connect | data-testid=connect-sendgrid | BUTTON |  | False |
| Setup Guide | data-testid=guide-sendgrid | BUTTON |  | False |
| Input / icon | data-testid=twilio-account_sid | text | ACxxxxxx | False |
| Input / icon | data-testid=twilio-auth_token | password | Your auth token | False |
| Input / icon | data-testid=twilio-phone_number | tel | +1234567890 | False |
| Connect | data-testid=connect-twilio | BUTTON |  | False |
| Setup Guide | data-testid=guide-twilio | BUTTON |  | False |
| Input / icon | data-testid=gohighlevel-api_key | password | pit-xxxxxxxx… | False |
| Input / icon | data-testid=gohighlevel-location_id | text | Your location ID | False |
| Connect | data-testid=connect-gohighlevel | BUTTON |  | False |
| Setup Guide | data-testid=guide-gohighlevel | BUTTON |  | False |
| Input / icon | data-testid=bank_account-provider | text | plaid | False |
| Input / icon | data-testid=bank_account-api_key | password | Your provider API key | False |
| Connect | data-testid=connect-bank_account | BUTTON |  | False |
| Setup Guide | data-testid=guide-bank_account | BUTTON |  | False |
| Input / icon | data-testid=notif-notifications | button |  | False |
| Input / icon | data-testid=notif-auto_optimize | button |  | False |
| Input / icon | data-testid=notif-email_reply_alerts | button |  | False |
| Input / icon | data-testid=notif-email_surge_alerts | button |  | False |
| Input / icon | data-testid=notif-email_coach_digest | button |  | False |
| 500 /  / $19 | data-testid=llm-pack-pack500 | BUTTON |  | False |
| 1,500 /  / $49 | data-testid=llm-pack-pack1500 | BUTTON |  | False |
| 5,000 /  / $129 | data-testid=llm-pack-pack5000 | BUTTON |  | False |
| 15,000 /  / $299 | data-testid=llm-pack-pack15000 | BUTTON |  | False |
| Switch to Free — $0/mo | data-testid=upgrade-free | BUTTON |  | False |
| Switch to Starter — $297/mo | data-testid=upgrade-starter | BUTTON |  | False |
| Switch to Command — $997/mo | data-testid=upgrade-command | BUTTON |  | False |
| Switch to Scale — $2,497/mo | data-testid=upgrade-scale | BUTTON |  | False |
| Switch to Enterprise — $6,497/mo | data-testid=upgrade-enterprise | BUTTON |  | False |
| Input / icon | data-testid=avatar-upload-input | file |  | False |
| Input / icon | data-testid=profile-name-input | INPUT |  | False |
| Input / icon | data-testid=profile-company-input | INPUT | e.g. Peak Margin Strategies | False |
| Input / icon | data-testid=profile-contact-email-input | INPUT | e.g. hello@yourbusiness.com | False |
| Input / icon | data-testid=profile-phone-input | INPUT |  | False |
| Save Profile | data-testid=save-profile-btn | BUTTON |  | False |
| English | data-testid=language-option-en | button |  | False |
| Español | data-testid=language-option-es | button |  | False |
| Input / icon | data-testid=agent-memory-textarea | TEXTAREA | Nothing learned yet — chat with your Veluro agent about your business and this fills in automatically. You can also type key facts here yourself (your offers, ideal customers, goals). | False |
| Reset memory | data-testid=agent-memory-reset | BUTTON |  | True |
| Save memory | data-testid=agent-memory-save | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/auth/profile` | read candidate; inspect endpoint side effects | api-0106 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/auth/profile` | create / edit / configuration; inspect before execution | api-0107 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/settings` | read candidate; inspect endpoint side effects | api-0555 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/settings` | create / edit / configuration; inspect before execution | api-0556 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/veluro-chat/memory` | account / access / configuration change | api-0632 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/veluro-chat/memory` | read candidate; inspect endpoint side effects | api-0633 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/veluro-chat/memory` | account / access / configuration change | api-0634 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `dialogs-02.json` — Brand Kit · 2026-09-08T17:13:46.990Z
- `ui-batch-07.json` — /settings?tab=integrations · 2026-09-08T17:06:44.730Z
- `ui-batch-07.json` — /settings?tab=notifications · 2026-09-08T17:06:46.264Z
- `ui-batch-07.json` — /settings?tab=billing · 2026-09-08T17:06:47.794Z
- `ui-batch-07.json` — /settings?tab=brand · 2026-09-08T17:06:49.361Z
- `ui-batch-01.json` — /settings · 2026-09-08T17:00:46.393Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
