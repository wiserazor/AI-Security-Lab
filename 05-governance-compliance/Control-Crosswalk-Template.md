# Control Crosswalk / 标准控制映射模板

**Status:** [DESIGN]. No exact clause identifiers are asserted without checking official current editions.

| Control family | Agent-specific requirement | Candidate reference families | Evidence sought |
|---|---|---|---|
| Governance & accountability | Intended use, owners and human oversight | NIST AI RMF, ISO/IEC 42001 | Governance record, approvals |
| Risk analysis | Agents, tools and environment threat modeling | ISO/IEC 23894, NIST AI RMF, OWASP | Risk register, DFD |
| Identity & access | Scoped tool auth and least privilege | OWASP, enterprise IAM controls | Permission matrix, deny tests |
| Data & secrets | Controlled file/memory/credential handling | OWASP, GxP data integrity | Redacted technical configuration |
| Adversarial evaluation | Repeatable prompt/tool safety tests | MITRE ATLAS, OWASP, NIST AI RMF | Test cases, run traces |
| Auditability | Event provenance, approvals, changes | ISO/IEC 42001, GxP lifecycle | Version history and logs |
| Lifecycle assurance | Reassessment after model/tool updates | ISO/IEC 42001, NIST AI RMF | Release/retest record |

## Research method
1. Record **standard name, edition, exact official source and applicability**.
2. Identify normative text versus informative guidance.
3. Translate intended use into a testable organization-level requirement.
4. Link one risk scenario to control, implementation, test and retained evidence.
5. Review gaps, compensating controls and responsible acceptance.
6. Revisit crosswalk when standards, tools or regulations change.

## GxP applicability note
Validation is contextual to regulated activities and quality systems. An agent security control map alone never proves GxP compliance.
