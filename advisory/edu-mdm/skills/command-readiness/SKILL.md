---
name: command-readiness
description: Use for Jamf School command compatibility, supervision and enrollment prerequisites, offline or pending commands, software update protocol differences, and action impact or recovery planning.
---

# Evaluate a command without dispatching it

Read [command compatibility](../../references/command-compatibility.md) before command advice. Establish the exact School action and platform; check its current Jamf row and relevant Apple protocol/item documentation. Keep product UI availability, protocol availability, permissions, ownership and actual device state separate.

Use the reference's preflight and recovery record. Distinguish console metadata changes from commands needing a device communication path. Do not call Refresh, sync, Check now, app install or any other action a read-only inspection just because its purpose is diagnostic. Do not execute during a study-only session.

Check exact per-item User Enrollment support; never infer it from the Settings parent or from supervision alone. For current OS update advice, resolve legacy-versus-DDM behavior before giving steps. Do not substitute an Apple MDM transport example for a Jamf School API endpoint.

When a prerequisite is missing, report the gap and the minimum read-only evidence needed. Never invent successful delivery, guarantee offline recovery, or delete history to troubleshoot. For high-impact work, provide a proposed validation and recovery plan for a separately authorized pilot. This skill adds guidance, not a device-control connection.
