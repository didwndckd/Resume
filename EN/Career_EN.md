# Jungchang Yang - Career Description

> iOS Developer

- **Email**: didwndckd@gmail.com
- **Phone**: +82-10-3334-9929
- **GitHub**: https://github.com/didwndckd



## Experience (6 Years)



### Kmong Inc.

> Jul 2023 – Mar 2026 (2 years 9 months)

Freelancer/outsourcing marketplace platform (3M MAU, 6.4M+ cumulative transactions)
Developed and maintained the iOS app (~360K LOC codebase) within a 4-member iOS team

- Language: Swift
- Architecture/Patterns: Clean Architecture, MVVM, Router
- UI: UIKit, SwiftUI
- Async/Reactive: Combine, Swift Concurrency
- Modularization: Tuist
- Testing: XCTest, Swift Testing
- Analytics/Operations: Amplitude, Hackle, Firebase (Crashlytics, Analytics)
- AI Tools: Claude Code

![Kmong_preview](Assets/compressed/Kmong_preview.png)

#### Modular Architecture Design & Adoption (Tuist)
- Introduced to resolve SwiftUI preview unavailability caused by growing build times and to improve dependency management
- Separated Domain and Data layers to isolate business logic from the data layer
- Modularized by role: Feature, Foundation, UIFoundation, DesignSystem, etc.
- Completed modular separation for 24% of the entire codebase; phased migration ongoing
- Managed module dependencies and build environments using Tuist
- Established Static/Dynamic linking criteria through Mach-O analysis
  - See [Mach-O Analysis](https://github.com/didwndckd/TIL/tree/master/XcodeBuildSystem/Mach-O) for details
- Shortened development feedback loop by enabling per-module builds and tests
- Established core logic verification through unit tests targeting Domain and Presentation layers

#### Tech Stack Modernization
- Incrementally migrated UIKit/Storyboard-based screens to SwiftUI, achieving a 52.6% conversion rate
- Migrated Combine/Completion Handler-based async processing to Swift Concurrency, achieving a 70.7% conversion rate

#### Real-time Chat (WebSocket) Architecture Improvement
- Transitioned from Delegate pattern to Combine-based Pub/Sub architecture, enabling multi-screen simultaneous event subscription
- Eliminated background resource waste through app lifecycle-aware automatic WebSocket connect/disconnect
- Stabilized message UI updates by adopting `DiffableDataSource` and buffering events during inactive states
- **Reduced chat screen crashes caused by index mismatches to 0**

#### Router Pattern for Navigation Management
- Introduced to resolve cross-module navigation limitations
- Designed with dependency injection to prevent circular references between modules and ensure testability
- Unified management of SwiftUI/UIKit screen transitions and custom transitions such as bottom sheets and tooltips

#### Endpoint Pattern for API Management
- Migrated 100+ APIs from Moya TargetType enum-based approach to individual Endpoint struct-based architecture
- Defined an Endpoint protocol adopted by each API for consistent structure
- Leveraged associatedtype-based type system to verify API-ResponseModel matching at compile time
- Request information consolidated in a single struct, improving API history tracking and maintainability

#### Design System Module
- Designed common UI components (buttons, text fields, etc.) as an independent module based on Atomic Design
- Ensured UI consistency by having the Presentation Layer depend on the DesignSystem module
- Built a demo app module for designer feedback

#### Unified API Error Model Across Versions
- Resolved the issue where the Presentation Layer had to directly handle version-specific API errors
- Unified disparate error models across API versions (v4, v5, MSA) into a single error type in the Data Layer
- Defined errors in the Domain Layer as needed, eliminating the Presentation Layer's need to know API versions

#### Service Card Model Consolidation & UI Logic Restructuring
- Consolidated scattered parsing/domain models for service listings into a single unified model
- Created a new ViewModel based on the unified model, eliminating duplicated service card logic across screens
- Adopted SwiftUI EnvironmentKey to flexibly handle varying service card display requirements across 10+ screens

#### Search Full Redesign & Enhancement
- Rebuilt Search Home, Search Results, and Search Filters from UIKit/Storyboard to SwiftUI + Clean Architecture
- Deployed behind Feature Flags for instant rollback capability; removed legacy screens after 2-sprint monitoring
- Designed and ran A/B tests for search filters; experimented with budget filters to improve purchase conversion
- Executed the integration of Search Home, Results, Filters, and Expert Search across 48 PRs in a phased approach

#### Expert Profile Screen Full Redesign (Using Claude Code)
- Rebuilt with SwiftUI + Clean Architecture
- Used Claude Code to progressively derive Spec → Plan → Task documents, linking 127 tasks to code implementation
- Implemented in Domain → Data → Presentation order, establishing business logic independently of UI
- Executed across 32 PRs



### Caflix Inc.

> Sep 2020 – Jun 2023 (2 years 10 months)

Developed and maintained iOS apps within a 2-member iOS team

- Language: Swift, Objective-C
- Design Pattern: MVVM
- UI: UIKit, Storyboard
- Async/Reactive: RxSwift
- Others: Moya, Firebase Analytics, Firebase Crashlytics, FCM

#### Mosaicar

Rental car pickup/return service

![Mosaicar_preview](Assets/compressed/Mosaicar_preview.png)

- Designed RxSwift-based Input/Output unidirectional architecture
  - Defined Input/Output as associatedtypes in the ViewModel protocol with `transform(input:) -> Output` for unidirectional data flow
  - Defined a ViewController protocol to standardize ViewModel binding and Storyboard-based instance creation
  - Unified MVVM implementation conventions across the team for consistent code structure
- Led full app redesign
  - Participated from the planning stage to redesign all screens' UI and functionality
  - Determined existing VIPER pattern caused excessive boilerplate for a small team; switched to MVVM to improve development velocity
- Designed RxSwift-based network communication module
  - Adopted Moya to establish type-safe API management
  - Integrated error handling into a consistent interface via Observable extensions
- Eliminated memory leaks across all screens
  - Analyzed and resolved circular references present in every screen due to structural navigation flaws
  - Resolved `WKUserContentController` strong reference issue using the Proxy pattern

#### JejuPass

Flight, accommodation, and rental car price comparison/booking service

![JejuPass_preview](Assets/compressed/JejuPass_preview.png)

- Designed login module (ID, SNS login, biometric authentication)
- Developed automatic token refresh plugin based on `Moya.PluginType`
- Designed unified app entry point handling for FCM push, dynamic links, quick actions, etc.
- Created Xcode file templates to standardize team development conventions

#### CafePass / MatjipPass

Jeju restaurant/cafe recommendation service

- Performed Objective-C → Swift migration
- Incrementally converted the existing Objective-C codebase to Swift
- Gradual migration in a mixed Objective-C/Swift environment using Bridging Header
