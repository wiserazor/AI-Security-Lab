\# Hermes Agent Security Baseline v0.5



\## 1. Project Overview



Project:

AI-Security-Lab



Component:

Nous Research Hermes Agent



Purpose:



Establish a secure baseline for an autonomous AI Agent deployment and evaluate:

\- Agent security posture

\- Configuration management

\- Capability control

\- Runtime behavior

\- Security hardening practices





\---



\# 2. Environment



\## Platform



Operating System:

Linux Container Environment



Deployment Path:

/opt/Hermes





Data Path:

/opt/data







\## Model Configuration



LLM:

kimi-k3





Provider:

kimi-coding-cn





API Endpoint:

https://api.moonshot.cn/v1







\---



\# 3. Initial Deployment Findings



\## 3.1 Gateway Startup Failure



\### Symptom



After Hermes upgrade, Gateway failed to start.





\### Root Cause



Legacy WeChat channel configuration remained active.



Configuration source:

Status:



Resolved





\---



\# 4. Agent Runtime Investigation



\## Symptom



User interaction did not receive immediate response.



Observed:



\- Dashboard chat appeared stuck

\- TUI appeared processing

\- Session history contained assistant responses





\## Investigation Result



LLM inference completed successfully.





Evidence:



Turn ended:

reason=text\_response(finish\_reason=stop)





Conclusion:



Agent runtime and model inference were healthy.



Issue was related to response delivery/rendering path.





\---



\# 5. STT / Voice Capability Hardening





\## Finding



Voice and Speech-To-Text capability was enabled but dependencies were unavailable.





Configuration before:





```yaml

stt:

&#x20; enabled: true

&#x20; provider: local

Runtime error:

Lazy-installing faster-whisper failed



STT provider 'local' configured but unavailable

Risk

Unnecessary capability increased:

Dependency attack surface

Runtime complexity

Package supply-chain risk

Remediation

Configuration changed to:

stt:

&#x20; enabled: false

&#x20; provider: local

Status:

Resolved

6\. Current Capability Baseline

Enabled

Capability	Status

LLM inference	Enabled

Agent Runtime	Enabled

Gateway	Enabled

Dashboard	Enabled

TUI	Enabled

Terminal Tool	Enabled

File Tool	Enabled





Disabled

Capability	Status

WeChat Channel	Disabled

STT	Disabled

Wake Word	Disabled

Browser	Disabled

MCP	Disabled

External Messaging	Disabled





7\. Security Principles Applied

Least Privilege

Only required capabilities are enabled.

Configuration Hygiene

Unused integrations are disabled.

Secure Default

External channels are not enabled unless explicitly required.

Capability Control

Agent tools are reviewed before activation.

8\. Security Findings Register

ID	Finding	Severity	Status

HERMES-CONFIG-001	Residual WeChat configuration	Medium	Resolved

HERMES-CONFIG-002	STT enabled without dependencies	Low	Resolved

HERMES-RUNTIME-001	Response rendering issue investigation	Low	Monitoring





9\. Future Hardening Roadmap

Phase 1

Completed:

Secure deployment baseline

Channel review

Capability reduction

Phase 2

Planned:

Tool permission matrix

Terminal security assessment

Memory security testing

Prompt injection testing

MCP security evaluation

Agent threat modeling

Version History

v0.5

Date:

2026-08-09

Changes:

Initial Hermes security baseline

Gateway recovery documentation

Configuration hardening record

