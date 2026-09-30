# Guardrails & Human Review

## Before AI coding
Define scope, allowed files, acceptance criteria, test commands and prohibited changes.

## After
Inspect diff, compile/build, run tests/static/security checks, verify behavior and review generated dependencies/config.

## Sensitive code/data
Follow organizational policy. Do not paste secrets, production credentials or restricted customer data into unapproved tools.

## Agent actions
Use least privilege and approvals for merges, deployments, destructive DB/file operations and external communications.
