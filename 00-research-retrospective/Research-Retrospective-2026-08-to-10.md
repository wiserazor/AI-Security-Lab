# AI Agent Security & Assurance — Research Retrospective / 研究复盘

**Updated:** 2026-10-13  
**Evidence status:** reconstructed from the repository's historical Hermes baseline and limited prior-conversation context. Private conversation links and operational identifiers are excluded. This is **not** a verbatim or exhaustive transcript.

## Executive summary / 核心结论

The research evolved from general AI security learning toward a practical **AI Agent Assurance** portfolio: assess an agent as a system with tools and side effects, build an inventory and threat model, derive authorized tests, map controls to evidence, and produce a qualified assurance report.

### Recovered assessment pipeline

`Agent Inventory → Threat Model → Test Matrix → Enterprise Control Mapping → Assurance Report`

### Deliverables identified

1. AI governance and risk framework
2. AI agent risk register
3. System and data-flow threat model
4. Authorized red-team/evaluation playbook
5. Reproducible evaluation pipeline
6. Regulated-systems extension
7. Sanitized security baseline and evidence pack

## Research chronology

| Period | Research thread | Contribution | Evidence quality |
|---|---|---|---|
| 2026-08 | Direction and baseline | AI Assurance focus; agent system selected as an assessment object; initial capability and runtime notes | Historical repository artifact and summarized context |
| 2026-09 | Threat intelligence | Separate platform observation, inference, attribution and confirmed impact | Discussion summary; sources require verification |
| 2026-09 to 2026-10 | Evaluation | Human-evaluator disagreement, false-positive/negative cost, benchmark gaming and independent revalidation | Discussion summary; primary literature requires verification |
| 2026-10 | Consolidation | Research domains, threat model, permission matrix and assurance framework | Current repository artifacts |

## Key lessons

- Agent risk is not limited to model output; it includes tools, identities, files, memory, external systems and side effects.
- Policy text and model refusal are weaker evidence than controls enforced by an independent boundary.
- A completed model inference does not prove end-to-end response delivery or safe action execution.
- Human approval should be tied to consequential operations and backed by technical enforcement and audit evidence.
- Threat intelligence must separate direct observation from inference, attribution and verified real-world impact.
- AI safety evaluation, cybersecurity assessment and regulated assurance share evidence discipline but have different acceptance criteria.
- Public documentation should retain methods and lessons while omitting credentials, exact infrastructure and private operational history.

## Research maturity

**Available:** historical sanitized baseline; threat categories; assessment workflow; draft permission matrix; assurance claim structure; reusable test and evidence templates.

**Not demonstrated:** current runtime verification; completed executable test suite; independently reproduced attacks or defenses; verified clause-by-clause standards mapping; external peer review; certification; regulated-process validation.

## Evidence labels

- **[OBSERVED-HISTORICAL]:** recorded in a dated artifact but not freshly verified.
- **[DISCUSSION]:** conclusion summarized from earlier conversation.
- **[DESIGN]:** proposed method, control or test.
- **[TODO-VERIFY]:** source, implementation or result still requires validation.

## Publication boundary

No private conversation URL is used as evidence in this public archive. Future additions should cite public primary sources where possible and follow [PUBLICATION-SAFETY.md](../PUBLICATION-SAFETY.md). Operational evidence should be retained privately and represented here only through reviewed, synthetic or redacted artifacts.
