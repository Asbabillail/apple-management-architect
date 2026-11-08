---
name: wifi-device-recovery
description: Use for iPad Wi-Fi auto-join, network-profile deployment, WPA Enterprise certificates, connectivity loss, post-restart network behavior, offline passcode commands, and recovery.
---

# Wi-Fi and offline-device recovery

**No guaranteed network availability after restart or before first unlock.** Distinguish behavior observed after restart, after lock, after passcode failure, after cert expiry and general out-of-range/offline status. Never promise a remote passcode-clear command to a disconnected Wi-Fi-only iPad; queued does not mean delivered.

Explain the specific documented limitation when restart is part of the report: [Apple's Restart Device command reference](https://developer.apple.com/documentation/devicemanagement/restart-device-command) warns that a passcode-locked iOS device does not rejoin Wi-Fi after restarting and may lose server communication. Identify this warning explicitly before discussing other network hypotheses; verify the actual model/OS/state rather than converting it into an unconditional claim about every locked device. Do not dilute it into a vague “network issue,” and do not promise that a new Wi-Fi profile or cable will fix it.

## Diagnostics
Identify the credential in the response: an iPad screen-unlock passcode is distinct from a Managed/personal Apple Account password or an app password. When the user has clearly named the device passcode, state that interpretation briefly rather than asking them to re-confirm the same fact. Clear Passcode is not an Apple Account password reset.

1. Reuse supplied facts about model/OS, supervision/enrollment, ownership, last check-in, restart and network authentication. Ask only the next missing fact needed to choose a recovery branch, rather than presenting the whole inventory as an intake form. Establish whether a management Wi-Fi profile is **already installed** and distinguish PSK from 802.1X/EAP-TLS/PEAP where relevant. Avoid asking for credentials.
2. Audit profile's exact SSID, Auto Join, security type, trust chain, SCEP identity cert validity, renewal strategy, RADIUS availability, device clock, AP reachability, captive portals, VLAN/firewall and Apple Push Notification reachability. Differentiate device-side and network-side failures. Managed Wi-Fi can improve reliability but not abolish boot/first-unlock constraints.
3. Validate that policies enabling 'only join Wi-Fi configured through profiles' or enforced Wi-Fi-on are rolled out **after** a working managed Wi-Fi profile. Jamf School explicitly warns of connection loss if order is reversed.
4. For offline passcode-clear: record command state; if authorized, escalate to on-site support to restore supported connectivity where possible; check for secure data preservation and documented backup policy; only consider device reset/re-enrollment as approved last resort, noting data loss and Activation Lock risks.
5. Trial on one school-owned pilot device through reboot and locked scenarios, include 802.1X credential/certificate rollover testing. Never instruct circumventing passcodes or student account controls.

## Output
Decision tree: 'offline/no management channel' vs 'online/command pending' vs 'online/command failed' and exact next safe step, plus risk of losing management. Include reproducible connectivity matrix (fresh boot, unlocked, re-locked, roaming, cert renewal), pass/fail observations, owner, rollback and source.

Official references: Apple managed Wi-Fi payload / join behavior; Jamf School network config, restrictions and quick action documentation in `../../references/vendor-sources.md`.

## Version-sensitive network review
Load `../../references/study-findings.md` and `../../references/command-compatibility.md` when analyzing restart recovery, app delivery versus management connectivity, current OS TLS requirements or pending actions. Do not declare the OS security change a root cause without relevant errors. Do not disable certificate validation or security inspection globally as a diagnostic shortcut.

