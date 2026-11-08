# Jamf School command readiness — reviewed 2026-11-05

## Scope and evidence

This is an iPad-first compatibility decision aid, covering the command families in Jamf School's [Quick Action reference](https://learn.jamf.com/r/en-US/jamf-school-documentation/Quick_Action_Commands_Reference). It is vendor-documentation study, not device testing. Use the current vendor page for an exact action, OS/build and tenant UI before operational instructions. Do not substitute Jamf Pro or assume every Apple MDM protocol capability is exposed by Jamf School.

Legend: E = iPadOS listed, with no additional prerequisite stated in this summary; S = supervised; A = ADE; H = Shared iPad; C = console-side operation; N = network path for device-side execution. E is **not** permission or proof of User Enrollment support. All actions remain unexecuted in read-only study. Console changes may work while a device is offline but their downstream device effects still need delivery.

## Jamf School family index

| Family | Additional prerequisites |
| --- | --- |
| Refresh | E |
| Rename; restart; shutdown; Bluetooth | S |
| Time zone | S,A,14+ |
| Passcode clear | Existing passcode |
| Screen Time clear | S |
| Lost Mode; sound | S; sound needs Lost Mode |
| Activation Lock enable/retry | S,ASM; enable bulk-only |
| Activation Lock clear | S,reported bypass code |
| Group/user/location/trash/log operations | C |
| Quota/cache/logout | H |
| Cellular-plan refresh | eSIM,cellular |
| Data/voice roaming | Cellular |
| Hotspot | E |
| Accessibility change/reset | 16+ |
| Update check | E |
| Update download/install | S,14+; see version gate |
| Profile install/disable | E |
| Managed/internal app installation | S |
| Managed app removal/deferred deletion | S |
| Document install/removal/deferred deletion | E |
| Disown | A |

Erase and unmanage require separate destructive/lifecycle analysis below. EFI password, Recovery Lock, Remote Desktop and the catalog's Install and Restart computer action are outside this iPad-first index; use Mac-specific references rather than recommending them for iPadOS. The family index intentionally omits bulk support except the unusual enable-Activation-Lock constraint: verify bulk separately for any selected action.

## Apple protocol cross-checks

The following links were reviewed as official search extracts on 2026-11-05. The Apple API is not a Jamf School REST endpoint. Never copy the sample MDM transport URL into a guessed Jamf API script.

| Action | Apple evidence to apply with the Jamf gate |
| --- | --- |
| [Clear Passcode](https://developer.apple.com/documentation/devicemanagement/clear-passcode-command) | Device channel; no supervision requirement stated; not listed for User Enrollment; requires passcode-removal access. Do not confuse missing supervision requirement with consent or ownership. |
| [Device Lock](https://developer.apple.com/documentation/devicemanagement/device-lock-command?changes=l_1_3) | Apple lists iOS User Enrollment availability. Do not apply a blanket ban on all lock/settings commands just because some destructive commands exclude User Enrollment. Validate actual Jamf support and authority. |
| [Erase Device](https://developer.apple.com/documentation/devicemanagement/erase-device-command?changes=l_5) | Full-device erase is not listed for User Enrollment. It can remove data without user warning; acknowledgment is not proof of completed re-enrollment or data recovery. |
| [Restart Device](https://developer.apple.com/documentation/devicemanagement/restart-device-command) | Requires applicable supervision; User Enrollment not listed. A locked iOS device may lose Wi-Fi reachability after restart. Establish a recovery path before proposing it. |
| [Shut Down Device](https://developer.apple.com/documentation/devicemanagement/shut-down-device-command?changes=latest_minor%2Clatest_minor) | Supervision required for iOS; User Enrollment not listed. Plan how an authorized person will restore power and connectivity. |
| [Install Application](https://developer.apple.com/documentation/devicemanagement/install-application-command?changes=_5_9) | Apple lists iOS User Enrollment and no general supervision prerequisite. That protocol capability does not override the supervised-device requirement shown for particular School quick actions. |
| [Install Profile](https://developer.apple.com/documentation/devicemanagement/install-profile-command) / [Remove Profile](https://developer.apple.com/documentation/devicemanagement/remove-profile-command?changes=la_7) | iOS User Enrollment is listed, but payload, channel, ownership and rights still constrain what can be installed/removed. Removing connectivity material can strand management. |
| [Settings](https://developer.apple.com/documentation/devicemanagement/settings-command) | Parent-command User Enrollment availability does not make every Settings item available. Verify the exact item and channel. |

## Version gate for software updates

[Apple Schedule OS Update](https://developer.apple.com/documentation/devicemanagement/schedule-os-update-command) is currently marked deprecated/removed in favor of declarative update management. [OS Update Status](https://developer.apple.com/documentation/devicemanagement/os-update-status-command?changes=_8) also directs readers to declarative status reporting. These notices do not prove that a Jamf School update button is broken: determine the target OS, legacy-versus-DDM path and current Jamf implementation before mapping UI labels to protocols. Never propose an unverified legacy API operation as the universal solution for current iPadOS.

## Preflight, evidence and recovery

For the exact action, record: owner/consent, role/rights, target count, hardware/OS/build, enrollment and channel, supervision, payload/group scope, applicable catalog row, existing delivery state, and a safe recovery path. Separate the console's acceptance of work from queueing, delivery, device processing and the intended final result. Use existing evidence during read-only study; do not send queries to obtain it.

For erase, establish a separately approved data/backup/re-enrollment plan. For unmanage, assess the managed apps/profiles and connectivity that would be removed. For disown/release, assess organization association and service/replacement consequences. Do not present any of them as an ordinary diagnostic reset.

For cellular actions, check actual cellular/eSIM capability rather than the iPad model family alone. For Shared iPad, verify that deployment mode instead of assuming that a device shared socially by several pupils is configured as Shared iPad. For Teacher/Parent restriction removal, identify which system owns the restriction; do not assume it removes organization profiles. Preserve logs rather than clearing evidence during troubleshooting.

Return a compact readiness record: action → verified prerequisites → missing evidence → impact → proposed validation/recovery. If a source is unavailable or conflicting, mark it unverified and give the smallest source/evidence check needed; do not fill gaps with invented minimum versions. Read-only study authorization never authorizes sending the selected command.
