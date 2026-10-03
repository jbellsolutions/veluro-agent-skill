# High-Intent Buyers and advanced search

**Route:** `/intent` · [Open Veluro](https://veluro.ai/intent)

**When:** Use to discover/filter potential buyers and prepare an activation audience.

**Prerequisites:** Approved audience, intended use, geography, topic meaning and lead allowance.

## Agent procedure

1. Choose Business buyers, Consumers or filter-only Advanced search.
2. For intent, search at least three characters and pick up to five relevant topic IDs; avoid irrelevant named-company matches.
3. Apply recency, state/city/ZIP and appropriate B2B or B2C filters.
4. Name the tracker and review its allocation before building; the observed default is large.
5. Record audience ID and poll until complete; inspect counts, sample quality and applied filters.
6. Export or activate only the intended audience, verifying provider match, CRM mapping and delivery authorization.

## Success and recovery

Completion proof: The returned list matches intended filters and its source/quality are understood.

No audience generation/export or match-rate test was run. Deletion releases quota next cycle. Advanced search is not intent evidence.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

3 captured screen states; 167 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Input / icon | data-testid=intent-help-btn | BUTTON |  | False |
| Complete profile | data-testid=complete-profile-btn | BUTTON |  | False |
| Track Intent | data-testid=tab-build | button |  | False |
| My Trackers / 1 | data-testid=tab-audiences | button |  | False |
| Input / icon | data-testid=auto-build-url-input | INPUT | yourwebsite.com | False |
| Build it for me | data-testid=auto-build-btn | BUTTON |  | True |
| Business buyers /  / Decision-makers at companies researching what you sell | data-testid=type-card-b2b | BUTTON |  | False |
| Consumers /  / Homeowners & individuals shopping for your services | data-testid=type-card-b2c | BUTTON |  | False |
| Advanced search /  / Build a list with filters only — no buying topics | data-testid=type-card-advanced_search | BUTTON |  | False |
| Let Veluro pick | data-testid=veluro-pick-btn | BUTTON |  | False |
| Input / icon | data-testid=topic-search-input | INPUT | Try "roofing", "solar", "CRM software"... | False |
| Input / icon | data-testid=icp-desc-input | TEXTAREA | e.g. "Roofing contractors in TX and FL with 50-500 employees, targeting owners and VPs" or "Homeowners in California aged 35-54, household income $100k+" | False |
| Build filters from this | data-testid=icp-build-btn | BUTTON |  | True |
| Advanced filters / 1 applied | data-testid=toggle-advanced-filters | BUTTON |  | False |
| AK | data-testid=chip-states-ak | button |  | False |
| AL | data-testid=chip-states-al | button |  | False |
| AR | data-testid=chip-states-ar | button |  | False |
| AZ | data-testid=chip-states-az | button |  | False |
| CA | data-testid=chip-states-ca | button |  | False |
| CO | data-testid=chip-states-co | button |  | False |
| CT | data-testid=chip-states-ct | button |  | False |
| DE | data-testid=chip-states-de | button |  | False |
| FL | data-testid=chip-states-fl | button |  | False |
| GA | data-testid=chip-states-ga | button |  | False |
| HI | data-testid=chip-states-hi | button |  | False |
| IA | data-testid=chip-states-ia | button |  | False |
| ID | data-testid=chip-states-id | button |  | False |
| IL | data-testid=chip-states-il | button |  | False |
| IN | data-testid=chip-states-in | button |  | False |
| KS | data-testid=chip-states-ks | button |  | False |
| KY | data-testid=chip-states-ky | button |  | False |
| LA | data-testid=chip-states-la | button |  | False |
| MA | data-testid=chip-states-ma | button |  | False |
| MD | data-testid=chip-states-md | button |  | False |
| ME | data-testid=chip-states-me | button |  | False |
| MI | data-testid=chip-states-mi | button |  | False |
| MN | data-testid=chip-states-mn | button |  | False |
| MO | data-testid=chip-states-mo | button |  | False |
| MS | data-testid=chip-states-ms | button |  | False |
| MT | data-testid=chip-states-mt | button |  | False |
| NC | data-testid=chip-states-nc | button |  | False |
| ND | data-testid=chip-states-nd | button |  | False |
| NE | data-testid=chip-states-ne | button |  | False |
| NH | data-testid=chip-states-nh | button |  | False |
| NJ | data-testid=chip-states-nj | button |  | False |
| NM | data-testid=chip-states-nm | button |  | False |
| NV | data-testid=chip-states-nv | button |  | False |
| NY | data-testid=chip-states-ny | button |  | False |
| OH | data-testid=chip-states-oh | button |  | False |
| OK | data-testid=chip-states-ok | button |  | False |
| OR | data-testid=chip-states-or | button |  | False |
| PA | data-testid=chip-states-pa | button |  | False |
| RI | data-testid=chip-states-ri | button |  | False |
| SC | data-testid=chip-states-sc | button |  | False |
| SD | data-testid=chip-states-sd | button |  | False |
| TN | data-testid=chip-states-tn | button |  | False |
| TX | data-testid=chip-states-tx | button |  | False |
| UT | data-testid=chip-states-ut | button |  | False |
| VA | data-testid=chip-states-va | button |  | False |
| VT | data-testid=chip-states-vt | button |  | False |
| WA | data-testid=chip-states-wa | button |  | False |
| WI | data-testid=chip-states-wi | button |  | False |
| WV | data-testid=chip-states-wv | button |  | False |
| WY | data-testid=chip-states-wy | button |  | False |
| Input / icon | data-testid=city-search-input | INPUT | Search a city, e.g. Florence | False |
| Input / icon | data-testid=zip-input | INPUT | Enter a 5-digit ZIP | False |
| Add | data-testid=add-zip-btn | button |  | True |
| 18-24 | data-testid=chip-age-range-18-24 | button |  | False |
| 25-34 | data-testid=chip-age-range-25-34 | button |  | False |
| 35-44 | data-testid=chip-age-range-35-44 | button |  | False |
| 45-54 | data-testid=chip-age-range-45-54 | button |  | False |
| 55-64 | data-testid=chip-age-range-55-64 | button |  | False |
| 65 AND OLDER | data-testid=chip-age-range-65-and-older | button |  | False |
| MALE | data-testid=chip-gender-m | button |  | False |
| FEMALE | data-testid=chip-gender-f | button |  | False |
| MARRIED | data-testid=chip-marital-status-y | button |  | False |
| NOT MARRIED | data-testid=chip-marital-status-n | button |  | False |
| LESS THAN $20,000 | data-testid=chip-household-income-less-than-20-000 | button |  | False |
| $20,000 TO $44,999 | data-testid=chip-household-income--20-000-to-44-999 | button |  | False |
| $45,000 TO $59,999 | data-testid=chip-household-income--45-000-to-59-999 | button |  | False |
| $60,000 TO $74,999 | data-testid=chip-household-income--60-000-to-74-999 | button |  | False |
| $75,000 TO $99,999 | data-testid=chip-household-income--75-000-to-99-999 | button |  | False |
| $100,000 TO $149,999 | data-testid=chip-household-income--100-000-to-149-999 | button |  | False |
| $150,000 TO $199,999 | data-testid=chip-household-income--150-000-to-199-999 | button |  | False |
| $200,000 TO $249,999 | data-testid=chip-household-income--200-000-to-249-999 | button |  | False |
| $250,000+ | data-testid=chip-household-income--250-000- | button |  | False |
| -$20,000 TO -$2,500 | data-testid=chip-net-worth--20-000-to-2-500 | button |  | False |
| -$2,499 TO $2,499 | data-testid=chip-net-worth--2-499-to-2-499 | button |  | False |
| $2,500 TO $24,999 | data-testid=chip-net-worth--2-500-to-24-999 | button |  | False |
| $25,000 TO $49,999 | data-testid=chip-net-worth--25-000-to-49-999 | button |  | False |
| $50,000 TO $74,999 | data-testid=chip-net-worth--50-000-to-74-999 | button |  | False |
| $75,000 TO $99,999 | data-testid=chip-net-worth--75-000-to-99-999 | button |  | False |
| $100,000 TO $149,999 | data-testid=chip-net-worth--100-000-to-149-999 | button |  | False |
| $150,000 TO $249,999 | data-testid=chip-net-worth--150-000-to-249-999 | button |  | False |
| $250,000 TO $374,999 | data-testid=chip-net-worth--250-000-to-374-999 | button |  | False |
| $375,000 TO $499,999 | data-testid=chip-net-worth--375-000-to-499-999 | button |  | False |
| $500,000 TO $749,999 | data-testid=chip-net-worth--500-000-to-749-999 | button |  | False |
| $750,000 TO $999,999 | data-testid=chip-net-worth--750-000-to-999-999 | button |  | False |
| MORE THAN $1,000,000 | data-testid=chip-net-worth-more-than-1-000-000 | button |  | False |
| Any | Use observed accessible label/placeholder | button |  | False |
| Input / icon | data-testid=audience-name-input | INPUT | "CA Roofing Buyers — Apr 2026" | False |
| Input / icon | data-testid=max-leads-input | number |  | False |
| Track this intent | data-testid=build-audience-btn | BUTTON |  | True |
| My Trackers / 0 | data-testid=tab-audiences | button |  | False |
| CXO | data-testid=chip-seniority-cxo | button |  | False |
| VP | data-testid=chip-seniority-vp | button |  | False |
| DIRECTOR | data-testid=chip-seniority-director | button |  | False |
| MANAGER | data-testid=chip-seniority-manager | button |  | False |
| STAFF | data-testid=chip-seniority-staff | button |  | False |
| ADMINISTRATIVE | data-testid=chip-department-administrative | button |  | False |
| ENGINEERING | data-testid=chip-department-engineering | button |  | False |
| EXECUTIVE | data-testid=chip-department-executive | button |  | False |
| FINANCE | data-testid=chip-department-finance | button |  | False |
| MARKETING | data-testid=chip-department-marketing | button |  | False |
| SALES | data-testid=chip-department-sales | button |  | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | e.g. VP Marketing, CFO | False |
| Input / icon | Use observed accessible label/placeholder | number | 500; min: 0 | False |
| Input / icon | Use observed accessible label/placeholder | number | 10000; min: 0 | False |
| 1 TO 10 | data-testid=chip-company-size-1-to-10 | button |  | False |
| 11 TO 25 | data-testid=chip-company-size-11-to-25 | button |  | False |
| 26 TO 50 | data-testid=chip-company-size-26-to-50 | button |  | False |
| 51 TO 100 | data-testid=chip-company-size-51-to-100 | button |  | False |
| 101 TO 250 | data-testid=chip-company-size-101-to-250 | button |  | False |
| 251 TO 500 | data-testid=chip-company-size-251-to-500 | button |  | False |
| 501 TO 1000 | data-testid=chip-company-size-501-to-1000 | button |  | False |
| 1001 TO 5000 | data-testid=chip-company-size-1001-to-5000 | button |  | False |
| 5001 TO 10000 | data-testid=chip-company-size-5001-to-10000 | button |  | False |
| 10000+ | data-testid=chip-company-size-10000- | button |  | False |
| UNDER 1 MILLION | data-testid=chip-company-revenue-under-1-million | button |  | False |
| 1 MILLION TO 5 MILLION | data-testid=chip-company-revenue-1-million-to-5-million | button |  | False |
| 5 MILLION TO 10 MILLION | data-testid=chip-company-revenue-5-million-to-10-million | button |  | False |
| 10 MILLION TO 25 MILLION | data-testid=chip-company-revenue-10-million-to-25-million | button |  | False |
| 25 MILLION TO 50 MILLION | data-testid=chip-company-revenue-25-million-to-50-million | button |  | False |
| 50 MILLION TO 100 MILLION | data-testid=chip-company-revenue-50-million-to-100-million | button |  | False |
| 100 MILLION TO 250 MILLION | data-testid=chip-company-revenue-100-million-to-250-million | button |  | False |
| 250 MILLION TO 500 MILLION | data-testid=chip-company-revenue-250-million-to-500-million | button |  | False |
| 500 MILLION TO 1 BILLION | data-testid=chip-company-revenue-500-million-to-1-billion | button |  | False |
| 1 BILLION AND OVER | data-testid=chip-company-revenue-1-billion-and-over | button |  | False |
| SOFTWARE | data-testid=chip-company-industries-software | button |  | False |
| INFORMATION TECHNOLOGY | data-testid=chip-company-industries-information-technology | button |  | False |
| MARKETING & ADVERTISING | data-testid=chip-company-industries-marketing-advertising | button |  | False |
| FINANCIAL SERVICES | data-testid=chip-company-industries-financial-services | button |  | False |
| INSURANCE | data-testid=chip-company-industries-insurance | button |  | False |
| REAL ESTATE | data-testid=chip-company-industries-real-estate | button |  | False |
| CONSTRUCTION | data-testid=chip-company-industries-construction | button |  | False |
| HEALTHCARE | data-testid=chip-company-industries-healthcare | button |  | False |
| MANUFACTURING | data-testid=chip-company-industries-manufacturing | button |  | False |
| RETAIL | data-testid=chip-company-industries-retail | button |  | False |
| E-COMMERCE | data-testid=chip-company-industries-e-commerce | button |  | False |
| EDUCATION | data-testid=chip-company-industries-education | button |  | False |
| PROFESSIONAL SERVICES | data-testid=chip-company-industries-professional-services | button |  | False |
| CONSULTING | data-testid=chip-company-industries-consulting | button |  | False |
| LEGAL | data-testid=chip-company-industries-legal | button |  | False |
| AUTOMOTIVE | data-testid=chip-company-industries-automotive | button |  | False |
| HOSPITALITY | data-testid=chip-company-industries-hospitality | button |  | False |
| FOOD & BEVERAGE | data-testid=chip-company-industries-food-beverage | button |  | False |
| TELECOMMUNICATIONS | data-testid=chip-company-industries-telecommunications | button |  | False |
| ENERGY & UTILITIES | data-testid=chip-company-industries-energy-utilities | button |  | False |
| LOGISTICS & SUPPLY CHAIN | data-testid=chip-company-industries-logistics-supply-chain | button |  | False |
| MEDIA & ENTERTAINMENT | data-testid=chip-company-industries-media-entertainment | button |  | False |
| NONPROFIT | data-testid=chip-company-industries-nonprofit | button |  | False |
| TRAVEL & LEISURE | data-testid=chip-company-industries-travel-leisure | button |  | False |
| AGRICULTURE | data-testid=chip-company-industries-agriculture | button |  | False |
| HOME SERVICES | data-testid=chip-company-industries-home-services | button |  | False |
| FITNESS & WELLNESS | data-testid=chip-company-industries-fitness-wellness | button |  | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | e.g. acme, salesforce | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | e.g. shopify.com, .edu | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/intent/ad-drafts` | read candidate; inspect endpoint side effects | api-0267 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/intent/ad-drafts/{parameter_1}` | delete / remove | api-0268 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/intent/ad-drafts/{parameter_1}` | read candidate; inspect endpoint side effects | api-0269 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/intent/ad-drafts/{parameter_1}/creatives/{parameter_2}` | delete / remove | api-0270 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PATCH | `/intent/ad-drafts/{parameter_1}/creatives/{parameter_2}` | generation / analysis; may consume credits or store output | api-0271 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intent/ad-drafts/{parameter_1}/creatives/{parameter_2}/revise` | generation / analysis; may consume credits or store output | api-0272 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/intent/audiences` | read candidate; inspect endpoint side effects | api-0273 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intent/audiences/build` | create / edit / configuration; inspect before execution | api-0274 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/intent/audiences/{parameter_1}` | delete / remove | api-0275 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/intent/audiences/{parameter_1}` | create / edit / configuration; inspect before execution | api-0276 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intent/audiences/{parameter_1}/activate-email-sequence` | delivery / publishing / provider or workflow change | api-0277 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intent/audiences/{parameter_1}/activate-fb-ads` | delivery / publishing / provider or workflow change | api-0278 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intent/audiences/{parameter_1}/activate-linkedin-ads` | delivery / publishing / provider or workflow change | api-0279 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intent/audiences/{parameter_1}/activate-linkedin-dm-sequence` | delivery / publishing / provider or workflow change | api-0280 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/intent/audiences/{parameter_1}/activation-status/{parameter_2}` | read candidate; inspect endpoint side effects | api-0281 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/intent/audiences/{parameter_1}/drafts` | read candidate; inspect endpoint side effects | api-0282 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/intent/audiences/{parameter_1}/export-csv` | read candidate; inspect endpoint side effects | api-0283 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intent/audiences/{parameter_1}/regenerate-fb-creatives` | generation / analysis; may consume credits or store output | api-0284 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/intent/audiences/{parameter_1}?li_active={parameter_2}` | read candidate; inspect endpoint side effects | api-0285 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intent/auto-build` | create / edit / configuration; inspect before execution | api-0286 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intent/auto-suggest-categories` | generation / analysis; may consume credits or store output | api-0287 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/intent/city-search` | read candidate; inspect endpoint side effects | api-0288 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intent/custom-ads/generate` | generation / analysis; may consume credits or store output | api-0289 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intent/describe-icp` | create / edit / configuration; inspect before execution | api-0290 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intent/leads/generate-outreach` | generation / analysis; may consume credits or store output | api-0291 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/intent/meta/connection` | read candidate; inspect endpoint side effects | api-0292 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/intent/provider-status` | read candidate; inspect endpoint side effects | api-0293 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/intent/quota` | read candidate; inspect endpoint side effects | api-0294 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/intent/reservations/me` | read candidate; inspect endpoint side effects | api-0295 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intent/reservations/{parameter_1}/claim` | create / edit / configuration; inspect before execution | api-0296 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/intent/status` | read candidate; inspect endpoint side effects | api-0297 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intent/targeting/reach-estimate` | create / edit / configuration; inspect before execution | api-0298 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intent/targeting/save-audience` | create / edit / configuration; inspect before execution | api-0299 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/intent/targeting/saved-audiences` | read candidate; inspect endpoint side effects | api-0300 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/intent/targeting/saved-audiences/{parameter_1}` | delete / remove | api-0301 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/intent/topics/search?q={parameter_1}&scope={parameter_2}` | read candidate; inspect endpoint side effects | api-0302 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intent/zip-audience` | create / edit / configuration; inspect before execution | api-0303 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/intent/zip-audience/preview` | create / edit / configuration; inspect before execution | api-0304 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `intent-b2c-filters.json` — B2C filters · 2026-09-08T17:16:11.633Z
- `dialogs-02.json` — toggle-advanced-filters · 2026-09-08T17:13:48.861Z
- `ui-batch-01.json` — /intent · 2026-09-08T17:00:54.142Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
