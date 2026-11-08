---
name: school-policy-architect
description: Use for differentiated student, teacher, staff, admin, IT, school-owned, and BYOD policy matrices, Jamf School Blueprint planning, rollout and migration.
---

# Role-based policy architecture

Propose age-appropriate profiles by instructional need, access scope and device ownership; not a one-size-fits-all lockdown. Cohorts: early grades, primary, middle, grades 9–12, teachers, administration, IT; further split by school-owned/BYOD and supervised/unsupervised where material. Do not infer student age from device model or class name without evidence.

## Design method
1. Inventory actual Blueprints, device groups, restrictions, apps, profile owners and known exceptions. Retain original snapshot/version and export before redesign.
2. Create a minimal **connectivity and enrollment baseline** separate from discretionary learning restrictions. Place managed Wi-Fi/certificates in first pilot, ensure emergency admin recovery.
3. Define roles with default educational capabilities, accessibility exceptions, account changes, app distribution, web/content protections, passcode expectations, location/privacy permissions, and support needs. Label each proposed control with Apple/Jamf School applicability and OS requirements rather than assuming it exists.
4. Prefer composable profiles and clearly scoped groups, with explicit owner and named exception rules; avoid overlapping/conflicting settings in independent Blueprints.
5. Publish an impact matrix: student access, accessibility, teacher workflow, device connectivity, support burden, BYOD privacy, out-of-school use. Obtain pedagogical/stakeholder signoff on restrictions affecting learning.
6. Stage rollout: baseline audit → prototype groups → pilot/simulate common tasks and restart → evaluate → cohort deployment → steady-state drift review. Never remove old policy first; define undo/restore path.

## Deliverables
Fill `../../templates/policy-matrix.csv` and `../../templates/migration-checklist.md`; include scope, proposed device settings, minimum support, exceptions, reason, risk, validation, rollback, documentation evidence. Avoid copying unsanitized student or staff rosters into reports.

For app catalogs, account switching and after-hours freedom, use `../../references/app-self-service.md`. Separate account modification, app acquisition, app installation and app usage. Check ownership and supervision for each proposed control. Do not freeze an existing personal account into place or promise instant start/end enforcement on locked or unreachable devices. Keep connectivity/recovery settings outside discretionary timed restrictions.
