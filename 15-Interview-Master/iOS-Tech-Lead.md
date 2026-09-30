# iOS Tech Lead — Interview Pack

## Core revision
- [iOS Deep Track](../01-Mobile-Engineering/iOS/README.md)
- [iOS Q&A](../01-Mobile-Engineering/iOS/QUESTIONS-ANSWERS.md)
- [Advanced Scenarios](../01-Mobile-Engineering/iOS/Advanced-Scenarios.md)
- [Modernization](../01-Mobile-Engineering/iOS/Modernization-Playbook.md)
- [30-Minute Revision](../16-Cheat-Sheets/iOS-30-Minute-Revision.md)

## Lead-level themes
Be ready to discuss:
- ownership/memory and concurrency failures;
- UIKit/SwiftUI coexistence;
- architecture complexity trade-offs;
- API/offline/data consistency;
- testing strategy;
- performance evidence;
- legacy modernization;
- release/observability;
- mentoring/review decisions.

## Answer pattern
**Context → decision → why → trade-off → validation.**

Example:
> I wouldn't choose SwiftUI merely because it is newer. I'd look at the feature boundary, supported OS versions, existing UIKit/navigation/design-system dependencies, team capability and test strategy. If the boundary is clean, incremental SwiftUI adoption can reduce migration risk while letting us validate the approach.
