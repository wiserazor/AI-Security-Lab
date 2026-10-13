# Foundations | AI Agent Security 基础

**Status:** Discussed concepts; not a completed curriculum.

## Agent versus LLM security
A language model generates outputs; an agent may also select tools, read files, remember context and initiate actions. Risk therefore extends beyond answer quality into authorization, data access and side effects.

## System boundary / 系统信任边界

`User → Agent / LLM → Tools → Data → External systems → Actions`

Inspect transitions at each edge: instruction source, identity, tool privilege, input provenance, network destination, data sensitivity, action approval and auditability.

## Working taxonomy
- **Instruction/data confusion:** lower-trust content tries to act as a higher-priority instruction.
- **Excessive tool agency:** tools are available with broader privileges than the task needs.
- **Sensitive information exposure:** outputs, logs, retrieval results or external tools leak data.
- **Memory or retrieval contamination:** persistent or retrieved materials affect future decisions.
- **Indirect action risk:** seemingly benign requests trigger downstream tool side effects.
- **Evaluation gaps:** hallucination, fabricated evidence and benchmark overfitting escape detection.

## Baseline principles
Least privilege; isolated runtime; limited capabilities; human confirmation for consequential actions; logging and traceability; controlled change management; repeatable testing; independent review.

## Open questions
What are the actual trust boundaries and allowed actions for the deployed Hermes instance? Which permissions are enforced technically rather than just prompted? What evidence would demonstrate containment?
