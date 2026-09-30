# CI/CD Fundamentals

CI integrates frequently with automated validation. Continuous delivery keeps software deployable with controlled release; continuous deployment automatically releases validated changes.

Pipeline: source → build → checks → tests → immutable artifact → deploy → verify → observe.

Build once/promote the same artifact where practical. A green pipeline proves only what was tested; production readiness also includes config, migrations, dependencies and observability.
