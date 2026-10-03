# Ad campaigns and optimization

**Route:** `/campaigns` · [Open Veluro](https://veluro.ai/campaigns)

**When:** Use to prepare, manage and optimize approved advertising.

**Prerequisites:** Complete client record, provider readiness, approved budget/optimization limits and verified conversion path.

## Agent procedure

1. Open New Campaign; use guided setup or the manual builder.
2. Choose platform, objective, name, lead method and destination.
3. Configure audience or Google keywords and explicit geography.
4. Set monthly budget and authorized optimization settings; inspect derived daily budget.
5. Review creative assets, copy variants, forms/privacy, tracking and nurture.
6. Save a local draft and read it back; choose paused provider creation or live launch only within authorization.
7. Poll the existing campaign/job and verify provider IDs, state and delivery before reporting success.

## Success and recovery

Completion proof: Draft read-back or provider state matches the chosen action; spend and conversion events match the client.

Local drafts are Tested. Live launch, pause, reallocation and autonomous optimization are not production-certified. Scores and simulations are not actual outcomes.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

18 captured screen states; 116 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Ad Campaigns | data-testid=tab-ad-campaigns | button |  | False |
| AI Ad Drafts | data-testid=tab-ad-drafts | button |  | False |
| Broad Audience | data-testid=tab-broad-audience | button |  | False |
| Campaigns | data-testid=view-campaigns | BUTTON |  | False |
| Performance | data-testid=view-performance | BUTTON |  | False |
| Audiences | data-testid=manage-audiences-btn | BUTTON |  | False |
| Pixels | data-testid=manage-pixels-btn | BUTTON |  | False |
| Hook Lab | data-testid=hook-lab-btn | BUTTON |  | False |
| Let Veluro plan my ads | data-testid=ai-strategist-btn | BUTTON |  | False |
| New Campaign | data-testid=new-campaign-btn | BUTTON |  | False |
| Input / icon | data-testid=cmo-target-cpa-input | number | e.g. 50 | False |
| Input / icon | data-testid=cmo-breakeven-roas-input | number | e.g. 2.5 | False |
| Input / icon | data-testid=cmo-monthly-budget-input | number | e.g. 3000 | False |
| Meta | data-testid=cmo-channel-meta | BUTTON |  | False |
| Google | data-testid=cmo-channel-google | BUTTON |  | False |
| LinkedIn | data-testid=cmo-channel-linkedin | BUTTON |  | False |
| TikTok | data-testid=cmo-channel-tiktok | BUTTON |  | False |
| Save targets | data-testid=cmo-params-save | BUTTON |  | False |
| Create Campaign | Use observed accessible label/placeholder | BUTTON |  | False |
| Meta Ads | data-testid=platform-meta | BUTTON |  | False |
| Google Ads | data-testid=platform-google | BUTTON |  | False |
| LinkedIn Ads | data-testid=platform-linkedin | BUTTON |  | False |
| TikTok Ads | data-testid=platform-tiktok | BUTTON |  | False |
| Cancel | Use observed accessible label/placeholder | BUTTON |  | False |
| Next | data-testid=next-step-btn | BUTTON |  | False |
| Lead Generation / Collect leads via forms or landing pages | data-testid=type-leads | BUTTON |  | False |
| Website Traffic / Drive visitors to your website | data-testid=type-traffic | BUTTON |  | False |
| Conversions / Optimize for purchases or signups | data-testid=type-conversions | BUTTON |  | False |
| Brand Awareness / Reach new audiences at scale | data-testid=type-brand_awareness | BUTTON |  | False |
| Input / icon | data-testid=campaign-name | text | e.g. Spring 2026 Lead Gen | False |
| Generate from a website URL | data-testid=url-brief-open | button |  | False |
| Input / icon | data-testid=dest-url | url | https://yoursite.com/landing | False |
| Objective chosen | data-testid=checklist-objective | BUTTON |  | False |
| Campaign name | data-testid=checklist-name | BUTTON |  | False |
| Destination URL · optional | data-testid=checklist-dest | BUTTON |  | False |
| Search keywords | data-testid=checklist-keywords | BUTTON |  | False |
| Monthly budget | data-testid=checklist-budget | BUTTON |  | False |
| Primary ad text · optional | data-testid=checklist-copy | BUTTON |  | False |
| Image / video creative · optional | data-testid=checklist-creatives | BUTTON |  | False |
| Headline · optional | data-testid=checklist-headline | BUTTON |  | False |
| Back | Use observed accessible label/placeholder | BUTTON |  | False |
| Save & finish later | data-testid=save-finish-later-btn | BUTTON |  | False |
| AI Suggest Keywords | data-testid=suggest-keywords-btn | BUTTON |  | False |
| Input / icon | data-testid=keyword-input | INPUT | Type a keyword, e.g. emergency plumber near me | False |
| Phrase match / Exact match / Negative | data-testid=keyword-match-select | SELECT | ; options: Phrase match, Exact match, Negative | False |
| Add | data-testid=add-keyword-btn | BUTTON |  | False |
| AI Suggest Budget | data-testid=suggest-budget-btn | BUTTON |  | False |
| Input / icon | data-testid=budget-input | number | 1500 | False |
| Input / icon | data-testid=auto-optimize-toggle | BUTTON |  | False |
| Input / icon | data-testid=max-increase | number |  | False |
| Upload / Pick from Library | data-testid=creative-media-picker-open | button |  | False |
| Input / icon | data-testid=ai-image-prompt | text | Describe a creative and Veluro designs it… | False |
| Open Creative Builder | data-testid=ai-image-generate-btn | BUTTON |  | False |
| AI Generate Copy | data-testid=generate-creatives-btn | BUTTON |  | False |
| Input / icon | data-testid=ad-headline-input | text | Headline (e.g. Grow Your Business on Autopilot) | False |
| Input / icon | data-testid=ad-copy-textarea | TEXTAREA | Primary text — the main message above your creative… | False |
| Input / icon | data-testid=ad-description-input | text | Description (optional, shows under the headline) | False |
| Learn More / Sign Up / Shop Now / Get Quote / Contact Us / Subscribe / Download / Book Now | data-testid=ad-cta-select | SELECT | ; options: Learn More, Sign Up, Shop Now, Get Quote, Contact Us, Subscribe, Download, Book Now | False |
| AI Suggest Variations | data-testid=suggest-variations-btn | BUTTON |  | False |
| + Add | data-testid=pt-variants-add | BUTTON |  | False |
| + Add | data-testid=hl-variants-add | BUTTON |  | False |
| + Add | data-testid=desc-variants-add | BUTTON |  | False |
| Run Simulation | data-testid=run-simulation-btn | BUTTON |  | False |
| Input / icon | data-testid=conversion-name-input | INPUT | Tag name (e.g. Website Lead) | False |
| Lead form submit / Purchase / Sign-up / Booked appointment / Contact | data-testid=conversion-category-select | SELECT | ; options: Lead form submit, Purchase, Sign-up, Booked appointment, Contact | False |
| Create tag | data-testid=create-conversion-btn | BUTTON |  | False |
| No auto-nurture | data-testid=nurture-select | SELECT | ; options: No auto-nurture | False |
| Save Draft | data-testid=save-draft-campaign | BUTTON |  | False |
| Launch Campaign | data-testid=launch-campaign-btn | BUTTON |  | False |
| Destination URL | data-testid=checklist-dest | BUTTON |  | False |
| Audience targeting · optional | data-testid=checklist-audience | BUTTON |  | False |
| Primary ad text | data-testid=checklist-copy | BUTTON |  | False |
| Image / video creative | data-testid=checklist-creatives | BUTTON |  | False |
| Lead Form / Collect leads directly on the platform | data-testid=lead-lead_form | BUTTON |  | False |
| Landing Page / Send to your website | data-testid=lead-destination_url | BUTTON |  | False |
| Lead collection method | data-testid=checklist-method | BUTTON |  | False |
| Form privacy URL | data-testid=checklist-privacy | BUTTON |  | False |
| Let Veluro build it /  / AI recommends high-intent audience segments tailored to this campaign. | data-testid=aud-mode-ai | BUTTON |  | False |
| Create a high-intent audience /  / Target people actively in-market, from your High-Intent Buyers. | data-testid=aud-mode-intent | BUTTON |  | False |
| Import a saved audience /  / Reuse an audience you already saved in Veluro. | data-testid=aud-mode-saved | BUTTON |  | False |
| Build a broad audience /  / Target by location, age, gender and interests. | data-testid=aud-mode-broad | BUTTON |  | False |
| Save as template | data-testid=lf-save-template | BUTTON |  | False |
| Input / icon | data-testid=lf-intro-title | text | Intro headline (e.g. Get your free quote) | False |
| Input / icon | data-testid=lf-intro | text | Intro text (e.g. Answer 3 quick questions to get your free quote) | False |
| Background image (optional) | data-testid=lf-intro-image-picker-open | button |  | False |
| Generate with AI | data-testid=lf-intro-image-ai | BUTTON |  | False |
| Full name | data-testid=lf-prefill-FULL_NAME | BUTTON |  | False |
| Email | data-testid=lf-prefill-EMAIL | BUTTON |  | False |
| Phone | data-testid=lf-prefill-PHONE | BUTTON |  | False |
| Company | data-testid=lf-prefill-COMPANY_NAME | BUTTON |  | False |
| Job title | data-testid=lf-prefill-JOB_TITLE | BUTTON |  | False |
| City | data-testid=lf-prefill-CITY | BUTTON |  | False |
| Suggest with AI | data-testid=lf-ai-suggest | BUTTON |  | False |
| Short answer / Multiple choice | data-testid=lf-custom-type | SELECT | ; options: Short answer, Multiple choice | False |
| Input / icon | data-testid=lf-custom-q | text | Question (e.g. What's your budget?) | False |
| Input / icon | data-testid=lf-custom-opts | text | — free text answer — | True |
| Add | data-testid=lf-add-custom | BUTTON |  | True |
| Input / icon | data-testid=lf-privacy | url | Privacy policy URL (required by Facebook) | False |
| Input / icon | data-testid=lf-privacy-text | text | Link text (default: "Privacy Policy") | False |
| Input / icon | data-testid=lf-thanks-title | text | Headline (default: "Thanks — we got it!") | False |
| Input / icon | data-testid=lf-thanks | text | Thank-you message (optional) | False |
| Input / icon | data-testid=lf-thanks-btn | text | Button text (default: "Visit website") | False |
| Input / icon | data-testid=lf-thanks-url | url | Button link (defaults to your destination URL) | False |
| Optimize it for me | data-testid=andromeda-autofix-btn | button |  | False |
| Add creatives | data-testid=andromeda-fix-creatives | button |  | False |
| Add variations | data-testid=andromeda-fix-copy-variants | button |  | False |
| No pixel | data-testid=pixel-select | SELECT | ; options: No pixel | False |
| Save as Paused on Meta | data-testid=push-meta-paused-btn | BUTTON |  | False |
| Make it Live | data-testid=push-meta-live-btn | BUTTON |  | False |
| Input / icon | data-testid=guided-close-btn | BUTTON |  | False |
| Connect ad account | data-testid=guided-connect-meta | BUTTON |  | False |
| Connect ad account | data-testid=guided-connect-google | BUTTON |  | False |
| Connect ad account | data-testid=guided-connect-linkedin | BUTTON |  | False |
| Connect ad account | data-testid=guided-connect-tiktok | BUTTON |  | False |
| I know what I'm doing — open the manual builder | data-testid=guided-manual-link | BUTTON |  | False |
| I need help | data-testid=guided-help-btn | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| POST | `/ads/audiences/lookalike` | create / edit / configuration; inspect before execution | api-0007 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/audiences/meta` | read candidate; inspect endpoint side effects | api-0008 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/audiences/suggest` | generation / analysis; may consume credits or store output | api-0009 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/budget/suggest` | generation / analysis; may consume credits or store output | api-0010 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/campaign-slots` | read candidate; inspect endpoint side effects | api-0011 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/campaigns` | read candidate; inspect endpoint side effects | api-0012 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/campaigns` | create / edit / configuration; inspect before execution | api-0013 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/campaigns/andromeda-review` | create / edit / configuration; inspect before execution | api-0014 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/campaigns/google-review` | create / edit / configuration; inspect before execution | api-0015 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/campaigns/quick-draft` | generation / analysis; may consume credits or store output | api-0016 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/campaigns/simulate` | generation / analysis; may consume credits or store output | api-0017 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/ads/campaigns/{parameter_1}` | delete / remove | api-0018 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/campaigns/{parameter_1}` | read candidate; inspect endpoint side effects | api-0019 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/ads/campaigns/{parameter_1}` | create / edit / configuration; inspect before execution | api-0020 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/campaigns/{parameter_1}/auto-pause-losers` | delivery / publishing / provider or workflow change | api-0021 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/campaigns/{parameter_1}/duplicate` | create / edit / configuration; inspect before execution | api-0022 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/campaigns/{parameter_1}/launch` | delivery / publishing / provider or workflow change | api-0023 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/campaigns/{parameter_1}/launch-meta` | delivery / publishing / provider or workflow change | api-0024 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/campaigns/{parameter_1}/meta-performance` | read candidate; inspect endpoint side effects | api-0025 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/campaigns/{parameter_1}/meta-{parameter_2}` | create / edit / configuration; inspect before execution | api-0026 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/campaigns/{parameter_1}/pause` | delivery / publishing / provider or workflow change | api-0027 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/campaigns/{parameter_1}/persona-ads` | create / edit / configuration; inspect before execution | api-0028 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/ads/campaigns/{parameter_1}/persona-ads/{parameter_2}` | delete / remove | api-0029 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/ads/campaigns/{parameter_1}/persona-ads/{parameter_2}` | create / edit / configuration; inspect before execution | api-0030 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/campaigns/{parameter_1}/persona-suggest` | generation / analysis; may consume credits or store output | api-0031 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/campaigns/{parameter_1}/readiness` | read candidate; inspect endpoint side effects | api-0032 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/connections` | read candidate; inspect endpoint side effects | api-0033 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/copy/suggest-variations` | generation / analysis; may consume credits or store output | api-0034 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/creatives/generate` | generation / analysis; may consume credits or store output | api-0035 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/creatives/generate-from-concept` | generation / analysis; may consume credits or store output | api-0036 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/creatives/generate-images` | generation / analysis; may consume credits or store output | api-0037 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/creatives/generate-images/{parameter_1}` | read candidate; inspect endpoint side effects | api-0038 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/creatives/generate-videos` | generation / analysis; may consume credits or store output | api-0039 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/daily-brief` | read candidate; inspect endpoint side effects | api-0040 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/google/keywords/suggest` | generation / analysis; may consume credits or store output | api-0041 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/guided/plan` | create / edit / configuration; inspect before execution | api-0042 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/lead-form/intro-image` | create / edit / configuration; inspect before execution | api-0043 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/lead-form/suggest-questions` | generation / analysis; may consume credits or store output | api-0044 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/lead-form/templates` | read candidate; inspect endpoint side effects | api-0045 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/lead-form/templates` | create / edit / configuration; inspect before execution | api-0046 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/meta-activation-request` | create / edit / configuration; inspect before execution | api-0047 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/meta-insights` | read candidate; inspect endpoint side effects | api-0048 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/meta-insights?date_preset=maximum` | read candidate; inspect endpoint side effects | api-0049 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/meta/identity` | read candidate; inspect endpoint side effects | api-0050 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/optimizer/cmo-settings` | read candidate; inspect endpoint side effects | api-0051 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/ads/optimizer/cmo-settings` | create / edit / configuration; inspect before execution | api-0052 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/optimizer/overview` | read candidate; inspect endpoint side effects | api-0053 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/optimizer/recommendations/{parameter_1}/approve` | delivery / publishing / provider or workflow change | api-0054 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/optimizer/recommendations/{parameter_1}/dismiss` | create / edit / configuration; inspect before execution | api-0055 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/optimizer/run-now` | create / edit / configuration; inspect before execution | api-0056 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/optimizer/settings` | create / edit / configuration; inspect before execution | api-0057 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/performance` | read candidate; inspect endpoint side effects | api-0058 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/performance/insights` | create / edit / configuration; inspect before execution | api-0059 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/pixels` | read candidate; inspect endpoint side effects | api-0060 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/pixels` | create / edit / configuration; inspect before execution | api-0061 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/pixels/meta` | read candidate; inspect endpoint side effects | api-0062 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/readiness-summary` | read candidate; inspect endpoint side effects | api-0063 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/stats` | read candidate; inspect endpoint side effects | api-0064 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/strategy/build` | create / edit / configuration; inspect before execution | api-0065 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/strategy/generate` | generation / analysis; may consume credits or store output | api-0066 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/ads/strategy/status/{parameter_1}` | read candidate; inspect endpoint side effects | api-0067 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/ads/tiktok/hook-lab` | create / edit / configuration; inspect before execution | api-0068 in [API catalog](../api/ENDPOINT_CATALOG.md) |
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
| POST | `/linkedin-marketing/launch-campaign` | delivery / publishing / provider or workflow change | api-0347 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/linkedin-marketing/push-audience` | create / edit / configuration; inspect before execution | api-0348 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `campaign-google-steps.json` — 1-google · 2026-09-08T17:28:47.858Z
- `campaign-google-steps.json` — 2-google · 2026-09-08T17:28:48.030Z
- `campaign-google-steps.json` — 3-google · 2026-09-08T17:28:48.163Z
- `campaign-google-steps.json` — 4-google · 2026-09-08T17:28:48.290Z
- `campaign-google-steps.json` — 5-google · 2026-09-08T17:28:48.419Z
- `campaign-google-steps.json` — 6-google · 2026-09-08T17:28:48.546Z
- `campaign-google-steps.json` — 7-google · 2026-09-08T17:28:48.677Z
- `campaign-manual-steps.json` — 1-platform · 2026-09-08T17:10:03.279Z
- `campaign-manual-steps.json` — 2-goal · 2026-09-08T17:10:03.322Z
- `campaign-manual-steps.json` — 2-meta-leads · 2026-09-08T17:10:38.769Z
- `campaign-manual-steps.json` — 3-meta-leads · 2026-09-08T17:10:38.949Z
- `campaign-manual-steps.json` — 4-meta-leads · 2026-09-08T17:10:39.123Z
- `campaign-manual-steps.json` — 5-meta-leads · 2026-09-08T17:10:39.306Z
- `campaign-manual-steps.json` — 6-meta-leads · 2026-09-08T17:10:39.492Z
- `campaign-manual-steps.json` — 7-meta-leads · 2026-09-08T17:10:39.683Z
- `campaign-guided.json` — campaign-entry · 2026-09-08T17:09:13.614Z
- `campaign-guided.json` — guided-meta · 2026-09-08T17:09:14.243Z
- `ui-batch-01.json` — /campaigns · 2026-09-08T17:00:52.569Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
