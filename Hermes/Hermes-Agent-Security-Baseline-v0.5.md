# Hermes Agent Security Baseline v0.5

> Sanitized public edition of a historical 2026-08-09 baseline. Exact infrastructure, service identifiers and private configuration are intentionally omitted. Statuses below were recorded at that time and have not been independently revalidated.

## 1. Purpose

Establish a security baseline for an autonomous agent deployment and evaluate:

- agent security posture;
- configuration management;
- capability control;
- runtime behavior;
- security hardening practices.

## 2. Sanitized environment

| Element | Public description |
|---|---|
| Runtime | Isolated Linux-based environment |
| Agent | Hermes-style agent runtime |
| Model access | External model service through an approved provider configuration |
| Storage | Dedicated application and data areas; exact paths withheld |
| Interfaces | Gateway plus local operator interfaces |

No credentials, endpoint URLs, hostnames, account identifiers or full configuration files are included.

## 3. Historical deployment findings

### HERMES-CONFIG-001 — residual channel configuration

**Symptom:** after an upgrade, the gateway did not start normally.

**Recorded cause:** configuration for an unused messaging channel remained active.

**Recorded remediation:** unused channel configuration was disabled or removed.

**Historical status:** resolved. Current configuration still requires verification.

### HERMES-RUNTIME-001 — response delivery inconsistency

**Symptom:** operator interfaces appeared to remain busy while session history contained a completed assistant response.

**Recorded conclusion:** model inference completed; investigation shifted to the response delivery/rendering path.

**Historical status:** monitoring. This observation did not establish a security impact by itself.

### HERMES-CONFIG-002 — unused speech capability

**Finding:** speech-to-text was enabled while its local dependency was unavailable.

**Risk:** unnecessary dependency, runtime complexity and package supply-chain exposure.

**Recorded remediation:** speech-to-text was disabled because it was not required.

**Historical status:** resolved. Current configuration still requires verification.

## 4. Historical capability snapshot

| Capability group | Historical status |
|---|---|
| Model inference, agent runtime, gateway, local operator interfaces | Enabled |
| Terminal and file tools | Enabled; permission depth not established by this baseline |
| Unused messaging channel, speech features, browser, external tool protocol and outbound messaging | Disabled |

This table is a dated observation, not proof of present-day configuration or effective containment.

## 5. Principles applied

- **Least privilege:** enable only required capabilities.
- **Configuration hygiene:** remove or disable unused integrations.
- **Secure defaults:** external channels remain off until reviewed and authorized.
- **Capability control:** review tool scope, identities and approval requirements before activation.
- **Evidence discipline:** distinguish observed behavior from enforced security controls.

## 6. Findings register

| ID | Finding | Historical severity | Historical status | Required revalidation |
|---|---|---:|---|---|
| HERMES-CONFIG-001 | Residual unused-channel configuration | Medium | Resolved | Current channel inventory and startup test |
| HERMES-CONFIG-002 | Unused speech capability and missing dependency | Low | Resolved | Current capability and dependency inventory |
| HERMES-RUNTIME-001 | Response delivery/rendering inconsistency | Low | Monitoring | Correlated end-to-end event trace |

## 7. Hardening backlog

1. Produce a versioned asset and capability inventory.
2. Define a tool permission and approval matrix.
3. Verify terminal, filesystem, identity and network boundaries.
4. Test prompt/tool separation with synthetic data in an isolated lab.
5. Evaluate memory and retrieval provenance before enabling persistence.
6. Review integrations and dependencies for supply-chain risk.
7. Retain redacted evidence and rerun regression tests after changes.

## 8. Evidence limitation

A successful model response does not prove that tool authorization, data boundaries, logging or containment work. Each claim should follow:

`Threat → Control → Evidence → Test → Residual Risk`

See [Hermes historical findings and verification backlog](../06-hermes-lab/Hermes-Historical-Findings-and-Verification.md) for the current public follow-up.
