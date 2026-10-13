# Hermes Agent Security Lab | 实战归档

**Original primary note:** [Hermes-Agent-Security-Baseline-v0.5.md](../Hermes/Hermes-Agent-Security-Baseline-v0.5.md) dated 2026-08-09. Retained unchanged.

## Environment summary
Previous discussion described Nous Research Hermes running in a Linux/container environment with Kimi via a model provider, gateway, dashboard and terminal/file tool capabilities. Internal filesystem locations and live secrets are intentionally excluded from this summary.

## Recorded operational findings
- Legacy WeChat channel configuration was associated with a gateway startup issue; the original baseline records resolution.
- Dashboard/TUI response delivery was problematic even when LLM inference completed; original baseline classifies rendering/response-path investigation separately from model generation.
- Locally configured speech-to-text dependencies were unavailable; unnecessary STT capability was disabled according to the recorded baseline.
- Capability inventory in the August baseline listed terminal and file tools active, and browser/MCP/external messaging disabled. **This is a historical snapshot, not verification of current settings.**

## Assurance lesson
Runtime functionality, control configuration and proof of security are different things. A successful model response cannot show that action authorization, data boundaries or tool containment work.

## Next verification plan
| Workstream | Artifact | Pass condition |
|---|---|---|
| Asset & capability inventory | Versioned sanitized inventory | All tools, channels and model endpoints accounted for |
| Permission matrix | Roles/actions/approval table | Unneeded privileges technically denied |
| Runtime isolation | OS/container evidence | Out-of-scope resources unreachable |
| Prompt/tool boundary | Synthetic adversarial tests | Disallowed side effects blocked |
| Memory & retrieval | Provenance and poisoning tests | Untrusted text cannot silently become policy |
| Supply chain | Dependency and integration review | Reviewed/pinned components and disable-unused evidence |
| Logging | Redacted audit trails | Action origin, decision and outcome traceable |
| Change control | Regression results | Baseline rechecked after changes |

## Evidence handling
Never commit API keys, OAuth tokens, E911 or payment data, environment dumps, personal conversations or private operational hostnames. Use redacted examples only.

## Known limitations
The original v0.5 note is a historical user-authored baseline. Its resolved statuses have not been independently retested as part of this archive.
