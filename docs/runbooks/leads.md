# Leads CRM and imports

**Route:** `/leads` · [Open Veluro](https://veluro.ai/leads)

**When:** Use to maintain the authorized client pipeline and route follow-up.

**Prerequisites:** Approved source data, contact permissions, deduplication rules and CRM field mapping.

## Agent procedure

1. Inspect table/pipeline, status/campaign/score filters and grouping.
2. Add a lead with email or phone, or import the authorized CSV through the file chooser.
3. Validate field mapping, imported/skipped counts and duplicate handling.
4. Review lead score and status using actual contact history.
5. Enroll only eligible contacts into the approved sequence; verify delivery logs and synchronization.

## Success and recovery

Completion proof: The intended records and counts match source data without unintended enrollment or duplicates.

Import and sync mutate the CRM. Custom-status read returned 404 in this account; validate before relying on custom stages.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

2 captured screen states; 23 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Sync Facebook Leads | data-testid=sync-facebook-leads-btn | BUTTON |  | False |
| Delivery Log | data-testid=lead-delivery-log-btn | BUTTON |  | False |
| Statuses | data-testid=manage-statuses-btn | BUTTON |  | False |
| AI Score All | data-testid=ai-score-all-btn | BUTTON |  | True |
| Input / icon | data-testid=import-csv-input | file |  | False |
| Import CSV | data-testid=import-csv-btn | BUTTON |  | False |
| Add Lead | data-testid=add-lead-btn | button |  | False |
| Input / icon | data-testid=leads-search | INPUT | Search leads... | False |
| All statuses | data-testid=filter-status | button |  | False |
| All campaigns | data-testid=filter-campaign | button |  | False |
| All scores | data-testid=filter-score | button |  | False |
| 🔥 Hottest first | data-testid=leads-sort | button |  | False |
| Table | data-testid=view-table | BUTTON |  | False |
| Pipeline | data-testid=view-pipeline | BUTTON |  | False |
| Input / icon | data-testid=group-by-campaign | button |  | False |
| Input / icon | data-testid=lead-name | INPUT | John Doe | False |
| Input / icon | data-testid=lead-email | INPUT | john@company.com | False |
| Input / icon | data-testid=lead-phone | INPUT | +1 555 000 1234 | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | Acme Inc | False |
| Select source | Use observed accessible label/placeholder | button |  | False |
| Input / icon | data-testid=lead-campaign-tag | INPUT | e.g. Q3 Webinar Push | False |
| Add Lead | data-testid=lead-submit-btn | BUTTON |  | True |
| Close | Use observed accessible label/placeholder | button |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/leads` | read candidate; inspect endpoint side effects | api-0330 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads` | create / edit / configuration; inspect before execution | api-0331 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/auto-score` | create / edit / configuration; inspect before execution | api-0332 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/bulk-delete` | create / edit / configuration; inspect before execution | api-0333 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/bulk/nurture` | create / edit / configuration; inspect before execution | api-0334 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/import-csv` | create / edit / configuration; inspect before execution | api-0335 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/leads/statuses` | read candidate; inspect endpoint side effects | api-0336 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/statuses` | create / edit / configuration; inspect before execution | api-0337 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/leads/statuses/{parameter_1}` | delete / remove | api-0338 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/leads/statuses/{parameter_1}` | create / edit / configuration; inspect before execution | api-0339 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/leads/{parameter_1}` | read candidate; inspect endpoint side effects | api-0340 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/leads/{parameter_1}` | create / edit / configuration; inspect before execution | api-0341 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/{parameter_1}/coach` | create / edit / configuration; inspect before execution | api-0342 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/{parameter_1}/draft-reply` | generation / analysis; may consume credits or store output | api-0343 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/{parameter_1}/score` | create / edit / configuration; inspect before execution | api-0344 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/{parameter_1}/send-reply` | delivery / publishing / provider or workflow change | api-0345 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/leads/{parameter_1}/send-sms` | delivery / publishing / provider or workflow change | api-0346 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-03.json` — /leads · 2026-09-08T17:01:57.063Z
- `dialogs-01.json` — Add Lead · 2026-09-08T17:12:59.309Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
