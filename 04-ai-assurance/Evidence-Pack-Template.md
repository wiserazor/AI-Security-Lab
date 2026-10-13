# AI Agent Assurance Evidence Pack Template

**Status:** reusable design artifact; completion does not by itself establish certification or regulatory conformity.

## 1. Scope and intended use

- System and release:
- Assessment date:
- Intended users and decisions:
- Allowed actions:
- Explicitly prohibited actions:
- Environment boundary:
- Out-of-scope dependencies:
- Assurance owner and reviewers:

## 2. Inventory

Record model/provider role, orchestrator, tools, identities, data stores, memory, retrieval, integrations, network destinations and logging. Use generic identifiers in the public version; retain exact configuration in controlled evidence storage.

## 3. Claim register

| Claim ID | Qualified claim | Threat | Enforced control | Evidence | Test | Result | Residual risk |
|---|---|---|---|---|---|---|---|
| C-001 | Consequential actions require authorization in the assessed release | Unauthorized side effect | Independent approval gate | Redacted policy + trace | AUTH-01 | | |
| C-002 | File access is confined to the assigned workspace | Data overreach | Scoped mount/access policy | Sanitized policy + deny event | FILE-01 | | |
| C-003 | Unapproved destinations cannot receive agent data | Data exfiltration | Egress allowlist | Sanitized rule + deny event | EGRESS-01 | | |

Claims must be bounded by version, environment and use case. “The agent is secure” is not a testable claim.

## 4. Evidence register

| Evidence ID | Type | Source/owner | Version/time | Integrity method | Redaction review | Retention |
|---|---|---|---|---|---|---|
| EV-001 | Policy excerpt | | | Hash/signature or controlled repository | | |
| EV-002 | Tool trace | | | Correlated event IDs | | |
| EV-003 | Negative test result | | | Test-run manifest | | |

## 5. Evaluation summary

Report sample design, held-out cases, ordinary/ambiguous/adversarial coverage, task success, unsafe tool-call rate, denied-action accuracy, unsupported-claim rate, false positives, false negatives, human-review effort and uncertainty. Separate development results from independent re-validation.

## 6. Deviations and limitations

List missing telemetry, untested tools, external dependencies, blocked tests, changes after testing and evidence that could not be made public. Explain how each limitation constrains the claims.

## 7. Residual-risk decisions

| Risk ID | Remaining exposure | Likelihood/impact rationale | Decision | Owner | Review trigger |
|---|---|---|---|---|---|
| | | | Accept / mitigate / avoid / transfer | | |

## 8. Change and regression triggers

Reassess after changes to models, system prompts, tools, permissions, connectors, memory/retrieval, dependencies, runtime images, identity scopes, egress policy or intended use.

## 9. Public release checklist

- All evidence is synthetic or approved and redacted.
- No secrets, personal data, private URLs, exact internal paths or service identifiers remain.
- Source claims have primary references or are labeled for verification.
- Observations, inferences and proposals are clearly distinguished.
- Compliance and certification language is appropriately qualified.
- Links render and point only to intended public resources.
