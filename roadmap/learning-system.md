# iOS Engineering Learning System
## Apps → Vertical Slices → Tasks → Concepts

> **Purpose**
>
> This document explains **how I will learn**, not **what I will learn**.
>
> The curriculum already defines **what** to study.
> This document defines **how** every topic is learned by building real production-quality apps.

---

# Learning Philosophy

I will not learn technologies in isolation.

I will learn them by building complete applications.

Each application is divided into small **Vertical Slices**.

Each Vertical Slice is divided into small **Tasks**.

Each Task teaches one or more **Concepts**.

Every concept maps back to one or more modules in my curriculum.

---

# Learning Hierarchy

```text
Curriculum
    ↓
Production App
    ↓
Vertical Slice
    ↓
Tasks
    ↓
Concepts
```

---

# Level 1 — Curriculum

The curriculum is my master roadmap.

It answers:

- What should I learn?
- In what order?
- How modules connect together?

The curriculum never changes because of an app.

Instead, apps exist to practice the curriculum.

---

# Level 2 — Production Apps

A production app is a complete real-world application.

Each app has one responsibility.

Examples:

- Expense Tracker
- Notes App
- News Reader
- Fitness Tracker
- Media Organizer

An app exists to teach a collection of related curriculum modules.

An app should never include technologies that do not naturally belong to it.

---

# Level 3 — Vertical Slices

A Vertical Slice is a very small, usable feature.

Each slice must provide value to the user.

Every slice should be fully working before moving to the next one.

Examples:

Expense App

- Create Expense
- View Expenses
- Edit Expense
- Delete Expense
- Search Expenses

News App

- View Headlines
- Read Article
- Bookmark Article
- Offline Reading
- Background Refresh

Notes App

- Create Note
- Edit Note
- Search Notes
- Cloud Sync
- Resolve Conflicts

Each slice introduces only the concepts needed to complete that feature.

---

# Level 4 — Tasks

A Vertical Slice is divided into very small coding tasks.

Each task should take approximately 15–60 minutes.

Every task has exactly one objective.

Example

Vertical Slice

Create Expense

Tasks

1. Create Expense model
2. Create Add Expense screen
3. Validate input
4. Save expense
5. Display success state
6. Refresh expense list

Each completed task should leave the project in a working state.

Never leave the project broken.

---

# Level 5 — Concepts

Every task exists to teach concepts.

Examples

Task

Create Expense Model

Concepts

- Struct
- SwiftData Model
- Property
- Identifiable

----------------------

Task

Save Expense

Concepts

- ModelContext
- Insert
- Save
- Error Handling

----------------------

Task

Refresh List

Concepts

- @Query
- Observation
- SwiftUI Rendering
- View Refresh

The goal is never to finish tasks.

The goal is to master concepts.

---

# Module Mapping

Every Vertical Slice must reference the curriculum.

Example

Slice

Create Expense

Curriculum Modules

- Module 03 — Swift Foundations
- Module 06 — SwiftUI
- Module 08 — Architecture
- Module 09 — Persistence

This keeps learning structured.

---

# Vertical Slice Template

Every slice should contain the following sections.

## 1. User Value

What can the user do after this slice?

Example

"The user can create an expense."

---

## 2. Curriculum Modules

Exactly which modules are being practiced?

---

## 3. Architecture

Describe the architecture used.

Describe the complete data flow.

Example

SwiftUI View

↓

ViewModel

↓

Repository

↓

SwiftData

↓

Repository

↓

ViewModel

↓

SwiftUI View

---

## 4. Technical Decisions

Every slice must define:

- UI Framework
- Storage
- Architecture
- Concurrency
- Testing Strategy

No decisions should be left for later.

---

## 5. Tasks

Provide a numbered checklist.

Every task should be small.

Every task should produce a working application.

---

## 6. Concepts

Every task should list:

- New concepts
- Previously reinforced concepts

Learning through repetition is required.

---

## 7. Definition of Done

The slice is complete only when:

- App builds successfully
- No warnings
- Feature works
- Edge cases handled
- Code follows architecture
- Tests pass (when applicable)

---

# Learning Rules

## Rule 1

Never learn a technology without using it.

---

## Rule 2

Never add a feature only to learn a framework.

Frameworks must solve real problems.

---

## Rule 3

Every new slice must build on the previous one.

No throwaway code.

---

## Rule 4

Refactor continuously.

Improve previous code as new concepts are introduced.

---

## Rule 5

Every new concept should be used again in future slices.

Repetition creates mastery.

---

## Rule 6

Only introduce complexity when it solves a real problem.

Don't build enterprise architecture for simple features.

---

## Rule 7

Every app should feel production-ready.

Not tutorial-ready.

---

## Rule 8

Every completed app should be worthy of a GitHub portfolio.

---

# Success Criteria

By the end of each app, I should be able to answer:

- Why was this architecture chosen?
- How does data flow through the app?
- Why does this concurrency model work?
- Where is memory allocated?
- How is state updated?
- How is data persisted?
- How is networking handled?
- How is the feature tested?
- How would I improve performance?
- How would I scale this feature?
- How would I ship this to production?

If I cannot answer these questions confidently, I have not mastered the app yet.

---

# Final Goal

The objective is **not** to complete apps.

The objective is to become the kind of engineer who can confidently design, build, test, optimize, maintain, and ship production-quality iOS applications by deeply understanding every concept through repeated, real-world practice.