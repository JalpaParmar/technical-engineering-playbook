# Authoring & Contribution Standards

## Principles
1. Prefer depth and accuracy over volume.
2. Never fabricate personal experience, metrics or achievements.
3. Distinguish facts, assumptions, examples and recommendations.
4. Flag version-sensitive guidance.
5. Explain trade-offs; avoid universal “best practice” claims.
6. Keep code small, runnable where practical, and explained.
7. Keep security material defensive.
8. Avoid duplication: link to canonical material.
9. Optimize Markdown for GitHub and phone reading.
10. Validate links after structural changes.

## Naming
- Number top-level learning areas to preserve navigation order.
- Use descriptive kebab-case for topic folders where needed.
- Use standard uppercase filenames only for recurring document types, e.g. `CHECKLIST.md`, `PLAYBOOK.md`, `QUESTIONS-ANSWERS.md`.
- Prefer one canonical page over multiple near-duplicates.

## Interview answers
Answers should normally contain:
- **Short interview answer** — natural and speakable.
- **Deep dive** — enough detail to understand the concept.
- **Example** — realistic, clearly marked when illustrative.
- **Trade-offs** — when a decision is involved.
- **Follow-ups** — likely interviewer probes.

## Code
Explain the problem, approach, code, why it works, alternatives and failure modes. Do not add code only to increase repository size.

## Diagrams
Use Mermaid when it improves understanding. Add prose explaining the diagram and key decisions.

## Review checklist
Before merging substantive content:
- [ ] technically accurate to the best available evidence
- [ ] assumptions/examples labeled
- [ ] no fabricated experience
- [ ] trade-offs included where appropriate
- [ ] version-sensitive guidance flagged
- [ ] links work
- [ ] readable on mobile
- [ ] no unnecessary duplication
