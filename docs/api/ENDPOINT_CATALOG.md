# Discovered API call catalog

Base: `https://veluro.ai/api`. Source observed; not a vendor-issued schema. Read [API guide](API_GUIDE.md) first.

Dynamic placeholders do not establish parameter types. Request expressions are the literal shapes found in the app and must be resolved against a current verified payload before use. Missing body fields mean unknown, not that no fields are required. Observed HTTP statuses prove only those read responses.

## api-0001 · POST /ad-lab/hormozi-copy

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/8947.ffec9124.chunk.js` offset 59341. Path expression: `/ad-lab/hormozi-copy`.

Request/configuration expression (source only):
```javascript
{offer:e,audience:a}
```

## api-0002 · GET /ad-lab/jobs/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/8947.ffec9124.chunk.js` offset 50155. Path expression: `/ad-lab/jobs/{t}`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/8947.ffec9124.chunk.js` offset 55638. Path expression: `/ad-lab/jobs/{e.data.job_id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0003 · POST /ad-lab/one-click

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/8947.ffec9124.chunk.js` offset 55412. Path expression: `/ad-lab/one-click`.

Request/configuration expression (source only):
```javascript
(0,s.A)((0,s.A)({},a),{},{budget:parseFloat(a.budget)||20,image_asset_id:null===l||void 0===l?void 0:l.asset_id})
```

## api-0004 · POST /ad-lab/silence-trim

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/8947.ffec9124.chunk.js` offset 63611. Path expression: `/ad-lab/silence-trim`.

Request/configuration expression (source only):
```javascript
{asset_id:a.asset_id,aspect:r}
```

## api-0005 · POST /ad-lab/template-render

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/8947.ffec9124.chunk.js` offset 69790. Path expression: `/ad-lab/template-render`.

Request/configuration expression (source only):
```javascript
(0,s.A)((0,s.A)({template_id:l,format:n},d),{},{music_track:d.music_track||null,image_asset_id:null===m||void 0===m?void 0:m.asset_id,logo_asset_id:null===h||void 0===h?void 0:h.asset_id})
```

## api-0006 · GET /ad-lab/templates

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/8947.ffec9124.chunk.js` offset 65508. Path expression: `/ad-lab/templates`.

No second argument at this call site. This does not establish the complete server contract.

## api-0007 · POST /ads/audiences/lookalike

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 104690. Path expression: `/ads/audiences/lookalike`.

Request/configuration expression (source only):
```javascript
{origin_audience_id:c.id,ratio:Number(m)/100,country:p,name:b.trim()}
```

Source: `bundles/5027.62c03e58.chunk.js` offset 38495. Path expression: `/ads/audiences/lookalike`.

Request/configuration expression (source only):
```javascript
{origin_audience_id:e,ratio:.01,country:"US",name:"".concat(t||"Intent audience"," \u2014 Lookalike 1% US")}
```

## api-0008 · GET /ads/audiences/meta

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 104357. Path expression: `/ads/audiences/meta`.

No second argument at this call site. This does not establish the complete server contract.

## api-0009 · POST /ads/audiences/suggest

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 222657. Path expression: `/ads/audiences/suggest`.

Request/configuration expression (source only):
```javascript
{platform:ee,campaign_type:xe}
```

## api-0010 · POST /ads/budget/suggest

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 249986. Path expression: `/ads/budget/suggest`.

Request/configuration expression (source only):
```javascript
{platform:ee,campaign_type:xe}
```

## api-0011 · GET /ads/campaign-slots

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 303330. Path expression: `/ads/campaign-slots`.

No second argument at this call site. This does not establish the complete server contract.

## api-0012 · GET /ads/campaigns

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 161349. Path expression: `/ads/campaigns`.

No second argument at this call site. This does not establish the complete server contract.

## api-0013 · POST /ads/campaigns

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 224519. Path expression: `/ads/campaigns`.

Request/configuration expression (source only):
```javascript
a
```

## api-0014 · POST /ads/campaigns/andromeda-review

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 214985. Path expression: `/ads/campaigns/andromeda-review`.

Request/configuration expression (source only):
```javascript
{campaign_type:xe,lead_method:ge,creative_count:gt.length,video_count:gt.filter(e=>"video"===e.kind).length,pt_variant_count:1+Pt.filter(Boolean).length,hl_variant_count:1+Vt.filter(Boolean).length,selected_audience_count:Ae.length,geo_count:je.length,auto_optimize:Ue,budget_monthly:parseFloat(Oe)||0,pixel_id:ta||null}
```

## api-0015 · POST /ads/campaigns/google-review

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 215463. Path expression: `/ads/campaigns/google-review`.

Request/configuration expression (source only):
```javascript
{hl_count:1+Vt.filter(Boolean).length,desc_count:(jt?1:0)+Ot.filter(Boolean).length,kw_exact:Se.length,kw_phrase:Me.length,kw_negative:Ie.length,geo_count:je.length,budget_monthly:parseFloat(Oe)||0,headlines:[vt,...Vt].filter(Boolean),keywords:[...Se,...Me]}
```

## api-0016 · POST /ads/campaigns/quick-draft

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/4278.c2617230.chunk.js` offset 36602. Path expression: `/ads/campaigns/quick-draft`.

Request/configuration expression (source only):
```javascript
{image_url:t,name:"Image ad",platform:"meta"}
```

## api-0017 · POST /ads/campaigns/simulate

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 277653. Path expression: `/ads/campaigns/simulate`.

Request/configuration expression (source only):
```javascript
{platform:ee,campaign_type:xe,budget_monthly:parseFloat(Oe)||1e3,audience_size:"broad"===Za||Ae.length>2?"large":Ae.length>0||rs?"medium":"small"}
```

## api-0018 · DELETE /ads/campaigns/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 184418. Path expression: `/ads/campaigns/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0019 · GET /ads/campaigns/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 32961. Path expression: `/ads/campaigns/{e}`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 163380. Path expression: `/ads/campaigns/{t}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0020 · PUT /ads/campaigns/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 50640. Path expression: `/ads/campaigns/{U.campaignId}`.

Request/configuration expression (source only):
```javascript
{destination_url:L.website_url.trim()}
```

Source: `bundles/1482.a74c6ab9.chunk.js` offset 224444. Path expression: `/ads/campaigns/{ct}`.

Request/configuration expression (source only):
```javascript
a
```

## api-0021 · POST /ads/campaigns/{parameter_1}/auto-pause-losers

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 200844. Path expression: `/ads/campaigns/{t.campaign_id}/auto-pause-losers`.

Request/configuration expression (source only):
```javascript
{enabled:e,budget_shift:c}
```

Source: `bundles/1482.a74c6ab9.chunk.js` offset 202338. Path expression: `/ads/campaigns/{t.campaign_id}/auto-pause-losers`.

Request/configuration expression (source only):
```javascript
{enabled:d,budget_shift:e}
```

## api-0022 · POST /ads/campaigns/{parameter_1}/duplicate

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 183926. Path expression: `/ads/campaigns/{e}/duplicate`.

No second argument at this call site. This does not establish the complete server contract.

## api-0023 · POST /ads/campaigns/{parameter_1}/launch

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 162581. Path expression: `/ads/campaigns/{e.campaign_id}/launch`.

Request/configuration expression (source only):
```javascript
t?{override_readiness:!0}:{}
```

## api-0024 · POST /ads/campaigns/{parameter_1}/launch-meta

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 50753. Path expression: `/ads/campaigns/{U.campaignId}/launch-meta`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 163045. Path expression: `/ads/campaigns/{t}/launch-meta`.

Request/configuration expression (source only):
```javascript
{mode:e,ad_account_id:ie||void 0,page_id:xe||void 0,override_readiness:!(null===Se||void 0===Se||null===(s=Se.critical)||void 0===s||!s.length)||void 0}
```

Source: `bundles/1482.a74c6ab9.chunk.js` offset 226397. Path expression: `/ads/campaigns/{e}/launch-meta`.

Request/configuration expression (source only):
```javascript
{mode:t,ad_account_id:de||void 0}
```

## api-0025 · GET /ads/campaigns/{parameter_1}/meta-performance

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 197955. Path expression: `/ads/campaigns/{t.campaign_id}/meta-performance`.

No second argument at this call site. This does not establish the complete server contract.

## api-0026 · POST /ads/campaigns/{parameter_1}/meta-{parameter_2}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 165415. Path expression: `/ads/campaigns/{e.campaign_id}/meta-{t}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0027 · POST /ads/campaigns/{parameter_1}/pause

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 182985. Path expression: `/ads/campaigns/{e}/pause`.

No second argument at this call site. This does not establish the complete server contract.

## api-0028 · POST /ads/campaigns/{parameter_1}/persona-ads

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 114633. Path expression: `/ads/campaigns/{t.campaign_id}/persona-ads`.

Request/configuration expression (source only):
```javascript
{roles:e}
```

## api-0029 · DELETE /ads/campaigns/{parameter_1}/persona-ads/{parameter_2}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 116697. Path expression: `/ads/campaigns/{t.campaign_id}/persona-ads/{e.persona_id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0030 · PUT /ads/campaigns/{parameter_1}/persona-ads/{parameter_2}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 118312. Path expression: `/ads/campaigns/{t.campaign_id}/persona-ads/{e.persona_id}`.

Request/configuration expression (source only):
```javascript
a
```

## api-0031 · POST /ads/campaigns/{parameter_1}/persona-suggest

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 109988. Path expression: `/ads/campaigns/{t.campaign_id}/persona-suggest`.

No second argument at this call site. This does not establish the complete server contract.

## api-0032 · GET /ads/campaigns/{parameter_1}/readiness

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 123575. Path expression: `/ads/campaigns/{t.campaign_id}/readiness`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 160539. Path expression: `/ads/campaigns/{ee.campaign_id}/readiness`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 162250. Path expression: `/ads/campaigns/{e.campaign_id}/readiness`.

No second argument at this call site. This does not establish the complete server contract.

## api-0033 · GET /ads/connections

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 32623. Path expression: `/ads/connections`.

No second argument at this call site. This does not establish the complete server contract.

## api-0034 · POST /ads/copy/suggest-variations

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 217225. Path expression: `/ads/copy/suggest-variations`.

Request/configuration expression (source only):
```javascript
{campaign_name:he,campaign_type:xe,platform:ee,current_copy:$e||void 0}
```

Source: `bundles/1482.a74c6ab9.chunk.js` offset 260927. Path expression: `/ads/copy/suggest-variations`.

Request/configuration expression (source only):
```javascript
{campaign_name:he,campaign_type:xe,platform:ee,current_copy:{primary_text:$e,headline:vt,description:jt}}
```

## api-0035 · POST /ads/creatives/generate

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 257440. Path expression: `/ads/creatives/generate`.

Request/configuration expression (source only):
```javascript
{platform:ee,campaign_type:xe,description:he}
```

## api-0036 · POST /ads/creatives/generate-from-concept

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 78459. Path expression: `/ads/creatives/generate-from-concept`.

Request/configuration expression (source only):
```javascript
{idea:a.data.next_step.idea,title:a.data.next_step.title}
```

Source: `bundles/1482.a74c6ab9.chunk.js` offset 263219. Path expression: `/ads/creatives/generate-from-concept`.

Request/configuration expression (source only):
```javascript
{title:t.title,idea:t.idea}
```

## api-0037 · POST /ads/creatives/generate-images

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 97670. Path expression: `/ads/creatives/generate-images`.

Request/configuration expression (source only):
```javascript
{prompt:x.trim(),count:g,aspect:u,apply_brand:v,platform:l,headline:w.trim(),cta:y.trim()}
```

Source: `bundles/1482.a74c6ab9.chunk.js` offset 217928. Path expression: `/ads/creatives/generate-images`.

Request/configuration expression (source only):
```javascript
{prompt:t,count:e,aspect:"1:1",headline:vt||"",cta:(null===(i=Lt.find(e=>{let[t]=e;return t===Nt}))||void 0===i?void 0:i[1])||""}
```

## api-0038 · GET /ads/creatives/generate-images/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 97947. Path expression: `/ads/creatives/generate-images/{t.data.job_id}`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 218184. Path expression: `/ads/creatives/generate-images/{a.data.job_id}`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 218985. Path expression: `/ads/creatives/generate-images/{s.data.job_id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0039 · POST /ads/creatives/generate-videos

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 97548. Path expression: `/ads/creatives/generate-videos`.

Request/configuration expression (source only):
```javascript
{prompt:x.trim(),count:g,aspect:u,duration:_,quality:C,platform:l}
```

Source: `bundles/1482.a74c6ab9.chunk.js` offset 218611. Path expression: `/ads/creatives/generate-videos`.

Request/configuration expression (source only):
```javascript
{prompt:a,count:1,aspect:"9:16",duration:8,quality:"standard"}
```

## api-0040 · GET /ads/daily-brief

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 161494. Path expression: `/ads/daily-brief`.

No second argument at this call site. This does not establish the complete server contract.

## api-0041 · POST /ads/google/keywords/suggest

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 237005. Path expression: `/ads/google/keywords/suggest`.

Request/configuration expression (source only):
```javascript
{campaign_name:he,campaign_type:xe,destination_url:fe}
```

## api-0042 · POST /ads/guided/plan

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 145037. Path expression: `/ads/guided/plan`.

Request/configuration expression (source only):
```javascript
{platform:w,website_url:A.trim(),goal:M,ideal_customer:I.trim(),notes:T.trim()}
```

## api-0043 · POST /ads/lead-form/intro-image

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 268190. Path expression: `/ads/lead-form/intro-image`.

No second argument at this call site. This does not establish the complete server contract.

## api-0044 · POST /ads/lead-form/suggest-questions

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 270004. Path expression: `/ads/lead-form/suggest-questions`.

No second argument at this call site. This does not establish the complete server contract.

## api-0045 · GET /ads/lead-form/templates

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 221019. Path expression: `/ads/lead-form/templates`.

No second argument at this call site. This does not establish the complete server contract.

## api-0046 · POST /ads/lead-form/templates

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 265697. Path expression: `/ads/lead-form/templates`.

Request/configuration expression (source only):
```javascript
{name:e,spec:{intro_title:_a,intro_body:Na,intro_image_url:Ca,privacy_policy_url:fa,privacy_link_text:ja,thank_you_title:La,thank_you_body:za,thank_you_button_text:Pa,thank_you_url:Ea,questions:ba}}
```

## api-0047 · POST /ads/meta-activation-request

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 195405. Path expression: `/ads/meta-activation-request`.

No second argument at this call site. This does not establish the complete server contract.

## api-0048 · GET /ads/meta-insights

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 58091. Path expression: `/ads/meta-insights`.

No second argument at this call site. This does not establish the complete server contract.

## api-0049 · GET /ads/meta-insights?date_preset=maximum

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 58253. Path expression: `/ads/meta-insights?date_preset=maximum`.

No second argument at this call site. This does not establish the complete server contract.

## api-0050 · GET /ads/meta/identity

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 208181. Path expression: `/ads/meta/identity`.

No second argument at this call site. This does not establish the complete server contract.

## api-0051 · GET /ads/optimizer/cmo-settings

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 71285. Path expression: `/ads/optimizer/cmo-settings`.

No second argument at this call site. This does not establish the complete server contract.

## api-0052 · PUT /ads/optimizer/cmo-settings

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 73974. Path expression: `/ads/optimizer/cmo-settings`.

Request/configuration expression (source only):
```javascript
e
```

## api-0053 · GET /ads/optimizer/overview

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 74817. Path expression: `/ads/optimizer/overview`.

No second argument at this call site. This does not establish the complete server contract.

## api-0054 · POST /ads/optimizer/recommendations/{parameter_1}/approve

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 78226. Path expression: `/ads/optimizer/recommendations/{e.rec_id}/approve`.

No second argument at this call site. This does not establish the complete server contract.

## api-0055 · POST /ads/optimizer/recommendations/{parameter_1}/dismiss

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 79601. Path expression: `/ads/optimizer/recommendations/{e.rec_id}/dismiss`.

No second argument at this call site. This does not establish the complete server contract.

## api-0056 · POST /ads/optimizer/run-now

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 76304. Path expression: `/ads/optimizer/run-now`.

No second argument at this call site. This does not establish the complete server contract.

## api-0057 · POST /ads/optimizer/settings

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 75056. Path expression: `/ads/optimizer/settings`.

Request/configuration expression (source only):
```javascript
(0,u.A)({campaign_id:e.campaign_id},t)
```

Source: `bundles/1482.a74c6ab9.chunk.js` offset 81308. Path expression: `/ads/optimizer/settings`.

Request/configuration expression (source only):
```javascript
{campaign_id:e.campaign_id,mode:t}
```

## api-0058 · GET /ads/performance

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 57964. Path expression: `/ads/performance`.

No second argument at this call site. This does not establish the complete server contract.

## api-0059 · POST /ads/performance/insights

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 65374. Path expression: `/ads/performance/insights`.

No second argument at this call site. This does not establish the complete server contract.

## api-0060 · GET /ads/pixels

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 161409. Path expression: `/ads/pixels`.

No second argument at this call site. This does not establish the complete server contract.

## api-0061 · POST /ads/pixels

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 172303. Path expression: `/ads/pixels`.

No second argument at this call site. This does not establish the complete server contract.

## api-0062 · GET /ads/pixels/meta

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 221504. Path expression: `/ads/pixels/meta`.

No second argument at this call site. This does not establish the complete server contract.

## api-0063 · GET /ads/readiness-summary

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 161562. Path expression: `/ads/readiness-summary`.

No second argument at this call site. This does not establish the complete server contract.

## api-0064 · GET /ads/stats

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 161381. Path expression: `/ads/stats`.

No second argument at this call site. This does not establish the complete server contract.

## api-0065 · POST /ads/strategy/build

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 54881. Path expression: `/ads/strategy/build`.

Request/configuration expression (source only):
```javascript
{platform:L.platform,inputs:{website_url:L.website_url,campaign_name:t},plan:E}
```

## api-0066 · POST /ads/strategy/generate

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 53047. Path expression: `/ads/strategy/generate`.

Request/configuration expression (source only):
```javascript
L
```

## api-0067 · GET /ads/strategy/status/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 53182. Path expression: `/ads/strategy/status/{t}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0068 · POST /ads/tiktok/hook-lab

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 121565. Path expression: `/ads/tiktok/hook-lab`.

Request/configuration expression (source only):
```javascript
{concept:a.trim()}
```

## api-0069 · POST /ai/chat

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/775.48368b84.chunk.js` offset 28675. Path expression: `/ai/chat`.

Request/configuration expression (source only):
```javascript
{message:K}
```

## api-0070 · GET /analytics/insights

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/775.48368b84.chunk.js` offset 13953. Path expression: `/analytics/insights`.

No second argument at this call site. This does not establish the complete server contract.

## api-0071 · POST /analytics/insights

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/775.48368b84.chunk.js` offset 14123. Path expression: `/analytics/insights`.

No second argument at this call site. This does not establish the complete server contract.

## api-0072 · GET /analytics/performance?period={parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/775.48368b84.chunk.js` offset 52263. Path expression: `/analytics/performance?period={h}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0073 · GET /analytics/summary

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/775.48368b84.chunk.js` offset 52321. Path expression: `/analytics/summary`.

No second argument at this call site. This does not establish the complete server contract.

## api-0074 · GET /analytics/unified

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/775.48368b84.chunk.js` offset 60450. Path expression: `/analytics/unified`.

No second argument at this call site. This does not establish the complete server contract.

## api-0075 · GET /appointments

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/4073.67a982c5.chunk.js` offset 10262. Path expression: `/appointments`.

No second argument at this call site. This does not establish the complete server contract.

## api-0076 · POST /appointments

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/4073.67a982c5.chunk.js` offset 14873. Path expression: `/appointments`.

Request/configuration expression (source only):
```javascript
(0,s.A)((0,s.A)({},me),{},{date:pe})
```

## api-0077 · GET /appointments/available-slots?date={parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/4073.67a982c5.chunk.js` offset 10401. Path expression: `/appointments/available-slots?date={pe}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0078 · POST /appointments/sync-google

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/4073.67a982c5.chunk.js` offset 21594. Path expression: `/appointments/sync-google`.

Request/configuration expression (source only):
```javascript
{appointment_id:e}
```

## api-0079 · DELETE /appointments/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/4073.67a982c5.chunk.js` offset 22161. Path expression: `/appointments/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0080 · POST /appointments/{parameter_1}/prep

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/4073.67a982c5.chunk.js` offset 10850. Path expression: `/appointments/{e.appointment_id}/prep`.

No second argument at this call site. This does not establish the complete server contract.

## api-0081 · POST /auth/avatar

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 30127. Path expression: `/auth/avatar`.

Request/configuration expression (source only):
```javascript
e
```

## api-0082 · GET /auth/google/connection

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 51489. Path expression: `/auth/google/connection`.

No second argument at this call site. This does not establish the complete server contract.

## api-0083 · DELETE /auth/google/disconnect

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 66498. Path expression: `/auth/google/disconnect`.

No second argument at this call site. This does not establish the complete server contract.

## api-0084 · GET /auth/google/ga4-properties

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 51599. Path expression: `/auth/google/ga4-properties`.

No second argument at this call site. This does not establish the complete server contract.

## api-0085 · POST /auth/google/select

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 57477. Path expression: `/auth/google/select`.

Request/configuration expression (source only):
```javascript
{ga4_property_id:e||null,calendar_id:t||"primary"}
```

## api-0086 · GET /auth/google/start

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 56729. Path expression: `/auth/google/start`.

No second argument at this call site. This does not establish the complete server contract.

## api-0087 · GET /auth/linkedin-marketing/ad-accounts

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 51296. Path expression: `/auth/linkedin-marketing/ad-accounts`.

No second argument at this call site. This does not establish the complete server contract.

## api-0088 · GET /auth/linkedin-marketing/connection

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 51173. Path expression: `/auth/linkedin-marketing/connection`.

No second argument at this call site. This does not establish the complete server contract.

## api-0089 · DELETE /auth/linkedin-marketing/disconnect

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 66267. Path expression: `/auth/linkedin-marketing/disconnect`.

No second argument at this call site. This does not establish the complete server contract.

## api-0090 · GET /auth/linkedin-marketing/organizations

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 51383. Path expression: `/auth/linkedin-marketing/organizations`.

No second argument at this call site. This does not establish the complete server contract.

## api-0091 · POST /auth/linkedin-marketing/select

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 56315. Path expression: `/auth/linkedin-marketing/select`.

Request/configuration expression (source only):
```javascript
{ad_account_urn:e,org_urn:t}
```

## api-0092 · GET /auth/linkedin-marketing/start

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 56022. Path expression: `/auth/linkedin-marketing/start`.

No second argument at this call site. This does not establish the complete server contract.

## api-0093 · GET /auth/linkedin/connection

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 51097. Path expression: `/auth/linkedin/connection`.

No second argument at this call site. This does not establish the complete server contract.

## api-0094 · DELETE /auth/linkedin/disconnect

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 66061. Path expression: `/auth/linkedin/disconnect`.

No second argument at this call site. This does not establish the complete server contract.

## api-0095 · GET /auth/linkedin/start

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 55726. Path expression: `/auth/linkedin/start`.

No second argument at this call site. This does not establish the complete server contract.

## api-0096 · POST /auth/login

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `client-bundle.js` offset 167884. Path expression: `/auth/login`.

Request/configuration expression (source only):
```javascript
{email:e,password:t}
```

## api-0097 · POST /auth/logout

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `client-bundle.js` offset 168830. Path expression: `/auth/logout`.

No second argument at this call site. This does not establish the complete server contract.

## api-0098 · GET /auth/me

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200, 500.

Source: `client-bundle.js` offset 167130. Path expression: `/auth/me`.

No second argument at this call site. This does not establish the complete server contract.

## api-0099 · GET /auth/meta/accounts

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 16308. Path expression: `/auth/meta/accounts`.

No second argument at this call site. This does not establish the complete server contract.

## api-0100 · POST /auth/meta/accounts/active

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 94271. Path expression: `/auth/meta/accounts/active`.

Request/configuration expression (source only):
```javascript
{account_ids:n}
```

## api-0101 · GET /auth/meta/diagnose?live=1

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 55464. Path expression: `/auth/meta/diagnose?live=1`.

No second argument at this call site. This does not establish the complete server contract.

## api-0102 · GET /auth/meta/health

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 51029. Path expression: `/auth/meta/health`.

No second argument at this call site. This does not establish the complete server contract.

## api-0103 · POST /auth/meta/pages/active

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 96318. Path expression: `/auth/meta/pages/active`.

Request/configuration expression (source only):
```javascript
{page_ids:n}
```

## api-0104 · POST /auth/meta/select

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 57902. Path expression: `/auth/meta/select`.

Request/configuration expression (source only):
```javascript
{ad_account_id:e,page_id:t}
```

## api-0105 · GET /auth/meta/start{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 55160. Path expression: `/auth/meta/start{e?"?classic=1":""}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0106 · GET /auth/profile

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 26070. Path expression: `/auth/profile`.

No second argument at this call site. This does not establish the complete server contract.

## api-0107 · PUT /auth/profile

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 33195. Path expression: `/auth/profile`.

Request/configuration expression (source only):
```javascript
te
```

## api-0108 · POST /auth/register

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `client-bundle.js` offset 168196. Path expression: `/auth/register`.

Request/configuration expression (source only):
```javascript
{email:e,password:t,name:n,ref_code:r,ref_asset:o}
```

## api-0109 · POST /auth/resend-code

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `client-bundle.js` offset 168601. Path expression: `/auth/resend-code`.

Request/configuration expression (source only):
```javascript
{email:e}
```

## api-0110 · GET /auth/session?session_id={parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `client-bundle.js` offset 655235. Path expression: `/auth/session?session_id={r}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0111 · GET /auth/tiktok-posting/start

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 120649. Path expression: `/auth/tiktok-posting/start`.

No second argument at this call site. This does not establish the complete server contract.

## api-0112 · POST /auth/verify-email

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `client-bundle.js` offset 168445. Path expression: `/auth/verify-email`.

Request/configuration expression (source only):
```javascript
{email:e,code:t}
```

## api-0113 · POST /billing/checkout

Effect classification: **billing / financial change**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 44303. Path expression: `/billing/checkout`.

Request/configuration expression (source only):
```javascript
{plan:e,origin_url:window.location.origin}
```

Source: `bundles/9093.5895cba5.chunk.js` offset 3807. Path expression: `/billing/checkout`.

Request/configuration expression (source only):
```javascript
{plan:J,origin_url:window.location.origin}
```

## api-0114 · GET /billing/plan

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 26385. Path expression: `/billing/plan`.

No second argument at this call site. This does not establish the complete server contract.

## api-0115 · GET /billing/status/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 26726. Path expression: `/billing/status/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0116 · POST /blog/generate

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/4240.aa292865.chunk.js` offset 2272. Path expression: `/blog/generate`.

Request/configuration expression (source only):
```javascript
{primary_keyword:e,secondary_keywords:t||[]}
```

## api-0117 · POST /blog/ideas

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/4240.aa292865.chunk.js` offset 6000. Path expression: `/blog/ideas`.

Request/configuration expression (source only):
```javascript
{topic_hint:D}
```

## api-0118 · GET /blog/posts

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/4240.aa292865.chunk.js` offset 1848. Path expression: `/blog/posts`.

No second argument at this call site. This does not establish the complete server contract.

## api-0119 · DELETE /blog/posts/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/4240.aa292865.chunk.js` offset 15597. Path expression: `/blog/posts/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0120 · GET /blog/posts/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/4240.aa292865.chunk.js` offset 2624. Path expression: `/blog/posts/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0121 · PUT /blog/posts/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/4240.aa292865.chunk.js` offset 13782. Path expression: `/blog/posts/{e}`.

Request/configuration expression (source only):
```javascript
{title:t,meta_description:s,body_markdown:a,keywords:i,faq:l}
```

## api-0122 · POST /blog/posts/{parameter_1}/publish

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/4240.aa292865.chunk.js` offset 14478. Path expression: `/blog/posts/{e.id}/publish`.

Request/configuration expression (source only):
```javascript
{origin:window.location.origin}
```

## api-0123 · POST /blog/posts/{parameter_1}/rescore

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/4240.aa292865.chunk.js` offset 10839. Path expression: `/blog/posts/{X.id}/rescore`.

No second argument at this call site. This does not establish the complete server contract.

## api-0124 · POST /blog/posts/{parameter_1}/unpublish

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/4240.aa292865.chunk.js` offset 14150. Path expression: `/blog/posts/{e.id}/unpublish`.

No second argument at this call site. This does not establish the complete server contract.

## api-0125 · GET /blog/settings

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/4240.aa292865.chunk.js` offset 1924. Path expression: `/blog/settings`.

No second argument at this call site. This does not establish the complete server contract.

## api-0126 · POST /booking-settings

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/4073.67a982c5.chunk.js` offset 9725. Path expression: `/booking-settings`.

Request/configuration expression (source only):
```javascript
{meeting_method:e,meeting_link:t||"",buffer_minutes:a,min_notice_hours:s}
```

## api-0127 · GET /booking-slug

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/4073.67a982c5.chunk.js` offset 10576. Path expression: `/booking-slug`.

No second argument at this call site. This does not establish the complete server contract.

## api-0128 · GET /brand-kit

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 89890. Path expression: `/brand-kit`.

No second argument at this call site. This does not establish the complete server contract.

## api-0129 · PUT /brand-kit

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 20499. Path expression: `/brand-kit`.

Request/configuration expression (source only):
```javascript
{logo_asset_id:e.logo_asset_id||null,primary_color:e.primary_color,secondary_color:e.secondary_color,accent_color:e.accent_color,font_family:e.font_family,creative_style:e.creative_style||""}
```

## api-0130 · POST /briefing/dismiss

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/4278.c2617230.chunk.js` offset 2332. Path expression: `/briefing/dismiss`.

No second argument at this call site. This does not establish the complete server contract.

## api-0131 · GET /briefing/today

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/4278.c2617230.chunk.js` offset 1456. Path expression: `/briefing/today`.

Request/configuration expression (source only):
```javascript
{timeout:6e4}
```

## api-0132 · POST /calendar/conflicts

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/4073.67a982c5.chunk.js` offset 8598. Path expression: `/calendar/conflicts`.

Request/configuration expression (source only):
```javascript
{calendar_ids:l}
```

## api-0133 · POST /calendar/disconnect

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/4073.67a982c5.chunk.js` offset 5915. Path expression: `/calendar/disconnect`.

No second argument at this call site. This does not establish the complete server contract.

## api-0134 · GET /calendar/list

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/4073.67a982c5.chunk.js` offset 3933. Path expression: `/calendar/list`.

No second argument at this call site. This does not establish the complete server contract.

## api-0135 · POST /calendar/select

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/4073.67a982c5.chunk.js` offset 7318. Path expression: `/calendar/select`.

Request/configuration expression (source only):
```javascript
{calendar_id:e,calendar_name:null===t||void 0===t?void 0:t.name,timezone:null===t||void 0===t?void 0:t.timezone}
```

## api-0136 · GET /calendar/status

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/4073.67a982c5.chunk.js` offset 3862. Path expression: `/calendar/status`.

No second argument at this call site. This does not establish the complete server contract.

## api-0137 · GET /competitors

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/4059.8bad539a.chunk.js` offset 2281. Path expression: `/competitors`.

No second argument at this call site. This does not establish the complete server contract.

## api-0138 · POST /competitors

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/4059.8bad539a.chunk.js` offset 5484. Path expression: `/competitors`.

Request/configuration expression (source only):
```javascript
V
```

Source: `bundles/4059.8bad539a.chunk.js` offset 12546. Path expression: `/competitors`.

Request/configuration expression (source only):
```javascript
{name:t.name,website:t.website||"",notes:e}
```

Source: `bundles/4059.8bad539a.chunk.js` offset 14433. Path expression: `/competitors`.

Request/configuration expression (source only):
```javascript
{name:t.name,website:t.website||"",notes:s}
```

## api-0139 · POST /competitors/analyze

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/4059.8bad539a.chunk.js` offset 3877. Path expression: `/competitors/analyze`.

No second argument at this call site. This does not establish the complete server contract.

## api-0140 · POST /competitors/find

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/4059.8bad539a.chunk.js` offset 9181. Path expression: `/competitors/find`.

Request/configuration expression (source only):
```javascript
{criteria:O,count:U}
```

## api-0141 · GET /competitors/reports

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/4059.8bad539a.chunk.js` offset 2311. Path expression: `/competitors/reports`.

No second argument at this call site. This does not establish the complete server contract.

## api-0142 · DELETE /competitors/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/4059.8bad539a.chunk.js` offset 17065. Path expression: `/competitors/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0143 · GET /copilot-briefing

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/4278.c2617230.chunk.js` offset 27730. Path expression: `/copilot-briefing`.

No second argument at this call site. This does not establish the complete server contract.

## api-0144 · GET /creative-insights/ads?date_preset={parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/3572.31d8a481.chunk.js` offset 9333. Path expression: `/creative-insights/ads?date_preset={R}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0145 · POST /creative-insights/analyze

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/3572.31d8a481.chunk.js` offset 11138. Path expression: `/creative-insights/analyze`.

No second argument at this call site. This does not establish the complete server contract.

## api-0146 · POST /creative-insights/chat

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/3572.31d8a481.chunk.js` offset 9733. Path expression: `/creative-insights/chat`.

Request/configuration expression (source only):
```javascript
{message:t,session_id:F}
```

## api-0147 · GET /credits

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 324. Path expression: `/credits`.

No second argument at this call site. This does not establish the complete server contract.

## api-0148 · POST /credits/topup

Effect classification: **billing / financial change**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 2486. Path expression: `/credits/topup`.

Request/configuration expression (source only):
```javascript
{pack:e}
```

## api-0149 · POST /credits/topup/confirm

Effect classification: **billing / financial change**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 441. Path expression: `/credits/topup/confirm`.

Request/configuration expression (source only):
```javascript
{session_id:e}
```

## api-0150 · PATCH /crm/auto-sync

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 7204. Path expression: `/crm/auto-sync`.

Request/configuration expression (source only):
```javascript
{enabled:!e.auto_sync}
```

## api-0151 · POST /crm/connect

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 10794. Path expression: `/crm/connect`.

Request/configuration expression (source only):
```javascript
{provider:l.provider,credentials:p}
```

## api-0152 · GET /crm/connection

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 3835. Path expression: `/crm/connection`.

No second argument at this call site. This does not establish the complete server contract.

## api-0153 · DELETE /crm/disconnect

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 6295. Path expression: `/crm/disconnect`.

No second argument at this call site. This does not establish the complete server contract.

## api-0154 · POST /crm/guide

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 4015. Path expression: `/crm/guide`.

Request/configuration expression (source only):
```javascript
{crm_name:a}
```

## api-0155 · POST /crm/sync/{parameter_1}

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 4228. Path expression: `/crm/sync/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0156 · GET /dashboard/charts

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/775.48368b84.chunk.js` offset 20901. Path expression: `/dashboard/charts`.

No second argument at this call site. This does not establish the complete server contract.

## api-0157 · POST /dashboard/copilot

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/775.48368b84.chunk.js` offset 21415. Path expression: `/dashboard/copilot`.

No second argument at this call site. This does not establish the complete server contract.

## api-0158 · GET /dashboard/metrics

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/775.48368b84.chunk.js` offset 20865. Path expression: `/dashboard/metrics`.

No second argument at this call site. This does not establish the complete server contract.

## api-0159 · POST /data-deletion-request

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/7278.d374b472.chunk.js` offset 3666. Path expression: `https://veluro.ai/api/data-deletion-request`.

Request/configuration expression (source only):
```javascript
{email:t.trim().toLowerCase(),reason:u}
```

## api-0160 · GET /demand-alerts

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/460.6795d769.chunk.js` offset 8201. Path expression: `/demand-alerts`.

No second argument at this call site. This does not establish the complete server contract.

## api-0161 · POST /demand-alerts

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/460.6795d769.chunk.js` offset 15252. Path expression: `/demand-alerts`.

Request/configuration expression (source only):
```javascript
{enabled:!!X.enabled,location:X.location,industries:X.industries||F,autopilot:e}
```

Source: `bundles/460.6795d769.chunk.js` offset 15786. Path expression: `/demand-alerts`.

Request/configuration expression (source only):
```javascript
{enabled:e,location:t,industries:F,autopilot:!!X.autopilot}
```

## api-0162 · POST /demand-map/drilldown

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/460.6795d769.chunk.js` offset 19211. Path expression: `/demand-map/drilldown`.

Request/configuration expression (source only):
```javascript
{area:e.area,location:a,industries:F}
```

## api-0163 · POST /demand-map/generate

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/460.6795d769.chunk.js` offset 12315. Path expression: `/demand-map/generate`.

Request/configuration expression (source only):
```javascript
{location:a,industries:e,audience_name:(null===n||void 0===n?void 0:n.name)||null,audience_context:n?'High-intent audience "'.concat(n.name,'" with ').concat(null!==(t=null!==(s=n.records_count)&&void 0!==s?s:n.count)&&void 0!==t?t:"many"," known in-market buyers."):null}
```

## api-0164 · GET /digest

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3028.e29a6d5d.chunk.js` offset 1458. Path expression: `/digest`.

No second argument at this call site. This does not establish the complete server contract.

## api-0165 · POST /digest/generate

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/3028.e29a6d5d.chunk.js` offset 1571. Path expression: `/digest/generate`.

No second argument at this call site. This does not establish the complete server contract.

## api-0166 · POST /digest/send-email

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/3028.e29a6d5d.chunk.js` offset 2518. Path expression: `/digest/send-email`.

Request/configuration expression (source only):
```javascript
{digest_id:A.digest_id}
```

## api-0167 · GET /email/accounts

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/356.63be27af.chunk.js` offset 1573. Path expression: `/email/accounts`.

No second argument at this call site. This does not establish the complete server contract.

## api-0168 · POST /email/accounts/connect

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/356.63be27af.chunk.js` offset 17862. Path expression: `/email/accounts/connect`.

Request/configuration expression (source only):
```javascript
{provider:c,credentials:x}
```

## api-0169 · DELETE /email/accounts/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/356.63be27af.chunk.js` offset 16437. Path expression: `/email/accounts/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0170 · POST /email/ai-draft

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/356.63be27af.chunk.js` offset 10600. Path expression: `/email/ai-draft`.

Request/configuration expression (source only):
```javascript
{email_id:M.email_id}
```

## api-0171 · POST /email/compose

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/356.63be27af.chunk.js` offset 20616. Path expression: `/email/compose`.

Request/configuration expression (source only):
```javascript
{to:n,subject:o,body:x}
```

## api-0172 · GET /email/inbox?folder={parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/356.63be27af.chunk.js` offset 1606. Path expression: `/email/inbox?folder={_}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0173 · DELETE /email/resend

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/659.f8c47505.chunk.js` offset 16581. Path expression: `/email/resend`.

No second argument at this call site. This does not establish the complete server contract.

## api-0174 · GET /email/resend

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/659.f8c47505.chunk.js` offset 4640. Path expression: `/email/resend`.

No second argument at this call site. This does not establish the complete server contract.

## api-0175 · POST /email/resend/connect

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/659.f8c47505.chunk.js` offset 2856. Path expression: `/email/resend/connect`.

Request/configuration expression (source only):
```javascript
{api_key:c.trim(),from_email:d.trim()}
```

## api-0176 · GET /email/stats

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/356.63be27af.chunk.js` offset 1654. Path expression: `/email/stats`.

No second argument at this call site. This does not establish the complete server contract.

## api-0177 · POST /email/triage

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/356.63be27af.chunk.js` offset 3060. Path expression: `/email/triage`.

No second argument at this call site. This does not establish the complete server contract.

## api-0178 · DELETE /email/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/356.63be27af.chunk.js` offset 9108. Path expression: `/email/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0179 · GET /email/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/356.63be27af.chunk.js` offset 6658. Path expression: `/email/{e.email_id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0180 · POST /email/{parameter_1}/star

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/356.63be27af.chunk.js` offset 1835. Path expression: `/email/{t}/star`.

No second argument at this call site. This does not establish the complete server contract.

## api-0181 · GET /flyers

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/9795.1ac08d65.chunk.js` offset 5076. Path expression: `/flyers`.

No second argument at this call site. This does not establish the complete server contract.

## api-0182 · POST /flyers

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/9795.1ac08d65.chunk.js` offset 6339. Path expression: `/flyers`.

Request/configuration expression (source only):
```javascript
{flyer_id:_,name:C,template_id:z,palette_id:F,fields:q,image_url:I}
```

## api-0183 · POST /flyers/ai-fill

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/9795.1ac08d65.chunk.js` offset 9397. Path expression: `/flyers/ai-fill`.

Request/configuration expression (source only):
```javascript
{topic:B}
```

## api-0184 · POST /flyers/generate-image

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/9795.1ac08d65.chunk.js` offset 14744. Path expression: `/flyers/generate-image`.

Request/configuration expression (source only):
```javascript
{prompt:e}
```

## api-0185 · POST /flyers/upload-image

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/9795.1ac08d65.chunk.js` offset 15850. Path expression: `/flyers/upload-image`.

Request/configuration expression (source only):
```javascript
e
```

## api-0186 · DELETE /flyers/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/9795.1ac08d65.chunk.js` offset 8499. Path expression: `/flyers/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0187 · GET /flyers/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/9795.1ac08d65.chunk.js` offset 8125. Path expression: `/flyers/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0188 · GET /folders

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 89060. Path expression: `/folders`.

No second argument at this call site. This does not establish the complete server contract.

## api-0189 · POST /folders

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5232.d3fe35f5.chunk.js` offset 9522. Path expression: `/folders`.

Request/configuration expression (source only):
```javascript
{name:e}
```

Source: `bundles/5232.d3fe35f5.chunk.js` offset 21259. Path expression: `/folders`.

Request/configuration expression (source only):
```javascript
{name:e.trim()}
```

## api-0190 · POST /folders/assign

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5232.d3fe35f5.chunk.js` offset 20735. Path expression: `/folders/assign`.

Request/configuration expression (source only):
```javascript
{item_type:t,item_id:a,folder_id:e}
```

Source: `bundles/5232.d3fe35f5.chunk.js` offset 21308. Path expression: `/folders/assign`.

Request/configuration expression (source only):
```javascript
{item_type:t,item_id:a,folder_id:l.data.folder_id}
```

## api-0191 · POST /folders/suggest

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/5232.d3fe35f5.chunk.js` offset 24039. Path expression: `/folders/suggest`.

Request/configuration expression (source only):
```javascript
{item_type:t,item_id:a}
```

## api-0192 · DELETE /folders/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/5232.d3fe35f5.chunk.js` offset 13964. Path expression: `/folders/{e.folder_id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0193 · PUT /folders/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5232.d3fe35f5.chunk.js` offset 9878. Path expression: `/folders/{e}`.

Request/configuration expression (source only):
```javascript
{name:t}
```

## api-0194 · GET /funnels

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 152900. Path expression: `/funnels`.

No second argument at this call site. This does not establish the complete server contract.

## api-0195 · POST /funnels

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 18284. Path expression: `/funnels`.

Request/configuration expression (source only):
```javascript
{name:x.product||x.goal||"AI Funnel",funnel_type:x.goal.toLowerCase().replace(/[^a-z]+/g,"_"),goal:x.goal,offer:{description:x.offer_desc,website:x.website,product:x.product,price:x.price,benefits:x.benefits,special_offer:x.special_offer},audience:{industry:x.industry,target_audience:x.audience,geographic_market:x.geo,pain_points:x.pains,desired_outcome:x.outcome},conversion_goal:x.conversion_goal,style:x.style.toLowerCase(),cta:x.cta}
```

## api-0196 · DELETE /funnels/automations/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 11849. Path expression: `/funnels/automations/{e.automation_id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0197 · PUT /funnels/automations/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 11362. Path expression: `/funnels/automations/{e.automation_id}`.

Request/configuration expression (source only):
```javascript
{enabled:!e.enabled}
```

## api-0198 · POST /funnels/automations/{parameter_1}/test

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 10812. Path expression: `/funnels/automations/{e.automation_id}/test`.

Request/configuration expression (source only):
```javascript
t?{phone:m}:{}
```

## api-0199 · POST /funnels/from-template

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 53842. Path expression: `/funnels/from-template`.

Request/configuration expression (source only):
```javascript
{key:e}
```

## api-0200 · DELETE /funnels/pages/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 27861. Path expression: `/funnels/pages/{e.page_id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0201 · GET /funnels/pages/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/3180.790a945b.chunk.js` offset 5370. Path expression: `/funnels/pages/{q}`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/479.0fb227a6.chunk.js` offset 30076. Path expression: `/funnels/pages/{e.page_id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0202 · PUT /funnels/pages/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3180.790a945b.chunk.js` offset 5689. Path expression: `/funnels/pages/{q}`.

Request/configuration expression (source only):
```javascript
{sections:e.sections,form_fields:e.form_fields,page_name:e.page_name,routing_rules:e.routing_rules||[],design:e.design||{}}
```

Source: `bundles/479.0fb227a6.chunk.js` offset 24671. Path expression: `/funnels/pages/{e.page_id}`.

Request/configuration expression (source only):
```javascript
{page_name:t.target.value}
```

Source: `bundles/479.0fb227a6.chunk.js` offset 24934. Path expression: `/funnels/pages/{e.page_id}`.

Request/configuration expression (source only):
```javascript
{page_type:t.target.value}
```

Source: `bundles/479.0fb227a6.chunk.js` offset 30269. Path expression: `/funnels/pages/{e.page_id}`.

Request/configuration expression (source only):
```javascript
{sections:s}
```

## api-0203 · POST /funnels/pages/{parameter_1}/ai-edit

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/3180.790a945b.chunk.js` offset 6884. Path expression: `/funnels/pages/{q}/ai-edit`.

Request/configuration expression (source only):
```javascript
{instruction:e,section_index:G}
```

## api-0204 · POST /funnels/pages/{parameter_1}/duplicate

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 25653. Path expression: `/funnels/pages/{e.page_id}/duplicate`.

No second argument at this call site. This does not establish the complete server contract.

## api-0205 · POST /funnels/pages/{parameter_1}/promote

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 25961. Path expression: `/funnels/pages/{e.page_id}/promote`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/479.0fb227a6.chunk.js` offset 32792. Path expression: `/funnels/pages/{e.pid}/promote`.

No second argument at this call site. This does not establish the complete server contract.

## api-0206 · POST /funnels/pages/{parameter_1}/variant

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 26360. Path expression: `/funnels/pages/{e.page_id}/variant`.

No second argument at this call site. This does not establish the complete server contract.

## api-0207 · POST /funnels/pages/{parameter_1}/variant-ai

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 26956. Path expression: `/funnels/pages/{e.page_id}/variant-ai`.

No second argument at this call site. This does not establish the complete server contract.

## api-0208 · POST /funnels/stripe/connect

Effect classification: **billing / financial change**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 37462. Path expression: `/funnels/stripe/connect`.

Request/configuration expression (source only):
```javascript
{origin:window.location.origin}
```

## api-0209 · GET /funnels/stripe/status

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 21451. Path expression: `/funnels/stripe/status`.

No second argument at this call site. This does not establish the complete server contract.

## api-0210 · GET /funnels/templates

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 52680. Path expression: `/funnels/templates`.

No second argument at this call site. This does not establish the complete server contract.

## api-0211 · DELETE /funnels/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 50923. Path expression: `/funnels/{e.funnel_id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0212 · GET /funnels/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/3180.790a945b.chunk.js` offset 5507. Path expression: `/funnels/{R}`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/479.0fb227a6.chunk.js` offset 20957. Path expression: `/funnels/{t}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0213 · PUT /funnels/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 20882. Path expression: `/funnels/{t}`.

Request/configuration expression (source only):
```javascript
{webhooks:e}
```

Source: `bundles/479.0fb227a6.chunk.js` offset 21695. Path expression: `/funnels/{t}`.

Request/configuration expression (source only):
```javascript
{status:e}
```

Source: `bundles/479.0fb227a6.chunk.js` offset 38921. Path expression: `/funnels/{t}`.

Request/configuration expression (source only):
```javascript
{tracking:I}
```

Source: `bundles/479.0fb227a6.chunk.js` offset 50662. Path expression: `/funnels/{e.funnel_id}`.

Request/configuration expression (source only):
```javascript
{name:t}
```

## api-0214 · GET /funnels/{parameter_1}/analytics

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 21104. Path expression: `/funnels/{t}/analytics`.

No second argument at this call site. This does not establish the complete server contract.

## api-0215 · GET /funnels/{parameter_1}/automations

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 2282. Path expression: `/funnels/{t}/automations`.

No second argument at this call site. This does not establish the complete server contract.

## api-0216 · POST /funnels/{parameter_1}/automations

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 7998. Path expression: `/funnels/{t}/automations`.

Request/configuration expression (source only):
```javascript
{name:p.name,trigger:p.trigger,page_id:p.page_id,steps:v.map(e=>({channel:e.channel,delay_minutes:Math.round(Number(e.delayN||0)*e.delayUnit),subject:e.subject,body:e.body}))}
```

## api-0217 · POST /funnels/{parameter_1}/duplicate

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 50402. Path expression: `/funnels/{e.funnel_id}/duplicate`.

No second argument at this call site. This does not establish the complete server contract.

## api-0218 · POST /funnels/{parameter_1}/generate

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 18757. Path expression: `/funnels/{e.data.funnel_id}/generate`.

No second argument at this call site. This does not establish the complete server contract.

## api-0219 · GET /funnels/{parameter_1}/leads

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 21200. Path expression: `/funnels/{t}/leads`.

No second argument at this call site. This does not establish the complete server contract.

## api-0220 · POST /funnels/{parameter_1}/optimize

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 28657. Path expression: `/funnels/{t}/optimize`.

No second argument at this call site. This does not establish the complete server contract.

## api-0221 · GET /funnels/{parameter_1}/orders

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 21298. Path expression: `/funnels/{t}/orders`.

No second argument at this call site. This does not establish the complete server contract.

## api-0222 · POST /funnels/{parameter_1}/steps

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 28079. Path expression: `/funnels/{t}/steps`.

Request/configuration expression (source only):
```javascript
{page_name:"New Step",page_type:"landing"}
```

## api-0223 · PUT /funnels/{parameter_1}/steps/reorder

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 21939. Path expression: `/funnels/{t}/steps/reorder`.

Request/configuration expression (source only):
```javascript
{page_ids:a}
```

## api-0224 · POST /funnels/{parameter_1}/webhooks/test

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/479.0fb227a6.chunk.js` offset 40775. Path expression: `/funnels/{t}/webhooks/test`.

Request/configuration expression (source only):
```javascript
{url:e}
```

## api-0225 · GET /gbp/accounts

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/4846.efd2ee0a.chunk.js` offset 774. Path expression: `/gbp/accounts`.

No second argument at this call site. This does not establish the complete server contract.

## api-0226 · GET /gbp/locations

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/4846.efd2ee0a.chunk.js` offset 1071. Path expression: `/gbp/locations`.

Request/configuration expression (source only):
```javascript
{params:{account:e}}
```

## api-0227 · GET /gbp/status

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/4846.efd2ee0a.chunk.js` offset 632. Path expression: `/gbp/status`.

No second argument at this call site. This does not establish the complete server contract.

## api-0228 · POST /geo/audit

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6979.1f4cb545.chunk.js` offset 15108. Path expression: `/geo/audit`.

Request/configuration expression (source only):
```javascript
{url:O}
```

## api-0229 · GET /geo/config

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/6979.1f4cb545.chunk.js` offset 2937. Path expression: `/geo/config`.

No second argument at this call site. This does not establish the complete server contract.

## api-0230 · PUT /geo/config

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6979.1f4cb545.chunk.js` offset 3384. Path expression: `/geo/config`.

Request/configuration expression (source only):
```javascript
i
```

Source: `bundles/6979.1f4cb545.chunk.js` offset 8521. Path expression: `/geo/config`.

Request/configuration expression (source only):
```javascript
e
```

## api-0231 · POST /geo/fix

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6979.1f4cb545.chunk.js` offset 16873. Path expression: `/geo/fix`.

Request/configuration expression (source only):
```javascript
{url:O,check_id:e}
```

## api-0232 · POST /geo/prompts/generate

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/6979.1f4cb545.chunk.js` offset 7194. Path expression: `/geo/prompts/generate`.

Request/configuration expression (source only):
```javascript
e
```

## api-0233 · POST /geo/scan

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/6979.1f4cb545.chunk.js` offset 8567. Path expression: `/geo/scan`.

No second argument at this call site. This does not establish the complete server contract.

## api-0234 · GET /geo/scans

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/6979.1f4cb545.chunk.js` offset 3121. Path expression: `/geo/scans`.

No second argument at this call site. This does not establish the complete server contract.

## api-0235 · GET /geo/scans/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/6979.1f4cb545.chunk.js` offset 3228. Path expression: `/geo/scans/{s.scan_id}`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/6979.1f4cb545.chunk.js` offset 8659. Path expression: `/geo/scans/{t}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0236 · POST /geo/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6979.1f4cb545.chunk.js` offset 3516. Path expression: `/geo/{e}`.

Request/configuration expression (source only):
```javascript
{url:O}
```

## api-0237 · GET /google-ads/accounts

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 52033. Path expression: `/google-ads/accounts`.

No second argument at this call site. This does not establish the complete server contract.

## api-0238 · GET /google-ads/auth/start

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 57013. Path expression: `/google-ads/auth/start`.

No second argument at this call site. This does not establish the complete server contract.

## api-0239 · GET /google-ads/connection

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 51923. Path expression: `/google-ads/connection`.

No second argument at this call site. This does not establish the complete server contract.

## api-0240 · POST /google-ads/conversion-action

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 129465. Path expression: `/google-ads/conversion-action`.

Request/configuration expression (source only):
```javascript
{name:l.trim(),category:r}
```

## api-0241 · GET /google-ads/conversion-actions

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 127974. Path expression: `/google-ads/conversion-actions`.

No second argument at this call site. This does not establish the complete server contract.

## api-0242 · DELETE /google-ads/disconnect

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 57281. Path expression: `/google-ads/disconnect`.

No second argument at this call site. This does not establish the complete server contract.

## api-0243 · POST /google-ads/launch/{parameter_1}

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 164763. Path expression: `/google-ads/launch/{e.campaign_id}`.

Request/configuration expression (source only):
```javascript
t?{override_readiness:!0}:{}
```

## api-0244 · GET /google-ads/recommendations

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 85758. Path expression: `/google-ads/recommendations`.

No second argument at this call site. This does not establish the complete server contract.

## api-0245 · POST /google-ads/recommendations/apply

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 87998. Path expression: `/google-ads/recommendations/apply`.

Request/configuration expression (source only):
```javascript
{rec_id:e.id}
```

## api-0246 · POST /google-ads/select

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 79845. Path expression: `/google-ads/select`.

Request/configuration expression (source only):
```javascript
{customer_id:e}
```

## api-0247 · GET /google/analytics?lookback_days=30

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/775.48368b84.chunk.js` offset 65748. Path expression: `/google/analytics?lookback_days=30`.

No second argument at this call site. This does not establish the complete server contract.

## api-0248 · GET /health-actions

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/628.0eed46e1.chunk.js` offset 14151. Path expression: `/health-actions`.

No second argument at this call site. This does not establish the complete server contract.

## api-0249 · POST /health-actions/{parameter_1}/{parameter_2}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/628.0eed46e1.chunk.js` offset 14324. Path expression: `/health-actions/{e}/{t}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0250 · GET /health-insights

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/628.0eed46e1.chunk.js` offset 14117. Path expression: `/health-insights`.

No second argument at this call site. This does not establish the complete server contract.

## api-0251 · GET /health-score

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/628.0eed46e1.chunk.js` offset 14086. Path expression: `/health-score`.

No second argument at this call site. This does not establish the complete server contract.

## api-0252 · POST /icp/auto-discover

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/775.48368b84.chunk.js` offset 21129. Path expression: `/icp/auto-discover`.

No second argument at this call site. This does not establish the complete server contract.

## api-0253 · GET /icp/brief

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/775.48368b84.chunk.js` offset 20936. Path expression: `/icp/brief`.

No second argument at this call site. This does not establish the complete server contract.

## api-0254 · GET /inbox/replies

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/9244.be0a4057.chunk.js` offset 1572. Path expression: `/inbox/replies`.

No second argument at this call site. This does not establish the complete server contract.

## api-0255 · POST /inbox/replies/{parameter_1}/read

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/9244.be0a4057.chunk.js` offset 1796. Path expression: `/inbox/replies/{e.reply_id}/read`.

No second argument at this call site. This does not establish the complete server contract.

## api-0256 · GET /inbox/unread-count

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/6184.08cd5e77.chunk.js` offset 18480. Path expression: `/inbox/unread-count`.

No second argument at this call site. This does not establish the complete server contract.

## api-0257 · GET /integrations

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 50755. Path expression: `/integrations`.

No second argument at this call site. This does not establish the complete server contract.

## api-0258 · POST /integrations/connect

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 68948. Path expression: `/integrations/connect`.

Request/configuration expression (source only):
```javascript
{service:e,credentials:f[e]||{}}
```

## api-0259 · GET /integrations/setup-guide/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 69785. Path expression: `/integrations/setup-guide/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0260 · DELETE /integrations/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 66945. Path expression: `/integrations/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0261 · GET /intelligence/knowledge

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/4334.85d9c682.chunk.js` offset 4316. Path expression: `/intelligence/knowledge`.

No second argument at this call site. This does not establish the complete server contract.

## api-0262 · POST /intelligence/knowledge/note

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/4334.85d9c682.chunk.js` offset 9575. Path expression: `/intelligence/knowledge/note`.

Request/configuration expression (source only):
```javascript
{kind:d,title:y,text:j}
```

Source: `bundles/5753.fcee46d5.chunk.js` offset 8356. Path expression: `/intelligence/knowledge/note`.

Request/configuration expression (source only):
```javascript
{text:d.trim(),title:"Growth engine note"}
```

## api-0263 · POST /intelligence/knowledge/upload

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/4334.85d9c682.chunk.js` offset 7172. Path expression: `/intelligence/knowledge/upload`.

Request/configuration expression (source only):
```javascript
s
```

Source: `bundles/5753.fcee46d5.chunk.js` offset 6815. Path expression: `/intelligence/knowledge/upload`.

Request/configuration expression (source only):
```javascript
a
```

## api-0264 · POST /intelligence/knowledge/website

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/4334.85d9c682.chunk.js` offset 3922. Path expression: `/intelligence/knowledge/website`.

Request/configuration expression (source only):
```javascript
{url:A.trim()}
```

Source: `bundles/5753.fcee46d5.chunk.js` offset 5660. Path expression: `/intelligence/knowledge/website`.

Request/configuration expression (source only):
```javascript
{url:n.trim()}
```

## api-0265 · DELETE /intelligence/knowledge/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/4334.85d9c682.chunk.js` offset 11213. Path expression: `/intelligence/knowledge/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0266 · GET /intelligence/score

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/4334.85d9c682.chunk.js` offset 1299. Path expression: `/intelligence/score`.

No second argument at this call site. This does not establish the complete server contract.

## api-0267 · GET /intent/ad-drafts

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 306270. Path expression: `/intent/ad-drafts`.

No second argument at this call site. This does not establish the complete server contract.

## api-0268 · DELETE /intent/ad-drafts/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/9232.dcf842a0.chunk.js` offset 23181. Path expression: `/intent/ad-drafts/{r.draft_id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0269 · GET /intent/ad-drafts/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 310716. Path expression: `/intent/ad-drafts/{p.draft_id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0270 · DELETE /intent/ad-drafts/{parameter_1}/creatives/{parameter_2}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/9232.dcf842a0.chunk.js` offset 14309. Path expression: `/intent/ad-drafts/{t}/creatives/{u}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0271 · PATCH /intent/ad-drafts/{parameter_1}/creatives/{parameter_2}

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/9232.dcf842a0.chunk.js` offset 9149. Path expression: `/intent/ad-drafts/{t}/creatives/{u}`.

Request/configuration expression (source only):
```javascript
{status:e}
```

Source: `bundles/9232.dcf842a0.chunk.js` offset 17416. Path expression: `/intent/ad-drafts/{t}/creatives/{u}`.

Request/configuration expression (source only):
```javascript
{headline:B.headline,description:B.description,primary_text:B.primary_text,cta:B.cta}
```

## api-0272 · POST /intent/ad-drafts/{parameter_1}/creatives/{parameter_2}/revise

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/9232.dcf842a0.chunk.js` offset 9483. Path expression: `/intent/ad-drafts/{t}/creatives/{u}/revise`.

Request/configuration expression (source only):
```javascript
{instruction:N.trim()}
```

## api-0273 · GET /intent/audiences

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 222163. Path expression: `/intent/audiences`.

No second argument at this call site. This does not establish the complete server contract.

## api-0274 · POST /intent/audiences/build

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 74689. Path expression: `/intent/audiences/build`.

Request/configuration expression (source only):
```javascript
e
```

## api-0275 · DELETE /intent/audiences/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 80469. Path expression: `/intent/audiences/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0276 · PUT /intent/audiences/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 96150. Path expression: `/intent/audiences/{Yt.id}`.

Request/configuration expression (source only):
```javascript
{name:Yt.name,max_leads:Number(Yt.max)||void 0}
```

## api-0277 · POST /intent/audiences/{parameter_1}/activate-email-sequence

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 40902. Path expression: `/intent/audiences/{us}/activate-email-sequence`.

No second argument at this call site. This does not establish the complete server contract.

## api-0278 · POST /intent/audiences/{parameter_1}/activate-fb-ads

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 39371. Path expression: `/intent/audiences/{us}/activate-fb-ads`.

No second argument at this call site. This does not establish the complete server contract.

## api-0279 · POST /intent/audiences/{parameter_1}/activate-linkedin-ads

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 40685. Path expression: `/intent/audiences/{us}/activate-linkedin-ads`.

No second argument at this call site. This does not establish the complete server contract.

## api-0280 · POST /intent/audiences/{parameter_1}/activate-linkedin-dm-sequence

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 41106. Path expression: `/intent/audiences/{us}/activate-linkedin-dm-sequence`.

No second argument at this call site. This does not establish the complete server contract.

## api-0281 · GET /intent/audiences/{parameter_1}/activation-status/{parameter_2}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 39797. Path expression: `/intent/audiences/{us}/activation-status/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0282 · GET /intent/audiences/{parameter_1}/drafts

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 38873. Path expression: `/intent/audiences/{e}/drafts`.

No second argument at this call site. This does not establish the complete server contract.

## api-0283 · GET /intent/audiences/{parameter_1}/export-csv

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 83491. Path expression: `/intent/audiences/{us}/export-csv`.

Request/configuration expression (source only):
```javascript
{responseType:"blob"}
```

## api-0284 · POST /intent/audiences/{parameter_1}/regenerate-fb-creatives

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/9232.dcf842a0.chunk.js` offset 22078. Path expression: `/intent/audiences/{r.audience_id}/regenerate-fb-creatives`.

Request/configuration expression (source only):
```javascript
g.trim()?{instructions:g.trim()}:{}
```

## api-0285 · GET /intent/audiences/{parameter_1}?li_active={parameter_2}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 37738. Path expression: `/intent/audiences/{us}?li_active={xt?1:0}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0286 · POST /intent/auto-build

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 35636. Path expression: `/intent/auto-build`.

Request/configuration expression (source only):
```javascript
{url:es.trim()}
```

## api-0287 · POST /intent/auto-suggest-categories

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 54612. Path expression: `/intent/auto-suggest-categories`.

Request/configuration expression (source only):
```javascript
{scope:"b2c"===It?"b2c":"b2b"===It?"b2b":"both"}
```

## api-0288 · GET /intent/city-search

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 98860. Path expression: `/intent/city-search`.

Request/configuration expression (source only):
```javascript
{params:{q:e}}
```

## api-0289 · POST /intent/custom-ads/generate

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 25405. Path expression: `/intent/custom-ads/generate`.

Request/configuration expression (source only):
```javascript
{offer:d.trim(),targeting:O(),instructions:c.trim()}
```

## api-0290 · POST /intent/describe-icp

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 59693. Path expression: `/intent/describe-icp`.

Request/configuration expression (source only):
```javascript
{description:is}
```

## api-0291 · POST /intent/leads/generate-outreach

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 17837. Path expression: `/intent/leads/generate-outreach`.

Request/configuration expression (source only):
```javascript
{lead:g,intent_topic:(null===g||void 0===g?void 0:g.topic_label)||""}
```

## api-0292 · GET /intent/meta/connection

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/5027.62c03e58.chunk.js` offset 30078. Path expression: `/intent/meta/connection`.

No second argument at this call site. This does not establish the complete server contract.

## api-0293 · GET /intent/provider-status

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/5027.62c03e58.chunk.js` offset 28548. Path expression: `/intent/provider-status`.

No second argument at this call site. This does not establish the complete server contract.

## api-0294 · GET /intent/quota

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/5027.62c03e58.chunk.js` offset 29585. Path expression: `/intent/quota`.

No second argument at this call site. This does not establish the complete server contract.

## api-0295 · GET /intent/reservations/me

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/5027.62c03e58.chunk.js` offset 30158. Path expression: `/intent/reservations/me`.

No second argument at this call site. This does not establish the complete server contract.

## api-0296 · POST /intent/reservations/{parameter_1}/claim

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 46640. Path expression: `/intent/reservations/{zt.reservation_id}/claim`.

No second argument at this call site. This does not establish the complete server contract.

## api-0297 · GET /intent/status

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/5027.62c03e58.chunk.js` offset 30009. Path expression: `/intent/status`.

No second argument at this call site. This does not establish the complete server contract.

## api-0298 · POST /intent/targeting/reach-estimate

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 22474. Path expression: `/intent/targeting/reach-estimate`.

Request/configuration expression (source only):
```javascript
{targeting:O()}
```

## api-0299 · POST /intent/targeting/save-audience

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 23727. Path expression: `/intent/targeting/save-audience`.

Request/configuration expression (source only):
```javascript
{name:e,targeting:O()}
```

Source: `bundles/1482.a74c6ab9.chunk.js` offset 24173. Path expression: `/intent/targeting/save-audience`.

Request/configuration expression (source only):
```javascript
{name:e,targeting:O(),allow_duplicate:!0}
```

## api-0300 · GET /intent/targeting/saved-audiences

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 222409. Path expression: `/intent/targeting/saved-audiences`.

No second argument at this call site. This does not establish the complete server contract.

## api-0301 · DELETE /intent/targeting/saved-audiences/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 248839. Path expression: `/intent/targeting/saved-audiences/{e.saved_audience_id||a}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0302 · GET /intent/topics/search?q={parameter_1}&scope={parameter_2}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 30762. Path expression: `/intent/topics/search?q={encodeURIComponent($t)}&scope={"b2c"===It?"b2c":"b2b"===It?"b2b":"both"}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0303 · POST /intent/zip-audience

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/460.6795d769.chunk.js` offset 27319. Path expression: `/intent/zip-audience`.

Request/configuration expression (source only):
```javascript
{area:re.area,metro:re.metro,location:a}
```

## api-0304 · POST /intent/zip-audience/preview

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/460.6795d769.chunk.js` offset 19826. Path expression: `/intent/zip-audience/preview`.

Request/configuration expression (source only):
```javascript
{area:e.area,metro:null===ae||void 0===ae?void 0:ae.area,location:a}
```

## api-0305 · GET /landing

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/459.ecd04828.chunk.js` offset 28203. Path expression: `/landing`.

No second argument at this call site. This does not establish the complete server contract.

## api-0306 · POST /landing/extract-design

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 40344. Path expression: `/landing/extract-design`.

Request/configuration expression (source only):
```javascript
{url:ye.trim()}
```

## api-0307 · POST /landing/generate

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 47973. Path expression: `/landing/generate`.

Request/configuration expression (source only):
```javascript
e
```

## api-0308 · GET /landing/quota

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/459.ecd04828.chunk.js` offset 28311. Path expression: `/landing/quota`.

No second argument at this call site. This does not establish the complete server contract.

## api-0309 · POST /landing/suggest-designs

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 28704. Path expression: `/landing/suggest-designs`.

Request/configuration expression (source only):
```javascript
{business_name:ve,prompt:ge,look_feel:Ae}
```

## api-0310 · GET /landing/templates

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/459.ecd04828.chunk.js` offset 28571. Path expression: `/landing/templates`.

No second argument at this call site. This does not establish the complete server contract.

## api-0311 · DELETE /landing/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 82796. Path expression: `/landing/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0312 · PUT /landing/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 29067. Path expression: `/landing/{Q.page_id}`.

Request/configuration expression (source only):
```javascript
e
```

## api-0313 · DELETE /landing/{parameter_1}/ab-variant

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 34984. Path expression: `/landing/{Q.page_id}/ab-variant`.

No second argument at this call site. This does not establish the complete server contract.

## api-0314 · POST /landing/{parameter_1}/ab-variant

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 72289. Path expression: `/landing/{Q.page_id}/ab-variant`.

No second argument at this call site. This does not establish the complete server contract.

## api-0315 · POST /landing/{parameter_1}/ab-variant/promote

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 71160. Path expression: `/landing/{Q.page_id}/ab-variant/promote`.

Request/configuration expression (source only):
```javascript
{winner:e}
```

## api-0316 · GET /landing/{parameter_1}/analytics

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 34813. Path expression: `/landing/{Q.page_id}/analytics`.

No second argument at this call site. This does not establish the complete server contract.

## api-0317 · POST /landing/{parameter_1}/autopilot

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 77810. Path expression: `/landing/{Q.page_id}/autopilot`.

Request/configuration expression (source only):
```javascript
{enabled:e}
```

## api-0318 · GET /landing/{parameter_1}/chat

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 17239. Path expression: `/landing/{f}/chat`.

No second argument at this call site. This does not establish the complete server contract.

## api-0319 · POST /landing/{parameter_1}/chat-edit

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 17691. Path expression: `/landing/{f}/chat-edit`.

Request/configuration expression (source only):
```javascript
{message:s}
```

## api-0320 · POST /landing/{parameter_1}/custom-domain

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 73798. Path expression: `/landing/{Q.page_id}/custom-domain`.

Request/configuration expression (source only):
```javascript
{domain:Ee}
```

## api-0321 · POST /landing/{parameter_1}/generate-ad-creatives

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 80217. Path expression: `/landing/{Q.page_id}/generate-ad-creatives`.

No second argument at this call site. This does not establish the complete server contract.

## api-0322 · POST /landing/{parameter_1}/generate-image

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 34083. Path expression: `/landing/{Q.page_id}/generate-image`.

Request/configuration expression (source only):
```javascript
{prompt:t,kind:e}
```

## api-0323 · POST /landing/{parameter_1}/hero-image

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 53309. Path expression: `/landing/{Q.page_id}/hero-image`.

No second argument at this call site. This does not establish the complete server contract.

## api-0324 · POST /landing/{parameter_1}/place-media-ai

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 32978. Path expression: `/landing/{Q.page_id}/place-media-ai`.

Request/configuration expression (source only):
```javascript
{media_url:"".concat("https://veluro.ai").concat(e.url),kind:t,instruction:a}
```

## api-0325 · POST /landing/{parameter_1}/publish

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 64875. Path expression: `/landing/{Q.page_id}/publish`.

Request/configuration expression (source only):
```javascript
Ue?{slug:Ue}:{}
```

## api-0326 · POST /landing/{parameter_1}/regenerate-section

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 56182. Path expression: `/landing/{Q.page_id}/regenerate-section`.

Request/configuration expression (source only):
```javascript
{section_index:e}
```

## api-0327 · POST /landing/{parameter_1}/unpublish

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 65866. Path expression: `/landing/{Q.page_id}/unpublish`.

No second argument at this call site. This does not establish the complete server contract.

## api-0328 · POST /landing/{parameter_1}/upload-asset

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3180.790a945b.chunk.js` offset 6557. Path expression: `/landing/{q}/upload-asset`.

Request/configuration expression (source only):
```javascript
s
```

Source: `bundles/459.ecd04828.chunk.js` offset 29359. Path expression: `/landing/{Q.page_id}/upload-asset`.

Request/configuration expression (source only):
```javascript
a
```

## api-0329 · POST /landing/{parameter_1}/verify-domain

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/459.ecd04828.chunk.js` offset 75012. Path expression: `/landing/{Q.page_id}/verify-domain`.

No second argument at this call site. This does not establish the complete server contract.

## api-0330 · GET /leads

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/531.d33736f5.chunk.js` offset 15167. Path expression: `/leads`.

No second argument at this call site. This does not establish the complete server contract.

## api-0331 · POST /leads

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6375.310dff5f.chunk.js` offset 76656. Path expression: `/leads`.

Request/configuration expression (source only):
```javascript
Aa
```

## api-0332 · POST /leads/auto-score

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6375.310dff5f.chunk.js` offset 71703. Path expression: `/leads/auto-score`.

No second argument at this call site. This does not establish the complete server contract.

## api-0333 · POST /leads/bulk-delete

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6375.310dff5f.chunk.js` offset 82237. Path expression: `/leads/bulk-delete`.

Request/configuration expression (source only):
```javascript
{lead_ids:e}
```

## api-0334 · POST /leads/bulk/nurture

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6375.310dff5f.chunk.js` offset 39692. Path expression: `/leads/bulk/nurture`.

Request/configuration expression (source only):
```javascript
{lead_ids:c,goal:m.trim(),channel:p,name:j.trim()}
```

## api-0335 · POST /leads/import-csv

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6375.310dff5f.chunk.js` offset 72489. Path expression: `/leads/import-csv`.

Request/configuration expression (source only):
```javascript
e
```

## api-0336 · GET /leads/statuses

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 404.

Source: `bundles/6375.310dff5f.chunk.js` offset 60920. Path expression: `/leads/statuses`.

No second argument at this call site. This does not establish the complete server contract.

## api-0337 · POST /leads/statuses

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6375.310dff5f.chunk.js` offset 32678. Path expression: `/leads/statuses`.

Request/configuration expression (source only):
```javascript
{label:c.trim(),color:o}
```

## api-0338 · DELETE /leads/statuses/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/6375.310dff5f.chunk.js` offset 33429. Path expression: `/leads/statuses/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0339 · PUT /leads/statuses/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6375.310dff5f.chunk.js` offset 30512. Path expression: `/leads/statuses/{e}`.

Request/configuration expression (source only):
```javascript
{label:y.trim(),color:z}
```

## api-0340 · GET /leads/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/6375.310dff5f.chunk.js` offset 45739. Path expression: `/leads/{c.lead_id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0341 · PUT /leads/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6375.310dff5f.chunk.js` offset 61047. Path expression: `/leads/{e}`.

Request/configuration expression (source only):
```javascript
{campaign_tag:za.trim()}
```

Source: `bundles/6375.310dff5f.chunk.js` offset 63259. Path expression: `/leads/{e}`.

Request/configuration expression (source only):
```javascript
{status:a}
```

## api-0342 · POST /leads/{parameter_1}/coach

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6375.310dff5f.chunk.js` offset 61320. Path expression: `/leads/{e.lead_id}/coach`.

No second argument at this call site. This does not establish the complete server contract.

## api-0343 · POST /leads/{parameter_1}/draft-reply

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/6375.310dff5f.chunk.js` offset 56474. Path expression: `/leads/{c.lead_id}/draft-reply`.

No second argument at this call site. This does not establish the complete server contract.

## api-0344 · POST /leads/{parameter_1}/score

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6375.310dff5f.chunk.js` offset 58159. Path expression: `/leads/{c.lead_id}/score`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/6375.310dff5f.chunk.js` offset 67192. Path expression: `/leads/{e}/score`.

No second argument at this call site. This does not establish the complete server contract.

## api-0345 · POST /leads/{parameter_1}/send-reply

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/2582.8768d086.chunk.js` offset 30115. Path expression: `/leads/{Y}/send-reply`.

Request/configuration expression (source only):
```javascript
{subject:ge.follow_up_email.subject||"Following up on our call",body:ge.follow_up_email.body}
```

Source: `bundles/6375.310dff5f.chunk.js` offset 51715. Path expression: `/leads/{c.lead_id}/send-reply`.

Request/configuration expression (source only):
```javascript
{subject:(null===(t=e.follow_up_email)||void 0===t?void 0:t.subject)||"Following up on our call",body:(null===(l=e.follow_up_email)||void 0===l?void 0:l.body)||""}
```

Source: `bundles/6375.310dff5f.chunk.js` offset 55150. Path expression: `/leads/{c.lead_id}/send-reply`.

Request/configuration expression (source only):
```javascript
h
```

Source: `bundles/9244.be0a4057.chunk.js` offset 5646. Path expression: `/leads/{e.lead_id}/send-reply`.

Request/configuration expression (source only):
```javascript
{subject:e.subject?"Re: ".concat(e.subject.replace(/^Re:\s*/i,"")):"Re: your message",body:v}
```

## api-0346 · POST /leads/{parameter_1}/send-sms

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/2582.8768d086.chunk.js` offset 30611. Path expression: `/leads/{Y}/send-sms`.

Request/configuration expression (source only):
```javascript
{message:ge.follow_up_sms}
```

Source: `bundles/6375.310dff5f.chunk.js` offset 52831. Path expression: `/leads/{c.lead_id}/send-sms`.

Request/configuration expression (source only):
```javascript
{message:e.follow_up_sms}
```

Source: `bundles/9244.be0a4057.chunk.js` offset 5572. Path expression: `/leads/{e.lead_id}/send-sms`.

Request/configuration expression (source only):
```javascript
{message:v}
```

## api-0347 · POST /linkedin-marketing/launch-campaign

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 227772. Path expression: `/linkedin-marketing/launch-campaign`.

Request/configuration expression (source only):
```javascript
{name:he||"".concat(xe," \xb7 ").concat((new Date).toISOString().slice(0,10)),daily_budget:parseFloat(Oe)?Math.round(parseFloat(Oe)/30*100)/100:50,objective:"WEBSITE_VISITS",headline:r.headline||he||"",description:r.description||"",landing_url:fe||""}
```

## api-0348 · POST /linkedin-marketing/push-audience

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 89033. Path expression: `/linkedin-marketing/push-audience`.

Request/configuration expression (source only):
```javascript
{audience_id:us,name:(null===e||void 0===e?void 0:e.name)||"Veluro Intent \xb7 audience #".concat(us)}
```

## api-0349 · POST /linkedin-messaging/save-sequence

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5027.62c03e58.chunk.js` offset 10553. Path expression: `/linkedin-messaging/save-sequence`.

Request/configuration expression (source only):
```javascript
{lead_id:(null===I||void 0===I?void 0:I.lead_id)||void 0,lead:null!==I&&void 0!==I&&I.lead_id?void 0:I,sequence:P.sequence,campaign_id:Y||void 0}
```

Source: `bundles/531.d33736f5.chunk.js` offset 10666. Path expression: `/linkedin-messaging/save-sequence`.

Request/configuration expression (source only):
```javascript
{lead_id:(null===I||void 0===I?void 0:I.lead_id)||void 0,lead:null!==I&&void 0!==I&&I.lead_id?void 0:I,sequence:R.sequence,campaign_id:W||void 0}
```

Source: `bundles/6375.310dff5f.chunk.js` offset 15831. Path expression: `/linkedin-messaging/save-sequence`.

Request/configuration expression (source only):
```javascript
{lead_id:(null===q||void 0===q?void 0:q.lead_id)||void 0,lead:null!==q&&void 0!==q&&q.lead_id?void 0:q,sequence:M.sequence,campaign_id:Y||void 0}
```

## api-0350 · POST /linkedin-messaging/tasks/{parameter_1}/mark-sent

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/531.d33736f5.chunk.js` offset 27086. Path expression: `/linkedin-messaging/tasks/{e}/mark-sent`.

No second argument at this call site. This does not establish the complete server contract.

## api-0351 · POST /linkedin-messaging/tasks/{parameter_1}/skip

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/531.d33736f5.chunk.js` offset 27645. Path expression: `/linkedin-messaging/tasks/{e}/skip`.

No second argument at this call site. This does not establish the complete server contract.

## api-0352 · GET /linkedin-messaging/tasks?status=pending&limit=50

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/531.d33736f5.chunk.js` offset 23287. Path expression: `/linkedin-messaging/tasks?status=pending&limit=50`.

No second argument at this call site. This does not establish the complete server contract.

## api-0353 · GET /linkedin/campaigns

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/5027.62c03e58.chunk.js` offset 2809. Path expression: `/linkedin/campaigns`.

No second argument at this call site. This does not establish the complete server contract.

## api-0354 · DELETE /linkedin/campaigns/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/531.d33736f5.chunk.js` offset 35095. Path expression: `/linkedin/campaigns/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0355 · GET /linkedin/inbox

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/531.d33736f5.chunk.js` offset 29081. Path expression: `/linkedin/inbox`.

No second argument at this call site. This does not establish the complete server contract.

## api-0356 · GET /linkedin/posting/posts

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 89488. Path expression: `/linkedin/posting/posts`.

No second argument at this call site. This does not establish the complete server contract.

## api-0357 · POST /linkedin/posting/publish

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 91770. Path expression: `/linkedin/posting/publish`.

Request/configuration expression (source only):
```javascript
{message:i,image_url:n||void 0}
```

## api-0358 · GET /linkedin/posting/status

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 89391. Path expression: `/linkedin/posting/status`.

No second argument at this call site. This does not establish the complete server contract.

## api-0359 · GET /linkedin/prospects

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/531.d33736f5.chunk.js` offset 29007. Path expression: `/linkedin/prospects`.

No second argument at this call site. This does not establish the complete server contract.

## api-0360 · POST /linkedin/prospects

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/531.d33736f5.chunk.js` offset 31816. Path expression: `/linkedin/prospects`.

Request/configuration expression (source only):
```javascript
e
```

## api-0361 · DELETE /linkedin/prospects/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/531.d33736f5.chunk.js` offset 33620. Path expression: `/linkedin/prospects/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0362 · GET /linkedin/stats

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/531.d33736f5.chunk.js` offset 29114. Path expression: `/linkedin/stats`.

No second argument at this call site. This does not establish the complete server contract.

## api-0363 · DELETE /media/assets/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/5232.d3fe35f5.chunk.js` offset 8838. Path expression: `/media/assets/{e.asset_id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0364 · GET /media/assets/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 134253. Path expression: `/media/assets/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0365 · POST /media/assets/{parameter_1}/ai-edit

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 47383. Path expression: `/media/assets/{t.asset_id}/ai-edit`.

Request/configuration expression (source only):
```javascript
{prompt:le.trim()}
```

## api-0366 · POST /media/assets/{parameter_1}/edit-video

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 54875. Path expression: `/media/assets/{t.asset_id}/edit-video`.

Request/configuration expression (source only):
```javascript
{trim_start:n,trim_end:c,caption:u.trim(),caption_position:v,font_size:b,thumbnail_at:w-n}
```

## api-0367 · POST /media/assets/{parameter_1}/remove-background

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 48721. Path expression: `/media/assets/{t.asset_id}/remove-background`.

No second argument at this call site. This does not establish the complete server contract.

## api-0368 · POST /media/assets/{parameter_1}/resize-pack

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 50017. Path expression: `/media/assets/{t.asset_id}/resize-pack`.

No second argument at this call site. This does not establish the complete server contract.

## api-0369 · GET /media/assets?kind={parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/5232.d3fe35f5.chunk.js` offset 1103. Path expression: `/media/assets?kind={T}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0370 · POST /media/slideshow

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/8947.ffec9124.chunk.js` offset 76017. Path expression: `/media/slideshow`.

Request/configuration expression (source only):
```javascript
{image_urls:a.map(e=>e.url),captions:a.map(e=>e.caption),seconds_per:l,ratio:c}
```

## api-0371 · POST /media/upload

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 61358. Path expression: `/media/upload`.

Request/configuration expression (source only):
```javascript
a
```

Source: `bundles/5232.d3fe35f5.chunk.js` offset 14883. Path expression: `https://veluro.ai/api/media/upload`.

Request/configuration expression (source only):
```javascript
s
```

## api-0372 · GET /media/video-edit-status/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 55140. Path expression: `/media/video-edit-status/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0373 · POST /meta/early-access-request

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 64905. Path expression: `/meta/early-access-request`.

Request/configuration expression (source only):
```javascript
{facebook_profile:m.trim()}
```

## api-0374 · POST /meta/pages/ai-caption

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 12772. Path expression: `/meta/pages/ai-caption`.

Request/configuration expression (source only):
```javascript
{context:(null===i||void 0===i?void 0:i.name)||"a branded design",platform:"both"}
```

## api-0375 · GET /meta/pages/analytics

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 122824. Path expression: `/meta/pages/analytics`.

No second argument at this call site. This does not establish the complete server contract.

## api-0376 · POST /meta/pages/analytics/recommendations

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 124525. Path expression: `/meta/pages/analytics/recommendations`.

No second argument at this call site. This does not establish the complete server contract.

## api-0377 · GET /meta/pages/connected

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 211202. Path expression: `/meta/pages/connected`.

No second argument at this call site. This does not establish the complete server contract.

## api-0378 · GET /meta/pages/instagram/account

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 13377. Path expression: `/meta/pages/instagram/account`.

No second argument at this call site. This does not establish the complete server contract.

## api-0379 · GET /meta/pages/instagram/posts

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 77351. Path expression: `/meta/pages/instagram/posts`.

No second argument at this call site. This does not establish the complete server contract.

## api-0380 · POST /meta/pages/instagram/publish

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 19364. Path expression: `/meta/pages/instagram/publish`.

Request/configuration expression (source only):
```javascript
{caption:k,image_url:J(i.url)}
```

Source: `bundles/2825.52a0948d.chunk.js` offset 81129. Path expression: `/meta/pages/instagram/publish`.

Request/configuration expression (source only):
```javascript
{caption:c,image_url:x||void 0,video_url:m||void 0}
```

## api-0381 · POST /meta/pages/instagram/schedule

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 83520. Path expression: `/meta/pages/instagram/schedule`.

Request/configuration expression (source only):
```javascript
{caption:c,image_url:x||void 0,video_url:m||void 0,scheduled_at:new Date(j).toISOString()}
```

## api-0382 · GET /meta/pages/instagram/scheduled

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2825.52a0948d.chunk.js` offset 77463. Path expression: `/meta/pages/instagram/scheduled`.

No second argument at this call site. This does not establish the complete server contract.

## api-0383 · DELETE /meta/pages/instagram/scheduled/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 84924. Path expression: `/meta/pages/instagram/scheduled/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0384 · PATCH /meta/pages/instagram/scheduled/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 145124. Path expression: `/meta/pages/instagram/scheduled/{a.id}`.

Request/configuration expression (source only):
```javascript
{scheduled_at:i}
```

## api-0385 · GET /meta/pages/profiles

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2825.52a0948d.chunk.js` offset 34006. Path expression: `/meta/pages/profiles`.

No second argument at this call site. This does not establish the complete server contract.

## api-0386 · POST /meta/pages/profiles

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 45073. Path expression: `/meta/pages/profiles`.

Request/configuration expression (source only):
```javascript
(0,Y.A)({page_id:J,page_name:(null===e||void 0===e?void 0:e.name)||""},ne)
```

## api-0387 · POST /meta/pages/publish

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 19050. Path expression: `/meta/pages/publish`.

Request/configuration expression (source only):
```javascript
{page_id:p,message:k,image_url:J(i.url)}
```

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 87783. Path expression: `/meta/pages/publish`.

Request/configuration expression (source only):
```javascript
{page_id:T,message:D,video_url:be(l.output_url)}
```

Source: `bundles/2825.52a0948d.chunk.js` offset 64155. Path expression: `/meta/pages/publish`.

Request/configuration expression (source only):
```javascript
{page_id:d,message:h,image_url:p||void 0,video_url:g||void 0}
```

## api-0388 · GET /meta/pages/published

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 59709. Path expression: `/meta/pages/published`.

No second argument at this call site. This does not establish the complete server contract.

## api-0389 · POST /meta/pages/published/{parameter_1}/refresh

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 59821. Path expression: `/meta/pages/published/{e}/refresh`.

No second argument at this call site. This does not establish the complete server contract.

## api-0390 · POST /meta/pages/schedule

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 66462. Path expression: `/meta/pages/schedule`.

Request/configuration expression (source only):
```javascript
{page_id:d,message:h,image_url:p||void 0,video_url:g||void 0,scheduled_at:new Date(D).toISOString()}
```

## api-0391 · GET /meta/pages/scheduled

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2825.52a0948d.chunk.js` offset 58834. Path expression: `/meta/pages/scheduled`.

No second argument at this call site. This does not establish the complete server contract.

## api-0392 · DELETE /meta/pages/scheduled/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 67968. Path expression: `/meta/pages/scheduled/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0393 · PATCH /meta/pages/scheduled/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 145046. Path expression: `/meta/pages/scheduled/{a.id}`.

Request/configuration expression (source only):
```javascript
{scheduled_at:i}
```

## api-0394 · POST /meta/pages/subscribe-webhook

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 100826. Path expression: `/meta/pages/subscribe-webhook`.

No second argument at this call site. This does not establish the complete server contract.

## api-0395 · POST /meta/pages/sync-leads

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 165929. Path expression: `/meta/pages/sync-leads`.

No second argument at this call site. This does not establish the complete server contract.

## api-0396 · GET /meta/pages/webhook-events

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/6375.310dff5f.chunk.js` offset 71137. Path expression: `/meta/pages/webhook-events`.

No second argument at this call site. This does not establish the complete server contract.

## api-0397 · GET /next-action

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/4278.c2617230.chunk.js` offset 14094. Path expression: `/next-action`.

No second argument at this call site. This does not establish the complete server contract.

## api-0398 · GET /notifications

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200, 500.

Source: `bundles/6184.08cd5e77.chunk.js` offset 25802. Path expression: `/notifications`.

No second argument at this call site. This does not establish the complete server contract.

## api-0399 · POST /notifications/mark-read

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6184.08cd5e77.chunk.js` offset 28371. Path expression: `/notifications/mark-read`.

Request/configuration expression (source only):
```javascript
{}
```

## api-0400 · GET /notifications/monitor-status

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200, 500.

Source: `bundles/6184.08cd5e77.chunk.js` offset 26086. Path expression: `/notifications/monitor-status`.

No second argument at this call site. This does not establish the complete server contract.

## api-0401 · GET /notifications/smart-alerts

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200, 500.

Source: `bundles/6184.08cd5e77.chunk.js` offset 25989. Path expression: `/notifications/smart-alerts`.

No second argument at this call site. This does not establish the complete server contract.

## api-0402 · POST /notifications/smart-alerts/{parameter_1}/dismiss

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6184.08cd5e77.chunk.js` offset 32902. Path expression: `/notifications/smart-alerts/{e}/dismiss`.

No second argument at this call site. This does not establish the complete server contract.

## api-0403 · POST /notifications/smart-alerts/{parameter_1}/read

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6184.08cd5e77.chunk.js` offset 32247. Path expression: `/notifications/smart-alerts/{t.alert_id}/read`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/7010.d6d62a55.chunk.js` offset 4105. Path expression: `/notifications/smart-alerts/{e}/read`.

No second argument at this call site. This does not establish the complete server contract.

## api-0404 · POST /notifications/smart-scan

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/6184.08cd5e77.chunk.js` offset 27959. Path expression: `/notifications/smart-scan`.

No second argument at this call site. This does not establish the complete server contract.

## api-0405 · GET /notifications/unread-count

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200, 500.

Source: `bundles/6184.08cd5e77.chunk.js` offset 25886. Path expression: `/notifications/unread-count`.

No second argument at this call site. This does not establish the complete server contract.

## api-0406 · GET /nurture/sequences

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 221632. Path expression: `/nurture/sequences`.

No second argument at this call site. This does not establish the complete server contract.

## api-0407 · POST /nurture/sequences/{parameter_1}/activate-send

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/659.f8c47505.chunk.js` offset 12156. Path expression: `/nurture/sequences/{Q.sequence_id}/activate-send`.

No second argument at this call site. This does not establish the complete server contract.

## api-0408 · GET /nurture/sequences/{parameter_1}/leads

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/659.f8c47505.chunk.js` offset 5070. Path expression: `/nurture/sequences/{e.sequence_id}/leads`.

No second argument at this call site. This does not establish the complete server contract.

## api-0409 · GET /oauth/calendar/connect

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/4073.67a982c5.chunk.js` offset 6330. Path expression: `/oauth/calendar/connect`.

No second argument at this call site. This does not establish the complete server contract.

## api-0410 · POST /omnirogue/assistant

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/8947.ffec9124.chunk.js` offset 3719. Path expression: `/omnirogue/assistant`.

Request/configuration expression (source only):
```javascript
{session_id:N.current,message:t}
```

## api-0411 · GET /omnirogue/assistant/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/8947.ffec9124.chunk.js` offset 3250. Path expression: `/omnirogue/assistant/{N.current}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0412 · POST /omnirogue/generate

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/8947.ffec9124.chunk.js` offset 32690. Path expression: `/omnirogue/generate`.

Request/configuration expression (source only):
```javascript
{model:T,prompt:a.prompt,aspect_ratio:C.ratio,duration:C.segment_duration,image_url:"",group_id:e,segment_index:t,segment_label:a.label}
```

Source: `bundles/8947.ffec9124.chunk.js` offset 32999. Path expression: `/omnirogue/generate`.

Request/configuration expression (source only):
```javascript
{model:T,prompt:C.prompt,aspect_ratio:C.ratio,duration:G?Math.min(m.duration,16):0,image_url:"",overlay_text:G?(C.overlay_text||"").trim():""}
```

Source: `bundles/8947.ffec9124.chunk.js` offset 44768. Path expression: `/omnirogue/generate`.

Request/configuration expression (source only):
```javascript
{model:e.model,prompt:e.prompt,aspect_ratio:e.aspect_ratio||"",duration:e.duration||0,image_url:"",group_id:e.group_id,segment_index:e.segment_index||0,segment_label:e.segment_label||""}
```

Source: `bundles/8947.ffec9124.chunk.js` offset 95240. Path expression: `/omnirogue/generate`.

Request/configuration expression (source only):
```javascript
{model:C,prompt:I,aspect_ratio:q,duration:"video"===A?U:0,image_url:Y,overlay_text:"video"===A?P.trim():"",overlay_style:"video"===A&&P.trim()?E:{},voice:"avatar"===A||"audio"===A?Q:""}
```

## api-0413 · GET /omnirogue/generations

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/8947.ffec9124.chunk.js` offset 79194. Path expression: `/omnirogue/generations`.

No second argument at this call site. This does not establish the complete server contract.

## api-0414 · GET /omnirogue/models

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/8947.ffec9124.chunk.js` offset 79444. Path expression: `/omnirogue/models`.

No second argument at this call site. This does not establish the complete server contract.

## api-0415 · POST /omnirogue/topup

Effect classification: **billing / financial change**. Evidence: source observed.

Source: `bundles/8947.ffec9124.chunk.js` offset 83051. Path expression: `/omnirogue/topup`.

Request/configuration expression (source only):
```javascript
{pack:e}
```

## api-0416 · POST /omnirogue/topup/confirm

Effect classification: **billing / financial change**. Evidence: source observed.

Source: `bundles/8947.ffec9124.chunk.js` offset 79938. Path expression: `/omnirogue/topup/confirm`.

Request/configuration expression (source only):
```javascript
{session_id:e}
```

## api-0417 · GET /omnirogue/usage

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/8947.ffec9124.chunk.js` offset 79363. Path expression: `/omnirogue/usage`.

No second argument at this call site. This does not establish the complete server contract.

## api-0418 · GET /onboarding

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/479.0fb227a6.chunk.js` offset 14487. Path expression: `/onboarding`.

No second argument at this call site. This does not establish the complete server contract.

## api-0419 · POST /onboarding/launch-prebuilt

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/4278.c2617230.chunk.js` offset 12209. Path expression: `/onboarding/launch-prebuilt`.

No second argument at this call site. This does not establish the complete server contract.

## api-0420 · GET /onboarding/prep-state

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/4278.c2617230.chunk.js` offset 9412. Path expression: `/onboarding/prep-state`.

No second argument at this call site. This does not establish the complete server contract.

## api-0421 · POST /onboarding/prep-state/dismiss

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/4278.c2617230.chunk.js` offset 13693. Path expression: `/onboarding/prep-state/dismiss`.

No second argument at this call site. This does not establish the complete server contract.

## api-0422 · POST /onboarding2/ack-upgrade

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6184.08cd5e77.chunk.js` offset 63250. Path expression: `/onboarding2/ack-upgrade`.

No second argument at this call site. This does not establish the complete server contract.

## api-0423 · POST /onboarding2/analyze-website

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/1505.10f94677.chunk.js` offset 6254. Path expression: `/onboarding2/analyze-website`.

Request/configuration expression (source only):
```javascript
{url:e}
```

## api-0424 · POST /onboarding2/answer

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1505.10f94677.chunk.js` offset 5455. Path expression: `/onboarding2/answer`.

Request/configuration expression (source only):
```javascript
{field:t.field,value:e,step:_+1}
```

Source: `bundles/1505.10f94677.chunk.js` offset 5594. Path expression: `/onboarding2/answer`.

Request/configuration expression (source only):
```javascript
{field:"social_urls",value:G,step:_+1}
```

## api-0425 · POST /onboarding2/complete

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1505.10f94677.chunk.js` offset 6828. Path expression: `/onboarding2/complete`.

No second argument at this call site. This does not establish the complete server contract.

## api-0426 · POST /onboarding2/event

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1505.10f94677.chunk.js` offset 5200. Path expression: `/onboarding2/event`.

Request/configuration expression (source only):
```javascript
{event:e,step:t}
```

## api-0427 · GET /onboarding2/first-win

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/4278.c2617230.chunk.js` offset 4338. Path expression: `/onboarding2/first-win`.

No second argument at this call site. This does not establish the complete server contract.

## api-0428 · POST /onboarding2/first-win/celebrated

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/4278.c2617230.chunk.js` offset 4465. Path expression: `/onboarding2/first-win/celebrated`.

No second argument at this call site. This does not establish the complete server contract.

## api-0429 · POST /onboarding2/help-icp

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1505.10f94677.chunk.js` offset 17017. Path expression: `/onboarding2/help-icp`.

No second argument at this call site. This does not establish the complete server contract.

## api-0430 · POST /onboarding2/skip

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1505.10f94677.chunk.js` offset 7138. Path expression: `/onboarding2/skip`.

No second argument at this call site. This does not establish the complete server contract.

## api-0431 · GET /onboarding2/state

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/1505.10f94677.chunk.js` offset 4564. Path expression: `/onboarding2/state`.

No second argument at this call site. This does not establish the complete server contract.

## api-0432 · GET /outreach/campaigns

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2484.7278fdd8.chunk.js` offset 24740. Path expression: `/outreach/campaigns`.

No second argument at this call site. This does not establish the complete server contract.

## api-0433 · POST /outreach/campaigns

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 63588. Path expression: `/outreach/campaigns`.

Request/configuration expression (source only):
```javascript
{name:n,list_id:d,purpose:h,value_prop:f,tone:w,sequence_length:N,cta_label:A,cta_url:_,send_via:q||void 0,own_emails:z.trim()||void 0}
```

## api-0434 · GET /outreach/campaigns/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 71772. Path expression: `/outreach/campaigns/{v.id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0435 · POST /outreach/campaigns/{parameter_1}/launch

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 71881. Path expression: `/outreach/campaigns/{v.id}/launch`.

Request/configuration expression (source only):
```javascript
{}
```

## api-0436 · POST /outreach/campaigns/{parameter_1}/pause

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 73579. Path expression: `/outreach/campaigns/{v.id}/pause`.

No second argument at this call site. This does not establish the complete server contract.

## api-0437 · POST /outreach/connect

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 43136. Path expression: `/outreach/connect`.

Request/configuration expression (source only):
```javascript
{api_key:n.trim()}
```

## api-0438 · GET /outreach/connection

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2484.7278fdd8.chunk.js` offset 27731. Path expression: `/outreach/connection`.

No second argument at this call site. This does not establish the complete server contract.

## api-0439 · DELETE /outreach/disconnect

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 35421. Path expression: `/outreach/disconnect`.

No second argument at this call site. This does not establish the complete server contract.

## api-0440 · POST /outreach/from-address

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 46199. Path expression: `/outreach/from-address`.

Request/configuration expression (source only):
```javascript
{from_name:g,from_email:w,reply_to_email:y||w,inbound_subdomain:k}
```

## api-0441 · GET /outreach/gmail-oauth/start

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 14719. Path expression: `/outreach/gmail-oauth/start`.

No second argument at this call site. This does not establish the complete server contract.

## api-0442 · GET /outreach/lists

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2484.7278fdd8.chunk.js` offset 24646. Path expression: `/outreach/lists`.

No second argument at this call site. This does not establish the complete server contract.

## api-0443 · POST /outreach/lists/upload

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 55654. Path expression: `/outreach/lists/upload`.

Request/configuration expression (source only):
```javascript
e
```

## api-0444 · DELETE /outreach/lists/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 53605. Path expression: `/outreach/lists/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0445 · GET /outreach/mailboxes

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2484.7278fdd8.chunk.js` offset 8253. Path expression: `/outreach/mailboxes`.

No second argument at this call site. This does not establish the complete server contract.

## api-0446 · POST /outreach/mailboxes

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 21238. Path expression: `/outreach/mailboxes`.

Request/configuration expression (source only):
```javascript
{provider:i,email:o.email,password:o.password,from_name:o.from_name,daily_cap:Number(o.daily_cap)||50,smtp_host:o.smtp_host||void 0,smtp_port:o.smtp_port?Number(o.smtp_port):void 0,imap_host:o.imap_host||void 0,imap_port:o.imap_port?Number(o.imap_port):void 0}
```

## api-0447 · POST /outreach/mailboxes/bulk

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 13496. Path expression: `/outreach/mailboxes/bulk`.

Request/configuration expression (source only):
```javascript
{rows:a,skip_verify:j}
```

## api-0448 · DELETE /outreach/mailboxes/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 8514. Path expression: `/outreach/mailboxes/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0449 · GET /outreach/mailboxes/{parameter_1}/health

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 4011. Path expression: `/outreach/mailboxes/{t}/health`.

No second argument at this call site. This does not establish the complete server contract.

## api-0450 · POST /outreach/mailboxes/{parameter_1}/test

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 18280. Path expression: `/outreach/mailboxes/{e}/test`.

Request/configuration expression (source only):
```javascript
{to:t}
```

## api-0451 · POST /outreach/mailboxes/{parameter_1}/{parameter_2}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 8576. Path expression: `/outreach/mailboxes/{e}/{s}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0452 · POST /outreach/refresh-domains

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 33542. Path expression: `/outreach/refresh-domains`.

No second argument at this call site. This does not establish the complete server contract.

## api-0453 · GET /outreach/replies

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 77823. Path expression: `/outreach/replies`.

No second argument at this call site. This does not establish the complete server contract.

## api-0454 · GET /outreach/suppressions

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 78984. Path expression: `/outreach/suppressions`.

No second argument at this call site. This does not establish the complete server contract.

## api-0455 · POST /outreach/test-send

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/2484.7278fdd8.chunk.js` offset 51115. Path expression: `/outreach/test-send`.

Request/configuration expression (source only):
```javascript
{to:I.trim()}
```

## api-0456 · GET /partner/display-ads

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/6258.e2179577.chunk.js` offset 36190. Path expression: `/partner/display-ads`.

No second argument at this call site. This does not establish the complete server contract.

## api-0457 · POST /partner/display-ads/launch

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/6258.e2179577.chunk.js` offset 16038. Path expression: `/partner/display-ads/launch`.

Request/configuration expression (source only):
```javascript
{template_id:t.template_id,platform:s,budget:parseFloat(d),audience:{locations:m,interests:b}}
```

## api-0458 · GET /partner/google-ads

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/6258.e2179577.chunk.js` offset 17429. Path expression: `/partner/google-ads`.

No second argument at this call site. This does not establish the complete server contract.

## api-0459 · POST /partner/google-ads/launch

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/6258.e2179577.chunk.js` offset 22914. Path expression: `/partner/google-ads/launch`.

Request/configuration expression (source only):
```javascript
{template_ids:n,budget:parseFloat(m),locations:p}
```

## api-0460 · GET /partner/marketing-materials

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/6258.e2179577.chunk.js` offset 36108. Path expression: `/partner/marketing-materials`.

No second argument at this call site. This does not establish the complete server contract.

## api-0461 · GET /partner/promo-ads

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/6258.e2179577.chunk.js` offset 36154. Path expression: `/partner/promo-ads`.

No second argument at this call site. This does not establish the complete server contract.

## api-0462 · POST /partner/promo-ads/launch

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/6258.e2179577.chunk.js` offset 11166. Path expression: `/partner/promo-ads/launch`.

Request/configuration expression (source only):
```javascript
{template_id:t.template_id,platform:s,budget:parseFloat(d),audience:{age_min:parseInt(m),age_max:parseInt(p),locations:u,interests:w}}
```

## api-0463 · GET /partner/sixthshock

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/6258.e2179577.chunk.js` offset 30767. Path expression: `/partner/sixthshock`.

No second argument at this call site. This does not establish the complete server contract.

## api-0464 · POST /partner/sixthshock/launch

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/6258.e2179577.chunk.js` offset 27309. Path expression: `/partner/sixthshock/launch`.

Request/configuration expression (source only):
```javascript
{template_id:t.template_id,platform:m,budget:parseFloat(p),audience:{locations:u,interests:w}}
```

## api-0465 · GET /partner/team

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3089.bd3bb770.chunk.js` offset 38735. Path expression: `/partner/team`.

No second argument at this call site. This does not establish the complete server contract.

## api-0466 · POST /partner/team/accept

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/7530.cbbca67f.chunk.js` offset 4057. Path expression: `/partner/team/accept`.

Request/configuration expression (source only):
```javascript
{token:e}
```

## api-0467 · POST /partner/team/invite

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/3089.bd3bb770.chunk.js` offset 45734. Path expression: `/partner/team/invite`.

Request/configuration expression (source only):
```javascript
{email:m.trim(),name:u.trim(),permissions:g,origin_url:window.location.origin}
```

## api-0468 · GET /partner/team/invite/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/7530.cbbca67f.chunk.js` offset 2699. Path expression: `/partner/team/invite/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0469 · DELETE /partner/team/{parameter_1}

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/3089.bd3bb770.chunk.js` offset 42048. Path expression: `/partner/team/{e.member_id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0470 · PATCH /partner/team/{parameter_1}

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/3089.bd3bb770.chunk.js` offset 43042. Path expression: `/partner/team/{e.member_id}`.

Request/configuration expression (source only):
```javascript
{permissions:r}
```

## api-0471 · POST /partner/team/{parameter_1}/resend

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/3089.bd3bb770.chunk.js` offset 41280. Path expression: `/partner/team/{e.member_id}/resend`.

Request/configuration expression (source only):
```javascript
{origin_url:window.location.origin}
```

## api-0472 · GET /partner/video-ads

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/6258.e2179577.chunk.js` offset 36228. Path expression: `/partner/video-ads`.

No second argument at this call site. This does not establish the complete server contract.

## api-0473 · POST /partner/video-ads/launch

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/6258.e2179577.chunk.js` offset 5195. Path expression: `/partner/video-ads/launch`.

Request/configuration expression (source only):
```javascript
{template_id:t.template_id,platform:s,budget:parseFloat(d),audience:{locations:m}}
```

## api-0474 · GET /pixels

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/9409.287a8f68.chunk.js` offset 4507. Path expression: `/pixels`.

No second argument at this call site. This does not establish the complete server contract.

## api-0475 · POST /pixels

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/9409.287a8f68.chunk.js` offset 21423. Path expression: `/pixels`.

Request/configuration expression (source only):
```javascript
(0,a.A)((0,a.A)({},p),{},{name:t})
```

## api-0476 · DELETE /pixels/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/9409.287a8f68.chunk.js` offset 12729. Path expression: `/pixels/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0477 · POST /pixels/{parameter_1}/assign

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/9409.287a8f68.chunk.js` offset 14043. Path expression: `/pixels/{D.pixel_id}/assign`.

Request/configuration expression (source only):
```javascript
{reseller_landing:!D.reseller_landing}
```

Source: `bundles/9409.287a8f68.chunk.js` offset 15374. Path expression: `/pixels/{e}/assign`.

Request/configuration expression (source only):
```javascript
{funnel_ids:[t]}
```

Source: `bundles/9409.287a8f68.chunk.js` offset 23215. Path expression: `/pixels/{g.pixel_id}/assign`.

Request/configuration expression (source only):
```javascript
{funnel_ids:[e]}
```

## api-0478 · GET /pixels/{parameter_1}/install-code

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/9409.287a8f68.chunk.js` offset 12362. Path expression: `/pixels/{e}/install-code`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/9409.287a8f68.chunk.js` offset 21512. Path expression: `/pixels/{s.data.pixel_id}/install-code`.

No second argument at this call site. This does not establish the complete server contract.

## api-0479 · POST /pixels/{parameter_1}/toggle

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/9409.287a8f68.chunk.js` offset 11879. Path expression: `/pixels/{e}/toggle`.

No second argument at this call site. This does not establish the complete server contract.

## api-0480 · GET /platform/flags

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 50889. Path expression: `/platform/flags`.

No second argument at this call site. This does not establish the complete server contract.

## api-0481 · GET /proposal-templates

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2359.92b50d8d.chunk.js` offset 3265. Path expression: `/proposal-templates`.

No second argument at this call site. This does not establish the complete server contract.

## api-0482 · DELETE /proposal-templates/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/2359.92b50d8d.chunk.js` offset 6017. Path expression: `/proposal-templates/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0483 · GET /proposals

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2359.92b50d8d.chunk.js` offset 3163. Path expression: `/proposals`.

No second argument at this call site. This does not establish the complete server contract.

## api-0484 · POST /proposals

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2359.92b50d8d.chunk.js` offset 3878. Path expression: `/proposals`.

Request/configuration expression (source only):
```javascript
a
```

## api-0485 · POST /proposals/ai-draft

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2359.92b50d8d.chunk.js` offset 18994. Path expression: `/proposals/ai-draft`.

Request/configuration expression (source only):
```javascript
{client_name:(null===a||void 0===a?void 0:a.client_name)||"",client_company:(null===a||void 0===a?void 0:a.client_company)||"",project:R,budget_hint:H}
```

## api-0486 · DELETE /proposals/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/2359.92b50d8d.chunk.js` offset 17243. Path expression: `/proposals/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0487 · POST /proposals/{parameter_1}/save-template

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2359.92b50d8d.chunk.js` offset 7199. Path expression: `/proposals/{e.proposal_id}/save-template`.

Request/configuration expression (source only):
```javascript
{name:a.title}
```

## api-0488 · POST /proposals/{parameter_1}/send

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/2359.92b50d8d.chunk.js` offset 8574. Path expression: `/proposals/{e.proposal_id}/send`.

Request/configuration expression (source only):
```javascript
{}
```

## api-0489 · POST /public/demand/claim

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6184.08cd5e77.chunk.js` offset 59718. Path expression: `/public/demand/claim`.

Request/configuration expression (source only):
```javascript
{session_id:e}
```

## api-0490 · GET /public/demand/session/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `client-bundle.js` offset 663399. Path expression: `/public/demand/session/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0491 · POST /public/track

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `client-bundle.js` offset 39372. Path expression: `/public/track`.

Request/configuration expression (source only):
```javascript
{event:e,session_id:localStorage.getItem("veluro_demand_session")||"",utm:s(),meta:(0,r.A)((0,r.A)({},t),{},{path:window.location.pathname})}
```

## api-0492 · GET /referrals/partner-info/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `client-bundle.js` offset 14540. Path expression: `/referrals/partner-info/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0493 · POST /referrals/partner-signup

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/7266.5664065e.chunk.js` offset 32029. Path expression: `/referrals/partner-signup`.

Request/configuration expression (source only):
```javascript
(0,s.A)((0,s.A)({},i),{},{plan:l,partner_type:t.type,payout_email:i.payout_email||i.email,origin_url:window.location.origin,ref_code:(0,o.VC)()})
```

## api-0494 · GET /referrals/partner-signup/status/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/7266.5664065e.chunk.js` offset 24962. Path expression: `/referrals/partner-signup/status/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0495 · POST /referrals/partner/activate

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/3089.bd3bb770.chunk.js` offset 98227. Path expression: `/referrals/partner/activate`.

No second argument at this call site. This does not establish the complete server contract.

## api-0496 · POST /referrals/partner/change-plan

Effect classification: **billing / financial change**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 43786. Path expression: `/referrals/partner/change-plan`.

Request/configuration expression (source only):
```javascript
{plan:e,origin_url:window.location.origin}
```

Source: `bundles/3089.bd3bb770.chunk.js` offset 58720. Path expression: `/referrals/partner/change-plan`.

Request/configuration expression (source only):
```javascript
{plan:e}
```

## api-0497 · POST /referrals/partner/connect-onboarding

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/3089.bd3bb770.chunk.js` offset 103220. Path expression: `/referrals/partner/connect-onboarding`.

Request/configuration expression (source only):
```javascript
{origin_url:window.location.origin,country:re,payout_email:e}
```

## api-0498 · GET /referrals/partner/dashboard

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3089.bd3bb770.chunk.js` offset 96852. Path expression: `/referrals/partner/dashboard`.

No second argument at this call site. This does not establish the complete server contract.

## api-0499 · PUT /referrals/partner/income-goal

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3089.bd3bb770.chunk.js` offset 68414. Path expression: `/referrals/partner/income-goal`.

Request/configuration expression (source only):
```javascript
{goal:m}
```

## api-0500 · GET /referrals/partner/kit-stats

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3089.bd3bb770.chunk.js` offset 27849. Path expression: `/referrals/partner/kit-stats`.

No second argument at this call site. This does not establish the complete server contract.

## api-0501 · GET /referrals/partner/leaderboard

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3089.bd3bb770.chunk.js` offset 87602. Path expression: `/referrals/partner/leaderboard`.

No second argument at this call site. This does not establish the complete server contract.

## api-0502 · GET /referrals/partner/network-tree

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3089.bd3bb770.chunk.js` offset 48540. Path expression: `/referrals/partner/network-tree`.

No second argument at this call site. This does not establish the complete server contract.

## api-0503 · GET /referrals/partner/payout-history

Effect classification: **billing / financial change**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3089.bd3bb770.chunk.js` offset 70752. Path expression: `/referrals/partner/payout-history`.

No second argument at this call site. This does not establish the complete server contract.

## api-0504 · GET /referrals/partner/performance

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3089.bd3bb770.chunk.js` offset 78773. Path expression: `/referrals/partner/performance`.

No second argument at this call site. This does not establish the complete server contract.

## api-0505 · GET /referrals/partner/pixel-events

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3089.bd3bb770.chunk.js` offset 83014. Path expression: `/referrals/partner/pixel-events`.

No second argument at this call site. This does not establish the complete server contract.

## api-0506 · POST /referrals/partner/starter-kit

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3089.bd3bb770.chunk.js` offset 32611. Path expression: `/referrals/partner/starter-kit`.

Request/configuration expression (source only):
```javascript
{name:x,email:p,url:f}
```

## api-0507 · GET /referrals/partner/statement.csv

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/3089.bd3bb770.chunk.js` offset 105429. Path expression: `/referrals/partner/statement.csv`.

Request/configuration expression (source only):
```javascript
{responseType:"blob"}
```

## api-0508 · PUT /referrals/partner/vanity

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3089.bd3bb770.chunk.js` offset 99649. Path expression: `/referrals/partner/vanity`.

Request/configuration expression (source only):
```javascript
{slug:H}
```

## api-0509 · POST /referrals/pixel-event

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `client-bundle.js` offset 15370. Path expression: `/referrals/pixel-event`.

Request/configuration expression (source only):
```javascript
{ref_code:e,event:"PageView",path:window.location.pathname}
```

Source: `client-bundle.js` offset 15584. Path expression: `/referrals/pixel-event`.

Request/configuration expression (source only):
```javascript
{ref_code:e,event:"Lead",path:window.location.pathname}
```

## api-0510 · GET /referrals/pixel/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `client-bundle.js` offset 14782. Path expression: `/referrals/pixel/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0511 · GET /referrals/resolve/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/6476.efb7adc1.chunk.js` offset 266. Path expression: `https://veluro.ai/api/referrals/resolve/{encodeURIComponent(e)}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0512 · POST /referrals/track

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `client-bundle.js` offset 14351. Path expression: `/referrals/track`.

Request/configuration expression (source only):
```javascript
{ref_code:n,landing_path:window.location.pathname,asset:c||l()}
```

## api-0513 · POST /reply-drafter/analyze

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2752.d5b19c2e.chunk.js` offset 6708. Path expression: `/reply-drafter/analyze`.

Request/configuration expression (source only):
```javascript
{email_text:s}
```

## api-0514 · POST /reply-drafter/draft

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2752.d5b19c2e.chunk.js` offset 2493. Path expression: `/reply-drafter/draft`.

Request/configuration expression (source only):
```javascript
{email_text:s,outcome_label:a?"":e.label,custom_outcome:a?R:"",tone:I}
```

## api-0515 · GET /reply-drafter/history

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2752.d5b19c2e.chunk.js` offset 2193. Path expression: `/reply-drafter/history`.

No second argument at this call site. This does not establish the complete server contract.

## api-0516 · POST /reply-drafter/refine

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2752.d5b19c2e.chunk.js` offset 3051. Path expression: `/reply-drafter/refine`.

Request/configuration expression (source only):
```javascript
{subject:s.subject,body:s.body,instruction:t}
```

## api-0517 · GET /reports

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/775.48368b84.chunk.js` offset 69892. Path expression: `/reports`.

No second argument at this call site. This does not establish the complete server contract.

## api-0518 · POST /reports/generate

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/775.48368b84.chunk.js` offset 70666. Path expression: `/reports/generate`.

No second argument at this call site. This does not establish the complete server contract.

## api-0519 · GET /reputation

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/628.0eed46e1.chunk.js` offset 2352. Path expression: `/reputation`.

No second argument at this call site. This does not establish the complete server contract.

## api-0520 · PUT /reputation/manual

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/628.0eed46e1.chunk.js` offset 8139. Path expression: `/reputation/manual`.

Request/configuration expression (source only):
```javascript
{platform:m.platform,rating:Number(m.rating),review_count:Number(m.review_count||0)}
```

## api-0521 · DELETE /reputation/platform/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/628.0eed46e1.chunk.js` offset 6303. Path expression: `/reputation/platform/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0522 · POST /reputation/scan

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/628.0eed46e1.chunk.js` offset 3647. Path expression: `/reputation/scan`.

Request/configuration expression (source only):
```javascript
{}
```

## api-0523 · GET /sales-coach/context

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2582.8768d086.chunk.js` offset 9979. Path expression: `/sales-coach/context`.

No second argument at this call site. This does not establish the complete server contract.

## api-0524 · POST /sales-coach/live

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2582.8768d086.chunk.js` offset 11971. Path expression: `/sales-coach/live`.

Request/configuration expression (source only):
```javascript
{session_id:X,transcript:e,recent_chunk:e.slice(-2400)}
```

## api-0525 · POST /sales-coach/objection

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2582.8768d086.chunk.js` offset 12272. Path expression: `/sales-coach/objection`.

Request/configuration expression (source only):
```javascript
{objection:ze,playbook:I.playbook||T,context:"".concat(I.offer||""," \u2192 ").concat(I.target_customer||"")}
```

## api-0526 · GET /sales-coach/playbooks

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2582.8768d086.chunk.js` offset 9939. Path expression: `/sales-coach/playbooks`.

No second argument at this call site. This does not establish the complete server contract.

## api-0527 · POST /sales-coach/post-analysis

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2582.8768d086.chunk.js` offset 29220. Path expression: `/sales-coach/post-analysis`.

Request/configuration expression (source only):
```javascript
{session_id:X,transcript:pe,playbook:I.playbook||T}
```

## api-0528 · POST /sales-coach/prep

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2582.8768d086.chunk.js` offset 18364. Path expression: `/sales-coach/prep`.

Request/configuration expression (source only):
```javascript
(0,t.A)((0,t.A)({},I),{},{known_objections:s,session_id:X,lead_id:Y})
```

## api-0529 · GET /sales-coach/seats

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 11596. Path expression: `/sales-coach/seats`.

No second argument at this call site. This does not establish the complete server contract.

## api-0530 · DELETE /sales-coach/seats/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 13655. Path expression: `/sales-coach/seats/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0531 · GET /sales-coach/sessions

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2582.8768d086.chunk.js` offset 10017. Path expression: `/sales-coach/sessions`.

No second argument at this call site. This does not establish the complete server contract.

## api-0532 · DELETE /sales-coach/sessions/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/2582.8768d086.chunk.js` offset 35409. Path expression: `/sales-coach/sessions/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0533 · GET /sales-coach/sessions/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2582.8768d086.chunk.js` offset 11028. Path expression: `/sales-coach/sessions/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0534 · POST /sales-coach/transcribe

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2582.8768d086.chunk.js` offset 27813. Path expression: `/sales-coach/transcribe`.

Request/configuration expression (source only):
```javascript
e
```

## api-0535 · GET /sales-coach/usage

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2582.8768d086.chunk.js` offset 9603. Path expression: `/sales-coach/usage`.

No second argument at this call site. This does not establish the complete server contract.

## api-0536 · GET /sales-coach/win-rate-report

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2582.8768d086.chunk.js` offset 10402. Path expression: `/sales-coach/win-rate-report`.

No second argument at this call site. This does not establish the complete server contract.

## api-0537 · POST /seo/audit

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5329.6535fc45.chunk.js` offset 8771. Path expression: `/seo/audit`.

Request/configuration expression (source only):
```javascript
{url:P||void 0}
```

## api-0538 · PUT /seo/competitor

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5329.6535fc45.chunk.js` offset 5832. Path expression: `/seo/competitor`.

Request/configuration expression (source only):
```javascript
{domain:e}
```

## api-0539 · POST /seo/keywords

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5329.6535fc45.chunk.js` offset 6387. Path expression: `/seo/keywords`.

Request/configuration expression (source only):
```javascript
{keywords:e}
```

## api-0540 · GET /seo/latest

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/5329.6535fc45.chunk.js` offset 6167. Path expression: `/seo/latest`.

No second argument at this call site. This does not establish the complete server contract.

## api-0541 · GET /seo/ranks

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/5329.6535fc45.chunk.js` offset 5568. Path expression: `/seo/ranks`.

No second argument at this call site. This does not establish the complete server contract.

## api-0542 · POST /seo/ranks/check

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5329.6535fc45.chunk.js` offset 12957. Path expression: `/seo/ranks/check`.

No second argument at this call site. This does not establish the complete server contract.

## api-0543 · GET /seo/ranks/history

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/5329.6535fc45.chunk.js` offset 5718. Path expression: `/seo/ranks/history`.

No second argument at this call site. This does not establish the complete server contract.

## api-0544 · PUT /seo/settings

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5329.6535fc45.chunk.js` offset 8167. Path expression: `/seo/settings`.

Request/configuration expression (source only):
```javascript
{rescan_enabled:e}
```

## api-0545 · GET /service-brain/catalog

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/5753.fcee46d5.chunk.js` offset 27470. Path expression: `/service-brain/catalog`.

No second argument at this call site. This does not establish the complete server contract.

## api-0546 · GET /service-brain/engines

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/5753.fcee46d5.chunk.js` offset 27654. Path expression: `/service-brain/engines`.

No second argument at this call site. This does not establish the complete server contract.

## api-0547 · POST /service-brain/engines

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5753.fcee46d5.chunk.js` offset 36334. Path expression: `/service-brain/engines`.

Request/configuration expression (source only):
```javascript
{industry:Z,service:t,market:H,goal:P,notes:U}
```

Source: `bundles/5753.fcee46d5.chunk.js` offset 36738. Path expression: `/service-brain/engines`.

Request/configuration expression (source only):
```javascript
{industry:Z,service:X[0],market:H,goal:P,notes:U}
```

## api-0548 · DELETE /service-brain/engines/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/5753.fcee46d5.chunk.js` offset 31111. Path expression: `/service-brain/engines/{t.engine_id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0549 · GET /service-brain/engines/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/5753.fcee46d5.chunk.js` offset 28059. Path expression: `/service-brain/engines/{e.engine_id}`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/5753.fcee46d5.chunk.js` offset 37188. Path expression: `/service-brain/engines/{e.data.engine_id}`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/5753.fcee46d5.chunk.js` offset 38611. Path expression: `/service-brain/engines/{T.engine_id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0550 · PATCH /service-brain/engines/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5753.fcee46d5.chunk.js` offset 15258. Path expression: `/service-brain/engines/{l.engine_id}`.

Request/configuration expression (source only):
```javascript
{blueprint:m}
```

## api-0551 · POST /service-brain/engines/{parameter_1}/creatives/edit

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5753.fcee46d5.chunk.js` offset 10593. Path expression: `/service-brain/engines/{s}/creatives/edit`.

Request/configuration expression (source only):
```javascript
{index:a,instruction:c.trim()}
```

## api-0552 · POST /service-brain/engines/{parameter_1}/creatives/overlay

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5753.fcee46d5.chunk.js` offset 10996. Path expression: `/service-brain/engines/{s}/creatives/overlay`.

Request/configuration expression (source only):
```javascript
{index:a,headline:x.trim(),include_logo:m}
```

## api-0553 · POST /service-brain/engines/{parameter_1}/creatives/revert

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/5753.fcee46d5.chunk.js` offset 12269. Path expression: `/service-brain/engines/{s}/creatives/revert`.

Request/configuration expression (source only):
```javascript
{index:a}
```

## api-0554 · POST /service-brain/engines/{parameter_1}/launch

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/5753.fcee46d5.chunk.js` offset 17003. Path expression: `/service-brain/engines/{l.engine_id}/launch`.

Request/configuration expression (source only):
```javascript
{generate_images:j,publish_landing:M}
```

## api-0555 · GET /settings

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200, 500.

Source: `client-bundle.js` offset 167172. Path expression: `/settings`.

No second argument at this call site. This does not establish the complete server contract.

## api-0556 · PUT /settings

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 34385. Path expression: `/settings`.

Request/configuration expression (source only):
```javascript
(0,s.A)((0,s.A)({},G||{}),{},{language:e})
```

Source: `bundles/3058.d2beb0a0.chunk.js` offset 49373. Path expression: `/settings`.

Request/configuration expression (source only):
```javascript
G
```

## api-0557 · POST /social-manager/analyze

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 34227. Path expression: `/social-manager/analyze`.

Request/configuration expression (source only):
```javascript
{website_url:w.trim()}
```

## api-0558 · POST /social-manager/approve-schedule

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 48574. Path expression: `/social-manager/approve-schedule`.

Request/configuration expression (source only):
```javascript
{post_ids:E,posts_per_day:R}
```

## api-0559 · GET /social-manager/best-times

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 58920. Path expression: `/social-manager/best-times`.

No second argument at this call site. This does not establish the complete server contract.

## api-0560 · POST /social-manager/generate-batch

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 41800. Path expression: `/social-manager/generate-batch`.

Request/configuration expression (source only):
```javascript
{categories:S,count:I,platforms:U,page_id:J}
```

## api-0561 · GET /social-manager/jobs/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 42030. Path expression: `/social-manager/jobs/{e.data.job_id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0562 · GET /social-manager/learnings

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2825.52a0948d.chunk.js` offset 33794. Path expression: `/social-manager/learnings`.

No second argument at this call site. This does not establish the complete server contract.

## api-0563 · GET /social-manager/plan

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2825.52a0948d.chunk.js` offset 33586. Path expression: `/social-manager/plan`.

No second argument at this call site. This does not establish the complete server contract.

## api-0564 · GET /social-stats/overview

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/775.48368b84.chunk.js` offset 43731. Path expression: `/social-stats/overview`.

No second argument at this call site. This does not establish the complete server contract.

## api-0565 · GET /social/autopilot

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 20325. Path expression: `/social/autopilot`.

No second argument at this call site. This does not establish the complete server contract.

## api-0566 · PUT /social/autopilot

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 31774. Path expression: `/social/autopilot`.

Request/configuration expression (source only):
```javascript
i
```

## api-0567 · GET /social/platform-status

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2825.52a0948d.chunk.js` offset 132667. Path expression: `/social/platform-status`.

No second argument at this call site. This does not establish the complete server contract.

## api-0568 · GET /social/posts

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 133032. Path expression: `/social/posts`.

No second argument at this call site. This does not establish the complete server contract.

## api-0569 · POST /social/posts

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 153395. Path expression: `/social/posts`.

Request/configuration expression (source only):
```javascript
{platforms:d,fb_page_id:h||null,content:f,tone:r,image_url:w||null,video_url:K||null,media_asset_id:X||null,media_kind:ee||null,scheduled_at:s,status:e}
```

## api-0570 · POST /social/posts/generate

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 156991. Path expression: `/social/posts/generate`.

Request/configuration expression (source only):
```javascript
{topic:n,tone:r,platforms:d}
```

## api-0571 · POST /social/posts/generate-image

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 159367. Path expression: `/social/posts/generate-image`.

Request/configuration expression (source only):
```javascript
{prompt:y}
```

## api-0572 · POST /social/posts/generate-video

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 161804. Path expression: `/social/posts/generate-video`.

Request/configuration expression (source only):
```javascript
{prompt:q}
```

## api-0573 · GET /social/posts/video-status/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 152960. Path expression: `/social/posts/video-status/{B}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0574 · DELETE /social/posts/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 17909. Path expression: `/social/posts/{t.post_id}`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/2825.52a0948d.chunk.js` offset 151194. Path expression: `/social/posts/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0575 · PUT /social/posts/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 14084. Path expression: `/social/posts/{t.post_id}`.

Request/configuration expression (source only):
```javascript
a
```

Source: `bundles/2825.52a0948d.chunk.js` offset 145463. Path expression: `/social/posts/{a.id}`.

Request/configuration expression (source only):
```javascript
{scheduled_at:s}
```

## api-0576 · POST /social/posts/{parameter_1}/approve

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 150759. Path expression: `/social/posts/{e}/approve`.

No second argument at this call site. This does not establish the complete server contract.

## api-0577 · POST /social/posts/{parameter_1}/publish

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 150248. Path expression: `/social/posts/{e}/publish`.

No second argument at this call site. This does not establish the complete server contract.

## api-0578 · POST /social/queue/generate

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 141443. Path expression: `/social/queue/generate`.

Request/configuration expression (source only):
```javascript
{platforms:W,focus_areas:U}
```

## api-0579 · GET /storyboard/projects

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3612.4edec266.chunk.js` offset 5340. Path expression: `/storyboard/projects`.

No second argument at this call site. This does not establish the complete server contract.

## api-0580 · POST /storyboard/projects

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3612.4edec266.chunk.js` offset 17114. Path expression: `/storyboard/projects`.

Request/configuration expression (source only):
```javascript
{brief:w.trim(),target_duration:k,aspect:A}
```

## api-0581 · GET /storyboard/projects/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/3612.4edec266.chunk.js` offset 5644. Path expression: `/storyboard/projects/{s.project_id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0582 · PUT /storyboard/projects/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3612.4edec266.chunk.js` offset 5845. Path expression: `/storyboard/projects/{s.project_id}`.

Request/configuration expression (source only):
```javascript
{scenes:e}
```

## api-0583 · POST /storyboard/projects/{parameter_1}/generate{parameter_2}

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/3612.4edec266.chunk.js` offset 6117. Path expression: `/storyboard/projects/{s.project_id}/generate{e?"?scene_id=".concat(e):""}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0584 · POST /storyboard/projects/{parameter_1}/recommendations

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3612.4edec266.chunk.js` offset 8161. Path expression: `/storyboard/projects/{s.project_id}/recommendations`.

No second argument at this call site. This does not establish the complete server contract.

## api-0585 · POST /storyboard/projects/{parameter_1}/stitch

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3612.4edec266.chunk.js` offset 9102. Path expression: `/storyboard/projects/{s.project_id}/stitch`.

Request/configuration expression (source only):
```javascript
{end_card_cta:s.end_card_cta||""}
```

## api-0586 · POST /studio-wizard/plan

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/8947.ffec9124.chunk.js` offset 17214. Path expression: `/studio-wizard/plan`.

Request/configuration expression (source only):
```javascript
{category:m.category,kind:m.kind,style:m.style,purpose:m.purpose,ratio:m.ratio,duration:m.duration,about:m.about,script_scenes:O?N:void 0}
```

## api-0587 · POST /studio-wizard/script

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/8947.ffec9124.chunk.js` offset 27301. Path expression: `/studio-wizard/script`.

Request/configuration expression (source only):
```javascript
(0,s.A)((0,s.A)({},"url"===h?{website_url:w.website_url}:w),{},{duration:m.duration})
```

## api-0588 · POST /studio-wizard/stitch

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/8947.ffec9124.chunk.js` offset 38125. Path expression: `/studio-wizard/stitch`.

Request/configuration expression (source only):
```javascript
{job_ids:a,narration:s.voiceOn?s.narration.trim():"",voice:s.voice,music_track:s.music,captions:s.voiceOn&&!!s.captions,trims:Object.fromEntries(Object.entries(b).filter(e=>{let[t,s]=e;return a.includes(t)&&s.end>s.start}))}
```

## api-0589 · GET /studio-wizard/stitches

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/8947.ffec9124.chunk.js` offset 35765. Path expression: `/studio-wizard/stitches`.

No second argument at this call site. This does not establish the complete server contract.

## api-0590 · GET /studio/creatives

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 89151. Path expression: `/studio/creatives`.

No second argument at this call site. This does not establish the complete server contract.

## api-0591 · POST /studio/creatives/from-media

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 68271. Path expression: `/studio/creatives/from-media`.

Request/configuration expression (source only):
```javascript
{video_url:be(l.output_url),name:l.name,aspect_ratio:l.aspect_ratio,cta:(null===(e=l.cta)||void 0===e?void 0:e.text)||""}
```

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 97236. Path expression: `/studio/creatives/from-media`.

Request/configuration expression (source only):
```javascript
{video_url:s.url,name:a.name.replace(/\.[^.]+$/,""),aspect_ratio:"9:16"}
```

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 98119. Path expression: `/studio/creatives/from-media`.

Request/configuration expression (source only):
```javascript
{image_url:s.url,name:a.name.replace(/\.[^.]+$/,""),aspect_ratio:"1:1"}
```

## api-0592 · POST /studio/creatives/launch-as-ads

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 75338. Path expression: `/studio/creatives/launch-as-ads`.

Request/configuration expression (source only):
```javascript
{creative_ids:[e]}
```

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 94381. Path expression: `/studio/creatives/launch-as-ads`.

Request/configuration expression (source only):
```javascript
{creative_ids:Pe.map(e=>e.creative_id),source_page_id:Pe[0].source_page_id,platforms:["meta","linkedin","google"]}
```

## api-0593 · DELETE /studio/creatives/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 104069. Path expression: `/studio/creatives/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0594 · PUT /studio/creatives/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 118830. Path expression: `/studio/creatives/{t.creative_id}`.

Request/configuration expression (source only):
```javascript
v
```

## api-0595 · POST /studio/creatives/{parameter_1}/render-image

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 90141. Path expression: `/studio/creatives/{e}/render-image`.

No second argument at this call site. This does not establish the complete server contract.

## api-0596 · POST /studio/creatives/{parameter_1}/render-video

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 90878. Path expression: `/studio/creatives/{e}/render-video`.

Request/configuration expression (source only):
```javascript
{duration:t,quality:a}
```

## api-0597 · POST /studio/from-script

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/4278.c2617230.chunk.js` offset 37838. Path expression: `/studio/from-script`.

Request/configuration expression (source only):
```javascript
{script:e.content}
```

## api-0598 · POST /studio/prompt-assist

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 126191. Path expression: `/studio/prompt-assist`.

Request/configuration expression (source only):
```javascript
{description:t,media_type:a,tone:d}
```

Source: `bundles/2825.52a0948d.chunk.js` offset 176304. Path expression: `/studio/prompt-assist`.

Request/configuration expression (source only):
```javascript
{description:t,media_type:s,tone:c}
```

## api-0599 · POST /studio/render-pending

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 89508. Path expression: `/studio/render-pending`.

No second argument at this call site. This does not establish the complete server contract.

## api-0600 · GET /studio/video-status/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 91380. Path expression: `/studio/video-status/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0601 · POST /subscriptions/cancel

Effect classification: **billing / financial change**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 48324. Path expression: `/subscriptions/cancel`.

No second argument at this call site. This does not establish the complete server contract.

## api-0602 · POST /subscriptions/portal

Effect classification: **billing / financial change**. Evidence: source observed.

Source: `client-bundle.js` offset 657038. Path expression: `/subscriptions/portal`.

Request/configuration expression (source only):
```javascript
{origin_url:window.location.origin}
```

## api-0603 · POST /subscriptions/resume

Effect classification: **billing / financial change**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 39525. Path expression: `/subscriptions/resume`.

No second argument at this call site. This does not establish the complete server contract.

## api-0604 · GET /team

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/9849.95354a0c.chunk.js` offset 5741. Path expression: `/team`.

No second argument at this call site. This does not establish the complete server contract.

## api-0605 · GET /team/activity

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/9849.95354a0c.chunk.js` offset 5981. Path expression: `/team/activity`.

No second argument at this call site. This does not establish the complete server contract.

## api-0606 · POST /team/invite

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/9849.95354a0c.chunk.js` offset 8506. Path expression: `/team/invite`.

Request/configuration expression (source only):
```javascript
w
```

## api-0607 · GET /team/my-role

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/9849.95354a0c.chunk.js` offset 5857. Path expression: `/team/my-role`.

No second argument at this call site. This does not establish the complete server contract.

## api-0608 · DELETE /team/{parameter_1}

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/9849.95354a0c.chunk.js` offset 11189. Path expression: `/team/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0609 · PUT /team/{parameter_1}/role

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/9849.95354a0c.chunk.js` offset 10463. Path expression: `/team/{e}/role`.

Request/configuration expression (source only):
```javascript
{role:a}
```

## api-0610 · DELETE /tiktok/disconnect

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 66701. Path expression: `/tiktok/disconnect`.

No second argument at this call site. This does not establish the complete server contract.

## api-0611 · GET /tiktok/posting/creator-info

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 98072. Path expression: `/tiktok/posting/creator-info`.

No second argument at this call site. This does not establish the complete server contract.

## api-0612 · POST /tiktok/posting/disconnect

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 100012. Path expression: `/tiktok/posting/disconnect`.

No second argument at this call site. This does not establish the complete server contract.

## api-0613 · GET /tiktok/posting/posts

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 97845. Path expression: `/tiktok/posting/posts`.

No second argument at this call site. This does not establish the complete server contract.

## api-0614 · POST /tiktok/posting/publish

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 111630. Path expression: `/tiktok/posting/publish`.

Request/configuration expression (source only):
```javascript
{video_url:i,caption:E,privacy_level:R,allow_comment:te,allow_duet:ae,allow_stitch:le,brand_organic:oe&&ce,brand_content:oe&&xe}
```

## api-0615 · POST /tiktok/posting/publish-photo

Effect classification: **delivery / publishing / provider or workflow change**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 110888. Path expression: `/tiktok/posting/publish-photo`.

Request/configuration expression (source only):
```javascript
{image_urls:r,caption:E,privacy_level:R,allow_comment:te,auto_add_music:x,brand_organic:oe&&ce,brand_content:oe&&xe}
```

## api-0616 · GET /tiktok/posting/publish-status/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 98622. Path expression: `/tiktok/posting/publish-status/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0617 · POST /tiktok/posting/schedule

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 115530. Path expression: `/tiktok/posting/schedule`.

Request/configuration expression (source only):
```javascript
{post_type:"photo"===n?"photo":"video",video_url:i,image_urls:r,caption:E,privacy_level:R,allow_comment:te,allow_duet:ae,allow_stitch:le,brand_organic:oe&&ce,brand_content:oe&&xe,auto_add_music:x,scheduled_at:new Date(g).toISOString()}
```

## api-0618 · GET /tiktok/posting/scheduled

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2825.52a0948d.chunk.js` offset 96397. Path expression: `/tiktok/posting/scheduled`.

No second argument at this call site. This does not establish the complete server contract.

## api-0619 · DELETE /tiktok/posting/scheduled/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 117205. Path expression: `/tiktok/posting/scheduled/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0620 · PATCH /tiktok/posting/scheduled/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 144940. Path expression: `/tiktok/posting/scheduled/{a.id}`.

Request/configuration expression (source only):
```javascript
{scheduled_at:i}
```

## api-0621 · GET /tiktok/posting/status

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 97966. Path expression: `/tiktok/posting/status`.

No second argument at this call site. This does not establish the complete server contract.

## api-0622 · POST /tiktok/posting/suggest-caption

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 104220. Path expression: `/tiktok/posting/suggest-caption`.

Request/configuration expression (source only):
```javascript
{topic:E}
```

## api-0623 · POST /tiktok/posting/upload-draft

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2825.52a0948d.chunk.js` offset 112873. Path expression: `/tiktok/posting/upload-draft`.

Request/configuration expression (source only):
```javascript
{video_url:i}
```

## api-0624 · POST /tiktok/select

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 88838. Path expression: `/tiktok/select`.

Request/configuration expression (source only):
```javascript
{advertiser_id:e}
```

## api-0625 · GET /tiktok/start

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 58357. Path expression: `/tiktok/start`.

No second argument at this call site. This does not establish the complete server contract.

## api-0626 · GET /tiktok/status

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 51858. Path expression: `/tiktok/status`.

No second argument at this call site. This does not establish the complete server contract.

## api-0627 · POST /upsell/feature-visit

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/6184.08cd5e77.chunk.js` offset 67856. Path expression: `/upsell/feature-visit`.

Request/configuration expression (source only):
```javascript
{feature:x}
```

## api-0628 · GET /usage/quota

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 159270. Path expression: `/usage/quota`.

No second argument at this call site. This does not establish the complete server contract.

## api-0629 · POST /veluro-chat/attach

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/4278.c2617230.chunk.js` offset 29166. Path expression: `/veluro-chat/attach`.

Request/configuration expression (source only):
```javascript
t
```

Source: `bundles/7010.d6d62a55.chunk.js` offset 6402. Path expression: `/veluro-chat/attach`.

Request/configuration expression (source only):
```javascript
a
```

## api-0630 · POST /veluro-chat/capture-email

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2349.49ee269a.chunk.js` offset 22955. Path expression: `/veluro-chat/capture-email`.

Request/configuration expression (source only):
```javascript
{email:C.trim(),name:L.trim(),session_id:P.current}
```

Source: `bundles/2382.dff3e565.chunk.js` offset 9620. Path expression: `/veluro-chat/capture-email`.

Request/configuration expression (source only):
```javascript
{email:C.trim(),name:D.trim(),session_id:L.current}
```

Source: `bundles/5224.851525a4.chunk.js` offset 191894. Path expression: `/veluro-chat/capture-email`.

Request/configuration expression (source only):
```javascript
{email:S.trim(),name:z.trim(),session_id:O.current}
```

Source: `bundles/7010.d6d62a55.chunk.js` offset 17810. Path expression: `/veluro-chat/capture-email`.

Request/configuration expression (source only):
```javascript
{email:ee.trim(),name:ae.trim(),session_id:U}
```

## api-0631 · POST /veluro-chat/claim-session

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/7010.d6d62a55.chunk.js` offset 4328. Path expression: `/veluro-chat/claim-session`.

Request/configuration expression (source only):
```javascript
{session_id:t.session_id}
```

## api-0632 · DELETE /veluro-chat/memory

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 24178. Path expression: `/veluro-chat/memory`.

No second argument at this call site. This does not establish the complete server contract.

## api-0633 · GET /veluro-chat/memory

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 22493. Path expression: `/veluro-chat/memory`.

No second argument at this call site. This does not establish the complete server contract.

## api-0634 · PUT /veluro-chat/memory

Effect classification: **account / access / configuration change**. Evidence: source observed.

Source: `bundles/3058.d2beb0a0.chunk.js` offset 25045. Path expression: `/veluro-chat/memory`.

Request/configuration expression (source only):
```javascript
{memory:e}
```

## api-0635 · GET /veluro-chat/my-sessions

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/4278.c2617230.chunk.js` offset 15783. Path expression: `/veluro-chat/my-sessions`.

No second argument at this call site. This does not establish the complete server contract.

## api-0636 · POST /veluro-chat/practice

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/3089.bd3bb770.chunk.js` offset 10783. Path expression: `/veluro-chat/practice`.

Request/configuration expression (source only):
```javascript
{persona:a,channel:i,messages:e,mode:t}
```

## api-0637 · GET /veluro-chat/proactive

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200, 500.

Source: `bundles/7010.d6d62a55.chunk.js` offset 3675. Path expression: `/veluro-chat/proactive`.

No second argument at this call site. This does not establish the complete server contract.

## api-0638 · DELETE /veluro-chat/session/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/4278.c2617230.chunk.js` offset 18313. Path expression: `/veluro-chat/session/{t}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0639 · GET /veluro-chat/session/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/4278.c2617230.chunk.js` offset 26525. Path expression: `/veluro-chat/session/{e.data.session_id}`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/4278.c2617230.chunk.js` offset 27004. Path expression: `/veluro-chat/session/{a}`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/4278.c2617230.chunk.js` offset 27475. Path expression: `/veluro-chat/session/{s.session_id}`.

No second argument at this call site. This does not establish the complete server contract.

Source: `bundles/4278.c2617230.chunk.js` offset 43177. Path expression: `/veluro-chat/session/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0640 · GET /veluro-chat/welcome

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/4278.c2617230.chunk.js` offset 26151. Path expression: `/veluro-chat/welcome`.

No second argument at this call site. This does not establish the complete server contract.

## api-0641 · GET /video-editor/music

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 66867. Path expression: `/video-editor/music`.

No second argument at this call site. This does not establish the complete server contract.

## api-0642 · GET /video-editor/projects

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 66736. Path expression: `/video-editor/projects`.

No second argument at this call site. This does not establish the complete server contract.

## api-0643 · POST /video-editor/projects

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 69469. Path expression: `/video-editor/projects`.

Request/configuration expression (source only):
```javascript
{name:"Video ".concat(r.length+1)}
```

## api-0644 · DELETE /video-editor/projects/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 72739. Path expression: `/video-editor/projects/{l.project_id}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0645 · GET /video-editor/projects/{parameter_1}

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 67672. Path expression: `/video-editor/projects/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0646 · PUT /video-editor/projects/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 67064. Path expression: `/video-editor/projects/{e.project_id||(null===l||void 0===l?void 0:l.project_id)}`.

Request/configuration expression (source only):
```javascript
e
```

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 70777. Path expression: `/video-editor/projects/{e.project_id}`.

Request/configuration expression (source only):
```javascript
{overlays:t.overlays,texts:t.texts,logo:t.logo}
```

## api-0647 · POST /video-editor/projects/{parameter_1}/render

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 73124. Path expression: `/video-editor/projects/{l.project_id}/render`.

No second argument at this call site. This does not establish the complete server contract.

## api-0648 · GET /video-editor/projects/{parameter_1}/status

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 67540. Path expression: `/video-editor/projects/{e}/status`.

No second argument at this call site. This does not establish the complete server contract.

## api-0649 · POST /web-extract

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/1482.a74c6ab9.chunk.js` offset 1847. Path expression: `/web-extract`.

Request/configuration expression (source only):
```javascript
{url:g.trim()}
```

Source: `bundles/2719.9c4a4a0f.chunk.js` offset 3306. Path expression: `/web-extract`.

Request/configuration expression (source only):
```javascript
{url:v.trim()}
```

Source: `bundles/2825.52a0948d.chunk.js` offset 4135. Path expression: `/web-extract`.

Request/configuration expression (source only):
```javascript
{url:b.trim()}
```

## api-0650 · GET /widgets

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed. Exact-path network statuses: 200.

Source: `bundles/7481.60cebc74.chunk.js` offset 13865. Path expression: `/widgets`.

No second argument at this call site. This does not establish the complete server contract.

## api-0651 · POST /widgets

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/7481.60cebc74.chunk.js` offset 28342. Path expression: `/widgets`.

Request/configuration expression (source only):
```javascript
o
```

## api-0652 · DELETE /widgets/{parameter_1}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/7481.60cebc74.chunk.js` offset 19987. Path expression: `/widgets/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0653 · PUT /widgets/{parameter_1}

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/7481.60cebc74.chunk.js` offset 5251. Path expression: `/widgets/{t.widget_id}`.

Request/configuration expression (source only):
```javascript
{bot_name:i.bot_name,welcome_message:i.welcome_message,tone:i.tone,personality_notes:i.personality_notes||"",goal:i.goal}
```

## api-0654 · POST /widgets/{parameter_1}/duplicate

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/7481.60cebc74.chunk.js` offset 19725. Path expression: `/widgets/{e}/duplicate`.

No second argument at this call site. This does not establish the complete server contract.

## api-0655 · GET /widgets/{parameter_1}/embed

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/7481.60cebc74.chunk.js` offset 19324. Path expression: `/widgets/{e}/embed`.

No second argument at this call site. This does not establish the complete server contract.

## api-0656 · GET /widgets/{parameter_1}/knowledge

Effect classification: **read candidate; inspect endpoint side effects**. Evidence: source observed.

Source: `bundles/7481.60cebc74.chunk.js` offset 1800. Path expression: `/widgets/{t.widget_id}/knowledge`.

No second argument at this call site. This does not establish the complete server contract.

## api-0657 · POST /widgets/{parameter_1}/knowledge/document

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/7481.60cebc74.chunk.js` offset 7673. Path expression: `/widgets/{t.widget_id}/knowledge/document`.

Request/configuration expression (source only):
```javascript
i
```

## api-0658 · POST /widgets/{parameter_1}/knowledge/text

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/7481.60cebc74.chunk.js` offset 10010. Path expression: `/widgets/{t.widget_id}/knowledge/text`.

Request/configuration expression (source only):
```javascript
E
```

## api-0659 · POST /widgets/{parameter_1}/knowledge/website

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/7481.60cebc74.chunk.js` offset 1972. Path expression: `/widgets/{t.widget_id}/knowledge/website`.

Request/configuration expression (source only):
```javascript
{url:b.trim()}
```

Source: `bundles/7481.60cebc74.chunk.js` offset 28457. Path expression: `/widgets/{t}/knowledge/website`.

Request/configuration expression (source only):
```javascript
{url:o.website_url.trim()}
```

## api-0660 · DELETE /widgets/{parameter_1}/knowledge/{parameter_2}

Effect classification: **delete / remove**. Evidence: source observed.

Source: `bundles/7481.60cebc74.chunk.js` offset 11541. Path expression: `/widgets/{t.widget_id}/knowledge/{e}`.

No second argument at this call site. This does not establish the complete server contract.

## api-0661 · POST /widgets/{parameter_1}/simulate

Effect classification: **generation / analysis; may consume credits or store output**. Evidence: source observed.

Source: `bundles/7481.60cebc74.chunk.js` offset 2433. Path expression: `/widgets/{t.widget_id}/simulate`.

Request/configuration expression (source only):
```javascript
{message:e,session_id:U.current}
```

## api-0662 · POST /widgets/{parameter_1}/toggle

Effect classification: **create / edit / configuration; inspect before execution**. Evidence: source observed.

Source: `bundles/7481.60cebc74.chunk.js` offset 18841. Path expression: `/widgets/{e}/toggle`.

No second argument at this call site. This does not establish the complete server contract.
