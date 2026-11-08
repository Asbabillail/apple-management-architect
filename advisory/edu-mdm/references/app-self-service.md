# Approved app catalog and time-based access

Reviewed 8 November 2026. General source-backed guidance; no tenant configuration or device pilot is asserted.

## Design objective

Reduce repeated installation requests while retaining an approved app selection and proportionate usage rules. Prefer a reusable workflow before building a custom app-request system or migrating MDM.

## Separate these questions

| Layer | Evidence needed |
| --- | --- |
| Ownership/enrollment | Organization-owned or BYOD; supervision and enrollment type verified separately |
| Acquisition/license | Correct app and organization/location entitlement; exact device/user assignment |
| Installation | Required automatic app or approved optional on-demand app; all scope paths checked |
| Account settings | What account changes are allowed, what is already signed in and how recovery works |
| App usage | Which app can run during which period; actual supported restriction |
| Connectivity | Management and content reachability; state at schedule boundaries |

## Jamf School installation model

[JSS1](https://support.jamf.com/en/articles/11012773-jamf-school-ios-application-installation-types) distinguishes automatic installation from on-demand availability in Jamf Student. Proposed workflow: required learning apps remain automatic; approved optional apps go in the on-demand catalog; new apps use a separate approval route. Inspect Apps > Inventory, select the example app and read its group assignment cards. Confirm the current UI before describing a change. The article's illustrated change is toward automatic installation; do not invent the reverse menu label if it is not visible.

[JSS2](https://support.jamf.com/en/articles/11013282-do-my-students-need-an-apple-account-to-install-applications-in-jamf-school) says device-assigned volume-purchasing apps do not require an Apple Account on the iPad. Confirm integration and entitlement rather than recommending a personal account. Its quantity/purchase wording may lag Apple's newer free-app flow: use `study-findings.md` and current Apple guidance for exact free-app/location behavior. Unsupervised installation prompts need separate handling.

## Account and usage controls

[ASR1](https://support.apple.com/en-gb/guide/deployment/dep0f7dd3d8/1/web/1.0) documents supervised controls for account modification, App Store installation and app usage. Verify the target's current OS and MDM mapping. Changing an account alone is not proof of enrollment removal. Do not trap an existing personal account by applying a restriction without an approved transition and recovery route. Do not treat blanket lockdown as the default for BYOD. Review accessibility, essential apps and after-hours requirements before setting the policy.

[JSS4](https://learn.jamf.com/r/en-US/jamf-school-documentation/Configuring_a_Safelist_and_Blocklist_Profile_for_Mobile_Devices) notes that safelisted/blocklisted category keys are deprecated in iOS/iPadOS/tvOS 27. Check explicit app identifiers and current OS-specific controls instead of promising a category-based rule covers every game. Do not assume the app catalog and the usage allow/block list are the same configuration.

## Timed profile caveats

[JSS3](https://support.jamf.com/en/articles/11750353-setting-time-restrictions-on-a-profile-in-jamf-school) describes installation at the active period's start, a scheduled removal date, and possible delays while locked or offline. Do not promise an exact instant for every device or generalize its broad InstallProfile wording beyond the relevant payload/OS. Test awake, locked, restarted, offline and reconnected states. Review timezone/date settings and ownership-appropriate controls. Keep managed Wi-Fi, enrollment and recovery outside discretionary timed restrictions.

## Proposed pilot, not deployment

Use one authorized test iPad or a small pilot group. Record the current app methods/scopes and profile values; identify other assignment paths and ownership. Verify catalog-client availability, content entitlement and network prerequisites. Agree an example required app, optional app, new-app request and usage exception. Make proposed changes only within separate change authority.

Acceptance: optional app can be found/installed without an IT visit; required apps remain available; account and schedule behavior match the documented policy; accessibility tasks work; failures and recovery are recorded. Restore only the specifically changed assignment/profile values after checking app-data and licensing impact; do not remove an app from the fleet as a rollback shortcut.

The expected benefit is a hypothesis until support visits and handling time are measured. This reference does not add a catalog to any tenant.
