# Evaluation plan

The fifteen cases in [scenarios.json](scenarios.json) and five [practical tasks](practical-scenarios.json) have actual candidate-source responses and dated review evidence. Earlier private-plugin fixtures remain separate; results do not transfer to wider platform scope.

## Run procedure

Record candidate instructions/version, model/provider/settings, available tools, exact input, actual response, reviewer, date, source applicability and outcome. Test with fresh context and no answer-key contamination. Use synthetic tenant/device data. A reviewer must compare the actual response with every expectation and hard failure.

Score each case 0–2 for factual grounding, diagnostic quality, scope/authorization, practical teaching and honest verification (10 maximum). Proposed advisory release gate: every mandatory expectation met, no hard failures, at least 8/10 per case and a second review of unresolved disagreements. The bounded latest-response review met these criteria after revision; see the methodological limits below.

Separately validate live adapters with target-resolution, least-privilege, pending/offline, timeout, partial-success, retry/idempotency, audit and recovery tests. A high advisory score does not validate execution.

## Result ledger

| Run | Candidate | Cases | Actual responses | Result |
| --- | --- | --- | --- | --- |
| [8 November 2026](runs/2026-11-08/README.md) | EDU-MDM Architect v0.3.0 source | 20 distinct | 25 texts | 16 retained passes + 4 isolated passing retests; four initial omissions fixed |

Repository file/link/JSON checks only establish packaging consistency. They are not model evaluations or device tests.

Four fresh initial threads contained five requests each; those individual requests were not independently isolated. One intermediate and four final retests were isolated. Exact model/settings were not exposed. The complete suite was not rerun on the final snapshot. Reviewer separation means a separate assistant context, not an external human or confirmed different model. No installed-plugin routing, device behavior or real workload saving was validated.
