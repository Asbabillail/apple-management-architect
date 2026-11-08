---
name: app-self-service
description: Use for repeated approved-app installation requests, Jamf School Student on-demand catalogs, optional versus required apps, app-request workflows, account switching, and balancing learning-hour restrictions with after-hours access.
---

# Approved apps with less helpdesk work

Use Jamf School-specific sources and `../../references/app-self-service.md`. Keep this release advisory: inspect supplied evidence, explain the next step or prepare a scoped pilot; do not claim any app or restriction is deployed.

1. Identify the desired outcome in ordinary language. Reuse supplied context. Ask only for missing facts needed now: ownership/supervision, exact MDM product, an approved example app, current assignment/license/install method and availability of Jamf School Student.
   If the MDM is unknown, offer the general approved-catalog pattern and confirm the product before Jamf School-specific menus or client instructions; an explicitly conditional School example is acceptable. Do not infer the product merely because this skill is School-focused.
2. Separate app acquisition, licensing, installation mode, account modification and permitted usage. Never equate signing out of an Apple Account with MDM removal, or assume device-based distribution needs a personal Apple Account.
3. Propose automatic installation for essential apps and an on-demand catalog for approved optional apps. Keep requests for new apps separate. Avoid turning all existing assignments into on-demand or opening the entire App Store to reduce tickets.
4. Guide a beginner through one read-only inspection at a time, with the expected observation. Give an expert a compact preflight and proposed pilot. Verify current UI labels before exact click steps; do not invent a missing button.
5. Treat timed restrictions as conditional delivery, not an exact offline guarantee. Keep management connectivity available. Evaluate account/app restrictions only for the actual ownership, enrollment, OS and supervision, with legitimate exceptions and recovery.
6. Draft a one-device or small-group pilot only after authority, existing configuration, acceptance checks and recovery are identified. Reconcile other assignment paths and app-data impact before reversing a scope. Do not remove apps or licenses as a casual rollback.
7. Measure comparable app-request visits and support time before/after a real pilot. Record failures, accessibility impact and user independence; never invent time savings or call a draft a successful deployment.

For each proposed change state: intended result, verified prerequisites, action or next inspection, expected evidence, stop condition and recovery. Use `../../templates/task-record.md` when a durable record is useful. Route missing-app incidents to `../jamf-school-management/SKILL.md`; route passcode/offline incidents to `../wifi-device-recovery/SKILL.md`.
