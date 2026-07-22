# Phase 04 — Professional App Architecture

> **Purpose:** Move from writing working code to designing maintainable systems.

---

# Goal

Move from writing working code to designing maintainable systems.

---

# Learning Outcomes

By the end of this phase you should be able to:

- Organize projects.
- Design maintainable features.
- Understand architectural trade-offs.
- Build modular apps.
- Apply SOLID and Clean Architecture with judgment.

---

# Module 1 — Project Organization

## Core Topics

- Folder structure
- Feature organization
- Separation of concerns
- Naming conventions
- Xcode groups vs folders

---

## Learning Objectives

After completing this module you should be able to:

- Understand Folder structure and recognize when it is the right tool.
- Understand Feature organization and recognize when it is the right tool.
- Understand Separation of concerns and recognize when it is the right tool.
- Understand Naming conventions and recognize when it is the right tool.
- Understand Xcode groups vs folders and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use pull requests for architecture refactors.
- Write PR descriptions that explain trade-offs.
- Keep generated project noise out of Git when using Tuist.

### Xcode

- Project navigator organization
- Find call hierarchy
- Refactor tools

### Apple Documentation

- Apple guidance on app structure when available
- Swift Package Manager docs

### WWDC

- Modularization / package sessions when relevant

### Best Practices

- Prefer clarity when working with Folder structure.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Folder structure solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study folder structure of a modular open-source app

### AI

- Ask AI to explain Folder structure after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Folder structure in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Folder structure, Feature organization, Separation of concerns, Naming conventions.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Folder structure to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Reorganize an existing app into feature-based folders and document the rules.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Folder structure correctly in a realistic scenario and explain the trade-offs.
- Use Feature organization correctly in a realistic scenario and explain the trade-offs.
- Use Separation of concerns correctly in a realistic scenario and explain the trade-offs.
- Use Naming conventions correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 2 — MVVM

## Core Topics

- Model
- View
- ViewModel
- Responsibilities
- Data flow
- Thin Views

---

## Learning Objectives

After completing this module you should be able to:

- Understand Model and recognize when it is the right tool.
- Understand View and recognize when it is the right tool.
- Understand ViewModel and recognize when it is the right tool.
- Understand Responsibilities and recognize when it is the right tool.
- Understand Data flow and recognize when it is the right tool.
- Connect the remaining core topics into one coherent mental model.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use pull requests for architecture refactors.
- Write PR descriptions that explain trade-offs.
- Keep generated project noise out of Git when using Tuist.

### Xcode

- Canvas
- Preview
- Live Preview
- View Debugger

### Apple Documentation

- SwiftUI data flow docs
- MVVM as applied to Apple platforms

### WWDC

- Data Essentials in SwiftUI

### Best Practices

- Keep Views thin
- Keep ViewModels free of view hierarchy details

### Design Thinking

- What belongs in Model vs ViewModel vs View?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study view structure in a small SwiftUI open-source app

### AI

- Ask AI to explain Model after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Model in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Model, View, ViewModel, Responsibilities.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Model to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Refactor one screen into clear Model, View, and ViewModel responsibilities.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Model correctly in a realistic scenario and explain the trade-offs.
- Use View correctly in a realistic scenario and explain the trade-offs.
- Use ViewModel correctly in a realistic scenario and explain the trade-offs.
- Use Responsibilities correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 3 — Dependency Injection

## Core Topics

- Constructor injection
- Protocol-based dependencies
- Dependency inversion
- Composition root
- Testability benefits

---

## Learning Objectives

After completing this module you should be able to:

- Understand Constructor injection and recognize when it is the right tool.
- Understand Protocol-based dependencies and recognize when it is the right tool.
- Understand Dependency inversion and recognize when it is the right tool.
- Understand Composition root and recognize when it is the right tool.
- Understand Testability benefits and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use pull requests for architecture refactors.
- Write PR descriptions that explain trade-offs.
- Keep generated project noise out of Git when using Tuist.

### Xcode

- Test Navigator
- Run selected tests
- Coverage report
- Debug failing tests

### Apple Documentation

- XCTest
- Testing in Xcode

### WWDC

- Testing your apps in Xcode
- XCTest related sessions

### Best Practices

- Prefer clarity when working with Constructor injection.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Constructor injection solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Read tests in a small open-source iOS library

### AI

- Ask AI to explain Constructor injection after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Constructor injection in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Constructor injection, Protocol-based dependencies, Dependency inversion, Composition root.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Constructor injection to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Introduce constructor injection for a service used by a ViewModel.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Constructor injection correctly in a realistic scenario and explain the trade-offs.
- Use Protocol-based dependencies correctly in a realistic scenario and explain the trade-offs.
- Use Dependency inversion correctly in a realistic scenario and explain the trade-offs.
- Use Composition root correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 4 — SOLID Principles

## Core Topics

- Single Responsibility Principle
- Open-Closed Principle
- Liskov Substitution Principle
- Interface Segregation Principle
- Dependency Inversion Principle

---

## Learning Objectives

After completing this module you should be able to:

- Understand Single Responsibility Principle and recognize when it is the right tool.
- Understand Open-Closed Principle and recognize when it is the right tool.
- Understand Liskov Substitution Principle and recognize when it is the right tool.
- Understand Interface Segregation Principle and recognize when it is the right tool.
- Understand Dependency Inversion Principle and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use pull requests for architecture refactors.
- Write PR descriptions that explain trade-offs.
- Keep generated project noise out of Git when using Tuist.

### Xcode

- Project navigator organization
- Find call hierarchy
- Refactor tools

### Apple Documentation

- Apple guidance on app structure when available
- Swift Package Manager docs

### WWDC

- Modularization / package sessions when relevant

### Best Practices

- Prefer clarity when working with Single Responsibility Principle.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Single Responsibility Principle solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study folder structure of a modular open-source app

### AI

- Ask AI to explain Single Responsibility Principle after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Single Responsibility Principle in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Single Responsibility Principle, Open-Closed Principle, Liskov Substitution Principle, Interface Segregation Principle.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Single Responsibility Principle to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Audit one feature against SOLID and refactor the highest-impact violation.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Single Responsibility Principle correctly in a realistic scenario and explain the trade-offs.
- Use Open-Closed Principle correctly in a realistic scenario and explain the trade-offs.
- Use Liskov Substitution Principle correctly in a realistic scenario and explain the trade-offs.
- Use Interface Segregation Principle correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 5 — Clean Architecture

## Core Topics

- Domain layer
- Data layer
- Presentation layer
- Dependency rule
- Use cases
- Boundaries

---

## Learning Objectives

After completing this module you should be able to:

- Understand Domain layer and recognize when it is the right tool.
- Understand Data layer and recognize when it is the right tool.
- Understand Presentation layer and recognize when it is the right tool.
- Understand Dependency rule and recognize when it is the right tool.
- Understand Use cases and recognize when it is the right tool.
- Connect the remaining core topics into one coherent mental model.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use pull requests for architecture refactors.
- Write PR descriptions that explain trade-offs.
- Keep generated project noise out of Git when using Tuist.

### Xcode

- Project navigator organization
- Find call hierarchy
- Refactor tools

### Apple Documentation

- Dependency Rule resources
- Swift Package Manager documentation

### WWDC

- Modularize sessions when relevant

### Best Practices

- Dependencies point inward
- Domain stays independent of frameworks

### Design Thinking

- Why separate Domain, Data, and Presentation?

### Architecture Thinking

- Draw dependency arrows before coding
- Protect the domain from UI and networking details

### Open Source

- Study folder structure of a modular open-source app

### AI

- Ask AI to explain Domain layer after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Domain layer in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Domain layer, Data layer, Presentation layer, Dependency rule.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Domain layer to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Implement one feature with Domain, Data, and Presentation boundaries.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Domain layer correctly in a realistic scenario and explain the trade-offs.
- Use Data layer correctly in a realistic scenario and explain the trade-offs.
- Use Presentation layer correctly in a realistic scenario and explain the trade-offs.
- Use Dependency rule correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 6 — Modularization

## Core Topics

- Swift Package Manager
- Reusable modules
- Module boundaries
- Public API design
- Dependency graphs

---

## Learning Objectives

After completing this module you should be able to:

- Understand Swift Package Manager and recognize when it is the right tool.
- Understand Reusable modules and recognize when it is the right tool.
- Understand Module boundaries and recognize when it is the right tool.
- Understand Public API design and recognize when it is the right tool.
- Understand Dependency graphs and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use pull requests for architecture refactors.
- Write PR descriptions that explain trade-offs.
- Keep generated project noise out of Git when using Tuist.

### Xcode

- Project navigator organization
- Find call hierarchy
- Refactor tools

### Apple Documentation

- Apple guidance on app structure when available
- Swift Package Manager docs

### WWDC

- Modularization / package sessions when relevant

### Best Practices

- Prefer clarity when working with Swift Package Manager.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Swift Package Manager solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study folder structure of a modular open-source app

### AI

- Ask AI to explain Swift Package Manager after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Swift Package Manager in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Swift Package Manager, Reusable modules, Module boundaries, Public API design.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Swift Package Manager to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Extract a reusable Swift package from shared code.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Swift Package Manager correctly in a realistic scenario and explain the trade-offs.
- Use Reusable modules correctly in a realistic scenario and explain the trade-offs.
- Use Module boundaries correctly in a realistic scenario and explain the trade-offs.
- Use Public API design correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 7 — Tuist

## Core Topics

- Targets
- Schemes
- Configurations
- Project.swift
- Workspace generation
- Why Tuist

---

## Learning Objectives

After completing this module you should be able to:

- Understand Targets and recognize when it is the right tool.
- Understand Schemes and recognize when it is the right tool.
- Understand Configurations and recognize when it is the right tool.
- Understand Project.swift and recognize when it is the right tool.
- Understand Workspace generation and recognize when it is the right tool.
- Connect the remaining core topics into one coherent mental model.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use pull requests for architecture refactors.
- Write PR descriptions that explain trade-offs.
- Keep generated project noise out of Git when using Tuist.

### Xcode

- Inspect generated projects
- Compare schemes and configurations
- Understand target membership

### Apple Documentation

- Tuist documentation
- Xcode project concepts: targets, schemes, configurations

### WWDC

- No required WWDC session — use Tuist docs and project automation materials

### Best Practices

- Version Project.swift, not generated noise
- Keep configurations explicit

### Design Thinking

- What problem does Targets solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study folder structure of a modular open-source app

### AI

- Ask AI to explain Targets after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Targets in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Targets, Schemes, Configurations, Project.swift.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Targets to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Generate a sample workspace with Tuist targets, schemes, and configurations.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Targets correctly in a realistic scenario and explain the trade-offs.
- Use Schemes correctly in a realistic scenario and explain the trade-offs.
- Use Configurations correctly in a realistic scenario and explain the trade-offs.
- Use Project.swift correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 8 — Architecture Decision Making

## Core Topics

- Trade-off analysis
- Technical debt
- Architecture Decision Records
- When not to add architecture
- Team communication

---

## Learning Objectives

After completing this module you should be able to:

- Understand Trade-off analysis and recognize when it is the right tool.
- Understand Technical debt and recognize when it is the right tool.
- Understand Architecture Decision Records and recognize when it is the right tool.
- Understand When not to add architecture and recognize when it is the right tool.
- Understand Team communication and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use pull requests for architecture refactors.
- Write PR descriptions that explain trade-offs.
- Keep generated project noise out of Git when using Tuist.

### Xcode

- Project navigator organization
- Find call hierarchy
- Refactor tools

### Apple Documentation

- Apple guidance on app structure when available
- Swift Package Manager docs

### WWDC

- Modularization / package sessions when relevant

### Best Practices

- Prefer clarity when working with Trade-off analysis.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Trade-off analysis solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study folder structure of a modular open-source app

### AI

- Ask AI to explain Trade-off analysis after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Trade-off analysis in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Trade-off analysis, Technical debt, Architecture Decision Records, When not to add architecture.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Trade-off analysis to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Write Architecture Decision Records for two competing approaches and choose one.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Trade-off analysis correctly in a realistic scenario and explain the trade-offs.
- Use Technical debt correctly in a realistic scenario and explain the trade-offs.
- Use Architecture Decision Records correctly in a realistic scenario and explain the trade-offs.
- Use When not to add architecture correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Phase Project

Refactor an existing SwiftUI app into a production-style project using MVVM, DI, SOLID, Clean Architecture boundaries, SPM/Tuist, and document architectural decisions.

---

# Exit Criteria

You are ready for the next phase when you can:

- Organize large projects.
- Explain architecture decisions.
- Apply MVVM and DI.
- Apply SOLID and Clean Architecture thoughtfully.
- Build modular codebases.

---

# Next Phase

➡️ Phase 05 — Networking & Data
