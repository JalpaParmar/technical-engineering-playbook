# Swift & Objective-C

## Swift mental model
Focus on value/reference semantics, optionals, protocols, generics, error handling, closures, memory ownership and concurrency safety—not syntax memorization.

### Value vs reference semantics
`struct` values are copied semantically; classes have identity/reference semantics. Swift may optimize copies internally, so do not equate value semantics with “always physically copied immediately.”

**Use value types** when independent state and predictable mutation are valuable. **Use reference types** when identity, shared mutable state or framework requirements matter.

### Optionals
An optional models “value may be absent.” Prefer explicit unwrapping, optional binding and transformations such as `map`/flat-map style operations over force-unwrapping. Force unwrap only where the invariant is genuinely guaranteed and failure should be programmer-visible.

### Protocol-oriented design
Protocols define capabilities/contracts. They are useful for boundaries and test seams, but excessive protocol abstraction can make navigation harder. Abstract because multiple implementations, testing or architectural boundaries justify it—not automatically.

## ARC and memory
ARC manages reference-counted object lifetime. Retain cycles occur when strong references form a cycle. Common sources include closures capturing `self`, delegates that should be weak, timers/callbacks and long-lived asynchronous work.

### Closure capture example
```swift
final class ProfileLoader {
    var onLoaded: (() -> Void)?

    func configure() {
        onLoaded = { [weak self] in
            guard let self else { return }
            self.render()
        }
    }

    private func render() {}
}
```

Do not add `weak self` mechanically. Decide based on intended ownership and whether the work should keep the owner alive.

## Objective-C → Swift interoperability
Understand:
- nullability annotations improve imported Swift APIs;
- Objective-C lightweight generics improve collection types;
- bridging headers expose Objective-C to Swift;
- `@objc`/NSObject interoperability may be required for Objective-C runtime features;
- migration can be incremental.

## Modernization decision
Do not rewrite stable Objective-C solely to “be modern.” Prioritize modules with high change rate, defect cost, difficult testability, unsafe interfaces, or where new Swift-only architecture materially improves delivery.

## Interview check
**Q: Struct or class?**  
**Short answer:** I start with value semantics when the model represents data without identity. I choose a class when identity/shared lifecycle/reference semantics are part of the design. I also consider framework constraints and mutation behavior.

**Follow-up:** How does copy-on-write affect performance? Why can reference types create concurrency risks?
