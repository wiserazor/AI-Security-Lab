# AI Evaluation, Human Feedback and Benchmark Research Notes

**Source class:** [DISCUSSION], discussions during September–October 2026 academic visits; confirm paper bibliographies before citing externally.

## Human evaluation
RLHF and preference learning depend on the evaluator population, annotation criteria and context; different valid preferences may produce disagreement. Sampled human review gives evidence only about the reviewed sample and sampling method. Reliability should not be reduced to a single aggregate score.

## Error asymmetry
False-positive and false-negative costs differ by use case (e.g., image triage vs low-consequence consumer assistance). Design thresholds and human escalation around intended use, severity and reversibility, rather than optimizing a universal accuracy target.

## AI cheat and benchmark gaming
The UCLA discussion emphasized repeated benchmarking, reference targets and ongoing checks of model behavior. But repeated optimization against a visible benchmark risks overfitting. Use held-out sets, independent evaluators, versioned protocols and adversarially diverse task families.

## Proposed evaluation card
| Field | Record |
|---|---|
| Claim | Precise behavior under test |
| Model/agent version | Immutable or uniquely identified build |
| Scenario distribution | Benign, ambiguous, adversarial, edge cases |
| Measures | Success, unauthorized action rate, recall/precision, unsupported statements |
| Ground truth | Human rubric and independent review |
| Limits | Coverage, uncertainty, false positive/negative cost |
| Regression gate | Decision before release / after change |

## Research questions
Can policy enforcement be tested separately from fluent refusal? What evaluation scenarios reproduce multistep tool side effects? How should human-review spend vary with severity?

## Associated research pointer
A research paper shared after UCLA discussion: https://arxiv.org/abs/2609.13009 . Its exact bibliographic metadata and relevance require direct verification before quotation.
