# Proposals and signatures

**Route:** `/proposals` · [Open Veluro](https://veluro.ai/proposals)

**When:** Use to prepare and deliver approved commercial proposals.

**Prerequisites:** Accurate client identity/email, authorized prices/terms and signing process.

## Agent procedure

1. Open New Proposal or an approved template.
2. Fill client, company, validity date, title, introduction, sections and line items.
3. Review totals, notes, scope and AI-drafted language against approved terms.
4. Save and inspect PDF output.
5. Send for Signature only after final scope authorization; verify the intended recipient and signature state.

## Success and recovery

Completion proof: The saved/exported proposal is correct; signing events are supported by the audit record.

AI Draft, Save, PDF and Send for Signature are distinct. Do not invent signature, agreement or pricing.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

2 captured screen states; 17 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| New Proposal | data-testid=proposal-new-btn | BUTTON |  | False |
| Close editor | Use observed accessible label/placeholder | BUTTON |  | False |
| AI Draft | data-testid=proposal-ai-draft-btn | BUTTON |  | False |
| Save as Template | data-testid=proposal-save-template-btn | BUTTON |  | False |
| Save | data-testid=proposal-save-btn | BUTTON |  | False |
| PDF | data-testid=proposal-pdf-btn | BUTTON |  | False |
| Send for Signature | data-testid=proposal-send-btn | BUTTON |  | False |
| Input / icon | data-testid=proposal-client-name | INPUT |  | False |
| Input / icon | data-testid=proposal-client-email | INPUT | client@company.com | False |
| Input / icon | data-testid=proposal-title | INPUT | Website Redesign for Acme Co. | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | Section heading | False |
| Input / icon | Use observed accessible label/placeholder | TEXTAREA | Section content… | False |
| Add section | Use observed accessible label/placeholder | BUTTON |  | False |
| Input / icon | data-testid=proposal-item-desc-0 | INPUT | Line item description | False |
| Input / icon | data-testid=proposal-item-qty-0 | number | ; min: 1 | False |
| Input / icon | data-testid=proposal-item-price-0 | number | Price; min: 0 | False |
| Add line | Use observed accessible label/placeholder | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/proposal-templates` | read candidate; inspect endpoint side effects | api-0481 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/proposal-templates/{parameter_1}` | delete / remove | api-0482 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/proposals` | read candidate; inspect endpoint side effects | api-0483 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/proposals` | create / edit / configuration; inspect before execution | api-0484 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/proposals/ai-draft` | generation / analysis; may consume credits or store output | api-0485 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/proposals/{parameter_1}` | delete / remove | api-0486 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/proposals/{parameter_1}/save-template` | create / edit / configuration; inspect before execution | api-0487 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/proposals/{parameter_1}/send` | delivery / publishing / provider or workflow change | api-0488 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-05.json` — /proposals · 2026-09-08T17:03:55.983Z
- `dialogs-01.json` — New Proposal · 2026-09-08T17:12:42.177Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
