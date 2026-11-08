---
name: asm-management
description: Use for Apple School Manager device assignment, Managed Apple Accounts, organization-to-MDM synchronization, Apple Configurator onboarding, ADE, and ASM/Jamf inventory discrepancies.
---

# Apple School Manager intelligence

Treat ASM as the organization assignment/enrollment identity plane; distinguish it from Jamf School device check-in and profile compliance. When reconciling, request sanitized counts by device source, management server, enrollment status, ownership, supervision, assigned user and timestamp, not full names or serials.

## Workflow
1. Establish whether the device is school-owned or personally owned; document proof of authority/consent and lifecycle policy. Do not assume a parent enrollment fee transfers ownership.
2. Confirm ASM membership, device source (reseller vs Apple Configurator manually added), assigned device management service, and any unassigned/misassigned units.
3. Independently verify Jamf School Automated Device Enrollment token/sync status, inventory presence, setup completion, supervision, and last check-in. ASM count and Jamf managed count are not directly interchangeable.
4. Inspect Managed Apple Account sync separately from Jamf users: role mapping, conflicts, deactivated users, account federation, account modifications and authentication lifecycle. Avoid exposing student PII.
5. Recommend low-risk corrective actions: recheck assignment, sync status, network, token lifetime, enrollment profile and Setup Assistant state before considering re-enrollment. Discuss erasure or release only as separately approved, high-impact changes.
6. For manually added devices, cite Apple's current **30-day provisional-release** rules and how the period is triggered; do not guarantee a non-removable profile or apply institution-owned controls to BYOD without authority.

## Deliverable
An ASM→Jamf exception matrix with categories 'not assigned', 'assigned but not enrolled', 'enrolled not checking in', 'ownership ambiguous', and 'user mapping issue'; evidence IDs, confidence, owner, remediation, privacy review, and validation. Use `../../templates/inventory-reconciliation.csv`.

Cross-check official references in `../../references/vendor-sources.md`. Do not invent enrollment menus, product-specific features, or live counts.

## Service and current workflow checks
Load `../../references/study-findings.md` before service/replacement or current Apps and Books advice. Distinguish plain assignment, explicit migration, unassignment, organization release and live unmanagement. Match current vendor preparation guidance before any proposed AppleCare repair procedure; route allowance/coverage questions to `applecare-enterprise`. Reconcile replacement enrollment from evidence rather than assuming it follows a serial record automatically.

