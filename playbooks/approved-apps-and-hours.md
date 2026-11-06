# Approved app access with time-based restrictions

Status: proposed design with selected vendor-documented behavior; not deployed or device-tested. Reviewed 6 November 2026.

## Desired result

Users install already-approved apps without repeated IT visits. The organization keeps appropriate learning/work controls, with explicit after-hours and accessibility exceptions. Newly requested apps still go through an approval process.

## Keep separate control surfaces

| Surface | Question |
| --- | --- |
| Enrollment and supervision | Does management remain installed and are the intended restrictions eligible? |
| Account modification | May users add or change accounts, and is an exception needed? |
| App acquisition | Which apps and licenses are approved? |
| Installation | Automatic required apps versus optional catalog apps |
| App usage | Which apps may run, and when? |
| Schedule | What happens if the device is locked or offline at a boundary? |

Changing an Apple Account alone does not prove MDM unenrollment. Apple documents supervised controls for account changes, App Store installation and allowed/disallowed app usage (A06). Confirm payload support and existing account/Activation Lock implications before recommending changes. An app's presence alone does not establish that it is managed.

## First Jamf School design to evaluate

Jamf documents On-Demand distribution through the Jamf Student app (J02). Proposed pattern: automatically install essential apps and the catalog client; make approved optional apps available on demand; route only new-app requests to IT. Validate license assignment, user/device association and policy compatibility on the target enrollment. Do not claim this has been configured by this project.

Jamf's timed-profile guidance describes installation at the start and profile removal at the end, with possible delays while a device is locked or offline (J03). Therefore do not promise an exact instant at which every device changes state. Treat connectivity and recovery settings as a separate baseline; removing a timed learning restriction must not remove the only management network configuration.

## Pilot acceptance checklist

- Approved optional app can be found and installed without an IT visit.
- An unapproved app is handled according to the documented ownership-appropriate policy.
- Required apps and accessibility tools remain usable.
- Account restrictions behave as intended without stranding existing accounts or recovery.
- Start/end time behavior is recorded when awake, locked, offline, reconnected and after restart.
- After-hours behavior and exception/recovery procedures are verified.
- Baseline support demand is compared with the pilot; no invented percentage reduction.

Use [the policy matrix](../templates/policy-matrix.csv) before implementation. Sources: [A06, J02 and J03](../references/sources.md). Other MDMs need their own verified mapping.
