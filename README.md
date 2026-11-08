# Apple Management Architect

Evidence-backed Apple administration guidance for schools, universities and businesses. Explain the task in ordinary language; get a practical plan, learn while doing it, and build toward carefully authorized automation.

**Status: practical advisory source v0.3.0 — 8 November 2026.** The existing private EDU-MDM Architect plugin was updated separately to v0.3.0 and its 37 text files matched the reviewed candidate on readback. This repository publishes its general [instructional source](advisory/edu-mdm/README.md) and [actual response evidence](evals/runs/2026-11-08/README.md). It contains no operational MDM integration and cannot dispatch device commands. Wider platform coverage remains unfinished. See [release scope](docs/practical-release.md).

## Start here

| Your goal | Read |
| --- | --- |
| Understand the project and supported scope | [Charter](docs/charter.md) and [coverage](docs/coverage.md) |
| Use the advisory instructions in an AI assistant | [Getting started](docs/getting-started.md) and [agent instructions](agent/INSTRUCTIONS.md) |
| Find a lost iPad | [Lost-device playbook](playbooks/ipad-lost-device.md) |
| Recover a passcode-locked, offline iPad | [Recovery playbook](playbooks/ipad-locked-offline.md) |
| Reduce repetitive app-installation requests | [Approved apps and restrictions](playbooks/approved-apps-and-hours.md) |
| Compare MDM options without assuming feature parity | [MDM registry](docs/mdm-registry.md) |
| Check evidence, tests and remaining work | [Sources](references/sources.md), [evaluations](evals/README.md) and [roadmap](ROADMAP.md) |
| Contribute a correction or scenario | [Contributing](CONTRIBUTING.md) |

## Design commitments

- Apple platform fundamentals first; separate MDM-specific instructions. Never substitute Jamf Pro instructions for Jamf School.
- Prioritize iPad families and iPadOS, then Mac hardware including MacBook, iMac, Mac mini, Mac Studio and Mac Pro where supported, then iPhone. A roadmap entry is not a compatibility claim for every model or OS.
- Cover Apple School Manager, Apple Business (including legacy Apple Business Manager terminology) and AppleCare service families in distinct modules.
- Offer Learn, Assist and Operate workflows. Operate is a future integration capability, not a switch that grants access or removes approvals.
- Separate reviewed documentation, user reports, UI observations, simulations and device-tested results.
- Keep each organization's confidential configuration outside the public project and outside other customers' contexts.

## First three use cases

1. A Wi-Fi-only iPad is lost and currently offline: distinguish last check-in from location; explain command-delivery limits; plan recovery.
2. An iPad is passcode-locked and restarted: diagnose network state before assuming that clearing the passcode remotely is possible.
3. Users repeatedly request apps or switch accounts: design an approved self-service catalog and evaluate account/app controls and scheduled restrictions.

These are generalized scenarios. They contain no customer inventory, location or identifiable records. No playbook in this preview has been validated on a live device by this project.

## Current terminology

Apple's current guide says Apple Business combines capabilities formerly provided by Apple Business Manager, Apple Business Essentials and Apple Business Connect. Keep historical labels for older documentation and console screenshots, and verify regional availability before recommendations. See source A01 in [the source register](references/sources.md).

## What this project does not promise

An assistant cannot deliver an MDM command to a device with no reachable management channel, guarantee an exact historical location, or turn incomplete evidence into proof. Better documentation and test results improve reliability; they do not mean the underlying model has been permanently retrained.

Independent community project; not affiliated with or endorsed by Apple, Jamf, Microsoft or other vendors. Original project material is available under the [MIT license](LICENSE). Vendor documentation and trademarks remain their owners' property.
