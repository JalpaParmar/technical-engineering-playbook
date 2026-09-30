# Deployment Strategies

**Rolling:** gradual instance replacement; mixed versions coexist.

**Blue/green:** old/new environments then traffic switch; fast mitigation but infrastructure/data concerns.

**Canary:** expose a subset, compare signals, expand/abort.

**Feature flags:** separate deployment/exposure but add state combinations and cleanup.

For DB changes, backward-compatible expand → migrate → contract can reduce deployment coupling. Data changes may not be reversible.
