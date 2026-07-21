# Phase 04 — Professional App Architecture

> **Purpose:** Learn how to design production-quality iOS applications that are scalable, maintainable, testable, and easy for teams to develop over many years.

---

# Goal

Move beyond writing working code and begin thinking like a software architect.

Learn how to organize applications so that features remain easy to build, bugs are easier to fix, and the project can grow without becoming difficult to maintain.

---

# Learning Outcomes

By the end of this phase you should be able to:

- Design scalable application architecture.
- Separate responsibilities correctly.
- Build loosely coupled systems.
- Apply MVVM confidently.
- Design reusable features.
- Build applications that are easy to test.
- Understand architectural trade-offs.
- Read large codebases comfortably.
- Continue improving architecture independently.

---

# Module 1 — Architecture Fundamentals

## Core Topics

- What is Software Architecture?
- Separation of Concerns
- Single Responsibility
- Coupling
- Cohesion
- Layers
- Abstractions
- SOLID Principles (Practical)
- Composition over Inheritance
- Dependency Direction
- Information Flow

---

## Learning Objectives

After completing this module you should understand:

- Why architecture exists.
- Why good architecture reduces complexity.
- How responsibilities should be divided.
- What makes code maintainable.
- How applications grow over time.
- Why architecture is about trade-offs rather than rules.

---

## Parallel Learning Layers

### Git

Learn:

- Organize commits around architectural changes.
- Separate refactoring from feature work.
- Write commit messages explaining architectural decisions.

Practice:

Whenever architecture changes, document *why* the change was made.

---

### Xcode

Learn:

- Project organization.
- Groups vs Folders.
- File templates.
- Project navigation.
- Build settings overview.

Practice:

Keep projects organized from the beginning instead of restructuring later.

---

### Apple Documentation

Read:

- Swift Programming Language
- Observation Framework
- Swift Packages
- App Architecture examples

Goal:

Understand Apple's preferred architectural direction.

---

### WWDC

Recommended Topics

- Structure SwiftUI Applications
- Modern App Architecture
- Meet Observation
- Organizing Swift Projects

Goal

Observe how Apple engineers organize applications.

---

### Best Practices

Learn:

- One responsibility per type.
- Prefer composition.
- Keep files focused.
- Minimize dependencies.
- Design for change.
- Make code readable before making it clever.

Avoid:

- Massive classes.
- Massive Views.
- Massive ViewModels.
- Circular dependencies.
- Copy-paste architecture.

---

### Design Thinking

Questions to ask:

- Who owns this responsibility?
- Does this object have more than one job?
- Could another developer understand this structure?
- Is this abstraction actually useful?

---

### Architecture Thinking

Understand relationships between:

- UI Layer
- Presentation Layer
- Domain Layer
- Data Layer
- Infrastructure Layer

Learn why each layer exists and how information should flow between them.

---

### Open Source

Study:

Large production applications.

Observe:

- Folder structure.
- Naming.
- Layer separation.
- Dependency direction.
- Shared code.

Ask:

"Why is this code placed here instead of somewhere else?"

---

### AI

Use AI to:

- Review architecture.
- Challenge design decisions.
- Compare approaches.
- Explain trade-offs.

Avoid:

- Letting AI design your entire application.

---

### English

Vocabulary

- Architecture
- Responsibility
- Abstraction
- Coupling
- Cohesion
- Layer
- Dependency
- Composition
- Maintainability

Practice:

Explain each architectural concept in your own words.

---

### Notes

Maintain notes for:

- Architecture principles.
- Common mistakes.
- Layer responsibilities.
- Design decisions.
- Useful examples.

---

### Reflection

Ask yourself:

- Why does architecture matter?
- Which responsibilities belong together?
- Which responsibilities should be separated?
- What makes code difficult to maintain?

---

## Mini Project

Take one of your previous projects.

Refactor it by:

- Separating responsibilities.
- Removing duplicated code.
- Improving folder structure.
- Improving naming.
- Reducing coupling.

Document every architectural improvement.

---

## Exit Criteria

✓ Explain software architecture.

✓ Explain separation of concerns.

✓ Identify coupling problems.

✓ Explain cohesion.

✓ Understand layered architecture.

✓ Justify architectural decisions.

---

# Module 2 — MVVM Deep Dive

## Core Topics

- MVVM Responsibilities
- View
- ViewModel
- Model
- Data Flow
- State Ownership
- Commands
- Presentation Logic
- Business Logic
- View Lifecycle
- Dependency Injection (Introduction)

---

## Learning Objectives

After completing this module you should understand:

- Why MVVM exists.
- Responsibilities of each layer.
- How data flows through MVVM.
- Why Views should remain lightweight.
- When MVVM begins to break down.
- Common MVVM mistakes.

---

## Parallel Learning Layers

### Git

Learn:

- Keep ViewModel refactors isolated.
- Track architecture improvements separately.

Practice:

Commit after each MVVM improvement.

---

### Xcode

Learn:

- File organization.
- Preview with ViewModels.
- Debug state updates.
- Project navigation.

Practice:

Keep Views and ViewModels clearly separated.

---

### Apple Documentation

Read:

- Observation Framework
- SwiftUI Data Flow
- Environment
- Bindings

Goal

Understand how modern SwiftUI naturally supports MVVM.

---

### WWDC

Recommended Topics

- Data Essentials in SwiftUI
- Meet Observation
- Demystify SwiftUI Data Flow

Goal

Understand how Apple expects data to move through applications.

---

### Best Practices

Learn:

- Thin Views.
- Small ViewModels.
- Business logic outside Views.
- Presentation logic inside ViewModels.
- Models represent data—not UI.

Avoid:

- Massive ViewModels.
- Business logic inside Views.
- Network calls directly from Views.
- Duplicated state.

---

### Design Thinking

Questions to ask:

- Does this belong in the View?
- Is this presentation logic?
- Is this business logic?
- Who owns this state?

---

### Architecture Thinking

Understand responsibilities of:

- View
- ViewModel
- Model
- Service
- Repository

Understand communication flow:

View ⇄ ViewModel ⇄ Domain ⇄ Data

---

### Open Source

Study:

Production SwiftUI MVVM projects.

Observe:

- ViewModels.
- Folder structure.
- Naming.
- State ownership.
- Dependency flow.

Ask:

"Would this still work after 100 screens?"

---

### AI

Use AI to:

- Review MVVM boundaries.
- Explain responsibilities.
- Compare multiple implementations.

Avoid:

- Copying ViewModels without understanding them.

---

### English

Vocabulary

- Presentation
- State
- Binding
- Responsibility
- Observable
- Business Logic
- Presentation Logic

Practice:

Explain the role of each MVVM component.

---

### Notes

Document:

- MVVM rules.
- View responsibilities.
- ViewModel responsibilities.
- Common mistakes.
- Examples.

---

### Reflection

Ask yourself:

- Is my View doing too much?
- Is my ViewModel becoming massive?
- Where should this logic live?
- Can another developer understand this data flow?

---

## Mini Project

Refactor a SwiftUI application into proper MVVM.

Requirements:

- Thin Views.
- Small ViewModels.
- Clear responsibilities.
- Proper state ownership.
- No duplicated business logic.

---

## Exit Criteria

✓ Explain MVVM confidently.

✓ Keep Views lightweight.

✓ Build maintainable ViewModels.

✓ Separate business and presentation logic.

✓ Design scalable feature architecture.

---
# Module 3 — Dependency Injection

## Core Topics

- What is Dependency Injection?
- Dependency vs Dependency Injection
- Constructor Injection
- Method Injection
- Property Injection
- Dependency Inversion Principle
- Composition Root
- Service Registration
- Lifetime Management
- Protocol-Oriented Programming
- Mock Dependencies

---

## Learning Objectives

After completing this module you should understand:

- Why Dependency Injection exists.
- How Dependency Injection reduces coupling.
- Why protocols improve flexibility.
- How to replace dependencies for testing.
- How to design scalable applications with loosely coupled components.
- Why Dependency Injection is an architectural pattern rather than a framework.

---

## Parallel Learning Layers

### Git

Learn:

- Keep DI refactoring separate from feature work.
- Document dependency changes in commit messages.
- Track architectural improvements independently.

Practice:

Create one branch for every major Dependency Injection refactor.

---

### Xcode

Learn:

- Project organization for services.
- Dependency folders.
- Protocol grouping.
- Debug injected dependencies.

Practice:

Organize Services, Protocols, and Implementations separately.

---

### Apple Documentation

Read:

- Swift Protocols
- Existentials (`any`)
- Generics
- Observation Framework
- Swift Packages

Goal

Understand how Swift language features support Dependency Injection.

---

### WWDC

Recommended Topics

- Modern Swift
- Protocol-Oriented Programming
- Swift Language Updates

Goal

Understand why Apple heavily uses protocols.

---

### Best Practices

Learn:

- Inject abstractions—not concrete types.
- Constructor Injection should be the default.
- Keep dependencies explicit.
- One object should not own dozens of dependencies.
- Build testable code.

Avoid:

- Singletons everywhere.
- Hidden dependencies.
- Service Locators.
- Global mutable state.

---

### Design Thinking

Questions to ask:

- Does this object really need this dependency?
- Could this dependency be replaced?
- Is this dependency required or optional?

---

### Architecture Thinking

Understand dependency direction:

UI

↓

Presentation

↓

Domain

↓

Infrastructure

Higher layers should never depend directly on implementation details.

---

### Open Source

Study:

Large SwiftUI projects.

Observe:

- Dependency Injection.
- Protocol usage.
- Composition Root.
- Service creation.

Ask:

"How do they avoid tight coupling?"

---

### AI

Use AI to:

- Review dependency graphs.
- Compare DI approaches.
- Explain protocol abstractions.

Avoid:

- Asking AI to design your dependency graph.

---

### English

Vocabulary

- Dependency
- Injection
- Abstraction
- Implementation
- Composition Root
- Protocol
- Mock

Practice:

Explain why Dependency Injection improves maintainability.

---

### Notes

Document:

- Dependency graph.
- Constructor Injection.
- Common mistakes.
- Protocol design.
- Lifetime rules.

---

### Reflection

Ask yourself:

- Could I replace this dependency easily?
- Is this object tightly coupled?
- Are dependencies obvious?

---

## Mini Project

Refactor an application using Constructor Injection.

Requirements

- Protocol abstractions.
- No global singletons.
- Replace concrete implementations with injected services.
- Prepare for testing.

---

## Exit Criteria

✓ Explain Dependency Injection.

✓ Use Constructor Injection confidently.

✓ Reduce coupling.

✓ Design replaceable dependencies.

✓ Understand Dependency Inversion.

---

# Module 4 — Feature-Based Architecture

## Core Topics

- Feature-first Organization
- Shared Module
- Common Components
- Feature Isolation
- Feature Communication
- Folder Structure
- Scalability
- Team Collaboration
- Code Ownership

---

## Learning Objectives

After completing this module you should understand:

- Why feature-based architecture scales better.
- How to organize applications around business features.
- How to reduce dependencies between features.
- How multiple developers work on the same application.
- How to prepare projects for modularization.

---

## Parallel Learning Layers

### Git

Learn:

- Create one branch per feature.
- Keep commits feature-focused.
- Review changes feature by feature.

Practice:

Never mix unrelated features in one branch.

---

### Xcode

Learn:

- Feature groups.
- Project organization.
- Build targets (introduction).

Practice:

Organize applications by feature instead of screen.

---

### Apple Documentation

Read:

- Swift Packages
- Xcode Project Organization
- Observation Framework

Goal

Understand how Apple's tools support scalable architecture.

---

### WWDC

Recommended Topics

- Organizing Swift Projects
- Scaling SwiftUI Applications
- Modular Development

Goal

Learn how Apple structures growing applications.

---

### Best Practices

Learn:

- Group by feature—not by file type.
- Keep feature boundaries clear.
- Share only reusable code.
- Keep dependencies one-directional.
- Minimize cross-feature communication.

Avoid:

- Huge Shared folders.
- Random Helpers folders.
- Cross-feature imports.
- Feature coupling.

---

### Design Thinking

Questions to ask:

- Is this code feature-specific?
- Should this become shared?
- Will another feature use this?

---

### Architecture Thinking

Separate:

- Features
- Shared Components
- Shared Services
- Infrastructure

Understand ownership of every module.

---

### Open Source

Study:

Production applications.

Observe:

- Feature folders.
- Shared UI.
- Shared Services.
- Dependency boundaries.

Ask:

"Why was this placed inside Shared instead of Feature?"

---

### AI

Use AI to:

- Review folder organization.
- Challenge architecture.
- Compare project structures.

Avoid:

- Letting AI decide folder organization without understanding your project.

---

### English

Vocabulary

- Feature
- Module
- Boundary
- Shared
- Ownership
- Isolation
- Organization

Practice:

Explain your folder structure to another developer.

---

### Notes

Document:

- Folder conventions.
- Shared module rules.
- Feature responsibilities.
- Naming conventions.

---

### Reflection

Ask yourself:

- Can another developer find code easily?
- Is every feature independent?
- Is shared code actually reusable?

---

## Mini Project

Refactor an existing application into a feature-first structure.

Requirements

- Feature folders.
- Shared UI module.
- Shared Services.
- Clear ownership.
- Minimal coupling.

---

## Exit Criteria

✓ Organize projects by feature.

✓ Build scalable folder structures.

✓ Understand feature boundaries.

✓ Reduce cross-feature dependencies.

---
# Module 5 — Modularization & Swift Packages

## Core Topics

- What is Modularization?
- Why Modularize?
- Swift Package Manager (SPM)
- Creating Swift Packages
- Local Packages
- Remote Packages
- Package Dependencies
- Public vs Internal APIs
- Package Boundaries
- Dependency Graph
- Build Performance
- Package Resources

---

## Learning Objectives

After completing this module you should understand:

- Why modularization becomes important as projects grow.
- How Swift Packages improve scalability.
- How to design package boundaries.
- How to reduce build times.
- How to build reusable modules across multiple applications.
- When modularization is beneficial—and when it is unnecessary.

---

## Parallel Learning Layers

### Git

Learn:

- Keep each package in its own branch when possible.
- Track package changes independently.
- Tag stable package versions.

Practice:

Extract one reusable feature into a Swift Package.

---

### Xcode

Learn:

- Package Dependencies
- Local Packages
- Package Resources
- Build System
- Package Testing

Practice:

Move reusable code into local packages.

---

### Apple Documentation

Read:

- Swift Package Manager
- Package.swift
- Package Resources
- Package Plugins (Overview)

Goal

Understand Apple's native modularization solution.

---

### WWDC

Recommended Topics

- Meet Swift Package Manager
- Swift Packages in Xcode
- Modular Swift Development

Goal

Learn how Apple expects projects to scale.

---

### Best Practices

Learn:

- Modularize only when necessary.
- Keep package APIs small.
- Hide implementation details.
- Design stable public interfaces.
- One responsibility per package.

Avoid:

- Creating dozens of tiny packages.
- Circular package dependencies.
- Exposing unnecessary APIs.
- Premature modularization.

---

### Design Thinking

Questions to ask:

- Will another project reuse this code?
- Does this module have one responsibility?
- Would modularization reduce complexity?

---

### Architecture Thinking

Understand package responsibilities:

- Feature Packages
- Shared UI
- Core
- Networking
- Persistence
- Utilities

Each package should have a clear purpose.

---

### Open Source

Study:

Large modular Swift applications.

Observe:

- Package organization.
- Public APIs.
- Dependency graph.
- Shared modules.

Ask:

"Why did they create this package?"

---

### AI

Use AI to:

- Review package boundaries.
- Compare modularization strategies.
- Challenge dependency graphs.

Avoid:

- Creating packages simply because AI suggested them.

---

### English

Vocabulary

- Module
- Package
- Dependency
- Public API
- Internal
- Reusable
- Distribution

Practice:

Explain why a package exists.

---

### Notes

Document:

- Package responsibilities.
- Dependency graph.
- Public APIs.
- Versioning strategy.

---

### Reflection

Ask yourself:

- Is this package solving a real problem?
- Could another application reuse it?
- Is the API too large?

---

## Mini Project

Extract from an existing application:

- Networking Package
- Design System Package
- Utilities Package

Requirements

- Public APIs
- Internal implementation
- Local Package references
- Documentation

---

## Exit Criteria

✓ Create Swift Packages.

✓ Design package boundaries.

✓ Build reusable modules.

✓ Understand dependency graphs.

✓ Scale projects using modularization.

---

# Module 6 — Tuist

## Core Topics

- Why Tuist?
- Project Generation
- Project.swift
- Workspace.swift
- Configurations
- Targets
- Schemes
- Packages
- Build Settings
- Environment Configuration
- Project Automation
- Project Templates

---

## Learning Objectives

After completing this module you should understand:

- Why large teams use Tuist.
- How Tuist improves project maintenance.
- How projects are generated.
- How to automate project configuration.
- How Tuist works together with Swift Packages.

---

## Parallel Learning Layers

### Git

Learn:

- Track Project.swift separately.
- Keep generated files out of Git.
- Review project configuration changes carefully.

Practice:

Version-control only project definitions.

---

### Xcode

Learn:

- Generated Projects
- Schemes
- Build Configurations
- Workspace Organization

Practice:

Generate projects instead of maintaining them manually.

---

### Apple Documentation

Read:

- Xcode Build Settings
- Build Configurations
- Schemes
- Swift Package Manager

Goal

Understand the concepts Tuist builds upon.

---

### Tuist Documentation

Read:

- Getting Started
- Project.swift
- Targets
- Settings
- Configurations
- Templates

Goal

Become comfortable reading official Tuist documentation.

---

### Best Practices

Learn:

- Keep Project.swift readable.
- Separate configuration from implementation.
- Use templates for consistency.
- Generate—not manually edit—projects.

Avoid:

- Complex project definitions.
- Duplicated configuration.
- Manual project maintenance.

---

### Design Thinking

Questions to ask:

- Can this project configuration be simplified?
- Is automation reducing manual work?
- Will a new developer understand this setup?

---

### Architecture Thinking

Understand:

Tuist manages project structure—not application architecture.

Keep concerns separate:

- Build System
- Project Configuration
- Application Architecture

---

### Open Source

Study:

Production Tuist projects.

Observe:

- Folder structure.
- Project.swift organization.
- Templates.
- Environment handling.

Ask:

"What problems is Tuist solving here?"

---

### AI

Use AI to:

- Explain Project.swift.
- Review Tuist configuration.
- Compare project organization strategies.

Avoid:

- Copying generated configurations without understanding them.

---

### English

Vocabulary

- Target
- Scheme
- Workspace
- Configuration
- Generation
- Template
- Build System

Practice:

Explain how Tuist generates an Xcode project.

---

### Notes

Document:

- Project structure.
- Targets.
- Build configurations.
- Common commands.
- Template ideas.

---

### Reflection

Ask yourself:

- Why use Tuist instead of a manually managed project?
- Is my configuration easy to maintain?
- Could another developer understand this setup?

---

## Mini Project

Create a Tuist-based workspace containing:

- App Target
- Core Package
- Networking Package
- Design System Package
- Unit Test Target
- UI Test Target

Requirements

- Multiple Build Configurations
- Local Swift Packages
- Clean Project Structure
- Generated Workspace

---

## Exit Criteria

✓ Build projects with Tuist.

✓ Organize scalable workspaces.

✓ Configure targets and schemes.

✓ Understand project automation.

✓ Maintain projects professionally.

---
# Module 7 — Repository Pattern

## Core Topics

- What is the Repository Pattern?
- Why use a Repository?
- Repository vs Service
- Repository Interface
- Local Data Source
- Remote Data Source
- Data Mapping
- Domain Models
- DTOs
- Caching Strategy
- Offline-first (Introduction)

---

## Learning Objectives

After completing this module you should understand:

- Why repositories exist.
- How repositories hide implementation details.
- How to combine local and remote data sources.
- How repositories improve maintainability.
- How repositories simplify testing.
- When a repository is unnecessary.

---

## Parallel Learning Layers

### Git

Learn:

- Keep repository refactoring separate from feature work.
- Track changes to data flow independently.

Practice:

Commit after introducing each repository.

---

### Xcode

Learn:

- Organize repositories.
- Debug data flow.
- Navigate dependencies.

Practice:

Keep repositories inside the data layer.

---

### Apple Documentation

Read:

- SwiftData
- URLSession
- Async/Await
- Codable

Goal

Understand the technologies repositories coordinate.

---

### WWDC

Recommended Topics

- Meet SwiftData
- Modern Networking
- Data Essentials in SwiftUI

Goal

Understand Apple's recommended data flow.

---

### Best Practices

Learn:

- One repository per business domain.
- Hide implementation details.
- Keep repositories focused.
- Return domain models.
- Keep networking and persistence separate.

Avoid:

- Repository doing business logic.
- One giant repository.
- Views accessing SwiftData directly.
- Views accessing URLSession directly.

---

### Design Thinking

Questions to ask:

- Where should this data come from?
- Does the caller need to know the source?
- Could the storage implementation change later?

---

### Architecture Thinking

Understand:

View

↓

ViewModel

↓

Repository

↓

Local Data Source

↓

Remote Data Source

Repositories coordinate data—they don't own business rules.

---

### Open Source

Study:

Projects using repositories.

Observe:

- Repository interfaces.
- Local vs Remote.
- Caching.
- Mapping.

Ask:

"Why was a repository introduced?"

---

### AI

Use AI to:

- Review repository boundaries.
- Compare repository designs.
- Explain caching strategies.

Avoid:

- Creating repositories for every tiny object.

---

### English

Vocabulary

- Repository
- Data Source
- Cache
- Mapping
- Synchronization
- DTO
- Domain Model

Practice:

Explain how data moves through the repository.

---

### Notes

Document:

- Repository responsibilities.
- Data flow.
- Mapping rules.
- Caching strategy.

---

### Reflection

Ask yourself:

- Does this repository hide implementation details?
- Can storage change without affecting UI?
- Is business logic leaking into the repository?

---

## Mini Project

Build a News Repository supporting:

- Local Cache
- Remote API
- Offline Reading
- Automatic Synchronization
- Domain Models

---

## Exit Criteria

✓ Explain the Repository Pattern.

✓ Separate local and remote data.

✓ Build reusable repositories.

✓ Design clean data flow.

---

# Module 8 — Services & Managers

## Core Topics

- What is a Service?
- What is a Manager?
- Service Layer
- Networking Service
- Storage Service
- Authentication Service
- Notification Service
- Location Service
- Analytics Service
- Logging Service
- Configuration Service

---

## Learning Objectives

After completing this module you should understand:

- The responsibility of services.
- When a manager is appropriate.
- How services interact with repositories.
- How to organize infrastructure code.
- Why services should remain independent.

---

## Parallel Learning Layers

### Git

Learn:

- Create dedicated commits for service changes.
- Separate infrastructure refactoring from feature work.

Practice:

Keep service implementations isolated.

---

### Xcode

Learn:

- Service folders.
- Shared infrastructure.
- Environment configuration.

Practice:

Organize services consistently across projects.

---

### Apple Documentation

Read:

- URLSession
- UserNotifications
- CoreLocation
- SwiftData

Goal

Understand the frameworks behind your services.

---

### WWDC

Recommended Topics

- Modern Networking
- SwiftData
- Core Location
- UserNotifications

Goal

Learn how Apple frameworks become reusable services.

---

### Best Practices

Learn:

- One responsibility per service.
- Stateless services whenever possible.
- Reusable infrastructure.
- Dependency Injection.
- Small public APIs.

Avoid:

- God Managers.
- One huge AppManager.
- Business logic inside services.
- Global mutable services.

---

### Design Thinking

Questions to ask:

- Is this really a service?
- Does this belong inside a repository?
- Will multiple features reuse this?

---

### Architecture Thinking

Understand relationships:

View

↓

ViewModel

↓

Repository

↓

Service

↓

Apple Framework

Services wrap platform APIs.

Repositories coordinate business data.

---

### Open Source

Study:

Production applications.

Observe:

- Service organization.
- Dependency Injection.
- Infrastructure layer.
- API boundaries.

Ask:

"Why was this implemented as a service?"

---

### AI

Use AI to:

- Review service responsibilities.
- Compare service designs.
- Challenge architecture.

Avoid:

- Creating services without a clear purpose.

---

### English

Vocabulary

- Service
- Manager
- Infrastructure
- Wrapper
- Configuration
- Analytics
- Logging

Practice:

Explain the responsibility of every service.

---

### Notes

Document:

- Service responsibilities.
- Public APIs.
- Dependencies.
- Configuration.

---

### Reflection

Ask yourself:

- Is this service doing one job?
- Could another application reuse it?
- Does this belong somewhere else?

---

## Mini Project

Build reusable services for:

- Networking
- Storage
- Authentication
- Notifications
- Location
- Analytics

Requirements

- Dependency Injection
- Protocol abstractions
- Independent testing
- Documentation

---

## Exit Criteria

✓ Design reusable services.

✓ Separate infrastructure from business logic.

✓ Avoid God Managers.

✓ Build maintainable service layers.

---

# Module 9 — Error Handling Strategy

## Core Topics

- Swift Error Handling
- Error Types
- Domain Errors
- Infrastructure Errors
- Result Type
- Throwing Functions
- Recovery Strategies
- User-Friendly Errors
- Retry Mechanisms
- Logging
- Assertions vs Fatal Errors

---

## Learning Objectives

After completing this module you should understand:

- Why good error handling improves software quality.
- How to categorize different types of errors.
- How to present meaningful errors to users.
- When to recover automatically.
- When an application should fail safely.
- How error handling affects architecture.

---

## Parallel Learning Layers

### Git

Learn:

- Separate error-handling improvements from feature work.
- Document why recovery strategies changed.

Practice:

Keep commits focused on reliability improvements.

---

### Xcode

Learn:

- Exception Breakpoints
- Symbolic Breakpoints
- Console Debugging
- Logging

Practice:

Debug failures instead of hiding them.

---

### Apple Documentation

Read:

- Error Handling
- Result
- OSLog
- Assertions

Goal

Understand Apple's recommended error-handling practices.

---

### WWDC

Recommended Topics

- Modern Error Handling
- Debugging Swift
- Logging Best Practices

Goal

Learn how professional applications handle failures.

---

### Best Practices

Learn:

- Create meaningful error types.
- Show actionable user messages.
- Log technical details separately.
- Fail gracefully.
- Recover automatically whenever reasonable.

Avoid:

- Empty catch blocks.
- Force unwraps.
- Silent failures.
- Showing raw system errors to users.
- Using fatalError() in production code.

---

### Design Thinking

Questions to ask:

- Can the user recover?
- Should this failure be hidden?
- What is the best experience after an error?

---

### Architecture Thinking

Separate:

- Infrastructure Errors
- Domain Errors
- Presentation Errors

Each layer should translate errors appropriately instead of exposing implementation details.

---

### Open Source

Study:

Production applications.

Observe:

- Error enums.
- Retry logic.
- User messaging.
- Logging.

Ask:

"How do they recover from failure?"

---

### AI

Use AI to:

- Review error hierarchies.
- Compare recovery strategies.
- Challenge exception handling.

Avoid:

- Using AI-generated error handling without understanding every case.

---

### English

Vocabulary

- Exception
- Failure
- Recovery
- Retry
- Logging
- Assertion
- Diagnostic

Practice:

Explain how your application handles failures.

---

### Notes

Document:

- Error hierarchy.
- Recovery flow.
- Logging strategy.
- Retry rules.

---

### Reflection

Ask yourself:

- Does every failure have a recovery strategy?
- Would users understand this error?
- Am I exposing implementation details?

---

## Mini Project

Improve an existing application by adding:

- Custom Error Types
- Retry Mechanism
- Offline Handling
- User-Friendly Error Messages
- Centralized Logging

---

## Exit Criteria

✓ Design robust error hierarchies.

✓ Handle failures gracefully.

✓ Log useful diagnostics.

✓ Build reliable applications.

---

# Module 10 — Scalability & Maintainability

## Core Topics

- Technical Debt
- Refactoring
- Code Smells
- Naming
- Documentation
- Code Reviews
- Folder Organization
- Feature Growth
- Maintainability
- Readability
- Reusability

---

## Learning Objectives

After completing this module you should understand:

- Why software becomes difficult to maintain.
- How to recognize technical debt.
- How to continuously improve code quality.
- How to prepare projects for long-term growth.
- Why readability is more important than cleverness.

---

## Parallel Learning Layers

### Git

Learn:

- Separate refactoring commits.
- Never mix refactoring with new features.
- Write meaningful commit messages explaining improvements.

Practice:

Create dedicated pull requests for maintainability improvements.

---

### Xcode

Learn:

- Refactoring Tools
- Rename
- Extract Method
- Find References
- Code Navigation

Practice:

Use Xcode's refactoring tools instead of manual edits whenever possible.

---

### Apple Documentation

Read:

- Swift API Design Guidelines
- Documentation Comments
- Access Control

Goal

Write code that feels like Apple's frameworks.

---

### WWDC

Recommended Topics

- Writing Great Swift Code
- API Design
- Code Organization
- Swift Best Practices

Goal

Learn Apple's philosophy for maintainable code.

---

### Best Practices

Learn:

- Write code for humans first.
- Keep functions small.
- Keep files focused.
- Prefer clarity over cleverness.
- Refactor continuously.

Avoid:

- Long methods.
- Massive files.
- Deep nesting.
- Abbreviated names.
- Duplicate logic.

---

### Design Thinking

Questions to ask:

- Would another developer understand this?
- Is this the simplest solution?
- Can this code be reused?

---

### Architecture Thinking

Understand maintainability across:

- UI
- Presentation
- Domain
- Data
- Infrastructure

Every layer should remain understandable and replaceable.

---

### Open Source

Study:

High-quality production repositories.

Observe:

- Naming conventions.
- Folder organization.
- Documentation.
- Refactoring history.

Ask:

"Why is this code easy to read?"

---

### AI

Use AI to:

- Review readability.
- Suggest refactoring opportunities.
- Identify code smells.

Avoid:

- Accepting refactoring suggestions blindly.

---

### English

Vocabulary

- Maintainability
- Readability
- Refactoring
- Technical Debt
- Code Smell
- Documentation
- Reusability

Practice:

Explain why one implementation is more maintainable than another.

---

### Notes

Document:

- Common code smells.
- Refactoring patterns.
- Naming conventions.
- Documentation standards.

---

### Reflection

Ask yourself:

- Would I enjoy maintaining this code in two years?
- Is the intent obvious?
- Can new developers contribute quickly?

---

## Mini Project

Take one of your previous projects and perform a full maintainability review.

Requirements

- Improve naming.
- Reduce duplication.
- Refactor large files.
- Improve documentation.
- Remove unnecessary complexity.

Document every improvement and explain why it increased maintainability.

---

## Exit Criteria

✓ Recognize technical debt.

✓ Refactor confidently.

✓ Write maintainable code.

✓ Design projects that scale over time.

---
# Module 11 — Architecture Decision Making

## Core Topics

- Engineering Trade-offs
- Architecture Decision Records (ADR)
- Buy vs Build
- Native vs Third-party Libraries
- Simplicity vs Flexibility
- Scalability
- Maintainability
- Technical Debt
- Cost of Change
- Future-proofing
- YAGNI (You Aren't Gonna Need It)
- KISS (Keep It Simple, Stupid)

---

## Learning Objectives

After completing this module you should understand:

- How senior engineers make architecture decisions.
- Why there is rarely a perfect solution.
- How to evaluate trade-offs objectively.
- How to justify architectural decisions.
- How to balance today's needs with future scalability.
- Why simplicity usually wins.

---

## Parallel Learning Layers

### Git

Learn:

- Record architecture changes separately.
- Write commits explaining architectural reasoning.
- Keep Architecture Decision Records (ADRs) inside the repository.

Practice:

Whenever a major architectural decision is made, document:

- The problem
- Available options
- Chosen solution
- Trade-offs
- Why alternatives were rejected

---

### Xcode

Learn:

- Project settings affected by architectural choices.
- Build configurations.
- Package dependencies.
- Project capabilities.

Practice:

Understand how project configuration influences architecture.

---

### Apple Documentation

Read:

- Swift API Design Guidelines
- Swift Package Manager
- Observation Framework
- Swift Concurrency
- SwiftData

Goal

Learn Apple's philosophy before introducing external solutions.

---

### WWDC

Recommended Topics

- API Design
- Modern Swift
- App Architecture
- Swift Evolution
- What's New in Swift

Goal

Observe how Apple engineers justify engineering decisions.

---

### Best Practices

Learn:

- Prefer simple solutions.
- Delay complexity until necessary.
- Measure before optimizing.
- Remove unnecessary abstractions.
- Design for today's requirements while allowing reasonable growth.
- Challenge every dependency.

Avoid:

- Overengineering.
- Premature optimization.
- Architecture driven by trends.
- Choosing technologies because they are popular.
- Building generic systems for imaginary future problems.

---

### Design Thinking

Questions to ask:

- What problem am I solving?
- Is there a simpler solution?
- Will users notice this complexity?
- What happens if requirements change?

---

### Architecture Thinking

Evaluate every decision using:

- Maintainability
- Scalability
- Testability
- Performance
- Readability
- Team Productivity
- Cost
- Learning Curve
- Long-term Ownership

Remember:

Architecture is about making **good trade-offs**, not perfect ones.

---

### Open Source

Study:

Large production applications.

Observe:

- Why specific frameworks were chosen.
- When third-party libraries were avoided.
- Dependency management.
- Evolution of architecture over time.

Ask:

"What problem was this decision solving?"

---

### AI

Use AI to:

- Challenge architecture.
- Compare trade-offs.
- Review decisions.
- Explain alternative approaches.

Avoid:

- Letting AI make engineering decisions for you.

AI should provide perspectives—not answers.

---

### English

Vocabulary

- Trade-off
- Decision
- Maintainability
- Simplicity
- Complexity
- Scalability
- Flexibility
- Ownership
- Architecture

Practice:

Explain why you chose one solution over another.

---

### Notes

Maintain an **Architecture Decision Journal** containing:

- Problem
- Constraints
- Possible Solutions
- Final Decision
- Trade-offs
- Lessons Learned

---

### Reflection

Ask yourself:

- Is this the simplest solution?
- Can I justify every dependency?
- Would another senior engineer agree with this decision?
- Am I solving today's problem or tomorrow's imaginary problem?

---

## Mini Project

Review one of your previous applications.

Create an Architecture Decision Record (ADR) for:

- Folder Structure
- MVVM
- Dependency Injection
- Repository Pattern
- Swift Packages
- Tuist
- SwiftData
- Networking

For every decision explain:

- Why it was chosen.
- Alternatives considered.
- Trade-offs.
- Future impact.

---

## Exit Criteria

✓ Evaluate architectural trade-offs.

✓ Write Architecture Decision Records.

✓ Choose technologies intentionally.

✓ Avoid unnecessary complexity.

✓ Think like a senior engineer.

---

# Phase Project

Build a **production-quality iOS application** that demonstrates everything learned in this phase.

## Requirements

Architecture

- MVVM
- Dependency Injection
- Repository Pattern
- Feature-based Architecture
- Layered Architecture
- Services
- Swift Packages
- Tuist

Application Quality

- Clean Folder Structure
- Consistent Naming
- Reusable Components
- Proper Error Handling
- Documentation
- Scalable Design

Technical Requirements

- SwiftData
- URLSession
- Async/Await
- Apple Framework Integration
- Local Storage
- Networking
- Offline Support (basic)
- Unit-test ready architecture

Documentation

Create documentation covering:

- Folder Structure
- Dependency Graph
- Architecture Diagram
- Repository Flow
- Service Responsibilities
- Package Structure
- ADRs
- Future Improvements

---

# Final Exit Criteria

Before moving to Phase 05 you should confidently be able to:

Architecture

✓ Design a scalable application.

✓ Explain every architectural layer.

✓ Build reusable services.

✓ Apply MVVM correctly.

✓ Apply Dependency Injection confidently.

✓ Design repositories.

✓ Organize projects by feature.

Project Organization

✓ Create Swift Packages.

✓ Configure Tuist projects.

✓ Separate responsibilities correctly.

✓ Keep dependencies flowing in one direction.

Engineering

✓ Evaluate architectural trade-offs.

✓ Write maintainable code.

✓ Refactor confidently.

✓ Build projects another developer can understand.

Mindset

✓ Think about maintainability before writing code.

✓ Design software for change.

✓ Make intentional engineering decisions.

---

# Phase Reflection

Before moving to **Phase 05**, answer these questions honestly.

## Architecture

- Can I explain every architectural layer without looking at notes?
- Can I identify responsibilities quickly?
- Do I understand why architecture exists?

---

## MVVM

- Can I explain the responsibility of View, ViewModel, and Model?
- Can I recognize when a ViewModel is becoming too large?
- Do I understand data flow?

---

## Dependency Injection

- Can I replace dependencies easily?
- Do I avoid global state?
- Are dependencies explicit?

---

## Feature Organization

- Can another developer immediately understand my project?
- Are features independent?
- Is shared code actually reusable?

---

## Repositories

- Can I separate business logic from data access?
- Can storage implementations change without affecting UI?
- Is my repository hiding implementation details?

---

## Services

- Does every service have one responsibility?
- Am I avoiding God Managers?
- Can services be reused across projects?

---

## Maintainability

- Is my project easy to navigate?
- Would I enjoy maintaining this application in two years?
- Can another developer contribute without confusion?

---

## Engineering Decisions

- Can I justify every dependency?
- Can I explain why I chose each framework?
- Am I avoiding unnecessary complexity?

---

If **every answer is "Yes"**, you're ready for the next phase.

If any answer is **"No"**, revisit the relevant module before moving forward.

---

# What You Can Build After Phase 04

After completing this phase, you should be capable of building applications with architecture similar to professional production projects.

Examples include:

- Expense Tracker
- Habit Tracking App
- Fitness Tracker
- Notes Application
- Weather Application
- Task Manager
- Movie Database
- Recipe App
- Travel Planner
- E-commerce Catalog

The focus is **not** on the app idea itself, but on producing software that is clean, scalable, maintainable, and easy to extend.

---

# Next Phase

➡️ **Phase 05 — Testing & Software Quality**

In the next phase you will learn how professional engineers ensure software correctness through:

- Unit Testing
- Integration Testing
- UI Testing
- Test-Driven Development (TDD)
- Mocking
- Continuous Testing
- Code Coverage
- Quality Assurance

The goal is to make your architecture not only scalable, but also **reliable and confidently maintainable**.