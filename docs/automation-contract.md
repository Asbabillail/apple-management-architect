# Future execution contract

Design only. No adapter or credential store is implemented in this preview.

Automation should remove repeated work without disguising uncertainty or expanding access. Prefer supported APIs for repeatable tasks; use browser UI only where appropriate and authorized. Do not invent endpoints from product names.

## Operation record

Each adapter operation must declare: provider/product and supported versions; read/write effect; tenant and target selection; required role; inputs and sensitivity; prerequisites; dry-run or preview availability; expected result; timeout; retry rules; idempotency limits; verification method; recovery; audit fields; and approval class.

## Execution sequence

Resolve intent and targets → inspect baseline → plan or dry-run → obtain any required approval → execute bounded batch → verify actual results → report and document.

Read-only discovery may proceed within existing authority. Write authority must name allowed operations and scope. Locks, passcode clears, location queries, app removals, erases, enrollment release, certificate changes and fleet policy changes require their applicable sensitivity and approval handling. Do not retry a possibly completed non-idempotent action blindly.

## Failure behavior

- Offline target: queue only if authorized and supported; report pending, timestamp and next observation. Never claim completion.
- Ambiguous target or tenant: stop the dependent write and ask for the missing identity privately.
- Missing permission: report the gap; do not create broader roles or credentials without separate authority.
- Partial success: preserve per-target outcomes, stop when thresholds are exceeded and use the documented recovery route.
- Unexpected prompt, changed UI or source discrepancy: stop and inspect; never bypass security controls.
- No integration: provide a guided procedure; do not claim auto mode is working.

Keep credentials in an appropriate secret store and logs in the customer's approved environment. Public evaluation fixtures must use synthetic data. Integration readiness requires real failure, recovery and authorization tests, not only model response scores.
