# Keeping the Veluro agent current

This is the update procedure for a future recurring operator. No recurring automation was created during this documentation milestone.

## Before every material operation

Check account identity, plan entitlements, the relevant integration, feature flags and the live page. Compare visible buttons, labels and required fields with the saved runbook. Fetch current model slugs/prices for creative generation and current allowance balances for batch work. If the route or payload changed, refresh the evidence before writing.

## Daily review procedure

1. Open Home, Help, Settings → Integrations, Billing and the modules used by active clients.
2. Inspect meaningful new notices, provider gates, errors, quotas and feature additions. Do not mark notifications read just to inspect them unless the operating scope includes that change.
3. Compare the current client build identifier and discovered module routes with the prior dated snapshot. A changed build is a signal to inspect, not proof that every workflow changed.
4. Review active/pending jobs using stored IDs. Check known failure conditions, including the health-data provenance issue, before using recommendations.
5. Refresh any changed instructions and label their evidence level. Keep the old version for rollback.
6. Notify the responsible operator only for material changes, failures, completed checks or a decision that is actually needed. Do not issue repetitive unchanged status reports.

## Weekly deeper review

Re-read the relevant built-in help and vendor release information visible in the product. Compare plan grids and quota endpoints, shipping UI labels and prior demo promises. Audit new feature claims against actual controls and backend responses. Check whether a previously Coming Soon or approval-gated feature has become usable.

Use this order of evidence: independently verified operation and resulting state; current authenticated API/UI; current vendor documentation; dated demo; inferred behavior. A more recent source can still be wrong. Preserve conflicts rather than overwrite them silently.

The current terms and the absence of a public API support contract must be considered when deciding how to maintain production API integrations. Obtain the vendor-approved interface and change process for the service. Keep the internal source inventory as dated research evidence, not as assumed permission or a compatibility promise.

## Refresh records

For each changed feature, record:

```yaml
change_id: unique_reference
discovered_at: timestamp
feature: module_name
old_behavior: prior_verified_description
new_behavior: current_observation
source_url: exact_route_or_vendor_reference
evidence_files: local_references
evidence_level: tested_or_ui_or_source_or_vendor
affected_clients: client_ids
affected_runbooks: filenames
affected_api_operations: method_and_path
action_risk: read_draft_publish_send_spend_or_account_change
validation: completed_test_and_result
remaining_gap: precise_unverified_behavior
rollback: previous_working_procedure
```

## Change validation rules

For a label-only change, update locators and verify navigation. For request/response changes, first validate a safe read, then a reversible draft and read-back. For changes to launch, sending, billing, permissions, publishing or integrations, prepare the exact test and ensure the existing engagement authorizes its final action. Never mass-run every endpoint as a discovery test.

Do not replay a stale POST after a timeout. Resolve the current object/job state before retrying. Record the running job ID durably. Generation can continue after a browser closes; restarting blindly risks duplicate work and charges.

Maintain a small capability registry for each client with `available`, `connected`, `permission_scope`, `tested_at`, `evidence`, `limits` and `known_failure`. An account may have a feature label without permission to execute it.

## Agent learning and regressions

Keep approved business facts separate from platform procedures. Refresh platform procedures globally; preserve each client's business knowledge and permissions separately. Do not train client facts into another client's account.

After a meaningful platform change, evaluate the agent on: choosing the correct portal; selecting the correct client/account; recognizing a quota or integration gate; creating a local draft; interpreting a source-observed API operation; recognizing that LinkedIn Compose does not send; rejecting unexplained health metrics as business evidence; and recovering from an interrupted job without duplication. Preserve actual outputs and failures, not just a self-reported pass.

Archive each release with its dated manifest. Update the searchable HTML and Markdown together. Keep credentials out of every release and keep account-specific evidence private.
