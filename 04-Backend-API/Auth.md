# Authentication & Authorization

Authentication asks who the principal is; authorization asks whether that principal may act on a resource.

JWT is a token format, not an authentication architecture. OAuth is primarily authorization delegation; OpenID Connect adds identity semantics. Verify current standards/provider guidance for exact flows.

Server operations must enforce authorization; hiding a client button is not security. Preserve tenant context and least privilege.
