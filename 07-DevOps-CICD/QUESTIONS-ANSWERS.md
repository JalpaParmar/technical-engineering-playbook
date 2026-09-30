# DevOps / CI-CD Q&A

**CI vs CD?** CI validates integration; continuous delivery keeps changes deployable; continuous deployment automatically releases validated changes.

**Blue/green vs canary?** Blue/green switches environments; canary gradually exposes traffic. Data/state complicate both.

**Why build once?** Promote the tested immutable artifact to reduce drift.

**Self-hosted runner risk?** You own patching, isolation, credentials and compromise containment.

**TPM metrics?** Feedback time, flaky/failed gates, release/deployment failures, recovery, environment drift, dependency readiness and production outcomes.
