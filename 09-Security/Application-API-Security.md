# Application & API Security

Defensive principles: validate untrusted input, authenticate identities, authorize every protected resource/action, minimize data, use secure transport, protect session/token lifecycle, rate-limit abuse-sensitive operations and return safe errors.

Client-side validation improves UX but server-side validation/authorization protects the system.

## Multi-tenant risk
Object identifiers must not allow cross-tenant access. Authorization checks include tenant/resource context.

## Logging
Do not log passwords, tokens, payment secrets or unnecessary personal data.
