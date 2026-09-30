# OOP & SOLID

Encapsulation protects invariants; abstraction exposes essential behavior; polymorphism allows behavior behind a contract. Inheritance is useful for genuine substitutable relationships, but composition often reduces coupling.

## SOLID as design prompts
- **SRP:** a module should have a coherent reason to change—not “one method per class.”
- **OCP:** create extension seams where variation is expected; avoid speculative plugin systems.
- **LSP:** implementations must preserve behavioral expectations, not merely share a type.
- **ISP:** consumers should not depend on capabilities they do not need.
- **DIP:** high-level policy should not be unnecessarily coupled to low-level details.

## Example
A payment workflow coupled directly to one provider SDK is difficult to test/change. A domain-facing gateway can isolate provider details when that boundary represents real business capability.

**Composition or inheritance?** Prefer composition for flexible behavior/lower coupling. Use inheritance where a genuine stable “is-a” contract exists.
