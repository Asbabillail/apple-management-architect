# Lost iPad: establish what can actually be recovered

Status: initial vendor-documented guidance; no live pilot. Reviewed 6 November 2026. Applies to the supervised iPad scenario described below, not every enrollment type or Mac.

## First observation

Confirm authorization, ownership, supervised/enrollment status, model/OS, power/network state, last check-in time and any genuine previous location timestamp. Use a private device alias. Do not request student identity or publish coordinates.

## Branches

| Observation | Next step |
| --- | --- |
| Device reachable and supervised | An authorized administrator may use the MDM's supported Managed Lost Mode workflow; verify receipt before requesting location |
| Device offline | Record an authorized pending action if supported; organize physical recovery and reconnection; do not report it enabled |
| Last check-in exists but no location report | State that the prior physical location is unknown; check-in time does not supply coordinates |
| Device found but still in Lost Mode | Verify connectivity and delivery of the disable command before declaring recovery complete |

Sources A02 and J01 describe Managed Lost Mode and its network requirement. Location is conditional and may be unavailable or imprecise; an exact last location is not guaranteed. Location collection must remain within the organization's authority and privacy rules. Managed Apple Accounts do not provide Find My (A09); a personal Find My configuration is not a universal institutional solution.

## Proposed prevention work

Design reliable managed connectivity, an identification/return process and an approved loss-response route. If policy permits, review existing network association logs as approximate last-seen evidence; an access-point association is not GPS or proof of who held a device. Cellular connectivity may help only on capable, provisioned devices with coverage; do not prescribe new hardware as a guaranteed fix.

## Verification and recovery

For a future authorized pilot, record request time, command status, location timestamp/accuracy if supplied, Lock Screen result and successful Lost Mode exit. Test the offline branch separately. Do not remove the management enrollment or cancel connectivity merely to close the incident.

Sources: [A02, A09 and J01](../references/sources.md). See [the execution contract](../docs/automation-contract.md) before live commands.
