# Scheduling and calendar

**Route:** `/scheduling` · [Open Veluro](https://veluro.ai/scheduling)

**When:** Use to offer slots, book meetings and maintain authorized calendars.

**Prerequisites:** Correct calendar, timezone, availability, contact and invitation authorization.

## Agent procedure

1. Select the intended day and inspect available slots.
2. Set title, time, duration, contact and notes.
3. Check conflicts and the calendar integration before confirming.
4. Create the appointment only within invitation scope.
5. Verify the actual calendar event, booking state and public reschedule/cancel path when used.

## Success and recovery

Completion proof: The right people have the correct event in the intended timezone and calendar.

Scheduling may send invites or sync externally. No connected calendar workflow was tested.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

2 captured screen states; 39 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| New Appointment | data-testid=create-appointment-btn | button |  | False |
| 30 | Use observed accessible label/placeholder | button |  | False |
| 31 | Use observed accessible label/placeholder | button |  | False |
| 1 | Use observed accessible label/placeholder | button |  | False |
| 2 | Use observed accessible label/placeholder | button |  | False |
| 3 | Use observed accessible label/placeholder | button |  | False |
| 4 | Use observed accessible label/placeholder | button |  | False |
| 5 | Use observed accessible label/placeholder | button |  | False |
| 6 | Use observed accessible label/placeholder | button |  | False |
| 7 | Use observed accessible label/placeholder | button |  | False |
| 8 | Use observed accessible label/placeholder | button |  | False |
| 9 | Use observed accessible label/placeholder | button |  | False |
| 10 | Use observed accessible label/placeholder | button |  | False |
| 11 | Use observed accessible label/placeholder | button |  | False |
| 12 | Use observed accessible label/placeholder | button |  | False |
| 13 | Use observed accessible label/placeholder | button |  | False |
| 14 | Use observed accessible label/placeholder | button |  | False |
| 15 | Use observed accessible label/placeholder | button |  | False |
| 16 | Use observed accessible label/placeholder | button |  | False |
| 17 | Use observed accessible label/placeholder | button |  | False |
| 18 | Use observed accessible label/placeholder | button |  | False |
| 19 | Use observed accessible label/placeholder | button |  | False |
| 20 | Use observed accessible label/placeholder | button |  | False |
| 21 | Use observed accessible label/placeholder | button |  | False |
| 22 | Use observed accessible label/placeholder | button |  | False |
| 23 | Use observed accessible label/placeholder | button |  | False |
| 24 | Use observed accessible label/placeholder | button |  | False |
| 25 | Use observed accessible label/placeholder | button |  | False |
| 26 | Use observed accessible label/placeholder | button |  | False |
| 27 | Use observed accessible label/placeholder | button |  | False |
| 28 | Use observed accessible label/placeholder | button |  | False |
| 29 | Use observed accessible label/placeholder | button |  | False |
| Input / icon | data-testid=appt-title | INPUT | Discovery Call | False |
| Select time | data-testid=appt-time | button |  | False |
| 30 min | Use observed accessible label/placeholder | button |  | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | John Doe | False |
| Input / icon | Use observed accessible label/placeholder | INPUT | Discuss pricing proposal | False |
| Schedule Appointment | data-testid=appt-submit-btn | BUTTON |  | True |
| Close | Use observed accessible label/placeholder | button |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/appointments` | read candidate; inspect endpoint side effects | api-0075 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/appointments` | create / edit / configuration; inspect before execution | api-0076 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/appointments/available-slots?date={parameter_1}` | read candidate; inspect endpoint side effects | api-0077 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/appointments/sync-google` | delivery / publishing / provider or workflow change | api-0078 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/appointments/{parameter_1}` | delete / remove | api-0079 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/appointments/{parameter_1}/prep` | generation / analysis; may consume credits or store output | api-0080 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/booking-settings` | create / edit / configuration; inspect before execution | api-0126 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/booking-slug` | read candidate; inspect endpoint side effects | api-0127 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/calendar/conflicts` | create / edit / configuration; inspect before execution | api-0132 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/calendar/disconnect` | account / access / configuration change | api-0133 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/calendar/list` | read candidate; inspect endpoint side effects | api-0134 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/calendar/select` | create / edit / configuration; inspect before execution | api-0135 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/calendar/status` | read candidate; inspect endpoint side effects | api-0136 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-04.json` — /scheduling · 2026-09-08T17:03:07.562Z
- `dialogs-01.json` — New Appointment · 2026-09-08T17:13:01.343Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
