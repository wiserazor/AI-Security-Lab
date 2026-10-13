# AI Assurance & Evaluation | 评估、基准与可靠性

**Status:** Notes from discussions and academic visits; no published experiment is claimed.

## Topics discussed
- RLHF and human evaluation: preference heterogeneity, limited sampled evaluation coverage and evolving policies.
- False positives and false negatives: different costs for different use cases, including clinical-imaging examples.
- Risk-tiered evaluation: stronger evidence and tighter thresholds for high-consequence actions.
- Performative prediction: deployment and behavioral feedback can change the distribution being measured.
- Evaluation economics: connect monitoring effort and tolerance to consequence, likelihood and risk reduction.

## UCLA world-model / AI-cheat discussion (2026-10)
A visiting expert described a benchmark-based approach: construct reference tasks, iteratively strengthen/evaluate open models and compare outputs to the benchmark in order to reduce hallucination or cheating behavior. The discussion also raised benchmark gaming and the need for independent re-validation. This is a **discussion summary**, not a claim that any particular method has proven to eliminate failures.

Working loop: `Ground-truth benchmark → Adversarial evaluation → Iterative improvement → Independent re-validation`.

## Experimental design proposal
1. Specify target agent behavior and failure taxonomy.
2. Create held-out cases spanning ordinary, ambiguous and adversarial inputs.
3. Define measurable metrics: task completion, unsafe tool-call rate, unsupported-claim rate, detection precision/recall and human review effort.
4. Log model/version, prompts, tools, policies, seeds where applicable and environment.
5. Evaluate both false-positive and false-negative costs.
6. Retest after changes; separate development tests from hidden holdouts.
7. Report uncertainty, limitations and evidence quality.

## Research questions
How can an agent detect that it is optimizing the benchmark rather than the real objective? How do we assess multi-step side effects rather than only individual model outputs? What evidence is enough for regulated use?
