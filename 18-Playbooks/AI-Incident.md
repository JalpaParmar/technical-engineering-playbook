# AI Feature Incident Playbook

## Trigger
Material incorrect output, data exposure risk, unsafe tool action, retrieval failure or severe cost/latency regression.

## Stabilize
Disable/limit affected feature or tool permissions where safe. Protect data first.

## Investigate
Model/prompt/version, retrieval corpus/index, authorization filters, tool calls, configuration, recent deployment and representative failed examples.

## Important
Separate model generation failure from retrieval, application logic and tool/backend failure.

## Recover
Validate with targeted evals plus production signals before restoring exposure. Add failed cases to regression evaluation where appropriate.
