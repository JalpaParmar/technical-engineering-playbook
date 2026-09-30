# UIKit & SwiftUI

## UIKit
UIKit is mature and imperative. Understand view-controller lifecycle, navigation, Auto Layout, collection/table views, responder chain, accessibility and containment.

### Lifecycle reasoning
Avoid putting expensive or repeated work into lifecycle callbacks without understanding how often they run. Keep business logic outside view controllers where practical.

## SwiftUI
SwiftUI is declarative: UI is derived from state. The difficult part is usually **state ownership and data flow**, not view syntax.

Ask:
- Who owns the state?
- Is the state local, shared or externally injected?
- What should survive view recreation?
- Which side effects belong outside the view?
- Is navigation state modeled explicitly?

## UIKit vs SwiftUI
| Consideration | UIKit | SwiftUI |
|---|---|---|
| Style | imperative | declarative |
| Mature legacy ecosystem | strong | integrates with UIKit |
| New UI iteration | explicit plumbing | often concise |
| Fine-grained established control | strong | improving/evolving |
| Migration | existing base | incremental adoption possible |

Avoid “rewrite everything.” Mixed UIKit/SwiftUI is a legitimate migration strategy.

## Scenario
**Existing UIKit app needs one new complex feature.**  
Evaluate OS support, team capability, interoperability boundary, navigation, design-system reuse, test strategy and maintenance. SwiftUI can be adopted at feature boundaries without requiring a whole-app rewrite.

## Accessibility checklist
- [ ] Dynamic Type behavior considered
- [ ] VoiceOver labels/hints meaningful
- [ ] controls have adequate semantic roles
- [ ] color is not the only information carrier
- [ ] focus/order makes sense
- [ ] localization and larger content tested
