# Public Research & Sanitization Policy

This repository is public. Publish reusable security knowledge, not operational secrets.

## Classification before publication

| Class | Examples | Public handling |
|---|---|---|
| Public research | Threat models, generic control patterns, synthetic test cases | Publish with sources and limitations |
| Sanitized evidence | Redacted screenshots, policy excerpts, summarized test traces | Publish only after review |
| Internal operations | Exact paths, hostnames, tenant IDs, account names, private workflow details | Generalize or omit |
| Secrets | API keys, tokens, cookies, private keys, recovery codes | Never commit; revoke if exposed |
| Personal or regulated data | Names, contact data, conversations, patient/customer records | Never use; replace with synthetic data |

## Required review

Before committing, check the staged content and rendered Markdown for:

- credentials and secret-like strings;
- private URLs, IP addresses, hostnames, filesystem paths and service identifiers;
- personal names, email addresses, conversation links and account metadata;
- complete configuration dumps, logs or screenshots;
- internal incident timelines, vendor relationships or operating procedures that are not already public;
- claims of compliance, certification or successful security testing without evidence.

## Redaction rules

1. Replace exact infrastructure with role-based labels such as `<agent-runtime>`, `<model-endpoint>` and `<workspace>`.
2. Preserve the security lesson, control decision, evidence type and test outcome.
3. Do not mask only part of a live secret. Remove it completely and rotate it.
4. Prefer synthetic examples over altered real records.
5. Keep dates only when they support version history and do not expose private operations.
6. Record evidence provenance without publishing private source conversations.

## Public evidence format

For each result, publish only:

- test ID and objective;
- sanitized environment/version;
- preconditions and synthetic input;
- expected and actual behavior;
- pass/fail decision;
- redacted evidence reference;
- limitation and residual risk.

Raw evidence remains outside the public repository under the owner's approved retention and access controls.

## If exposure is suspected

Stop further publication, remove the material from the active change, rotate affected credentials, assess repository history and access logs, and document the response privately. Deleting a file in a later commit does not remove it from Git history.
