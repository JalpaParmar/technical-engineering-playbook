# iOS Modernization Playbook

## Trigger
Legacy Objective-C/UIKit/MVC code is slowing safe change, testing or feature delivery.

## 1. Assess before rewriting
Measure change frequency, defect hotspots, coupling, testability, unsupported dependencies, build time, crash/performance issues and business roadmap.

## 2. Choose a boundary
Prefer incremental seams:
- new feature/module;
- networking boundary;
- domain service;
- screen/flow;
- shared component.

## 3. Define target
Examples: Swift for new domain code, async/await at a service boundary, SwiftUI for an isolated flow, MVVM/Clean separation where complexity justifies it.

## 4. Protect behavior
Add characterization/regression tests around critical legacy behavior before risky refactoring.

## 5. Migrate incrementally
Keep interoperability explicit. Avoid simultaneous language + architecture + UX + API rewrites unless unavoidable.

## 6. Measure
Compare defect rate, delivery friction, testability, performance and maintenance—not lines of Swift migrated.

## Decision rule
Modernization is successful when it improves the ability to change the product safely and economically. “Percentage rewritten” is not the outcome.
