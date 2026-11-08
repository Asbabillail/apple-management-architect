# Official vendor source registry — reviewed 2026-10-26

This is a dated source index, **not a promise** that every UI label/constraint remains current. For actionable technical claims, check the exact live official page before giving steps, and record review date, product, OS prerequisites, confidence and the affected command/profile. Jamf **School** docs are authoritative for School UI, not Jamf Pro / Now / Insights.

| Topic | Primary official URL | Review finding / qualification |
| --- | --- | --- |
| Apple ADE and management | https://support.apple.com/guide/deployment/automated-device-enrollment-management-dep73069dd57/web | ADE supports enrollment profile removal prevention for supervised organization devices; ownership matters. |
| Apple manual addition & provisional period | https://support.apple.com/guide/apple-school-manager/axm200a54d59/web | Devices added using Apple Configurator have a conditional 30-day provisional release period following successful assignment/enrollment. Reconfirm the specific path and current terms. |
| Apple provisioning sources | https://support.apple.com/guide/deployment/depb5ae24c4a/web | Manual addition mechanics and provisional period. |
| Apple managed Wi-Fi payload | https://support.apple.com/guide/deployment/dep168e876c9/web | Wi-Fi payload includes SSID, Auto Join and security settings; check enrollment/OS support. |
| Apple Wi-Fi join behavior | https://support.apple.com/guide/deployment/dep3b0448c58/web | Describes profile-configured Wi-Fi and auto-join; **does not establish unconditional first-unlock network access**. |
| Jamf School docs landing | https://learn.jamf.com/r/en-US/jamf-school-documentation/Jamf_School_Documentation | Navigate to current School product references; avoid Jamf Pro substitutions. |
| Jamf School quick action commands | https://learn.jamf.com/r/en-US/jamf-school-documentation/Quick_Action_Commands_Reference | Clear Passcode; Managed Lost Mode is conditional on supervision and network connection; prerequisites per action. |
| Jamf School restrictions profile | https://learn.jamf.com/r/en-US/jamf-school-documentation/Configuring_a_Restrictions_Profile | **Important:** deploy working Wi-Fi/network profile before restrictions that may block joining networks. |
| Jamf School network configuration | https://learn.jamf.com/r/en-US/jamf-school-documentation/Creating_a_Network_Configuration_Profile_for_Devices | Official profile steps and scope; certificate/SCEP dependencies, feature version review. |
| Jamf School mobile Wi-Fi profile | https://learn.jamf.com/r/en-US/jamf-school-documentation/Creating_a_Mobile_Device_Wi-Fi_Profile | Official iOS/iPadOS School profile workflow. |
| Jamf School device details | https://learn.jamf.com/r/en-US/jamf-school-documentation/Device_Details | Observability fields vary by model/OS. |
| Jamf School passcode management | https://learn.jamf.com/r/en-US/jamf-school-documentation/Passcode | Passcode payload and command guidance. |
| Jamf School API | https://learn.jamf.com/r/en-US/jamf-school-documentation/Jamf_School_API | API exists and configured by tenant admin; actual methods must be independently verified. |

## Claims that must not be assumed
- Continuous Wi-Fi connectivity after reboot/while locked or before first unlock.
- Delivery of Clear Passcode, Lost Mode or other MDM command while target has no viable network channel.
- Jamf School menu labels or payload behavior replicated from Jamf Pro or Jamf Now.
- Current supported OS minimums, restriction keys, non-removable enrollment, Configurator release behavior, or API endpoints without reference to the actual current docs.
- That Apple School Manager device count equals checked-in Jamf School device count.

## Source refresh routine
At each major audit and prior to change-control approval: (1) identify exact vendor feature + product + OS + enrollment mode; (2) open latest primary documentation; (3) date evidence and record direct URL; (4) distinguish vendor-confirmed, device-tested, conditional, unknown; (5) update issue record and release changelog on recurring fact changes. Document source unavailability honestly and suspend unverified fleet-wide recommendations.

## 2026-11-05 source supplement
Command matrix and per-command Apple references: `command-compatibility.md`. AppleCare terms and agreement evidence method: `applecare-service-pool.md`. Dated general findings and direct source links: `study-findings.md`. Read the specific relevant reference, not every document. Older rows remain historical pointers, not proof their labels are current. No school records or credentials are included.

# Practical advisory additions — reviewed 8 November 2026

- [Jamf School iOS installation types](https://support.jamf.com/en/articles/11012773-jamf-school-ios-application-installation-types): full short article reviewed; automatic/on-demand distinction and inventory assignment-card inspection.
- [Apple Account requirement for Jamf School apps](https://support.jamf.com/en/articles/11013282-do-my-students-need-an-apple-account-to-install-applications-in-jamf-school): official search extract reviewed; device-based distribution can avoid Apple Account sign-in; verify current Apple free-app entitlement wording separately.
- [Jamf School time restrictions](https://support.jamf.com/en/articles/11750353-setting-time-restrictions-on-a-profile-in-jamf-school): full article reviewed; schedule/removal behavior and locked/offline caveats; verify exact payload/OS behavior rather than extending every sentence universally.
- [Apple iPhone/iPad restrictions](https://support.apple.com/en-gb/guide/deployment/dep0f7dd3d8/1/web/1.0): relevant official extracts reviewed for account modification, App Store installation and app usage; full current payload and MDM mapping remain task-specific checks.
- [Jamf School app safelist/blocklist](https://learn.jamf.com/r/en-US/jamf-school-documentation/Configuring_a_Safelist_and_Blocklist_Profile_for_Mobile_Devices): relevant body reviewed; OS 27 category-key deprecation and explicit app selection.

