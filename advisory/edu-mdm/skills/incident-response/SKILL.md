---
name: incident-response
description: Use when a managed school iPad is lost, offline, passcode-locked, un-enrolled, missing apps, failing Wi-Fi, or experiencing an MDM incident requiring triage and escalation.
---

# School MDM incident response

Safety, privacy, legal/organizational authority and evidence preservation are part of incident handling. Confirm the reporter's authorized administrative role; avoid collecting exact student location or credentials in chat. Do not conduct covert surveillance.

## Severity and triage
1. Open incident ID, timestamp, affected device reference **pseudonym**, ownership, cohort, model/OS, last known check-in, enrollment/supervision and service impact.
2. Classify urgency by exposure and number affected. A stolen device with student data may require escalation to school security/privacy officials. Do not infer theft from missing inventory.
3. Route by symptom:
   - **Forgotten device passcode:** confirm authorization, last network connectivity, whether a Jamf School Clear Passcode command is supported; if offline, note the communication prerequisite, on-site escalation, data recovery concerns and reset as approved last resort.
   - **Forgotten Managed Apple Account:** route to identity/ASM-approved account recovery; never solicit or reproduce passwords.
   - **Lost/missing:** notify designated school authority, verify supervised and reachable, use Jamf School Managed Lost Mode only when authorized and supported; location is conditional on network connectivity and governed by school policy. Record every location access and disable Lost Mode after recovery.
   - **Offline:** troubleshoot power, Wi-Fi, certificate, APNs and profile installation; do not claim a command can locate or recover a disconnected device.
   - **Unsupervised/enrollment issue:** verify ASM/ADE/Configurator status before considering on-site re-enrollment.
   - **Missing app:** check Jamf scope, OS, managed distribution license, network, inventory and failed commands.
   - **Unwanted restrictions/conflicting profiles:** stop further rollout, compare effective scopes, choose smallest reversible change with pilot.
4. Define containment, authority, implementation, verification, stakeholder notification and post-incident actions. No automated mass erase.

## Outputs
Use `../../templates/incident-report.md` including timeline, evidence confirmed vs unconfirmed, suspected cause, minimal safe recovery path, signoffs, privacy handling, validation and postmortem. Use Jamf School Quick Actions source; do not substitute other Jamf products.

For ordinary task assistance, use `../../references/task-guidance.md` to avoid burying the next useful observation in a full report. For recurring approved-app requests, route to `../app-self-service/SKILL.md`. For a missing device, distinguish a last check-in timestamp from an actual location report; do not invent historical coordinates or treat an access-point association as an exact physical location. A cable or newly proposed Wi-Fi profile is not a guaranteed recovery method for a locked device after restart.
