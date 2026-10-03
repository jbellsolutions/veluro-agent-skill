# Veluro operating manual

Evidence date: September 8, 2026. This manual describes the authenticated Partner Growth account and the browser build `main.613ac379.js`. Use the [verification register](VERIFICATION.md) to distinguish tested behavior from a visible control or vendor description. Detailed screen inventories and instructions are in [Feature runbooks](runbooks/INDEX.md).

## 1. What the platform contains

Veluro combines business knowledge and an AI chat operator with customer acquisition, creative production, conversion and reporting tools. The authenticated application is at `https://veluro.ai`. The supplied login first enters the partner dashboard at `/partner`; its purple **Back to App** button enters the client application at `/home`. There was no second login in this account.

The partner portal manages referral tracking, recruited resellers, partner staff, promotional assets, commissions and payouts. The client application manages the business's operating work. Returning to the client app does not establish a separate workspace for every downstream customer. No tested multi-client switcher or isolation workflow was found in this account. Do not mix multiple clients' business knowledge, leads, mailboxes or budgets in one workspace without verifying the intended tenancy model.

The client sidebar is grouped into **Get Customers**, **Nurture & Close**, **Social Media & Creative Engine**, **Dashboard & Analytics**, and **Workspace**, with a separate Partner group. Groups can collapse. The search button says **Jump to…** and supports a displayed keyboard shortcut. The Home screen offers conversational tasks and feature shortcuts; direct routes and stable observed test IDs are included in each runbook.

## 2. Account, brand and business knowledge

Complete these foundations before generating a campaign:

1. **Settings → Profile:** verify name, business name, public contact email and optional phone. Login email is displayed as not editable there. Check the distinction between login email and the contact email printed on marketing materials. Save Profile and Save Changes are separate controls.
2. **Settings → Brand Kit:** select a logo, primary/secondary/accent colors and font. Add creative style instructions describing approved imagery, tone and exclusions. Save Brand Kit. The app lists Outfit, Inter, DM Sans, Manrope, Poppins, Playfair Display, Instrument Serif and Roboto.
3. **Workspace → Veluro Intelligence**, route `/teach-veluro`: teach the business using websites, uploaded documents and explicit notes. The UI accepts PDF, DOCX, PPTX, TXT, MD and CSV up to 30 MB. Note categories include company note, competitor, customer persona, FAQ, pricing and goal. Inspect the resulting knowledge list; uploading a document alone is not proof that all facts were understood.
4. Review the AI agent's memory in Settings. Treat automatically learned facts as editable, fallible memory. Keep credentials out of training data. Distinguish offer facts from exploratory ideas and unapproved prices.
5. Configure only the provider accounts assigned to the client. Verify the account/page IDs after authorization.

The current account reports `has_onboarded: true`, but High-Intent Buyers warns that the business description, industry and ideal customer are missing. “Onboarded” therefore does not prove a complete business profile.

## 3. Integrations and prerequisites

| Integration | What the screen supports | Current evidence / operator requirement |
|---|---|---|
| Meta Ads & Facebook Pages | Multiple ad accounts and pages; ads, custom audiences, social pages | Disconnected. Banner says the app is in Meta's final review and general one-click launch/auto-posting unlocks after approval. Verify current access before promising delivery. |
| Google Ads | Account authorization with `adwords` scope; Search / Performance Max described | Disconnected. UI says campaigns launch paused; verification is still in progress. Review the real authorization screen and provider state. |
| Google Analytics + Calendar | GA4 reporting and booking calendar sync | Disconnected. Verify correct property, calendar and timezone. |
| Google Analytics credential form | Measurement ID and API Secret | Separate from the combined OAuth connection. Do not assume one configures the other. |
| LinkedIn identity | OpenID Connect | This connection alone does not prove ad or messaging capability. |
| LinkedIn Ads | Marketing API, Sponsored Content, analytics, Matched Audiences, company posting | UI labels it approved Development Tier; disconnected here. Validate the intended ad account and page. |
| TikTok Ads | Campaigns, video creatives and reporting | Disconnected. UI describes paused creation. Posting is also a separate surface. |
| Email Outreach & Warmup | Gmail, Outlook and SMTP mailboxes | Live UI and client code expose these; actual delivery was not exercised. |
| Resend | Outreach and nurture delivery | Not connected. Outreach campaign tabs are gated until a usable sending route is connected. |
| SendGrid | Emails such as reports, notifications and outreach | Separate integration, with API key and sender email fields. Do not infer that it replaces Resend for nurture. |
| Twilio | SMS | Account SID, auth token and phone fields. Nurture says SMS stays queued until connected. |
| CRM connector | HubSpot, Pipedrive, GoHighLevel, Zoho or webhook | Two-way sync described. Validate direction, mapping, deduplication and delivery logs before client use. |
| GoHighLevel | Private Integration Token and Location ID | Help specifies contacts, opportunities, pipelines and calendars scopes. Use the specific sub-account's authorized token. |
| Bank / Financial | Provider and API key fields | Disconnected; data provenance and actual provider behavior remain unverified. |

The review did not connect third-party services, send support requests, change billing, or launch live work. Connection buttons may leave Veluro or open a new tab. They are authorization flows, not ordinary navigation.

## 4. Usage and the meaning of unlimited

The account's plan is `partner_growth`, displayed at $497/month in its partner plan grid. Its active billing subscription status is null and `has_billing` is false in the API; this establishes the entitlement label, not a verified charge.

| Meter | Verified allowance / state | How an operator uses it |
|---|---|---|
| General AI credits | 3,500 available; 0 used this cycle; rollover cap 10,500; renewal October 5 | Check `/credits` before costly batches. Purchased credits form a separate bank. |
| Creative Studio credits | 6,000 allowance; 0 used | Check `/omnirogue/usage` and model prices. These are separate from general AI credits. |
| Active campaigns | 5; 0 active | UI says drafts and paused campaigns do not consume a live slot. Draft test confirmed no active slot usage. |
| Intent leads | 75,000/month; 500 used; 74,500 remaining; reset October 1 | Check `/intent/quota`. Deleting a tracker does not immediately restore its allocation. |
| Landing pages | 3; 0 used | Check `/landing/quota`. Funnel accounting should not be assumed identical. |
| Social pages | 3 | Verify the actual connected pages and plan enforcement. |
| Coach seats | 1 | Billing says first use claims a seat; freeing a seat permits another person. |
| Coach analysis | 10 calls / 300 minutes; 0 used; renewal October 5 | This cap is additional to the seat limit. |
| Outreach mailboxes | 50; 0 connected; max daily cap 50 per mailbox | A maximum field is not an assurance of deliverability or an instruction to send at maximum. |
| Legacy media quota response | 300 images, 40 standard videos, 10 premium videos | The account also exposes Studio credits. Both counters exist; their interaction was not validated. |

Partner plan grid observed: Free $0; Starter $297; Growth $497; Command $997; Scale $2,497; Enterprise $6,497 monthly. Even the partner Enterprise grid shows finite general AI and Studio credits. Never translate “unlimited campaigns/leads/pages” into unlimited images, videos, mailboxes, people, labor or ad spend.

Customer retail pricing is a separate schedule:

| Customer plan | Monthly price | Campaigns | Intent leads | Studio credits |
|---|---:|---:|---:|---:|
| Starter | $497 | 3 | 50,000 | 4,000 |
| Growth | $1,197 | 5 | 150,000 | 9,000 |
| Command | $2,497 | 15 | 500,000 | 20,000 |
| Scale | $4,997 | 25 | 750,000 | 40,000 |
| Enterprise | from $9,997 | Unlimited | Unlimited | 80,000 |

These are public retail figures, not this partner account's limits. The page advertises a seven-day trial. [Veluro pricing](https://veluro.ai/pricing).

For the future service, the operational unit should be an approved client request with defined inputs, output and completion criteria. Maintain a queue, prioritize work, and measure credits and operator time. The coaching/Skool benefit is part of the proposed service; no native Skool integration was established. Agency servicing rights, client isolation, data redistribution rights and any volume agreement remain to be confirmed before packaging multi-client unlimited access.

## 5. Customer acquisition workflow

### High-Intent Buyers

Navigate to `/intent`. Choose **Business buyers**, **Consumers**, or **Advanced search**. The first two use buying topics; Advanced search is filter-only and must not be described as intent-qualified.

For intent tracking, search with at least three characters and select up to five relevant topics. Topic search returns a `topic_id`, label and matching metadata. For example, the observed B2C roofing search returns broad roofing, specific service categories and named businesses; operators must choose semantic relevance rather than select the first result. Null `person_count` is unknown, not zero, and `match_score` describes topic matching, not purchase probability.

Apply geography using state, city and ZIP controls. A city search can return the same city name in several states: the Austin search returned multiple states, so explicitly select Austin, TX if that is intended. The visible signal recency field permits 1–14 days.

B2B filters include seniority, department, job title, LinkedIn connection counts, company size, revenue, industry, name and URL. B2C filters include age, gender, marital status, income, net worth, children and homeowner status. Apply only relevant and appropriate targeting criteria for the client's service and channel. The detailed runbook preserves the actual available options.

Name the tracker, set the lead allocation, review the summary and initiate it once. The UI currently defaults the allocation field to 25,000 and sets a minimum of 100; review this before using it. Creating a tracker can allocate quota. Poll the existing audience ID; the shipped UI polls about every six seconds until completion. Inspect records, counts and filters before export or activation. Audience quality, match rates and delivery were not independently tested in this account.

The call describes advanced search as unlimited and outside intent quota. The live screen's advanced-search notice should be checked at execution time; no bulk extraction was used to test quota accounting. Intent is a prioritization signal, not a complete census or a guaranteed buyer list.

### Demand Map

Choose the actual operating area and the products/services to analyze. Optionally choose a saved high-intent audience. Generate a map, inspect hotspots and selected location, then review any campaign it prepares. The observed request supplies `location`, `industries`, audience name and descriptive audience context; it does not establish deterministic person-level matching between every hotspot and the saved audience. Treat lead-volume and revenue estimates as model outputs until traced to a verifiable data source.

### Growth Engine

`/service-brain` assembles ads, landing content, outreach, booking and lead scoring around an industry/service/market/goal. The catalog currently has nine industry groups and 43 named services, plus custom inputs in the client code. The source-observed create request is `industry`, `service`, `market`, `goal`, `notes`. Capture the returned engine ID and poll it; inspect every component before launch. A launch payload includes `generate_images` and `publish_landing`, so launch can create media and publish a page rather than merely save text. Multi-service selection creates multiple engines and can multiply resource use.

### Manual ad campaign builder

Open **Campaigns → New Campaign → I know what I'm doing — open the manual builder**. The guided path checks platform connections first. The manual path has seven steps:

1. **Platform:** Meta, Google, LinkedIn or TikTok.
2. **Campaign:** objective, name and destination. Meta lead generation offers platform lead form or destination landing page. The common objectives displayed are leads, traffic, conversions and brand awareness.
3. **Audience / Google keywords:** choose AI recommendations, high-intent, a saved audience or broad targeting. Inspect geography. Google exposes exact, phrase and negative keywords; check terms and match types manually.
4. **Budget:** monthly budget, auto-optimization and maximum increase per adjustment. The draft's daily budget is derived from monthly budget divided by 30 and rounded. The default review showed auto-optimization enabled with a $100 maximum increase; turn it off or replace it with authorized settings before launch.
5. **Creative:** assets, primary text, headline, description, CTA and variations. Meta permits up to ten creatives in this UI, four additional primary texts, four additional headlines and two additional descriptions. Lead forms include intro, prefill/custom questions, privacy link and thank-you screen. A privacy URL is required for the Meta form.
6. **Simulate:** generates a prediction. It is not measured performance, proof of conversion or a guarantee.
7. **Review:** check full content, account/page identity, destination, budget, optimization, pixel and nurture sequence. A quality score may recommend changes; it does not replace launch validation.

**Save & finish later** preserves a local draft. **Save Draft** does not push an ad to Meta. **Save as Paused on Meta** creates provider objects in a paused state. **Make it Live** is a live advertising action. Source code also exposes platform-specific launch, pause, duplicate and optimizer operations; their contracts appear in the API catalog. For all providers, verify provider IDs and actual provider state rather than infer from the local campaign label.

A controlled UI/API test proved local draft create/read/update/delete, with auto-optimization false and no linked account, creatives, pixel or nurture. It used no credits or spend. The temporary draft was removed and the campaign total returned to zero.

## 6. Conversion and fulfillment workflow

Build the destination before directing traffic. **Funnels** provide multi-step flows, AI creation and templates; the editor source exposes page editing, step order, variants, automations, webhooks, payment connection and optimization. **Landing Pages** offer single-page generation, design inspiration, editing, assets, A/B variants, publishing and custom-domain controls. Generated copy and preview do not prove a served page, payment or conversion works.

**Pixels** support Meta, Google, LinkedIn, TikTok and custom script choices. Establish the provider pixel/tag ID, generate the install code, place it in the intended site or funnel, and verify events in the actual provider after an authorized test. A pixel listed in Veluro is not proof of correct installation.

**Chat Widgets** require bot identity, welcome message, goal, tone and business knowledge. Train using websites, files or notes. Test representative questions and lead capture before embedding. Inspect the generated snippet, placement, source domain and CRM destination. Do not let the bot invent policies, offers or availability.

**Leads CRM** supplies filtering, table/pipeline view, campaign grouping, scoring, import, manual creation, Meta lead sync and delivery log. Manual entry requires contactability by email or phone. A successful CSV upload is followed by header mapping, row/error checks and deduplication; validate against the original authorized list. Do not enroll people merely because they exist in the CRM.

**Nurture Campaigns** show sequences, statuses and enrolled leads. Email and SMS connection banners are separate. The activation action in this build is named `activate-send`; it is a delivery action. Review channels, timing, copy and stop conditions before activation. Funnel automation tests can send actual email/SMS; “test” is not synonymous with no external effect.

**Outreach (CSV)** handles lists, AI-created email sequences, replies and sender setup. It describes automatic routing through Resend when available, otherwise connected mailboxes. The current campaign tabs are disabled until delivery setup exists. The request supports list ID, purpose, value proposition, tone, sequence length, CTA and route choice. Verify the selected route against the intended sender, reputation and audience before sending.

**Email Triage** is a separate inbox/account workflow; **Replies Inbox** aggregates lead replies; **AI Reply Drafter** can prepare text from an email. Avoid reading unrelated inboxes. Copying or generating a draft is distinct from sending it. **LinkedIn Compose** explicitly generates copy for manual sending; the queue stores day-stamped reminders and status bookkeeping.

**Scheduling** manages dates, available slots, duration and linked contacts. Verify calendar selection, timezone, availability, conflict checks and event destinations. The public booking flow and calendar sync need production tests after connection. **Proposals** distinguish draft/save/PDF from sending for signature. **Sales Coach** separates prep, armed live capture and post-call review; the review meter exposes both calls and minutes.

## 7. Creative, organic growth and reporting

Creative Studio includes Guided, Pro mode, Photos → Video, Ad Lab and Storyboard Builder. Pro mode exposes video, image, avatar and voice/audio categories, though the returned model catalog currently contains image/video entries only. Use current model slugs and prices. Duplicate model names represent different variants. The captured catalog contains 66 entries; generation itself has not been certified.

Photos → Video says it joins 2–10 images with captions and transitions at no AI-credit cost. Ad Lab includes one-click ad assembly, template rendering, silence trimming and copy generation. Storyboard starts with script, duration and aspect ratio, then creates scenes/clips and stitches them. Store all job/project IDs and poll existing work before retrying. Review finished media for text, brand, facts, likeness rights and audio before client use.

Creative Library stores generated and uploaded assets, folders and video editing. Creative Insights needs a connected Meta account and should be assessed against actual ad data. Flyers expose text, business contact information, offer, CTA, QR destination, design choice, PDF download and image import. Validate QR and phone/website details in the exported artifact.

Social Media combines manual posts, AI strategy, batch queue and autopilot. Connect the correct profile, review generated content, set schedule and timezone, then authorize publication. Dragging calendar posts can reschedule saved work. Treat “approve and schedule” as a write that may lead to publishing. Provider approval gates remain relevant.

SEO Engine provides site audit, recommended changes, keywords and ranking tools; Blog Engine generates articles and publishes to the business blog. GEO exposes buyer prompts, scans, site audit, llms.txt and FAQ schema. These tools generate candidates for review; neither a GEO score nor a generated file guarantees rankings or AI recommendations. **Local Listings is Coming Soon** in both UI and help.

Dashboard separates Overview, Analytics, Command Center and Reports. Weekly Digest and reports can generate summaries, export PDFs and send email. Check date range, timezone, currency, source account and attribution definitions. Empty or disconnected source data must never be converted into a claimed result.

Business Health's populated account data is currently unexplained. Its API returned $220,602 monthly revenue, performance trends and budget recommendations while ad connections were false and total campaigns zero; the account's `demo_account` flag is false. This is a provenance conflict, not evidence of those business results. Do not execute health actions until the source is established. Some UI captures remained on “Calculating Business Health”; the separate API read succeeded.

## 8. Partner operation

The current links are:

- Public introduction: `https://veluro.ai/usingaitoscale`
- Direct signup: `https://veluro.ai/signup?ref=JUSTIN`
- Recruit resellers: `https://veluro.ai/resellpartners?ref=JUSTIN`

The portal describes 90-day visitor tracking and recurring customer attribution. Commission clearing is shown as 30 days; payout timing is the first of the month after clearing. These are portal terms observed, not a completed payout test.

The account's rates are 20% of direct referred customer payments; 10% of recruited reseller subscriptions; 5% override on reseller client revenue. The September 8 call states the same three-part structure. Account **My Team** means recruited resellers; **Team Members** means people working in the partner account. Partner staff permissions include earnings, marketing materials and campaigns, while bank/payout settings remain with the owner. The client app's **Team** page has a different Owner/Admin/Member permission matrix.

Starter Kit includes a personalized one-pager, share link, social copy, objection practice, objection cards and email templates. Marketing Library adds promotional assets and prebuilt campaigns with asset attribution. Treat templates and statistics as material to fact-check, not as automatically substantiated marketing claims. In particular, the proposed “every person in your area” claim goes beyond the evidence gathered here.

## 9. Operating cadence

For each new engagement, establish the client record and delivery chain before launch. Each operating day: check connections and allowances, failures and queued jobs, spending against approved limits, lead replies and suppression, and scheduled content. Check source-data freshness before following any recommendation.

Each week: reconcile CRM outcomes with ad and delivery data; report qualified leads, bookings and actual sales rather than only impressions; review creative fatigue and unsuccessful steps; refresh the knowledge base; track outstanding client requests and operator capacity. Prepare proposed changes with their expected effect and evidence, then execute changes already within the engagement's authorization.

Use the agent checklist and checkpoint format in [Agent instructions](AGENT_INSTRUCTIONS.md). Use [Maintenance](MAINTENANCE.md) for continuing platform expertise. This documentation does not itself deploy or schedule an autonomous operator.

## 10. Terms and documentation limits

Veluro's current terms disclaim guaranteed marketing and intent-data outcomes, assign responsibility for data and campaign decisions to the user, and prohibit misuse and reverse engineering. They do not establish a public developer API support contract or the multi-client/data-resale rights needed for the proposed service. Confirm approved automation access and service licensing before relying on the discovered internal interface as a production integration. [Veluro terms](https://veluro.ai/terms).

The API catalog is evidence of the app build and the controlled tests described here. It is not a vendor-issued OpenAPI specification, a promise of backward compatibility, or certification of every endpoint. The manual preserves these limits so an agent can operate accurately and improve the evidence over time.
