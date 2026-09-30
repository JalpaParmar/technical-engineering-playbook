# Git, PRs & Code Review

Choose branching based on release/team constraints. Short-lived branches reduce integration drift; some environments need additional release controls.

## Review priority
1. correctness/business behavior;
2. security/data integrity;
3. concurrency/failure;
4. architecture/maintainability;
5. tests;
6. observability;
7. readability/style.

Automate formatting where possible. Prefer evidence-based questions: “What happens if this request retries after the server commits?”

CI passing is necessary, not sufficient for high-risk releases.
