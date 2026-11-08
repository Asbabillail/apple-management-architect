---
name: automation-readiness
description: Use when planning future read-only Jamf School APIs, automation feasibility, inventory sync, policy drift checks, compliance dashboards, or integration security without live credentials.
---

# Automation and API architecture — advisory only

No connected Jamf School API, ASM tenant, database, scheduler, or server exists in this version. Never imply real-time telemetry, successful synchronization or policy mutation. Research official Jamf School documentation *specifically*; don't borrow endpoint shapes from Jamf Pro, Jamf Now, or third-party blog posts.

## Assessment procedure
1. Define desired report/action, data owner, legal basis, fields, cadence, retention, privacy risk, ROI and read-only vs mutation categorization.
2. Verify endpoint/method/parameters in the authenticated tenant's current **Jamf School API documentation** and current official vendor developer materials before writing executable integration code. Avoid inventing endpoint paths; general Jamf School API base URL from official docs does not prove a particular operation is supported.
3. Design **least-privilege**, per-function API access: tokens/keys in secrets manager, encrypted in transit, no credentials in prompts, GitHub, archives, logs or screenshots; key rotation and revocation.
4. Plan read-only reconciliation pilot first: limited sample, rate limits, pagination, retry/timeout rules, data minimization, audit logs, idempotent ingestion, discrepancy confidence, controlled retention and rollback (disable integration / delete imported data per policy).
5. Identify unsupported or unknown data and required human approvals. Separate proof-of-concept from production readiness and any authorized write operations; no unattended erase, enrollment or Lost Mode changes.

## Deliverable
An integration design brief: problem; validated official API source + review date; endpoint-level evidence pending if not accessed; scopes and secrets handling; mapped data fields; privacy review; test plan; failure modes; estimate; explicit 'NOT CONNECTED' status.

Source: Jamf School API official docs in `../../references/vendor-sources.md`. No invented API operations.

