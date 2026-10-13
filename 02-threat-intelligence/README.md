# AI Threat Intelligence | 威胁情报与可信度

**Historical discussion:** 2026-09-12, review of an Anthropic September 2026 threat-intelligence report. **Caution:** title, report URL, case specifics and any independent corroboration must be rechecked against primary sources before citation in publication.

## Evidence taxonomy / 证据分层
1. **Direct platform observation:** telemetry/activity a platform operator can actually see; strongest for activity within that platform, not automatically for real-world outcomes.
2. **Technical inference:** deductions from patterns, tooling and behavior; record alternative explanations.
3. **Threat actor attribution:** identity or affiliation claims; require independent corroboration and explicit confidence.
4. **Real-world impact:** distinguish prototype, trial, attempted misuse, deployed activity and confirmed consequences.

## Prior assessment / 既有讨论结论
The earlier conversation treated the report as likely authentic but warned that underlying incidents, actor attribution and downstream effects cannot all be independently verified without raw evidence. A described pilot-stage surveillance scenario did **not** establish deployment against real targets; avoid repeating such claims as fact.

## Proposed analysis template
| Field | Required question |
|---|---|
| Source | Primary report, edition, date, immutable URL? |
| Observation | What did the platform directly observe? |
| Inference | What was inferred rather than observed? |
| Attribution | Who was blamed and with what confidence? |
| Impact | Confirmed outcome or untested hypothetical? |
| Counterevidence | Independent reporting or conflicting findings? |
| Controls | Relevant identity, tool, monitoring and data controls? |
| Verification | What would falsify the conclusion? |

## Application to agents
Use the chain `Threat → Control → Evidence → Test → Residual risk`; keep evidence limitations visible in the final risk register.

## Source-validation backlog
Locate the exact September 2026 Anthropic report and dated independent coverage; cross-check named incidents and preserve source URLs rather than relying on secondary recollection.
