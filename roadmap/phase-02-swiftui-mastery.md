# Phase 02 — SwiftUI Mastery

> **Purpose:** Learn SwiftUI by understanding how it works internally and how to build maintainable, production-quality user interfaces.

---

# Goal

Move beyond building screens. Learn to design reusable, performant, and maintainable SwiftUI applications.

---

# Learning Outcomes

By the end of this phase you should be able to:

- Build complex interfaces confidently.
- Understand SwiftUI's rendering system.
- Manage state correctly.
- Create reusable components.
- Navigate between screens using modern APIs.
- Debug common SwiftUI issues.
- Follow Apple's Human Interface Guidelines.

---

# Module 1 — SwiftUI Fundamentals

## Core Topics

- Declarative UI
- View protocol
- View hierarchy
- Body
- Modifiers

---

## Learning Objectives

After completing this module you should be able to:

- Understand Declarative UI and recognize when it is the right tool.
- Understand View protocol and recognize when it is the right tool.
- Understand View hierarchy and recognize when it is the right tool.
- Understand Body and recognize when it is the right tool.
- Understand Modifiers and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use feature branches for each SwiftUI screen.
- Make one commit per working preview.
- Open a draft pull request for review practice.

### Xcode

- SwiftUI App template
- Canvas
- Preview
- Live Preview

### Apple Documentation

- SwiftUI Overview
- View
- ViewBuilder
- App
- Scene

### WWDC

- Introduction to SwiftUI
- Demystify SwiftUI

### Best Practices

- Keep Views small
- Prefer composition
- Avoid massive body blocks

### Design Thinking

- Why is SwiftUI declarative?
- Why are Views structs?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study view structure in a small SwiftUI open-source app

### AI

- Ask AI to explain Declarative UI after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Declarative UI in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Declarative UI, View protocol, View hierarchy, Body.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Declarative UI to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Build simple profile-style screens with small composable Views.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Declarative UI correctly in a realistic scenario and explain the trade-offs.
- Use View protocol correctly in a realistic scenario and explain the trade-offs.
- Use View hierarchy correctly in a realistic scenario and explain the trade-offs.
- Use Body correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 2 — Layout System

## Core Topics

- VStack
- HStack
- ZStack
- Spacer
- Padding
- Frame
- Alignment
- GeometryReader
- Safe Area

---

## Learning Objectives

After completing this module you should be able to:

- Understand VStack and recognize when it is the right tool.
- Understand HStack and recognize when it is the right tool.
- Understand ZStack and recognize when it is the right tool.
- Understand Spacer and recognize when it is the right tool.
- Understand Padding and recognize when it is the right tool.
- Connect the remaining core topics into one coherent mental model.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use feature branches for each SwiftUI screen.
- Make one commit per working preview.
- Open a draft pull request for review practice.

### Xcode

- Canvas
- Preview
- Live Preview
- View Debugger

### Apple Documentation

- SwiftUI documentation for: VStack, HStack, ZStack, Spacer

### WWDC

- SwiftUI sessions matching this module

### Best Practices

- Prefer clarity when working with VStack.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does VStack solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study view structure in a small SwiftUI open-source app

### AI

- Ask AI to explain VStack after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of VStack in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document VStack, HStack, ZStack, Spacer.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach VStack to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Recreate common app layouts with stacks, spacer, frame, and safe area.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use VStack correctly in a realistic scenario and explain the trade-offs.
- Use HStack correctly in a realistic scenario and explain the trade-offs.
- Use ZStack correctly in a realistic scenario and explain the trade-offs.
- Use Spacer correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 3 — State Management

## Core Topics

- @State
- @Binding
- @StateObject
- @ObservedObject
- @Environment
- @EnvironmentObject
- Observation framework

---

## Learning Objectives

After completing this module you should be able to:

- Understand @State and recognize when it is the right tool.
- Understand @Binding and recognize when it is the right tool.
- Understand @StateObject and recognize when it is the right tool.
- Understand @ObservedObject and recognize when it is the right tool.
- Understand @Environment and recognize when it is the right tool.
- Connect the remaining core topics into one coherent mental model.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use feature branches for each SwiftUI screen.
- Make one commit per working preview.
- Open a draft pull request for review practice.

### Xcode

- Canvas
- Preview
- Live Preview
- View Debugger

### Apple Documentation

- Managing model data in your app
- Migrating from the Observable Object protocol to the Observable macro

### WWDC

- Data Essentials in SwiftUI
- Discover Observation in SwiftUI

### Best Practices

- Choose the narrowest property wrapper
- Avoid unnecessary object ownership

### Design Thinking

- Who owns this state?
- What should be derived vs stored?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study view structure in a small SwiftUI open-source app

### AI

- Ask AI to explain @State after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of @State in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document @State, @Binding, @StateObject, @ObservedObject.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach @State to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Build forms and interactive screens using the correct state tools.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use @State correctly in a realistic scenario and explain the trade-offs.
- Use @Binding correctly in a realistic scenario and explain the trade-offs.
- Use @StateObject correctly in a realistic scenario and explain the trade-offs.
- Use @ObservedObject correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 4 — Navigation

## Core Topics

- NavigationStack
- NavigationPath
- TabView
- Sheets
- Full Screen Covers
- Alerts
- Confirmation Dialogs

---

## Learning Objectives

After completing this module you should be able to:

- Understand NavigationStack and recognize when it is the right tool.
- Understand NavigationPath and recognize when it is the right tool.
- Understand TabView and recognize when it is the right tool.
- Understand Sheets and recognize when it is the right tool.
- Understand Full Screen Covers and recognize when it is the right tool.
- Connect the remaining core topics into one coherent mental model.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use feature branches for each SwiftUI screen.
- Make one commit per working preview.
- Open a draft pull request for review practice.

### Xcode

- Canvas
- Preview
- Live Preview
- View Debugger

### Apple Documentation

- SwiftUI documentation for: NavigationStack, NavigationPath, TabView, Sheets

### WWDC

- SwiftUI sessions matching this module

### Best Practices

- Prefer clarity when working with NavigationStack.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does NavigationStack solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study view structure in a small SwiftUI open-source app

### AI

- Ask AI to explain NavigationStack after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of NavigationStack in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document NavigationStack, NavigationPath, TabView, Sheets.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach NavigationStack to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Build a multi-screen application with NavigationStack, sheets, and alerts.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use NavigationStack correctly in a realistic scenario and explain the trade-offs.
- Use NavigationPath correctly in a realistic scenario and explain the trade-offs.
- Use TabView correctly in a realistic scenario and explain the trade-offs.
- Use Sheets correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 5 — Lists & Forms

## Core Topics

- List
- ScrollView
- LazyVStack
- LazyHStack
- Form
- Sections
- Swipe Actions

---

## Learning Objectives

After completing this module you should be able to:

- Understand List and recognize when it is the right tool.
- Understand ScrollView and recognize when it is the right tool.
- Understand LazyVStack and recognize when it is the right tool.
- Understand LazyHStack and recognize when it is the right tool.
- Understand Form and recognize when it is the right tool.
- Connect the remaining core topics into one coherent mental model.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use feature branches for each SwiftUI screen.
- Make one commit per working preview.
- Open a draft pull request for review practice.

### Xcode

- Canvas
- Preview
- Live Preview
- View Debugger

### Apple Documentation

- SwiftUI documentation for: List, ScrollView, LazyVStack, LazyHStack

### WWDC

- SwiftUI sessions matching this module

### Best Practices

- Prefer clarity when working with List.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does List solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study view structure in a small SwiftUI open-source app

### AI

- Ask AI to explain List after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of List in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document List, ScrollView, LazyVStack, LazyHStack.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach List to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Create a notes application interface with List, Form, and swipe actions.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use List correctly in a realistic scenario and explain the trade-offs.
- Use ScrollView correctly in a realistic scenario and explain the trade-offs.
- Use LazyVStack correctly in a realistic scenario and explain the trade-offs.
- Use LazyHStack correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 6 — Custom Components

## Core Topics

- Reusable Views
- View Composition
- Custom Modifiers
- Preference Keys (introduction)

---

## Learning Objectives

After completing this module you should be able to:

- Understand Reusable Views and recognize when it is the right tool.
- Understand View Composition and recognize when it is the right tool.
- Understand Custom Modifiers and recognize when it is the right tool.
- Understand Preference Keys (introduction) and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use feature branches for each SwiftUI screen.
- Make one commit per working preview.
- Open a draft pull request for review practice.

### Xcode

- Canvas
- Preview
- Live Preview
- View Debugger

### Apple Documentation

- SwiftUI documentation for: Reusable Views, View Composition, Custom Modifiers, Preference Keys (introduction)

### WWDC

- SwiftUI sessions matching this module

### Best Practices

- Prefer clarity when working with Reusable Views.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Reusable Views solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study view structure in a small SwiftUI open-source app

### AI

- Ask AI to explain Reusable Views after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Reusable Views in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Reusable Views, View Composition, Custom Modifiers, Preference Keys (introduction).
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Reusable Views to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Build a reusable UI component library with custom modifiers.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Reusable Views correctly in a realistic scenario and explain the trade-offs.
- Use View Composition correctly in a realistic scenario and explain the trade-offs.
- Use Custom Modifiers correctly in a realistic scenario and explain the trade-offs.
- Use Preference Keys (introduction) correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 7 — Animation

## Core Topics

- Implicit Animation
- Explicit Animation
- Matched Geometry Effect
- Transitions

---

## Learning Objectives

After completing this module you should be able to:

- Understand Implicit Animation and recognize when it is the right tool.
- Understand Explicit Animation and recognize when it is the right tool.
- Understand Matched Geometry Effect and recognize when it is the right tool.
- Understand Transitions and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use feature branches for each SwiftUI screen.
- Make one commit per working preview.
- Open a draft pull request for review practice.

### Xcode

- Canvas
- Preview
- Live Preview
- View Debugger

### Apple Documentation

- SwiftUI documentation for: Implicit Animation, Explicit Animation, Matched Geometry Effect, Transitions

### WWDC

- SwiftUI sessions matching this module

### Best Practices

- Prefer clarity when working with Implicit Animation.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Implicit Animation solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study view structure in a small SwiftUI open-source app

### AI

- Ask AI to explain Implicit Animation after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Implicit Animation in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Implicit Animation, Explicit Animation, Matched Geometry Effect, Transitions.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Implicit Animation to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Animate screen transitions and interactive elements with implicit and explicit animations.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Implicit Animation correctly in a realistic scenario and explain the trade-offs.
- Use Explicit Animation correctly in a realistic scenario and explain the trade-offs.
- Use Matched Geometry Effect correctly in a realistic scenario and explain the trade-offs.
- Use Transitions correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 8 — Accessibility

## Core Topics

- VoiceOver
- Labels
- Traits
- Dynamic Type
- Color Contrast

---

## Learning Objectives

After completing this module you should be able to:

- Understand VoiceOver and recognize when it is the right tool.
- Understand Labels and recognize when it is the right tool.
- Understand Traits and recognize when it is the right tool.
- Understand Dynamic Type and recognize when it is the right tool.
- Understand Color Contrast and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use feature branches for each SwiftUI screen.
- Make one commit per working preview.
- Open a draft pull request for review practice.

### Xcode

- Canvas
- Preview
- Live Preview
- View Debugger

### Apple Documentation

- SwiftUI documentation for: VoiceOver, Labels, Traits, Dynamic Type

### WWDC

- SwiftUI sessions matching this module

### Best Practices

- Prefer clarity when working with VoiceOver.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does VoiceOver solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study view structure in a small SwiftUI open-source app

### AI

- Ask AI to explain VoiceOver after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of VoiceOver in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document VoiceOver, Labels, Traits, Dynamic Type.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach VoiceOver to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Make one existing screen fully accessible with VoiceOver, labels, and Dynamic Type.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use VoiceOver correctly in a realistic scenario and explain the trade-offs.
- Use Labels correctly in a realistic scenario and explain the trade-offs.
- Use Traits correctly in a realistic scenario and explain the trade-offs.
- Use Dynamic Type correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 9 — Performance

## Core Topics

- View identity
- Equatable
- Lazy containers
- Rendering performance
- Common performance mistakes

---

## Learning Objectives

After completing this module you should be able to:

- Understand View identity and recognize when it is the right tool.
- Understand Equatable and recognize when it is the right tool.
- Understand Lazy containers and recognize when it is the right tool.
- Understand Rendering performance and recognize when it is the right tool.
- Understand Common performance mistakes and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use feature branches for each SwiftUI screen.
- Make one commit per working preview.
- Open a draft pull request for review practice.

### Xcode

- Instruments launch
- Memory Graph
- Time Profiler
- Debug Navigator

### Apple Documentation

- Instruments Help
- Debugging with Xcode

### WWDC

- Instruments sessions
- SwiftUI performance sessions when relevant

### Best Practices

- Prefer clarity when working with View identity.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does View identity solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Read a performance-related pull request

### AI

- Ask AI to explain View identity after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of View identity in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document View identity, Equatable, Lazy containers, Rendering performance.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach View identity to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Profile a scrolling screen and fix one measurable SwiftUI performance issue.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use View identity correctly in a realistic scenario and explain the trade-offs.
- Use Equatable correctly in a realistic scenario and explain the trade-offs.
- Use Lazy containers correctly in a realistic scenario and explain the trade-offs.
- Use Rendering performance correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Phase Project

Build a production-quality SwiftUI application that includes: - Multiple screens - NavigationStack - Forms - Lists - State management - Custom reusable components - Animations - Accessibility support Document: - UI decisions - State management decisions - Reusable components - Trade-offs ------------------------------------------------------------------------

---

# Exit Criteria

You are ready for the next phase when you can:

- Design maintainable SwiftUI interfaces.
- Select the correct state management solution.
- Build reusable UI components.
- Navigate complex applications.
- Debug SwiftUI layout and state issues.
- Follow Apple's Human Interface Guidelines.

---

# Next Phase

➡️ Phase 03 — Apple Frameworks
