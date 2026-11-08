# General study findings — 2026-11-05

These are portable, dated lessons from official references and sanitized UI inspection. They contain no tenant records. Reviewed sources are not live device tests. Recheck current primary documentation for action-sensitive facts and resolve inconsistencies before giving operational steps.

## Platform and lifecycle separation

Treat ASM organization/assignment/identity, Jamf School enrollment/management and ACE service coverage as different evidence systems. A row in one does not prove the state of another. Inspect ownership, device source, service association, active enrollment, supervision, scope and current device status independently. Keep service replacement reconciliation distinct from an ordinary device return.

Apple distinguishes unassignment for service from release and warns against releasing devices sent for repair. Read [service preparation](https://support.apple.com/en-us/101937) and [release guidance](https://support.apple.com/en-is/guide/apple-school-manager/axmec4d28461/web) before a proposed workflow. No service preparation is authorized merely by discussing the guide. Explicit migration/deadline workflows need their own applicability check; plain reassignment is not a universal migration procedure.

## Tokens and content

APNs trust, ADE enrollment integration and Apps and Books licensing use different certificate/token relationships. For APNs renewal identify the original certificate/account rather than creating a casual replacement. Check [Jamf push renewal](https://learn.jamf.com/r/en-US/jamf-school-documentation/Renewing_an_Apple_Push_Certificate).

[Apple's content-token guide](https://support.apple.com/en-mide/guide/apple-school-manager/axme0f8659ec/1/web/1) identifies both annual validity and password-change invalidation. Avoid deleting existing licensing integrations as a renewal shortcut; see [Jamf token considerations](https://learn.jamf.com/r/en-US/jamf-school-documentation/Volume_Purchasing_Service_Token_Considerations).

Current [Apple content guidance](https://support.apple.com/guide/apple-school-manager/get-apps-and-books-axmc21817890/1/web/1) differs from older fixed-quantity instructions for free apps. [Apple's asset API](https://developer.apple.com/documentation/devicemanagement/managing-assets?changes=_3_5) explains a maximum-integer representation for unlimited assets. Do not infer corruption or actual paid inventory from that representation. Check legacy/location exceptions and the exact app instead of applying a universal free-license rule.

Scope, device/user license assignment and automatic/on-demand installation are independent. Use [Jamf group distribution](https://learn.jamf.com/r/en-US/jamf-school-documentation/Distributing_Apps_and_Packages_to_Groups) and [assignment troubleshooting](https://learn.jamf.com/r/en-US/jamf-school-documentation/App_Assignment_Troubleshooting). An app opening on the device does not by itself establish its managed-app state.

## Identity and profile evidence

Federation concerns authentication; directory syncing concerns account data/lifecycle. Follow [Apple federation](https://support.apple.com/en-gb/guide/apple-school-manager/axmb19317543/web) and [directory-sync](https://support.apple.com/guide/apple-school-manager/intro-to-directory-syncing-axmcf6446c6e/1/web/1) sources, not a sign-in screenshot alone.

Do not make a universal newest-profile or most-restrictive-wins claim. Compare actual payload identifiers and declarations, channels, eligibility and observed outcomes. [Apple profile planning](https://support.apple.com/en-hk/guide/deployment/dep9a318a393/1/web/1.0) and [payload support](https://support.apple.com/guide/deployment/review-device-management-payloads-dep5370d089/web) describe payload-specific limits. A pending declaration is not effective enforcement.

An important specific exception is documented in [Jamf Blueprint components](https://learn.jamf.com/r/en-US/jamf-school-blueprints-configuration-guide/Blueprints_Components): opposing Restrictions keys use the stricter value, while other profile/Blueprint conflicts may behave unexpectedly. Do not extrapolate this rule to every payload.

For DDM updates, distinguish Software Update Settings from the enforcing Software Updates component. [Jamf's update guide](https://support.jamf.com/en/articles/15862413-updating-devices-with-jamf-school-blueprints) documents the iOS/iPadOS 17+ workflow and warns of download/network impact. Verify current OS and component eligibility before a proposed pilot; no Blueprint is deployed by this reference.

## Networks and evidence quality

Separate device management, licensing and content-delivery reachability. Consult [Apple enterprise networking](https://support.apple.com/en-us/101555) and current Jamf School network requirements. Consider the dated [OS 27 TLS guidance](https://support.apple.com/en-au/126655) only as an applicability-sensitive hypothesis when relevant error evidence exists. Do not disable security globally or label a documented change the root cause without evidence.

Read-only investigation uses existing status; dispatching Refresh, sync, Check now or an installation creates work. Keep queued, processed, installed and usable outcomes separate. Use `command-compatibility.md` for detailed gating.

## UI and continuity discipline

Observed labels differed from some vendor instructions: ASM displayed Management Assignment and Device Management Service language; content navigation separated App Store, Custom Apps and Library. Use the current visible UI rather than replaying stale names. A typed search term without verified results does not establish absence. A filtered empty case list does not establish no cases. Stop repeated ineffective interactions, identify the next minimal evidence check and record the limit.

For continuity, update a dated study record with confirmed facts, source conflicts, remaining evidence and the next step using an actual authorized persistence tool. Do not claim automatic cross-chat recall, a school-specific memory database or underlying-model training. Keep general learning and restricted school evidence separate.
