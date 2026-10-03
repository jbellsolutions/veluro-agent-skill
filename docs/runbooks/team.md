# Client workspace team and roles

**Route:** `/team` · [Open Veluro](https://veluro.ai/team)

**When:** Use to provision or audit operator access in the client application.

**Prerequisites:** Owner/admin scope and approved person/role.

## Agent procedure

1. Read the actual role matrix and current member list.
2. Choose Owner/Admin/Member according to the required tasks.
3. Prepare the specific invite or role change; verify the exact email/person.
4. Send or save only when member-management authorization covers it.
5. Verify membership status and that only intended permissions changed.

## Success and recovery

Completion proof: The right operator has the required access in the correct client workspace.

Member cannot run AI agents in the displayed matrix. Only Owner can manage billing/settings. Invites send external messages.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

2 captured screen states; 6 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Invite Member | data-testid=invite-member-btn | button |  | False |
| Input / icon | data-testid=invite-name | INPUT | Jane Smith | False |
| Input / icon | data-testid=invite-email | INPUT | jane@company.com | False |
| Member - View and manage campaigns | data-testid=invite-role | button |  | False |
| Send Invitation | data-testid=invite-submit-btn | BUTTON |  | True |
| Close | Use observed accessible label/placeholder | button |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/team` | read candidate; inspect endpoint side effects | api-0604 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/team/activity` | read candidate; inspect endpoint side effects | api-0605 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/team/invite` | account / access / configuration change | api-0606 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/team/my-role` | read candidate; inspect endpoint side effects | api-0607 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/team/{parameter_1}` | account / access / configuration change | api-0608 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/team/{parameter_1}/role` | account / access / configuration change | api-0609 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-06.json` — /team · 2026-09-08T17:05:22.832Z
- `dialogs-01.json` — Invite Member · 2026-09-08T17:13:12.268Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
