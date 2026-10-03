# Provider and CRM integrations

**Route:** `/settings?tab=integrations` · [Open Veluro](https://veluro.ai/settings?tab=integrations)

**When:** Use before any channel-specific launch, sync, reporting or delivery.

**Prerequisites:** Authorized provider credentials/account access; intended account, page, property, calendar and scope.

## Agent procedure

1. Read approval and verification banners before choosing a connection.
2. Choose the exact integration; follow its OAuth or credential form using the authorized client account.
3. Verify returned connection state and selected provider IDs.
4. For CRM, specify sync direction and map fields; test a controlled authorized record before bulk sync.
5. Check expiry/reconnect behavior and keep secrets outside business knowledge and reports.

## Success and recovery

Completion proof: The required operation works with the intended account; a connected label alone is insufficient.

Connections may authorize external access. The current account has no ad or delivery integrations; Meta review gating remains.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 39 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Profile | data-testid=settings-tab-profile | button |  | False |
| Integrations | data-testid=settings-tab-integrations | button |  | False |
| Notifications | data-testid=settings-tab-notifications | button |  | False |
| Billing | data-testid=settings-tab-billing | button |  | False |
| Brand Kit | data-testid=settings-tab-brand-kit | button |  | False |
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
| Save Changes | data-testid=save-settings-btn | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/auth/linkedin-marketing/ad-accounts` | read candidate; inspect endpoint side effects | api-0087 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/auth/linkedin-marketing/connection` | read candidate; inspect endpoint side effects | api-0088 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/auth/linkedin-marketing/disconnect` | account / access / configuration change | api-0089 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/auth/linkedin-marketing/organizations` | read candidate; inspect endpoint side effects | api-0090 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/auth/linkedin-marketing/select` | create / edit / configuration; inspect before execution | api-0091 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/auth/linkedin-marketing/start` | read candidate; inspect endpoint side effects | api-0092 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/auth/linkedin/connection` | read candidate; inspect endpoint side effects | api-0093 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/auth/linkedin/disconnect` | account / access / configuration change | api-0094 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/auth/linkedin/start` | read candidate; inspect endpoint side effects | api-0095 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/auth/meta/accounts` | read candidate; inspect endpoint side effects | api-0099 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/auth/meta/accounts/active` | create / edit / configuration; inspect before execution | api-0100 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/auth/meta/diagnose?live=1` | read candidate; inspect endpoint side effects | api-0101 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/auth/meta/health` | read candidate; inspect endpoint side effects | api-0102 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/auth/meta/pages/active` | create / edit / configuration; inspect before execution | api-0103 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/auth/meta/select` | create / edit / configuration; inspect before execution | api-0104 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/auth/meta/start{parameter_1}` | read candidate; inspect endpoint side effects | api-0105 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/calendar/conflicts` | create / edit / configuration; inspect before execution | api-0132 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/calendar/disconnect` | account / access / configuration change | api-0133 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/calendar/list` | read candidate; inspect endpoint side effects | api-0134 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/calendar/select` | create / edit / configuration; inspect before execution | api-0135 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/calendar/status` | read candidate; inspect endpoint side effects | api-0136 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PATCH | `/crm/auto-sync` | delivery / publishing / provider or workflow change | api-0150 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/crm/connect` | account / access / configuration change | api-0151 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/crm/connection` | read candidate; inspect endpoint side effects | api-0152 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/crm/disconnect` | account / access / configuration change | api-0153 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/crm/guide` | create / edit / configuration; inspect before execution | api-0154 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/crm/sync/{parameter_1}` | delivery / publishing / provider or workflow change | api-0155 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/google-ads/accounts` | read candidate; inspect endpoint side effects | api-0237 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/google-ads/auth/start` | read candidate; inspect endpoint side effects | api-0238 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/google-ads/connection` | read candidate; inspect endpoint side effects | api-0239 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/google-ads/conversion-action` | create / edit / configuration; inspect before execution | api-0240 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/google-ads/conversion-actions` | read candidate; inspect endpoint side effects | api-0241 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/google-ads/disconnect` | account / access / configuration change | api-0242 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/google-ads/launch/{parameter_1}` | delivery / publishing / provider or workflow change | api-0243 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/google-ads/recommendations` | read candidate; inspect endpoint side effects | api-0244 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/google-ads/recommendations/apply` | create / edit / configuration; inspect before execution | api-0245 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/google-ads/select` | create / edit / configuration; inspect before execution | api-0246 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/google/analytics?lookback_days=30` | read candidate; inspect endpoint side effects | api-0247 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/integrations` | read candidate; inspect endpoint side effects | api-0257 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/integrations/connect` | account / access / configuration change | api-0258 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/integrations/setup-guide/{parameter_1}` | read candidate; inspect endpoint side effects | api-0259 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/integrations/{parameter_1}` | delete / remove | api-0260 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/oauth/calendar/connect` | read candidate; inspect endpoint side effects | api-0409 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/platform/flags` | read candidate; inspect endpoint side effects | api-0480 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-07.json` — /settings?tab=integrations · 2026-09-08T17:06:44.730Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
