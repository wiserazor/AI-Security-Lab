# AI Security Lab | AI Agent Security & Assurance Research

> Research archive updated 2026-10-13 | 研究档案（持续迭代）

This repository consolidates work on **Agent Security, AI Assurance, Evaluation, Threat Intelligence, Governance and the Hermes Agent lab**. It distinguishes historical observations, discussion summaries, design proposals and verified evidence.

## Start here / 从这里开始

1. **[Research retrospective](00-research-retrospective/Research-Retrospective-2026-08-to-10.md)** — research chronology, lessons and evidence status
2. **[Agent Threat Model v0.1](03-agent-security/Agent-Threat-Model-v0.1.md)** — assets, trust boundaries, threat scenarios and controls
3. **[Agent Tool Permission Matrix](03-agent-security/Agent-Tool-Permission-Matrix.md)** — default access, approval and evidence requirements
4. **[Authorized Test Playbook](03-agent-security/Authorized-Test-Playbook.md)** — isolated synthetic test matrix and result template
5. **[AI Agent Assurance Framework v0.1](04-ai-assurance/Assurance-Framework-v0.1.md)** — `Threat → Control → Evidence → Test → Residual Risk`
6. **[Evidence Pack Template](04-ai-assurance/Evidence-Pack-Template.md)** — claim, evidence, evaluation and residual-risk registers
7. **[Hermes verification backlog](06-hermes-lab/Hermes-Historical-Findings-and-Verification.md)** — historical findings and revalidation work
8. **[Publication Safety](PUBLICATION-SAFETY.md)** — mandatory public redaction and evidence-handling rules

## Domains / 研究目录

| Domain | Focus | Key artifacts |
|---|---|---|
| [00-research-retrospective](00-research-retrospective/Research-Retrospective-2026-08-to-10.md) | Research chronology and recovered decisions | Retrospective |
| [01-foundations](01-foundations/README.md) | Trust boundaries, architecture and attack surfaces | Foundations notes |
| [02-threat-intelligence](02-threat-intelligence/README.md) | Observation, inference and attribution evidence | Analysis template |
| [03-agent-security](03-agent-security/README.md) | Threat modeling, tool authorization and least privilege | Threat model, permission matrix, test playbook |
| [04-ai-assurance](04-ai-assurance/README.md) | Evidence-based assurance and evaluation design | Assurance framework, evidence pack |
| [05-governance-compliance](05-governance-compliance/README.md) | NIST, ISO, OWASP, MITRE and GxP research | [Control crosswalk](05-governance-compliance/Control-Crosswalk-Template.md) |
| [06-hermes-lab](06-hermes-lab/README.md) | Sanitized lab lessons and verification | Findings backlog |
| [07-roadmap](07-roadmap/README.md) | Research and skills roadmap | Prioritized backlog |
| [Hermes](Hermes/Hermes-Agent-Security-Baseline-v0.5.md) | Sanitized historical baseline | Baseline v0.5 |

## Methodology / 研究方法

**Assessment flow:** `Agent Inventory → Threat Model → Test Matrix → Enterprise Control Mapping → Assurance Report`

**Traceability:** `Threat → Control → Evidence → Test → Residual Risk`

Key distinctions:

- policy statements versus technically enforced guardrails;
- model responses versus downstream tool effects;
- demonstrations versus reproducible verification;
- model quality/safety versus system security and regulated assurance.

## Evidence policy

- **Historical observed:** recorded previously; potentially stale until revalidated.
- **Discussion:** synthesis from earlier research conversations.
- **Design/proposal:** draft method, control or test; not a deployed safeguard.
- **TODO verify:** missing primary source, current version, applicability or independent result.

Do not commit secrets, complete private configurations, personal data, private conversation links or sensitive operational details. Use synthetic inputs and sanitized evidence. This archive does **not** claim certification, completed penetration testing or GxP validation.

## Next deliverables / 下一步

- Validate primary sources and exact standards editions/clauses.
- Inventory the current agent configuration and prove enforced permissions with redacted evidence.
- Implement the authorized synthetic-data tests and structured findings register.
- Produce a version-scoped assurance report with limitations, residual risk and change-control rules.
