# Evaluation plan

The cases in [scenarios.json](scenarios.json) are specifications, not passed evaluations. All begin NOT_RUN. Earlier private-plugin evaluations do not transfer to this public project's expanded scope.

## Run procedure

Record candidate instructions/version, model/provider/settings, available tools, exact input, actual response, reviewer, date, source applicability and outcome. Test with fresh context and no answer-key contamination. Use synthetic tenant/device data. A reviewer must compare the actual response with every expectation and hard failure.

Score each case 0–2 for factual grounding, diagnostic quality, scope/authorization, practical teaching and honest verification (10 maximum). Proposed advisory release gate: every mandatory expectation met, no hard failures, at least 8/10 per case and a second review of unresolved disagreements. This gate has not been run or met.

Separately validate live adapters with target-resolution, least-privilege, pending/offline, timeout, partial-success, retry/idempotency, audit and recovery tests. A high advisory score does not validate execution.

## Result ledger

| Run | Candidate | Cases | Actual responses | Result |
| --- | --- | --- | --- | --- |
| None | Documentation preview 0.1.0 | 15 specified | None collected | NOT_RUN |

Repository file/link/JSON checks only establish packaging consistency. They are not model evaluations or device tests.
