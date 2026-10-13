# Agent Security | 威胁模型与安全控制

**Status:** Draft architecture and controls; no penetration-test findings are implied.

## Assets
Model credentials; conversation content; local files; persistent memory; tool permissions; agent runtime; external-system identities; logs and test evidence.

## Trust boundaries
User instruction ↔ lower-trust retrieved content; agent ↔ terminal/file/browser/MCP tools; agent ↔ external APIs; runtime ↔ host; memory ↔ new sessions.

## Risk register starter
| Risk | Possible impact | Proposed control | Evidence to collect | Test |
|---|---|---|---|---|
| Indirect prompt injection | Unauthorized instruction following | Mark source trust; segregate instructions/data; tool authorization | Prompt/tool traces | Benign simulated injection in isolated test |
| Excessive terminal privileges | Unsafe system changes | Least privilege; sandbox; explicit approval | Tool and OS policies | Verify disallowed commands cannot run |
| File/data overreach | Confidential data exposure | Scoped filesystem, secrets handling, egress control | Access policy and redacted logs | Attempt out-of-scope read in lab |
| Memory contamination | Misleading later actions | Memory provenance, write controls, expiry | Memory-write audit | Validate suspicious memory cannot override policy |
| MCP/integration expansion | Enlarged attack surface | Allowlist servers and capabilities, pin/review packages | Dependency inventory | Check default-deny integration |
| Unapproved external action | Irreversible side effect | Approval gate, dry-run, action limits | Approval and execution trace | Verify no action without authorization |

## Acceptance criteria
Each control must name an owner, an enforceable mechanism, reproducible steps, redacted evidence and a recorded residual risk. A policy statement alone is not proof of technical enforcement.

## Boundaries
Only perform adversarial testing in authorized, isolated systems with synthetic data; do not test third-party environments.
