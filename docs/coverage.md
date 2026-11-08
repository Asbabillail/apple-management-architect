# Coverage and evidence levels

Last reviewed: 8 November 2026.

General advisory source and a bounded twenty-request response review are now available; [evidence and limits](../evals/runs/2026-11-08/README.md). No live pilot has run.

| Area | Present in this preview | Remaining work |
| --- | --- | --- |
| iPad lost-device handling | Source-backed initial playbook | Per-version applicability and live pilot |
| Passcode-locked/offline iPad | Source-backed limitation and diagnostic plan | Model/OS/network recovery matrix and authorized pilot |
| Jamf School approved apps | On-demand advisory source and response review | Installed-host check, console walk-through and pilot results |
| Timed restrictions | Source-backed behavior and caveats | Payload-specific timing tests, exceptions and rollback |
| Apple School Manager | General source published; selected response checks | Comprehensive review and operational validation |
| Apple Business / legacy ABM | Naming verified | Enrollment, content, accounts, regional features and migration study |
| Jamf Pro | Planned adapter | Product-specific workflows and evaluation |
| Intune | Vendor support reference identified | Apple-specific workflows and evaluation |
| Other MDMs | Discovery registry | Feature, cost, privacy and migration comparison |
| Mac families | Planned second phase | Processor/OS/model-specific enrollment, updates, FileVault and recovery |
| iPhone | Later phase | Connectivity, ownership and iOS-specific workflows |
| AppleCare families | ACE general source and selected response checks | Other plans, country/agreement-specific evidence and operational repair validation |
| Live automation | Architecture contract only | Runtime, credentials custody, API/UI contracts, tests and deployment |

## Labels

- **Planned:** scope accepted; operational guidance incomplete.
- **Vendor-documented:** a linked primary source supports the stated behavior, with retrieval date and limits.
- **Observed:** actual UI/API output in a named authorized environment; does not prove device behavior.
- **Simulated:** a model answered a scenario; does not prove that an API or device action works.
- **Pilot-validated:** a documented task succeeded on identified test hardware and OS with authorization.
- **Operationally validated:** success and recovery verified in an explicitly named deployment scope.

Do not promote an entire product to “supported” because one task was verified. Documentation review dates are not vendor publication dates or guarantees of continued applicability.
