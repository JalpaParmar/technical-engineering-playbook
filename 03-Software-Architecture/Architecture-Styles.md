# Architecture Styles

**Monolith:** one deployable; operationally simpler and transaction-friendly. Poor internal boundaries—not deployment count—often cause the “big ball of mud.”

**Modular monolith:** one deployable with strong internal boundaries; useful when independent deployment is not justified.

**Microservices:** independent deployment/scaling/ownership can help, but add network failure, distributed data, observability and operational complexity.

Split when a boundary has measurable organizational, scaling, reliability or change value—not because microservices are fashionable.
