# Modularization & Dependency Injection

## Why modularize?
Potential benefits: ownership boundaries, reduced coupling, reuse, independent testing and sometimes build improvements. Costs: APIs between modules, dependency graph complexity and discoverability.

Modularize around meaningful product/technical boundaries—not arbitrary file counts.

## Dependency direction
High-level policy should not depend unnecessarily on concrete infrastructure. Protocol/interface boundaries are valuable when they protect a real seam.

## DI
Constructor injection is often the clearest default because dependencies are visible and testable. Platform/framework constraints may require other techniques.

## Avoid abstraction inflation
An interface with one implementation can still be justified by a meaningful boundary, but “everything needs an interface” is not a rule.

## Review questions
- Is ownership clear?
- Can modules form cycles?
- Is shared code actually stable/shared?
- Are public APIs minimal?
- Does the boundary improve testing/change isolation?
- Is DI lifetime/scope correct?
