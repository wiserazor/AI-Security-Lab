# Agent Tool Permission & Approval Matrix / 工具权限与审批矩阵

**Status:** [DESIGN] template derived from Hermes hardening discussion. This is a **proposed policy**, not observed live settings.

| Capability | Default proposal | Scope | Approval condition | Required evidence |
|---|---|---|---|---|
| LLM inference | Enabled | Approved model/provider | Model/provider changes | Sanitized config version |
| Terminal | Restricted | Isolated non-privileged environment | Write or system-changing commands | OS policy + denied-action test |
| Read files | Restricted | Designated work area | Access outside assigned workspace | Mount/policy + trace |
| Write files | Restricted | Test output only | Destructive or external changes | Before/after diff + approval |
| Browser/retrieval | Disabled unless needed | Allowed sources | New domains or authenticated actions | Policy, destination log |
| Memory | Disabled until evaluated | Named/test memory store | Persistent policy-relevant writes | Attribution and replay check |
| MCP | Disabled unless reviewed | Allowlisted trusted servers | Adding/changing server | Server inventory and review |
| External messaging | Disabled by default | Explicitly authorized destination | Every external transmission | Approval and delivery record |
| Speech-to-text | Disabled when unused | None | Enable only after dependency review | Capability inventory |
| Secrets access | Never through general workspace | Dedicated secret mechanism | Provision/rotate credential | Sanitized access evidence |

## Approval model
Classify operations as **observe**, **draft**, **modify**, **transmit** and **destructive**. Approval decisions should occur outside prompt text when feasible; policy should be enforced by tool broker and system boundaries.

## Evidence fields
Policy identifier, environment/version, reviewer, date, action, actor, requested resource, allow/deny decision, tool execution result, redaction state and residual risk.

## Non-goals
Do not publish real keys, authorization tokens or internal-only system details in the public repo.
