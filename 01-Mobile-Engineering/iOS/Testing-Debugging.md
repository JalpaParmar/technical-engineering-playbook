# iOS Testing, Debugging & Performance

## Testing strategy
Test behavior at the cheapest reliable level.

- unit: domain logic, state transitions, mappings;
- integration: repository/network/persistence boundaries;
- UI: critical user journeys, not every permutation;
- exploratory/performance: risks difficult to encode as unit tests.

## Dependency seam example
Inject transport/time/storage instead of hard-wiring globals when the behavior needs deterministic tests.

## Crash investigation playbook
1. establish affected version/device/OS and user impact;
2. symbolicate and inspect stack;
3. correlate release/change/feature flag;
4. reproduce if possible;
5. distinguish symptom from root cause;
6. mitigate first if impact is high;
7. add regression test where feasible;
8. monitor after fix.

## Memory
Look for:
- retain cycles;
- unbounded caches;
- large images;
- repeated observers;
- long-lived tasks;
- view controllers not deallocating.

## Performance
Measure before optimizing. Consider launch, scrolling, rendering, main-thread work, networking, decoding, database queries, memory and energy.

## Scenario: UI freezes after API response
Investigate whether decoding, mapping, image processing or persistence is happening on the UI execution path. Measure with profiling tools rather than assuming the network itself is the cause.

## Interview answer
**How do you debug an intermittent crash?**  
I first bound the problem by app version, OS/device, affected flow and crash frequency. I use the symbolicated stack plus logs/telemetry to form hypotheses, correlate it with recent changes, and try to reproduce under the same state. For high-impact issues I separate mitigation from permanent root-cause work. The fix is followed by a regression test where practical and post-release monitoring.
