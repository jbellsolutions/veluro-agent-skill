# Weekly Digest

**Route:** `/digest` · [Open Veluro](https://veluro.ai/digest)

**When:** Use for a reviewed weekly operating summary.

**Prerequisites:** Verified data and a defined reporting period; permission for email delivery if used.

## Agent procedure

1. Read an existing digest or generate the first.
2. Compare figures with source records and annotate missing data.
3. Review optimization recommendations against approved goals.
4. Preserve the reviewed digest and next actions.
5. Send via Email only if delivery is authorized; verify intended recipient and delivery result.

## Success and recovery

Completion proof: The summary is accurate and delivered only through the intended channel.

Generate and Send via Email are separate operations; no digest email was sent.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 3 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Send via Email | data-testid=send-digest-email-btn | BUTTON |  | True |
| Generate Digest | data-testid=generate-digest-btn | BUTTON |  | False |
| Generate First Digest | Use observed accessible label/placeholder | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/digest` | read candidate; inspect endpoint side effects | api-0164 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/digest/generate` | generation / analysis; may consume credits or store output | api-0165 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/digest/send-email` | delivery / publishing / provider or workflow change | api-0166 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-06.json` — /digest · 2026-09-08T17:05:20.973Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
