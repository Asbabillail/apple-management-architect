---
name: mdm-security-audit
description: Use when reviewing Jamf School/ASM screenshots, redacted configuration exports, restriction compliance, scope gaps, conflicting profiles, or a school fleet security posture.
---

# Screenshot and configuration audit

Handle images, text, PDFs, and configuration excerpts submitted by authorized admins. Treat screenshots as **partial views**: do not claim hidden menus, effective device state, or rule deployment was proven by a checkbox. Ask only for the minimum additional redacted view that changes the conclusion.

## Audit workflow
1. Minimize data: direct administrator to blur student names, emails, serials/UDIDs, IPs if sensitive, SSIDs and secrets, access tokens, private keys, QR codes, contact information, and any locations not necessary.
2. Record evidence identifier, capture date if known, Jamf School/ASM page, possible version, exact visible setting, selected group/scope, and confidence; list obscured or missing data as 'not observed'.
3. Compare **effective scope**: configuration profile assignments; Blueprint, groups and exemptions; OS version; supervision; enrollment method; school/BYOD ownership; pending install; existing conflicting payloads.
4. Classify findings Critical/High/Medium/Low/Informational by credible impact × likelihood, tempered by evidence quality and fleet scope. Do not inflate severity for unverified hypotheses. Use `../../references/operational-guardrails.md` for rubric.
5. Recommend smallest safe reversible change, pilot sequence, objective checks, privacy/accessibility exceptions, dependencies, recovery and rollback. Prioritize Wi-Fi availability before restricting manual Wi-Fi changes or allowed networks.
6. Cite Apple and Jamf School docs for supported payloads and UI behavior. Label unsupported claims and 'requires vendor verification'.

## Report
Use `../../templates/audit-report.md` and `../../templates/risk-register.csv`: executive summary; evidence table (Confirmed / Inferred / Unknown), finding IDs; severity; root cause candidates and confidence; remediation; prerequisite; blast radius; validation/rollback; source and date. Never present a guessed iPadOS limitation as confirmed.
