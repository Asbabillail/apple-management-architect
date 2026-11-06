# Passcode-locked and offline iPad

Status: initial vendor-documented limitation and proposed diagnostic procedure; no live pilot. Reviewed 6 November 2026.

## Identify the credential first

A device passcode is different from a Managed Apple Account password or an application password. Record the exact lock-screen message privately, whether restart occurred, the last check-in, ownership/enrollment, model/OS and network type. Do not keep trying passcodes or request the user's password.

Apple's Restart Device documentation warns that a passcode-locked iOS device does not rejoin Wi-Fi after restart and may lose server communication (A03, official search extract; full-page retrieval limited). Treat this as a platform recovery constraint, not proof of a broken Jamf token. A managed Wi-Fi profile is not a guaranteed cure for every before-first-unlock scenario.

## Read-only decision path

| State | Action to prepare |
| --- | --- |
| Reachable, passcode problem confirmed | Check MDM command applicability, required rights and available recovery state before an authorized clear-passcode action |
| Offline after restart | Stop promising remote clearing; determine supported ways to restore connectivity with on-site staff/vendor support |
| Online but command pending/error | Read actual command responses and timestamps; distinguish network, authorization and command-specific failure |
| Connectivity cannot be restored | Escalate a data-preservation/recovery decision; do not silently erase |

Do not promise that a cable, hotspot, Wi-Fi profile or Ethernet adapter will work on every locked iPad. Accessory authorization, pairing, policy, hardware and OS matter. Investigate any supported wired option in a controlled pilot; do not disable security protections to force connectivity.

Apple documents recovery-mode restore as an erasing process (A05). Before considering it, establish explicit authority, backup/data impact, Activation Lock handling and enrollment recovery. This preview intentionally does not automate restore or provide a bulk-reset procedure.

## Future pilot record

Use a spare authorized device and known test data. Record unlocked, locked, restarted-before-first-unlock, network-restored and recovered states; authentication method; exact OS/model; MDM responses; data preservation; failures and recovery. Never test repeated wrong-passcode behavior on a production user's data merely to reproduce the issue.

Sources: [A03–A05](../references/sources.md). Use the [private observation template](../templates/observation.md) outside public GitHub.
