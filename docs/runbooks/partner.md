# Partner dashboard, resellers and payouts

**Route:** `/partner` · [Open Veluro](https://veluro.ai/partner)

**When:** Use for referral tracking, recruitment attribution and partner staff operations.

**Prerequisites:** Correct partner account, referral code and agreement.

## Agent procedure

1. Use Overview for referred customers and settled/pending commissions.
2. Use My Team for recruited resellers and Team Members for staff; do not conflate them.
3. Use the appropriate main, trial or reseller invite link and preserve tracking.
4. Use the calculator with 20% direct, 10% reseller subscription and 5% reseller-client revenue bases.
5. Inspect payout/clearing records; verify actual payout separately from projected commission.
6. Prepare staff/income/link changes deliberately and perform them only within scope.

## Success and recovery

Completion proof: Attribution, commission base, staff relationship and actual payout states are accurately recorded.

Payout/bank changes and invitations require the appropriate authority. No recruitment message or payout action was performed.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

Account-specific member identifiers are replaced with `{record_id}` in this published edition. Resolve the actual authorized member from the live page before acting.

9 captured screen states; 75 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Statement (CSV) | data-testid=download-statement-btn | BUTTON |  | False |
| Back to App | data-testid=back-to-app-btn | BUTTON |  | False |
| Copy | data-testid=copy-referral-link-btn | BUTTON |  | False |
| Copy | data-testid=copy-trial-link-btn | BUTTON |  | False |
| ✨ Customize your link name / (e.g. veluro.ai/mikesmarketing) | data-testid=customize-link-btn | BUTTON |  | False |
| Overview | data-testid=partner-tab-overview | BUTTON |  | False |
| My Team | data-testid=partner-tab-team | BUTTON |  | False |
| Team Members | data-testid=partner-tab-members | BUTTON |  | False |
| Starter Kit | data-testid=partner-tab-starterkit | BUTTON |  | False |
| Plans | data-testid=partner-tab-plans | BUTTON |  | False |
| Earnings Calculator | data-testid=partner-tab-calculator | BUTTON |  | False |
| Payouts | data-testid=partner-tab-payouts | BUTTON |  | False |
| Leaderboard | data-testid=partner-tab-leaderboard | BUTTON |  | False |
| Asset Performance | data-testid=partner-tab-performance | BUTTON |  | False |
| Set a monthly income goal /  / Pick a target in the Earnings Calculator and we'll track your real commissions against it right here, every month. | data-testid=set-goal-cta | BUTTON |  | False |
| Downgrade | data-testid=plan-change-free | BUTTON |  | False |
| Downgrade | data-testid=plan-change-starter | BUTTON |  | False |
| Upgrade — $997/mo | data-testid=plan-change-command | BUTTON |  | False |
| Upgrade — $2497/mo | data-testid=plan-change-scale | BUTTON |  | False |
| Upgrade — $6497/mo | data-testid=plan-change-enterprise | BUTTON |  | False |
| Copy | data-testid=copy-invite-link-btn | BUTTON |  | False |
| Invite team member | data-testid=invite-member-btn | BUTTON |  | False |
| Input / icon | data-testid=remove-member-tm_{record_id} | BUTTON |  | False |
| Input / icon | data-testid=perm-view_earnings-tm_{record_id} | button |  | False |
| Input / icon | data-testid=perm-marketing-tm_{record_id} | button |  | False |
| Input / icon | data-testid=perm-campaigns-tm_{record_id} | button |  | False |
| Input / icon | data-testid=resend-invite-tm_{record_id} | BUTTON |  | False |
| Input / icon | data-testid=remove-member-tm_{record_id} | BUTTON |  | False |
| Input / icon | data-testid=perm-view_earnings-tm_{record_id} | button |  | False |
| Input / icon | data-testid=perm-marketing-tm_{record_id} | button |  | False |
| Input / icon | data-testid=perm-campaigns-tm_{record_id} | button |  | False |
| Input / icon | data-testid=resend-invite-tm_{record_id} | BUTTON |  | False |
| Input / icon | data-testid=remove-member-tm_{record_id} | BUTTON |  | False |
| Input / icon | data-testid=perm-view_earnings-tm_{record_id} | button |  | False |
| Input / icon | data-testid=perm-marketing-tm_{record_id} | button |  | False |
| Input / icon | data-testid=perm-campaigns-tm_{record_id} | button |  | False |
| Copy share link | data-testid=copy-kit-share-link-btn | BUTTON |  | False |
| Download one-pager | data-testid=download-onepager-btn | BUTTON |  | False |
| Copy post | data-testid=copy-social-li-story | BUTTON |  | False |
| Copy post | data-testid=copy-social-li-stat | BUTTON |  | False |
| Copy post | data-testid=copy-social-fb-local | BUTTON |  | False |
| Copy post | data-testid=copy-social-fb-results | BUTTON |  | False |
| Alex — tech business owner / Susan — insurance agent / James — real estate agent / Margaret — enterprise CEO / Maria — small business owner | data-testid=practice-persona | SELECT | ; options: Alex — tech business owner, Susan — insurance agent, James — real estate agent, Margaret — enterprise CEO, Maria — small business owner | False |
| Start practice | data-testid=start-practice-btn | BUTTON |  | False |
| Zoom call | data-testid=practice-channel-zoom | BUTTON |  | False |
| Email | data-testid=practice-channel-email | BUTTON |  | False |
| Text / SMS | data-testid=practice-channel-text | BUTTON |  | False |
| Copy answer | data-testid=copy-ob-1 | BUTTON |  | False |
| Copy answer | data-testid=copy-ob-2 | BUTTON |  | False |
| Copy answer | data-testid=copy-ob-3 | BUTTON |  | False |
| Copy answer | data-testid=copy-ob-4 | BUTTON |  | False |
| Copy answer | data-testid=copy-ob-5 | BUTTON |  | False |
| Copy answer | data-testid=copy-ob-6 | BUTTON |  | False |
| Copy answer | data-testid=copy-ob-7 | BUTTON |  | False |
| Copy answer | data-testid=copy-ob-8 | BUTTON |  | False |
| Copy answer | data-testid=copy-ob-9 | BUTTON |  | False |
| Copy answer | data-testid=copy-ob-10 | BUTTON |  | False |
| Copy email | data-testid=copy-template-cold-intro | BUTTON |  | False |
| Copy email | data-testid=copy-template-follow-up | BUTTON |  | False |
| Copy email | data-testid=copy-template-pain-point | BUTTON |  | False |
| Copy email | data-testid=copy-template-closing | BUTTON |  | False |
| Switch | data-testid=plan-switch-starter | BUTTON |  | False |
| Upgrade | data-testid=plan-switch-command | BUTTON |  | False |
| Upgrade | data-testid=plan-switch-scale | BUTTON |  | False |
| Input / icon | data-testid=calc-slider-starter | range | ; min: 0; max: 200 | False |
| Input / icon | data-testid=calc-slider-growth | range | ; min: 0; max: 200 | False |
| Input / icon | data-testid=calc-slider-command | range | ; min: 0; max: 200 | False |
| Input / icon | data-testid=calc-slider-scale | range | ; min: 0; max: 200 | False |
| Input / icon | data-testid=calc-slider-enterprise | range | ; min: 0; max: 200 | False |
| Input / icon | data-testid=goal-slider | range | ; min: 250; max: 100000 | False |
| Save as my monthly goal | data-testid=save-goal-btn | BUTTON |  | False |
| Starter ($297/mo) / Growth ($497/mo) / Command ($997/mo) / Scale ($2,497/mo) / Enterprise ($6,497/mo) | data-testid=team-reseller-plan | SELECT | ; options: Starter ($297/mo), Growth ($497/mo), Command ($997/mo), Scale ($2,497/mo), Enterprise ($6,497/mo) | False |
| Input / icon | data-testid=team-resellers-slider | range | ; min: 0; max: 50 | False |
| Starter ($497/mo) / Growth ($1,197/mo) / Command ($2,497/mo) / Scale ($4,997/mo) / Enterprise ($9,997/mo) | data-testid=team-client-plan | SELECT | ; options: Starter ($497/mo), Growth ($1,197/mo), Command ($2,497/mo), Scale ($4,997/mo), Enterprise ($9,997/mo) | False |
| Input / icon | data-testid=team-clients-slider | range | ; min: 0; max: 25 | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/partner/team` | read candidate; inspect endpoint side effects | api-0465 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/partner/team/accept` | account / access / configuration change | api-0466 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/partner/team/invite` | account / access / configuration change | api-0467 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/partner/team/invite/{parameter_1}` | read candidate; inspect endpoint side effects | api-0468 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/partner/team/{parameter_1}` | account / access / configuration change | api-0469 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PATCH | `/partner/team/{parameter_1}` | account / access / configuration change | api-0470 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/partner/team/{parameter_1}/resend` | account / access / configuration change | api-0471 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/referrals/partner-info/{parameter_1}` | read candidate; inspect endpoint side effects | api-0492 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/referrals/partner-signup` | create / edit / configuration; inspect before execution | api-0493 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/referrals/partner-signup/status/{parameter_1}` | read candidate; inspect endpoint side effects | api-0494 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/referrals/partner/activate` | delivery / publishing / provider or workflow change | api-0495 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/referrals/partner/change-plan` | billing / financial change | api-0496 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/referrals/partner/connect-onboarding` | account / access / configuration change | api-0497 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/referrals/partner/dashboard` | read candidate; inspect endpoint side effects | api-0498 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/referrals/partner/income-goal` | create / edit / configuration; inspect before execution | api-0499 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/referrals/partner/kit-stats` | read candidate; inspect endpoint side effects | api-0500 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/referrals/partner/leaderboard` | read candidate; inspect endpoint side effects | api-0501 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/referrals/partner/network-tree` | read candidate; inspect endpoint side effects | api-0502 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/referrals/partner/payout-history` | billing / financial change | api-0503 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/referrals/partner/performance` | read candidate; inspect endpoint side effects | api-0504 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/referrals/partner/pixel-events` | read candidate; inspect endpoint side effects | api-0505 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/referrals/partner/starter-kit` | create / edit / configuration; inspect before execution | api-0506 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/referrals/partner/statement.csv` | read candidate; inspect endpoint side effects | api-0507 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/referrals/partner/vanity` | create / edit / configuration; inspect before execution | api-0508 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `partner-tabs.json` — overview · 2026-09-08T17:08:12.604Z
- `partner-tabs.json` — team · 2026-09-08T17:08:12.884Z
- `partner-tabs.json` — members · 2026-09-08T17:08:13.155Z
- `partner-tabs.json` — starterkit · 2026-09-08T17:08:13.446Z
- `partner-tabs.json` — plans · 2026-09-08T17:08:13.726Z
- `partner-tabs.json` — calculator · 2026-09-08T17:08:14.019Z
- `partner-tabs.json` — payouts · 2026-09-08T17:08:14.298Z
- `partner-tabs.json` — leaderboard · 2026-09-08T17:08:14.582Z
- `partner-tabs.json` — performance · 2026-09-08T17:08:14.862Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
