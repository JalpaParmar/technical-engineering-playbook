# Secrets, Identity & Access

Prefer workload identity/managed identity where supported over long-lived shared credentials. Apply least privilege and separation of duties.

Secrets require controlled storage, rotation, revocation, auditing and incident procedures.

## Common failures
Secrets in source/history, overly broad service principals, production credentials in developer machines/CI logs, forgotten test keys and no rotation owner.
