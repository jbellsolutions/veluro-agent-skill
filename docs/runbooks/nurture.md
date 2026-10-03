# Nurture Campaigns

**Route:** `/nurture` · [Open Veluro](https://veluro.ai/nurture)

**When:** Use for approved follow-up to eligible leads.

**Prerequisites:** Reviewed sequence, eligible enrolled leads, sender route, Twilio for SMS and stop/suppression rules.

## Agent procedure

1. Inspect campaign statuses and enrolled leads.
2. Review each step’s channel, delay, subject and body.
3. Confirm email and SMS delivery connections separately.
4. Activate/send only under the approved outreach scope.
5. Inspect delivery, replies and failures; stop or suppress leads according to the client rules.

## Success and recovery

Completion proof: Actual delivery and enrollment states match the approved sequence.

The visible activation API is activate-send. Emails/SMS can remain queued without the corresponding connection.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

1 captured screen states; 2 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Connect Resend | data-testid=resend-connect-open-btn | BUTTON |  | False |
| Connect Twilio | data-testid=twilio-settings-link | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/nurture/sequences` | read candidate; inspect endpoint side effects | api-0406 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/nurture/sequences/{parameter_1}/activate-send` | delivery / publishing / provider or workflow change | api-0407 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/nurture/sequences/{parameter_1}/leads` | read candidate; inspect endpoint side effects | api-0408 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-04.json` — /nurture · 2026-09-08T17:02:32.785Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
