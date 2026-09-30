# DAY 1 — Technical Engineering Playbook
## Master Build Specification for Codex

**Repository:** `JalpaParmar/technical-engineering-playbook`

## Mission
Build a durable personal **Technical Engineering Playbook** for technical reference, hands-on refresh, mobile engineering, software architecture, backend/API, cloud/DevOps, system design, debugging, AI engineering, technical leadership, TPM work, and interviews.

> **Learn it → Build/Use it → Troubleshoot it → Review it → Explain it in an interview**

This must NOT become a shallow collection of AI-generated notes. Prefer depth, accuracy, practical examples, and durable navigation over file count.

## Knowledge-depth strategy

| Area | Target depth |
|---|---|
| iOS / Mobile Engineering | DEEP |
| Mobile Architecture | DEEP |
| Software Engineering | STRONG |
| Software Architecture | STRONG |
| System Design | STRONG |
| Backend / APIs | STRONG architecture/integration knowledge |
| Azure / Cloud | STRONG TPM/architect knowledge |
| DevOps / CI/CD | STRONG |
| Android | STRONG working/architecture knowledge |
| Testing / Quality | STRONG |
| Security | STRONG defensive/practical knowledge |
| Debugging / Incidents | STRONG |
| AI Engineering | STRONG working knowledge |
| AI-Assisted Development | STRONG practical knowledge |
| Technical Leadership | DEEP |
| TPM technical decision-making | DEEP |

Do not manufacture personal experience. Label illustrative examples clearly.

## Target repository structure

```text
technical-engineering-playbook/
├── README.md
├── ROADMAP.md
├── CONTRIBUTING.md
├── GLOSSARY.md
├── 00-Start-Here/
├── 01-Mobile-Engineering/
│   ├── iOS/
│   ├── Android/
│   ├── Mobile-Architecture/
│   └── Cross-Platform-Concepts/
├── 02-Software-Engineering/
├── 03-Software-Architecture/
├── 04-Backend-API/
├── 05-System-Design/
├── 06-Cloud-Azure/
├── 07-DevOps-CICD/
├── 08-Testing-Quality/
├── 09-Security/
├── 10-Debugging-Incidents/
├── 11-AI-Engineering/
├── 12-AI-Assisted-Development/
├── 13-Requirement-Engineering/
├── 14-Technical-Leadership/
├── 15-Interview-Master/
├── 16-Cheat-Sheets/
├── 17-Checklists/
├── 18-Playbooks/
└── examples/
```

## Standard content model

For substantial topics, use the relevant subset of:

```text
README.md
QUESTIONS-ANSWERS.md
PLAYBOOK.md
CHECKLIST.md
EXAMPLES.md
SCENARIOS.md
TROUBLESHOOTING.md
BEST-PRACTICES.md
CHEAT-SHEET.md
```

Do not blindly create every file for every topic. Avoid empty/repetitive files.

## Q&A standard

Progress through fundamentals, intermediate, senior, lead/architect, scenarios, troubleshooting, trade-offs, and TPM/leadership implications.

Preferred answer structure:

### Question
**Short interview answer:** concise and speakable.

**Deep dive:** technical explanation.

**Example:** practical example.

**Trade-offs:** when relevant.

**Follow-up questions:** likely interviewer follow-ups.

Optimize for understanding rather than memorization.

## Checklists and playbooks

Checklists must be operational: architecture review, API readiness, mobile release, production readiness, code review, security, performance, App Store/Play Store, CI/CD, migrations, incident response, RCA, feature flags, rollback, observability, testing and accessibility.

Playbooks answer **“A real situation occurred. What should I do?”**

```text
Trigger → Assess → Gather evidence → Stabilize → Decide → Execute
→ Validate → Communicate → Monitor → Prevent recurrence
```

Include decision points, questions, common mistakes and escalation criteria.

## Practical examples

Examples must explain problem, approach, code/design, why it works, alternatives, trade-offs and common failures. Prefer small clean reference implementations over large demo apps.

# Technical coverage roadmap

## Mobile Engineering — highest priority

### iOS — DEEP
Eventually cover Swift, Objective-C/interoperability, UIKit, SwiftUI, lifecycle/navigation/state/accessibility, async/await, actors, structured concurrency, GCD, races/thread safety, Combine/delegates/notifications/callbacks, URLSession/REST/auth/token refresh/retry/timeouts/caching/pagination, Core Data/UserDefaults/Keychain/files/cache/migrations, push/deep links/background work/permissions/analytics/crash reporting/feature flags/localization, XCTest/UI testing/mocking/DI, retain cycles/memory leaks/main-thread blocking/startup/performance, signing/provisioning/TestFlight/App Store/phased rollout/hotfix.

Create an **iOS modernization bridge** for Objective-C→Swift, UIKit→SwiftUI, callbacks→async/await, delegates→Combine where appropriate, MVC→MVVM/Clean Architecture, legacy networking→modern network layers, and monolith→modular architecture. Explain trade-offs; newer is not automatically better.

### Android — STRONG
Eventually cover Kotlin, Java/interoperability, lifecycle, Jetpack Compose, Jetpack, ViewModel, Navigation, Coroutines/Flow, Retrofit/OkHttp, Room, Hilt/Dagger/Koin awareness, Firebase, WorkManager, background work, notifications/deep links, storage/permissions, testing, ANR/performance, Play Store lifecycle and architecture patterns. Do not falsely present years of Android hands-on experience.

### Mobile Architecture — DEEP
Cover MVC, MVVM, MVI, Clean Architecture, Repository, Coordinator, DI, modularization, domain/data/presentation layers, offline-first, sync, caching, pagination, auth, feature flags and observability. Explain problem, structure, examples, pros/cons, when to use/not use, testing and migration.

## Software Engineering
OOP, SOLID, clean code, patterns, refactoring, error handling, concurrency, data structures fundamentals, Git, branching, PRs, code review, technical debt, dependencies, semantic versioning, documentation, maintainability and scalability.

## Backend/API
HTTP, REST, JSON, OAuth/JWT, authn/authz, versioning, pagination, rate limiting, caching, retry/backoff, idempotency, webhooks, API gateway, microservices, queues, SQL/NoSQL, Redis/cache, transactions, consistency, observability and API security. Eventually add a small Python/FastAPI reference API when valuable.

## Software Architecture
Monolith/modular monolith/microservices, sync/async communication, event-driven architecture, queues, caching, load balancing, availability, scalability, resilience, fault tolerance, observability, data architecture, security, ADRs and trade-off analysis.

## System Design
Create reusable frameworks and worked designs for appointment booking, payments, notifications, messaging, offline mobile sync, multi-location SaaS, media upload and analytics/event pipelines. Cover requirements, constraints, explicit scale assumptions, architecture, APIs, data, mobile considerations, caching, consistency, availability, security, observability, failure modes, trade-offs and evolution.

## Azure / Cloud
Azure Functions, App Service, Storage, Azure SQL, Key Vault, Service Bus, Application Insights, monitoring/logging, identity/access, config/secrets, scaling, resilience and cost awareness. Focus on engineer/architect/TPM decision-making, not portal tutorials.

## DevOps / CI-CD
CI/CD, GitHub Actions, Azure DevOps, Docker fundamentals, environments, secrets/config, pipelines, automated tests/static checks, deployment strategies, feature flags, rollback, observability and governance.

Deep mobile flow:
```text
Commit → Build → Static checks → Tests → Signing → Artifact
→ Internal distribution → QA → Store submission → Rollout
→ Monitoring → Hotfix/Rollback decision
```

## Testing / Quality
Testing pyramid, unit/integration/UI/contract testing, regression, exploratory testing, mocks/stubs/fakes, automation strategy, testability, quality gates, defect leakage, flaky tests, release quality and mobile-specific testing.

## Security
Defensive engineering only: secure storage, TLS/certificates, authentication/authorization, tokens, secrets, sensitive logging, OWASP awareness, API/mobile security, dependency vulnerabilities, least privilege and threat modeling fundamentals.

## Debugging / Incidents
Eventually cover crashes, races, memory leaks, retain cycles, ANRs, main-thread blocking, API timeouts, duplicate calls, token expiry, corrupted cache, DB migration failures, pagination defects, background failures, slow launch, battery/network issues, push failures, backend outages, DB issues and cloud configuration.

Reasoning:
```text
Symptom → Impact → Evidence → Possible components → Hypotheses
→ Isolation → Mitigation → Root cause → Fix → Validation
→ Monitoring → Prevention
```

Design an Incident Analyzer workflow accepting logs, stack traces, API responses, errors and deployment context. Never present AI hypotheses as proven causes.

## AI Engineering
LLM fundamentals, prompting/context, structured output, embeddings, vector DB concepts, RAG, agents, tool/function calling, MCP concepts, hallucination/grounding, evaluation, security/privacy, bias awareness, token/cost, observability and human review. Target product/architecture competence, not ML-research depth.

## AI-Assisted Development
Practical use of Codex, GitHub Copilot, ChatGPT, Claude and Cursor for legacy understanding, architecture exploration, planning, code/refactoring, Objective-C→Swift analysis, UIKit→SwiftUI planning, Java→Kotlin planning, tests, debugging, crash analysis, security-review assistance, API contracts, PR review/summaries and docs.

```text
Requirement → Human clarification → AI analysis → Architecture/plan
→ Implementation → AI-assisted review → Checks/tests
→ Human review → PR → Validation
```

Document where human judgment is mandatory.

## Requirement Engineering
Eventually support:
```text
Problem → Epic → Features → Stories → Acceptance criteria
→ Technical considerations → APIs → Dependencies → Edge cases
→ Security → Testing → Release considerations
```

## Technical Leadership
Architecture/code reviews, planning, estimation, technical debt, mentoring, engineering health, quality, dependencies, decisions, conflict resolution, metrics, risk, release readiness, incidents and explaining technical trade-offs to stakeholders. Use scenarios, not generic slogans.

## Interview Master
Eventually consolidate into Mobile Tech Lead, iOS Tech Lead, Technical Project Manager, Technical Program Manager, Software Architect, AI Project Manager, System Design, Cloud/DevOps, Scenario-Based Questions and 30-Minute-Before-Interview. Link to canonical material instead of duplicating it.

## Cheat Sheets
Eventually provide 5–30 minute revision sheets for Swift/iOS, Android/Kotlin, architecture, REST/API, system design, Azure, DevOps, Git, testing, security, AI, incidents and technical leadership.

## Diagrams
Use Mermaid only where it improves understanding. Every diagram needs explanatory text.

## Navigation / learning paths
Root README must explain purpose, audience, usage, depth legend, repository status and roadmap. Include paths for Mobile Developer, iOS Refresh, Android Architecture Refresh, Software Architect, TPM, Technical Program Manager, AI-Enabled TPM, Mobile Tech Lead, Interview in 30 Minutes, and Interview in 3 Days.

# Accuracy and quality rules

1. Prefer official/current terminology.
2. Flag version-sensitive guidance.
3. Do not invent APIs/framework behavior.
4. Explain uncertainty.
5. Distinguish facts from recommendations.
6. Avoid unsupported performance claims.
7. Do not fabricate personal achievements.
8. Keep code small and understandable.
9. Avoid duplication; link to canonical explanations.
10. Do not optimize for repository size.
11. Keep Markdown readable on GitHub and mobile.
12. Use tables only when useful.
13. Include trade-offs, not just best practices.
14. Keep interview answers human and speakable.
15. Keep security content defensive.
16. Validate internal links/navigation.

# PHASED EXECUTION — CRITICAL

Do **not** generate the entire repository in one pass.

## PHASE 1 — Repository Foundation ONLY

Start with Phase 1.

Create:
- high-level directory structure
- root `README.md`
- `ROADMAP.md`
- `CONTRIBUTING.md`
- `GLOSSARY.md`
- `00-Start-Here/README.md`
- documentation standards/templates for Q&A, checklists, playbooks, examples/scenarios and cheat sheets
- depth legend
- learning paths
- interview paths
- navigation conventions
- naming conventions
- quality rules
- clear roadmap references for later phases

Do not fill all later folders with shallow content.

### Phase 1 acceptance criteria
Before stopping:
- repository structure is coherent
- root README is useful as a home page
- future phases are clearly documented
- templates encourage high-quality content
- navigation conventions are defined
- no major duplicate structure exists
- no empty-file explosion
- internal links created in Phase 1 are checked
- Markdown renders cleanly
- repository is easy to browse from a phone
- produce a concise Phase 1 completion summary

**STOP after Phase 1. Do not begin Phase 2 automatically.**

## Later phases
- **Phase 2:** Deep Mobile Engineering — iOS first, then Android and Mobile Architecture.
- **Phase 3:** Software Engineering + Software Architecture + System Design.
- **Phase 4:** Backend/API + Azure + DevOps/CI-CD.
- **Phase 5:** Testing + Security + Debugging/Incident Engineering.
- **Phase 6:** AI Engineering + AI-Assisted Development.
- **Phase 7:** Requirement Engineering + Technical Leadership.
- **Phase 8:** Consolidated Q&A + scenarios + checklists + playbooks + cheat sheets.
- **Phase 9:** Role-specific interview master packs and rapid-revision packs.
- **Phase 10:** Repository-wide accuracy, link, duplication, code, navigation and coverage audit.

# Codex instructions for the first run

1. Inspect the CURRENT repository before changing anything.
2. Preserve useful existing work.
3. Work directly in `JalpaParmar/technical-engineering-playbook`.
4. Execute **Phase 1 only**.
5. Do not bulk-create shallow topic documents.
6. Prefer a small number of excellent foundational files.
7. Check the resulting diff.
8. Validate Markdown/internal links that can reasonably be validated.
9. Summarize exactly what changed.
10. Identify anything needing owner confirmation.
11. Stop and wait for approval before Phase 2.
