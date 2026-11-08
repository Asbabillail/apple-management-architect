---
name: jamf-school-management
description: Use for Jamf School profiles, Blueprints, Device Groups, restrictions, apps, inventory, commands, enrollment, and Jamf School UI troubleshooting.
---

# Jamf School operations

Use **Jamf School** product documentation, not Jamf Pro, Jamf Now, or generic Jamf documentation for UI steps and feature availability. Verify current school product labels before giving click-by-click guidance; variant/version-dependent controls should be marked as such.

## Read-only investigation
1. Confirm device group, Blueprint, scoped profiles, time filters, enrollment channel, installed/pending/failed state, check-in date, current iPadOS, supervision and user assignment.
2. For a profile question, map payload category, scope, installation type, device OS support, conflicting payload keys, precedence, and the observed on-device result. Distinguish two simultaneously installed payloads from proof of a conflict.
3. For apps, audit Apple Apps and Books licensing (location and available licenses), app assignment method, VPP/content token state, app compatibility and network reachability. Never infer license availability from historical recurring-license totals.
4. For quick actions (Clear Passcode, Lost Mode, Restart, etc.), validate prerequisites in the **Jamf School Quick Action Commands Reference**, whether device is online, supervision or iPadOS constraints, and whether command is queued vs delivered. A queued command is not executed.
5. For new profiles: draft, test with one identified pilot group, observe checks and reboots, then stage progressively. Export/document existing profiles first. For dangerous actions get explicit approval in the authorized management UI.

## Output
Blueprint/profile inventory table with name, scope, owner, payload, enrollment applicability, version/prereq, overlap, operational risk, recommendation and rollback. Present menu steps only if the official Jamf School source supports them. Cite the actual Jamf School page and date.

Vendor reference registry: `../../references/vendor-sources.md`. Risk rubric: `../../references/operational-guardrails.md`.

## Expanded readiness and current-source checks
Use `../command-readiness/SKILL.md` for the command family matrix and per-item enrollment checks before advising an action. Load `../../references/study-findings.md` for app licensing, token, profile and network caveats. Keep the installation method, license-assignment method and scope separate. Do not confuse a protocol capability with a School UI feature or classify a dispatched inventory query as passive reading.

For approved optional apps, repeated IT installation requests, Jamf School Student or learning-hour app access, use `../app-self-service/SKILL.md` and `../../references/app-self-service.md`. Compare the current configuration with the desired workflow before proposing changes. Do not change every group's installation method or remove current app scopes to create a catalog.

