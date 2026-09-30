# Design Multi-Tenant SaaS

## Requirements
Many businesses/tenants, users/roles, tenant data isolation, configuration, reporting and regional/scaling needs.

## Tenant isolation
Every data access path must preserve tenant context. Options range from shared tables with tenant keys to separate schemas/databases depending on scale, compliance and operational requirements.

## Authorization
Authentication identifies principal; authorization evaluates role/resource/tenant permissions on trusted server boundaries.

## Noisy neighbor
Use quotas/rate limits, workload isolation and capacity telemetry as needed.

## Configuration
Tenant configuration needs versioning/defaults and safe rollout. Avoid configuration combinations that cannot be tested/operated.

## Observability
Include tenant dimension carefully without exposing sensitive data. Detect tenant-specific failures and resource hotspots.
