# AI Security, Privacy & Cost

## Security/privacy
Classify data before sending it to a model/provider. Minimize sensitive context, enforce tenant/user authorization before retrieval, constrain tools and protect secrets.

Threats include prompt injection, data exfiltration through tools/context, over-permissioned agents and unsafe generated code/actions.

## Cost
Cost drivers can include input/output tokens, model tier, repeated agent steps, retrieval/reranking and infrastructure.

Optimize after measuring: reduce irrelevant context, cache safe reusable results, choose suitable model/task routing and bound agent loops.

## Principle
Never trade required privacy/security for token savings.
