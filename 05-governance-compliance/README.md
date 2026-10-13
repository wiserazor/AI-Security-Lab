# Governance & Compliance | 治理、GRC 与 GxP

**Status:** Preliminary crosswalk proposal; not a verified control-by-control mapping or compliance opinion.

## Frameworks in scope
- **NIST AI RMF:** governance, mapping, measuring and management of AI risks.
- **ISO/IEC 42001:** organizational AI management system.
- **ISO/IEC 23894:** guidance on AI risk management.
- **OWASP:** relevant LLM and agentic application threats and mitigations.
- **MITRE ATLAS:** adversarial tactics/techniques for AI-enabled systems.
- **GxP / regulated validation:** intended use, risk-based controls, lifecycle documentation, traceable test evidence and change control.
- **Regulatory research backlog:** EU AI Act and sector-specific FDA/EMA expectations where applicable.

Framework editions, control identifiers and jurisdiction/applicability must be checked before formal adoption.

## Proposed assurance workflow
`Threat → Control → Evidence → Test → Residual Risk`

| Stage | Output | Example |
|---|---|---|
| Threat | Risk scenario tied to assets and intended use | Tool-induced data disclosure |
| Control | Technical and procedural safeguard | Scoped access + approval |
| Evidence | Config, logs, inventories, approvals | Sanitized policy and tool trace |
| Test | Objective test against criterion | Denied out-of-scope access |
| Residual risk | Accepted, mitigated or escalated risk | Remaining indirect-input uncertainty |

## GxP adaptation
Record intended use and system boundaries, data integrity needs, supplier/model dependencies, human oversight, risk-based verification, deviations, change history and periodic review. A safe agent demonstration does not establish GxP validation; validate within the actual regulated process.

## Mapping TODO
Add exact standards editions, clauses, OWASP categories and ATLAS technique identifiers with citations; do not invent one-to-one mappings.
