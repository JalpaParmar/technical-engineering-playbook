# Design Patterns

Patterns name recurring structures. Use them because the problem fits.

- **Strategy:** interchangeable policy.
- **Factory:** construction varies.
- **Adapter:** translate interfaces.
- **Decorator:** add behavior around an object.
- **Observer:** publish change; manage lifecycle/coupling.
- **Command:** represent an operation.
- **Repository:** data-access boundary.
- **State:** behavior varies explicitly by state.
- **Coordinator:** orchestration/navigation boundary.

## Pattern-stacking smell
Factory + repository + mediator + strategy around simple CRUD can create more cost than it removes.

Ask: What variation are we protecting? Does this improve testing/changeability? Is a simpler function/type enough?
