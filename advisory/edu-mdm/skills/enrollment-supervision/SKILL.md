---
name: enrollment-supervision
description: Use for ADE, Apple Configurator manually added iPads, supervision mismatches, enrollment persistence, MDM removal defenses, and ownership-aware hardening.
---

# Enrollment, supervision and policy hardening

Only advise authorized configuration to **protect** school management, not to evade it. Identify which controls require Automated Device Enrollment, which require supervision, which work with other enrollment types, and whether Apple Configurator provisional release applies. School-owned and personally owned devices must be separately handled.

## Decision flow
1. Verify device source, current owner, written authority/consent, ASM assignment, Jamf School enrollment method, supervised flag, current OS, and whether device completed Setup Assistant.
2. Determine if a restriction is **supported / supervised-only / ADE-dependent / version-dependent / BYOD-inappropriate / unverified**. Quote or link exact vendor guidance for setting names and minimum versions.
3. Analyze MDM profile removal, account changes, app installation, erase restrictions, Activation Lock, managed accounts and app distribution as **separate control surfaces**. A settings UI restriction does not necessarily prevent all device recovery/erase paths.
4. For Apple Configurator manual additions, verify Apple's **30-day provisional-release period** after successful assignment and enrollment; avoid promising permanence during that period.
5. Draft defense-in-depth with least privilege, accepted educational exceptions, institutional recovery route and audit trail; never claim device control is permanent or unbreakable.
6. Sequence: verify/repair Wi-Fi profile → validate enrollment and supervision → stage supported account/app/erase restrictions → pilot → broaden carefully. Log explicit authorization for any destructive action.

## Output
Ownership × enrollment × supervision × iPadOS capability grid with confidence, documentation link, applicable configuration, privacy review, pilot and rollback plan. For personally owned devices default to minimally necessary controls and consensual enrollment or a different organization-approved solution.
