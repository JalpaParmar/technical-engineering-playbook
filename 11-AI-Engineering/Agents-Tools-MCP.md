# Agents, Tools & MCP

## Tool-using systems
A model can decide/request structured tool calls to search, calculate, read data or perform permitted actions. The application remains responsible for permissions, validation and side-effect control.

## Agent
Useful when a task requires iterative planning/tool use/state. Do not use an agent where a deterministic workflow is simpler.

## MCP
Model Context Protocol provides a standardized way for AI applications to connect to tools/context providers. Treat connected tools as capability/security boundaries.

## Guardrails
Least privilege, explicit approval for consequential actions, idempotency, audit trail, bounded loops, time/cost limits and validation of tool arguments/results.
