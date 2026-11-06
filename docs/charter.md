# Project charter

Decision date: 6 November 2026. Working name: Apple Management Architect. Maintainer: [Asbabillail](https://github.com/Asbabillail).

## Purpose

Reduce the repetitive administration burden on small and large IT teams while helping administrators learn. Support schools, universities and businesses, including a sole IT administrator who needs clear steps and less routine work. A customer's environment is one case study, never the default for every organization.

## Accepted scope

| Area | Direction |
| --- | --- |
| Apple services | Apple School Manager, Apple Business and legacy ABM terminology; AppleCare families with product/region/contract distinctions |
| Devices | iPad first; Mac models second; iPhone later; record model, processor and OS applicability |
| MDM approach | Vendor-neutral foundations plus independently verified product adapters; start with Jamf School, then Jamf Pro and Intune |
| Other MDMs | Discover and assess as needs arise; no automatic endorsement or forced migration |
| Human interaction | Understand everyday language; support beginner guidance, expert assistance and future bounded execution |
| Initial execution | Advice and read-only study; integrations and write actions are separate development stages |
| Public material | Original general knowledge, sanitized patterns, source register, evaluation cases and contributions |
| Private material | Organization configurations, identities, inventories, agreements, credentials, recovery data and location evidence remain outside public GitHub |

## Definition of reliable coverage

Each supported task needs prerequisites, current sources, known limitations, an evidence label, a failure path and evaluation cases. For action-capable features, additionally require tested integration behavior, target verification, recovery planning and audit results. No claim of complete mastery of all Apple products or MDMs.

## Initial priorities

Lost/offline recovery, locked-device connectivity, approved app access, account restrictions, timed policies and reduction of recurring helpdesk requests. Enrollment, token/certificate lifecycle, identity, updates and repair/service workflows follow in the coverage backlog.

## Publication and continuity

The public repository was created on 6 November 2026 at [Asbabillail/apple-management-architect](https://github.com/Asbabillail/apple-management-architect). This documentation is the initial public starter publication. Resume from [STATUS.md](../STATUS.md), inspect the current remote and preserve work already completed. A local package does not establish the current remote state.

Changing this public documentation does not silently change the installed private plugin. A later plugin update must name its release, contents and evaluation evidence separately.
