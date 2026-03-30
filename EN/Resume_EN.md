# Joongchang Yang - Resume

> iOS Developer

- **Email**: didwndckd@gmail.com
- **Phone**: +82-10-3334-9929
- **GitHub**: https://github.com/didwndckd



## Introduction

iOS developer who enjoys analyzing and improving structural issues that arise as services scale.
I have worked on Tuist-based modularization, architecture refactoring, and legacy migration to enhance codebase maintainability and scalability.
I aim to design architectures that operate reliably even in complex service environments, with clear intent and well-defined responsibilities in implementation.



## Tech Stack

- **Languages**: Swift, Objective-C
- **Architecture/Patterns**: Clean Architecture, MVVM, Router
- **UI**: UIKit, SwiftUI, Storyboard
- **Async/Reactive**: RxSwift, Combine, Swift Concurrency
- **Modularization**: Tuist
- **Testing**: XCTest, Swift Testing
- **Analytics/Operations**: Amplitude, Hackle, Firebase (Crashlytics, Analytics)
- **AI Tools**: Claude Code
- **Collaboration**: Slack, Jira, Confluence, Figma
- **Version Control**: Git, GitHub, GitLab



## Experience (5+ Years)

### Kmong Inc.

> Jul 2023 – Mar 2026 (2 years 9 months)

Freelancer/outsourcing marketplace platform (3M MAU, 6.4M+ cumulative transactions)
Developed and maintained the iOS app (~360K LOC codebase) within a 4-member iOS team

- Designed and adopted Tuist-based modular architecture for a large-scale iOS codebase; completed modular separation for 24% of the entire codebase
- Improved real-time chat (WebSocket) architecture to a Combine-based Pub/Sub structure, achieving **0 chat screen crashes**
- Introduced Router pattern to improve cross-module navigation and prevent circular dependencies
- Built a design system module based on Atomic Design; operated a demo app module for designer feedback
- Introduced Endpoint pattern to improve management of 100+ APIs with compile-time verification via associatedtype
- Fully rebuilt Search Home, Results, and Filter screens with SwiftUI + Clean Architecture; safely deployed via Feature Flags (48 PRs)
- Led full redesign of Expert Profile screen using Claude Code; progressively derived Spec → Plan → Task, linking 127 tasks to code implementation (32 PRs)



### Kaflix Inc.

> Sep 2020 – Jun 2023 (2 years 10 months)

Developed and maintained iOS apps within a 2-member iOS team

- Designed RxSwift-based Input/Output unidirectional architecture, unifying MVVM conventions across the team
- Led full redesign of rental car pickup/return service app (Mosaicar); transitioned from VIPER to MVVM to improve development velocity
- Analyzed and resolved memory leaks across all screens caused by structural navigation flaws
- Designed login module, token refresh plugin, and unified app entry point handling for flight/accommodation/rental car booking app (JejuPass)
- Built RxSwift + Moya-based network layer and established common API communication structure
- Migrated Jeju restaurant/cafe recommendation apps (CafePass/MatjipPass) from Objective-C to Swift



## Open Source

### JCJoystick

> Apr 2022

Custom joystick view library for games/controllers (distributed via CocoaPods)

**GitHub**: https://github.com/didwndckd/JCJoystick



## Awards

### AngelHack Seoul 2020 Winner

> Jul 2020

Developed an online study app focused on improving completion rates in remote learning environments



## Education

### National Institute for Lifelong Education (Credit Bank System)

> Sep 2019 – Aug 2023

Computer Science (GPA: 4.1 / 4.5)
