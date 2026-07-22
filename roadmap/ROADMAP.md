# iOS Engineering System Roadmap

> **Version:** 1.0.0
>
> This roadmap is the single source of truth for the iOS Engineering System repository.
>
> It defines **what to learn**, **why to learn it**, and **when to learn it**.
>
> The roadmap is **mastery-based**, not time-based.

---

# Vision

The goal of this repository is **not** to memorize Swift syntax or complete tutorials.

The goal is to become an engineer who can:

- Design software
- Build production-quality applications
- Read and understand large codebases
- Make good engineering decisions
- Learn new technologies independently
- Contribute to open source
- Build products and businesses

This repository focuses on long-term engineering skills rather than short-term interview preparation.

---

# Learning Philosophy

## Foundation First

Everything in this roadmap builds on strong fundamentals.

We do **not** skip fundamentals simply because they look easy.

A weak foundation always becomes a problem later.

---

## Learn by Building

Every important concept should eventually be used in a project.

Learning does not end after watching a video or reading documentation.

A concept is considered learned only after it has been implemented.

---

## Mastery Over Speed

There are no deadlines.

There are no weekly targets.

Progress is based on mastery.

Do not move to the next lesson until you can confidently explain and use the current one.

---

## Context Before Complexity

Advanced concepts should only be introduced after the problems they solve become visible.

Example:

- Learn Protocols before Dependency Injection.
- Learn Dependency Injection before Clean Architecture.
- Learn Concurrency before advanced networking.

Every topic must answer:

> **"Why does this exist?"**

before answering:

> **"How does it work?"**

---

## Build Mental Models

The objective is to understand systems rather than memorize APIs.

Whenever possible:

- understand the problem
- understand the trade-offs
- understand why Apple designed something this way

---

## Official Sources First

When learning a topic, follow this priority:

1. Apple Documentation
2. Swift Language Documentation
3. WWDC Sessions
4. Open Source Code
5. Carefully selected books
6. Carefully selected videos

Whenever multiple resources disagree, prefer Apple's official documentation unless there is a strong engineering reason not to.

---

# Learning Rules

The following rules apply throughout the entire roadmap.

## Rule 1

Understand before memorizing.

---

## Rule 2

Read code every week.

---

## Rule 3

Build continuously.

Learning without building is incomplete.

---

## Rule 4

Do not blindly copy code from AI.

Always understand every line.

---

## Rule 5

Read official documentation regularly.

Documentation is part of the learning process, not a last resort.

---

## Rule 6

Write permanent notes.

Notes should explain concepts in your own words.

---

## Rule 7

Keep Git history clean.

Every commit should have a clear purpose.

---

## Rule 8

Review your own code before considering a task complete.

---

## Rule 9

Prefer simplicity over cleverness.

Readable code wins.

---

## Rule 10

Never chase technology trends without understanding the fundamentals first.

---

# Parallel Learning Layers

These layers continue throughout the entire roadmap.

They never stop.

| Layer | Purpose |
|--------|---------|
| Swift | Language mastery |
| SwiftUI | UI development |
| UIKit | Production understanding & legacy systems |
| Git | Version control |
| Xcode | IDE mastery |
| Apple Documentation | Official knowledge |
| WWDC | Best practices & latest APIs |
| Software Design | API design, architecture, UI thinking |
| Best Practices | Production-quality engineering |
| Testing | Build reliable software |
| Open Source | Reading and contributing |
| AI | Use AI effectively without becoming dependent |
| DSA | Engineering thinking and interview preparation |
| English | Technical communication |
| Notes | Build a permanent knowledge base |
| Weekly Review | Prevent forgetting |
| Engineering Review | Evaluate code quality |

---

# Roadmap Structure

The roadmap is divided into fourteen phases (Phase 00 through Phase 13).

Each phase contains multiple modules.

Detailed module content lives in the `roadmap/phase-*.md` files.

```
Roadmap

↓

Phase

↓

Module

↓

Lesson

↓

Mini Practice

↓

Challenge

↓

Lab

↓

Capstone

↓

Engineering Review

↓

Next Module
```

---

# Module Structure

Every module follows the same structure.

```
Core Topics

↓

Learning Objectives

↓

Parallel Learning Layers
  - Git
  - Xcode
  - Apple Documentation
  - WWDC
  - Best Practices
  - Design Thinking
  - Architecture Thinking
  - Open Source
  - AI
  - English
  - Notes
  - Reflection

↓

Mini Project

↓

Exit Criteria
```

---

# Lesson Structure

Every lesson follows the same structure.

```
Overview

↓

Why This Matters

↓

Learning Objectives

↓

Main Concepts

↓

Best Practices

↓

Common Mistakes

↓

Official Resources

↓

Book References

↓

Xcode Layer

↓

Git Layer

↓

AI Layer

↓

Mini Practice

↓

Notes Task

↓

Engineering Review

↓

Interview Questions

↓

Reflection

↓

Exit Criteria

↓

Connections

↓

What's Next
```

---

# Phase Overview

The roadmap contains fourteen phases, from Phase 00 through Phase 13.

Detailed module content lives in the phase files under `roadmap/`.
This overview is the agreed learning order and module inventory.

```
Phase 00 — Engineering Foundation

↓

Phase 01 — Swift Mastery

↓

Phase 02 — SwiftUI Mastery

↓

Phase 03 — Apple Frameworks

↓

Phase 04 — Professional App Architecture

↓

Phase 05 — Networking & Data

↓

Phase 06 — Testing

↓

Phase 07 — Performance & Debugging

↓

Phase 08 — Security

↓

Phase 09 — System Design

↓

Phase 10 — Production Engineering

↓

Phase 11 — Open Source & Code Reading

↓

Phase 12 — Apple Ecosystem

↓

Phase 13 — Product & Business Engineering
```

---

# Phase 00 — Engineering Foundation

> Details: [`phase-00-engineering-foundation.md`](./phase-00-engineering-foundation.md)

**Purpose:** Build the engineering habits, workflow, and tools that will support every later phase.

### Modules

- Module 0.1 — Engineering Mindset
- Module 0.2 — Git Foundations
- Module 0.3 — Xcode Fundamentals
- Module 0.4 — Documentation & Research
- Module 0.5 — Debugging Basics
- Module 0.6 — Engineering Notes

---

# Phase 01 — Swift Mastery

> Details: [`phase-01-swift-mastery.md`](./phase-01-swift-mastery.md)

**Purpose:** Master the Swift language deeply before focusing on advanced frameworks. Build strong fundamentals that support every future phase.

### Modules

- Module 1 — Swift Basics
- Module 2 — Collections & Optionals
- Module 3 — Structs, Classes & Enums
- Module 4 — Memory Management
- Module 5 — Protocol-Oriented Programming
- Module 6 — Generics
- Module 7 — Error Handling
- Module 8 — Concurrency

---

# Phase 02 — SwiftUI Mastery

> Details: [`phase-02-swiftui-mastery.md`](./phase-02-swiftui-mastery.md)

**Purpose:** Learn SwiftUI by understanding how it works internally and how to build maintainable, production-quality user interfaces.

### Modules

- Module 1 — SwiftUI Fundamentals
- Module 2 — Layout System
- Module 3 — State Management
- Module 4 — Navigation
- Module 5 — Lists & Forms
- Module 6 — Custom Components
- Module 7 — Animation
- Module 8 — Accessibility
- Module 9 — Performance

---

# Phase 03 — Apple Frameworks

> Details: [`phase-03-apple-frameworks.md`](./phase-03-apple-frameworks.md)

**Purpose:** Learn Apple's frameworks by solving real-world problems instead of studying APIs in isolation.

### Modules

- Module 1 — Foundation Framework
- Module 2 — Persistence
- Module 3 — Networking Foundation
- Module 4 — Media Frameworks
- Module 5 — Location & Maps
- Module 6 — Notifications
- Module 7 — Background Work
- Module 8 — Widgets & App Intents
- Module 9 — Cloud & Purchases

---

# Phase 04 — Professional App Architecture

> Details: [`phase-04-professional-app-architecture.md`](./phase-04-professional-app-architecture.md)

**Purpose:** Move from writing working code to designing maintainable systems.

### Modules

- Module 1 — Project Organization
- Module 2 — MVVM
- Module 3 — Dependency Injection
- Module 4 — SOLID Principles
- Module 5 — Clean Architecture
- Module 6 — Modularization
- Module 7 — Tuist
- Module 8 — Architecture Decision Making

---

# Phase 05 — Networking & Data

> Details: [`phase-05-networking-and-data.md`](./phase-05-networking-and-data.md)

**Purpose:** Learn how production iOS applications communicate with servers, store data, and provide a reliable user experience even without an internet connection.

### Modules

- Module 1 — Networking Fundamentals
- Module 2 — URLSession
- Module 3 — Codable & JSON
- Module 4 — Error Handling
- Module 5 — Authentication
- Module 6 — Local Persistence
- Module 7 — Caching & Offline-First
- Module 8 — Repository Pattern

---

# Phase 06 — Testing

> Details: [`phase-06-testing.md`](./phase-06-testing.md)

**Purpose:** Learn to build reliable, maintainable software through automated testing. Testing is a core engineering skill, not an afterthought.

### Modules

- Module 1 — Testing Fundamentals
- Module 2 — Unit Testing
- Module 3 — Test Doubles
- Module 4 — Testable Architecture
- Module 5 — Integration Testing
- Module 6 — UI Testing
- Module 7 — Test-Driven Development (TDD)
- Module 8 — Snapshot & Performance Testing

---

# Phase 07 — Performance & Debugging

> Details: [`phase-07-performance-and-debugging.md`](./phase-07-performance-and-debugging.md)

**Purpose:** Learn to find, understand, and fix performance, memory, rendering, and runtime issues using professional engineering tools.

### Modules

- Module 1 — Debugging Mindset
- Module 2 — Instruments
- Module 3 — Memory Management
- Module 4 — SwiftUI Performance
- Module 5 — Performance Optimization
- Module 6 — Crash Analysis

---

# Phase 08 — Security

> Details: [`phase-08-security.md`](./phase-08-security.md)

**Purpose:** Learn to build secure iOS applications that protect user data, defend against common threats, and follow Apple's security recommendations.

### Modules

- Module 1 — Security Fundamentals
- Module 2 — Secure Storage
- Module 3 — Authentication & Authorization
- Module 4 — Secure Networking
- Module 5 — Privacy
- Module 6 — Secure Coding

---

# Phase 09 — System Design

> Details: [`phase-09-system-design.md`](./phase-09-system-design.md)

**Purpose:** Learn to design software before writing code. This phase focuses on engineering decisions, trade-offs, scalability, and building systems that are easy to maintain and evolve.

### Modules

- Module 1 — System Design Fundamentals
- Module 2 — Domain Modeling
- Module 3 — Feature Design
- Module 4 — API & Data Flow Design
- Module 5 — Scalability & Modularity
- Module 6 — Engineering Decision Making

---

# Phase 10 — Production Engineering

> Details: [`phase-10-production-engineering.md`](./phase-10-production-engineering.md)

**Purpose:** Learn everything required to build, ship, monitor, maintain, and continuously improve production-quality iOS applications.

### Modules

- Module 1 — Production Mindset
- Module 2 — Build & Release
- Module 3 — CI/CD
- Module 4 — Analytics
- Module 5 — Crash Reporting & Logging
- Module 6 — Feature Flags & Configuration
- Module 7 — Maintenance & Technical Debt

---

# Phase 11 — Open Source & Code Reading

> Details: [`phase-11-open-source-and-code-reading.md`](./phase-11-open-source-and-code-reading.md)

**Purpose:** Learn how to understand, evaluate, contribute to, and maintain real-world codebases. Great engineers spend as much time reading code as writing it.

### Modules

- Module 1 — Reading Large Codebases
- Module 2 — Code Reviews
- Module 3 — Debugging Unfamiliar Projects
- Module 4 — Contributing to Open Source
- Module 5 — Maintaining Open Source

---

# Phase 12 — Apple Ecosystem

> Details: [`phase-12-apple-ecosystem.md`](./phase-12-apple-ecosystem.md)

**Purpose:** Expand beyond iPhone development and learn how to build applications across Apple's platforms while understanding shared technologies and platform-specific design principles.

### Modules

- Module 1 — Apple Ecosystem Overview
- Module 2 — UIKit Interoperability
- Module 3 — Widgets & App Intents
- Module 4 — watchOS & visionOS
- Module 5 — macOS & Catalyst
- Module 6 — Multiplatform Engineering

---

# Phase 13 — Product & Business Engineering

> Details: [`phase-13-product-and-business-engineering.md`](./phase-13-product-and-business-engineering.md)

**Purpose:** Transform your engineering skills into successful products by learning product thinking, business fundamentals, and long-term product management. This phase is about building products people want, shipping them professionally, and continuously improving them.

### Modules

- Module 1 — Product Thinking
- Module 2 — MVP Planning
- Module 3 — Shipping to the App Store
- Module 4 — Analytics & User Feedback
- Module 5 — Monetization
- Module 6 — Marketing & Personal Brand
- Module 7 — Long-Term Product Management

---

# Book Strategy

Books are **not** read from cover to cover.

Books are used as references.

Read only the chapters that support the current module.

---

# Official Resources

Always prioritize learning in this order:

1. Apple Documentation
2. Swift Documentation
3. WWDC
4. Open Source Code
5. Books
6. Carefully Selected Videos

---

# Graduation Requirements

The roadmap is considered complete only when you can:

- Design software before writing code.
- Read unfamiliar production code confidently.
- Debug problems independently.
- Build complete production-quality applications.
- Publish applications.
- Contribute to open source.
- Explain engineering decisions.
- Learn new Apple technologies independently.

---

# Final Goal

The purpose of this roadmap is **not** to become someone who knows Swift.

The purpose is to become an engineer capable of solving real-world problems, building valuable products, and continuously improving throughout an entire career.