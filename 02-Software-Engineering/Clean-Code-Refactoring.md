# Clean Code & Refactoring

Prefer intent-revealing names, cohesive modules, explicit errors, minimal surprise and tests around critical behavior.

## Safe refactoring
1. identify pain/risk;
2. establish tests/characterization;
3. make small structural changes;
4. run checks;
5. verify the intended maintainability/performance benefit.

Code smells—long method, shotgun surgery, hidden global state, duplication, feature envy—are investigation prompts, not automatic rewrite triggers.

For legacy code, first understand and protect behavior.

> What future change becomes easier because of this abstraction?
