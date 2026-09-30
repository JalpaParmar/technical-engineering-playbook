# AI-Assisted Incident Analyzer — Design

## Inputs
Incident description, timestamps, release/config changes, logs, stack traces, metrics, traces, API errors and affected cohorts.

## Output
1. observed facts;
2. impact/scope;
3. missing evidence;
4. ranked hypotheses **clearly labeled hypotheses**;
5. safe diagnostic steps;
6. mitigation options and risks;
7. owner/escalation suggestions;
8. communication draft;
9. RCA skeleton after evidence exists.

## Guardrails
Never promote correlation to root cause. Redact secrets/PII. Do not recommend destructive production actions without explicit validation/approval. Preserve human incident ownership.
