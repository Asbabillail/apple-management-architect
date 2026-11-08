---
name: documentation-reporting
description: Use to write MDM SOPs, incident reports, change requests, migration plans, inventory reconciliations, policy standards, audit findings, and reports from supplied sanitized data.
---

# Documentation and reporting

Write actionable technical documents with source traceability and uncertainty; only use data the admin supplied or connected tools actually returned. Clearly distinguish historical snapshots and assumptions from verified live inventory. Do not claim documents, screenshots or reports are persistently stored unless a storage action actually succeeded.

## Document controls
- Use document ID, owner/approver, creation/review date, version, classification, applicable devices and revision history.
- Mark each factual claim as observed evidence or vendor source (link + date), inferred assumption, or unverified. No invented ticket numbers, counts, incidents, test results, or credentials.
- Prefer aggregate statistics; pseudonymize device identities; keep exact school name, serials, email addresses, UDIDs, student information, Wi-Fi passwords, credentials and certificate material out of broad-distribution documents.
- Use versioned change records with risk tier, affected cohort, implementation prerequisite, test evidence, owner approval, go/no-go, rollback trigger and closure.
- Standard outputs: audit report, incident SOP, configuration baseline, Blueprint change register, license utilization gap analysis, risk register, privacy assessment, fleet reconciliation and migration checklist.
- For screenshot notes, attach evidence ID and list what is actually visible, not an imagined hidden console state.

## Templates
See `../../templates/` for report, inventory, change, risk, migration and cohort matrices. Refer to `../../references/vendor-sources.md` for official source links; mark last review date and prompt re-verification for version-dependent claims. If the user requests a file, create it only with actual permitted tooling and link a verified artifact; otherwise provide copyable Markdown/CSV text.
