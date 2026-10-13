# Hermes — Historical Findings and Verification Backlog

**Source:** [OBSERVED-HISTORICAL] original 2026-08-09 v0.5 GitHub baseline, augmented by recovered prior-conversation summaries. Status below refers to historical notes, **not** independently confirmed October runtime.

| ID | Recorded issue | Historic disposition | Verification needed |
|---|---|---|---|
| HERMES-CONFIG-001 | Leftover WeChat channel configuration associated with Gateway startup issue | Marked resolved | Inventory all channel-related keys and current startup behavior |
| HERMES-CONFIG-002 | STT enabled while local speech dependency unavailable | Marked resolved (feature disabled) | Check actual config and package inventory |
| HERMES-RUNTIME-001 | Model output completed but Dashboard/TUI response delivery inconsistent | Monitoring | Correlate end-to-end event IDs and delivery logs |

## Historical capability inventory
Original v0.5 listed **enabled:** LLM inference, Agent Runtime, Gateway, Dashboard, TUI, Terminal Tool, File Tool.
It listed **disabled:** WeChat, STT, Wake Word, Browser, MCP, External Messaging.
Previous conversation recollection additionally mentions Memory as disabled; because Memory is not in the current GitHub v0.5 capability table, its status is **unverified** pending current configuration inspection.

## Key technical insight
A successful model invocation with a completed response does not prove that Dashboard or TUI propagated the reply. Likewise, disabled optional components reduce attack surface but are not comprehensive evidence of tool isolation or prompt-injection resistance.

## Testing work packages
- **Inventory:** agent version, channel list, integrations, all tools, config source, dependency versions.
- **Boundary verification:** minimal OS identity, workspace confinement, egress scope, secret-injection method.
- **Control verification:** approval for side-effecting operations, audit completeness, deny tests.
- **Resilience:** gateway recovery, error handling, log traceability and availability.
- **Security evaluation:** synthetic-data indirect prompt-injection and memory contamination scenarios in an isolated environment.
- **Regression:** rerun on provider, image, tool or configuration changes.

## Public documentation boundary
Use only sanitized snippets. Do not publish full environment files, tokens, personal information, security-sensitive exact host details or live service identifiers.

## Source reconciliation
Do not retroactively modify historical baseline statuses. Store new findings as dated appendices with evidence links and explicit test results.
