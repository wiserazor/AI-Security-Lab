# AI Security Lab | AI Agent Security & Assurance Research

> Research archive updated 2026-10-13 | 研究档案（持续迭代）

This repository consolidates prior work on **Agent Security, AI Assurance, Evaluation, Threat Intelligence, Governance and the Hermes Agent lab**. 研究内容明确区分历史观察、历史讨论、设计方案与待验证结论。

## Start here / 从这里开始

1. **[Detailed research retrospective (Aug–Oct 2026)](00-research-retrospective/Research-Retrospective-2026-08-to-10.md)** — 历史讨论时间线、研究方法、遗漏内容及证据状态
2. **[Agent Threat Model v0.1](03-agent-security/Agent-Threat-Model-v0.1.md)** — 资产、威胁边界、风险场景及控制设计
3. **[Agent Tool Permission Matrix](03-agent-security/Agent-Tool-Permission-Matrix.md)** — 工具能力、默认权限、审批和审计证据
4. **[AI Agent Assurance Framework v0.1](04-ai-assurance/Assurance-Framework-v0.1.md)** — Threat → Control → Evidence → Test → Residual Risk
5. **[Hermes Findings & Verification Backlog](06-hermes-lab/Hermes-Historical-Findings-and-Verification.md)** — 历史发现与待验证的加固工作

## Domains / 研究目录

| Domain | Focus | Key files |
|---|---|---|
| [00-research-retrospective](00-research-retrospective/Research-Retrospective-2026-08-to-10.md) | Research chronology and recovered decisions | Research-Retrospective-2026-08-to-10.md |
| [01-foundations](01-foundations/README.md) | Trust boundaries, architecture, attack surfaces | README.md |
| [02-threat-intelligence](02-threat-intelligence/README.md) | Observation, inference and attribution evidence | README.md |
| [03-agent-security](03-agent-security/README.md) | Threat modeling, tool authorization, least privilege | Threat Model; Permission Matrix |
| [04-ai-assurance](04-ai-assurance/README.md) | Evidence-based assurance and evaluation design | Assurance Framework; Evaluation Notes |
| [05-governance-compliance](05-governance-compliance/README.md) | NIST, ISO, OWASP, MITRE and GxP research | [Control Crosswalk](05-governance-compliance/Control-Crosswalk-Template.md) |
| [06-hermes-lab](06-hermes-lab/README.md) | Hermes security lab, historical lessons, verification | Findings and Verification |
| [07-roadmap](07-roadmap/README.md) | Research and skills roadmap | README.md |
| [Hermes](Hermes/Hermes-Agent-Security-Baseline-v0.5.md) | Original baseline preserved as-is | Hermes Agent Security Baseline v0.5 |

## Research methodology / 研究方法

**Original research flow:** `Agent Inventory → Threat Model → OWASP Test Matrix → Enterprise Control Mapping → Assurance Report`

**Traceability chain:** `Threat → Control → Evidence → Test → Residual Risk`

Distinguish policy statements from enforced guardrails; agent model responses from downstream tool actions; demonstration from reproducible verification; model safety from security and regulated assurance.

## Source & evidence policy

- **Historical observed:** a recorded prior finding; may be stale and has not automatically been retested.
- **Discussion:** conversation or academic-visit synthesis; source references to be validated.
- **Design/proposal:** draft threat models, controls and tests; not deployed controls.
- **TODO verify:** missing primary publication, current version, regulatory applicability or independent result.
- Do not commit secrets, complete private configurations, personally identifying information or unsafe operational detail.
- **This is not a claim of certification, completed penetration testing or GxP validation.**

## Research origin and limitation

Research discussions began in August 2026. Original v0.5 baseline dated 2026-08-09. A shared ChatGPT conversation ([reference](https://chatgpt.com/share/6ace317a-7b98-83ea-9941-139878317d40)) was supplied for reconciliation, but automated retrieval of the full shared-chat body was unavailable on 2026-10-13. The retrospective is a best-effort reconstruction from available conversation context and repo artifacts, **not a verified complete export**.

## Next deliverables / 下一步

- Validate primary source references and exact standard editions/clauses.
- Inventory current Hermes settings and prove enforced permissions with redacted evidence.
- Implement an authorized, synthetic-data test suite and structured findings register.
- Produce a version-scoped Assurance Report with limitations, residual risk and change-control rules.
