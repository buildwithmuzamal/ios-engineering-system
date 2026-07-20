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

The roadmap is divided into six phases.

Each phase contains multiple modules.

Each module contains multiple lessons.

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
Overview

↓

Goal

↓

Prerequisites

↓

Lessons

↓

Parallel Layers

↓

Resources

↓

Challenge

↓

Lab

↓

Engineering Review

↓

Interview Check

↓

Exit Criteria

↓

Reflection
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

The roadmap contains six major phases.

Detailed phase breakdown begins in the next section.

```
Phase 1
Swift Engineering Foundations

↓

Phase 2
SwiftUI Foundations

↓

Phase 3
iOS Engineering

↓

Phase 4
Software Engineering

↓

Phase 5
Production Engineering

↓

Phase 6
Senior iOS Engineering
```

---

# Phase 1 — Swift Engineering Foundations

> Goal: Build a deep understanding of the Swift language and develop strong programming fundamentals before learning iOS frameworks.

---

## Module 1 — Swift Fundamentals

### Goal

Learn the core syntax and concepts that every Swift developer uses daily.

### Lessons

- Variables & Constants
- Types & Type Inference
- Operators
- Control Flow
- Functions
- Collections (Array, Set, Dictionary)
- Optionals

### Lab

- Command Line Habit Tracker

### Challenge

- Swift Fundamentals Challenge

### Capstone

- Build a Command Line Productivity App

---

## Module 2 — Modeling Data

### Goal

Understand how Swift models real-world data.

### Lessons

- Structures
- Classes
- Enumerations
- Properties
- Methods
- Initializers
- Value vs Reference Semantics

### Lab

- Expense Tracker Domain Model

### Challenge

- Data Modeling Challenge

### Capstone

- Design a Small Business Domain

---

## Module 3 — Protocol-Oriented Swift

### Goal

Write reusable, flexible and maintainable code.

### Lessons

- Protocols
- Extensions
- Protocol Composition
- Generics
- Associated Types
- Opaque Types (`some`)
- Existentials (`any`)

### Lab

- Reusable Components Library

### Challenge

- Generic Programming Challenge

### Capstone

- Build a Small Swift Package

---

## Module 4 — Memory & Concurrency

### Goal

Understand memory management and modern Swift concurrency.

### Lessons

- ARC
- Strong, Weak & Unowned References
- Closures
- Escaping Closures
- async/await
- Tasks
- Task Groups
- Actors
- MainActor
- Sendable

### Lab

- Image Downloader

### Challenge

- Concurrency Challenge

### Capstone

- Concurrent File Downloader

---

## Module 5 — Swift Engineering

### Goal

Combine all Swift knowledge to write production-quality code.

### Lessons

- Error Handling
- Result Type
- Codable
- Property Wrappers
- Key Paths
- Standard Library Deep Dive
- API Design Guidelines
- Performance Basics
- Debugging Basics
- Refactoring Fundamentals

### Lab

- JSON Processing Library

### Challenge

- Production Swift Challenge

### Capstone

- Build a Reusable Swift Framework

---

# Phase 2 — SwiftUI Foundations

> Goal: Learn to build modern Apple user interfaces using SwiftUI while applying the Swift knowledge gained in Phase 1.

---

## Module 1 — SwiftUI Basics

Lessons

- Views
- Modifiers
- Layout System
- Stacks
- Spacer
- Frame
- Safe Area
- View Lifecycle

Lab

- Personal Profile Screen

Challenge

- SwiftUI Basics Challenge

Capstone

- Multi-Screen Demo App

---

## Module 2 — State Management

Lessons

- @State
- @Binding
- @Observable
- Environment
- EnvironmentObject
- Observation
- Data Flow

Lab

- Counter Application

Challenge

- State Management Challenge

Capstone

- Habit Tracker UI

---

## Module 3 — Navigation

Lessons

- NavigationStack
- NavigationPath
- Sheets
- Full Screen Covers
- Alerts
- Confirmation Dialogs
- Deep Linking Basics

Lab

- Multi-Screen Navigation App

Challenge

- Navigation Challenge

Capstone

- Small Shopping App

---

## Module 4 — Lists & Forms

Lessons

- List
- Section
- Form
- Swipe Actions
- Search
- Refreshable
- Context Menus

Lab

- Task Manager

Challenge

- CRUD UI Challenge

Capstone

- Notes Application

---

## Module 5 — Animation & Custom Components

Lessons

- Animation
- Transition
- GeometryReader
- PreferenceKey
- Custom Controls
- Reusable Components

Lab

- Animated Dashboard

Challenge

- Custom UI Challenge

Capstone

- Design System Demo

---


# Phase 3 — iOS Engineering

> Goal: Learn how production iOS applications are designed, built, tested, debugged, and maintained.

---

## Module 1 — App Architecture

### Goal

Understand how large iOS applications are organized.

### Lessons

- What is Architecture?
- Separation of Concerns
- SOLID Principles
- MV Pattern
- MVC
- MVP
- MVVM
- Clean Architecture (Introduction)
- Feature-Based Architecture
- Modularization (Introduction)

### Lab

- Refactor a Small Application

### Challenge

- Architecture Selection Challenge

### Capstone

- Build a Modular Feature

---

## Module 2 — Networking

### Goal

Communicate with remote services using modern networking techniques.

### Lessons

- URLSession
- HTTP Fundamentals
- REST APIs
- JSON
- Codable Review
- Request Building
- Response Handling
- Error Handling
- Authentication
- File Upload & Download
- Pagination
- Retry Strategies
- Network Monitoring
- Caching Basics

### Lab

- Movie Database App

### Challenge

- Networking Challenge

### Capstone

- Production Networking Layer

---

## Module 3 — Local Persistence

### Goal

Store, retrieve and synchronize application data.

### Lessons

- FileManager
- UserDefaults
- Keychain
- SQLite Fundamentals
- Core Data
- SwiftData
- Data Migration
- Offline First Basics
- Repository Pattern

### Lab

- Offline Notes App

### Challenge

- Persistence Challenge

### Capstone

- Offline-First Application

---

## Module 4 — Dependency Management

### Goal

Build loosely coupled and maintainable applications.

### Lessons

- Dependency Injection
- Constructor Injection
- Protocol Injection
- Composition Root
- Factory Pattern
- Service Locator (Why to Avoid)
- Swift Package Manager
- Package Design

### Lab

- Dependency Injection Playground

### Challenge

- DI Challenge

### Capstone

- Modular Service Layer

---

## Module 5 — Testing

### Goal

Build confidence through automated testing.

### Lessons

- Testing Mindset
- XCTest
- Unit Testing
- Test Doubles
- Mocking
- Integration Testing
- UI Testing
- Snapshot Testing
- Testable Architecture
- Test-Driven Development (Introduction)

### Lab

- Testing Existing Code

### Challenge

- Testing Challenge

### Capstone

- Fully Tested Feature

---

## Module 6 — Debugging & Performance

### Goal

Find problems efficiently and optimize applications.

### Lessons

- LLDB Basics
- Breakpoints
- Debug Navigator
- Memory Graph
- Instruments Overview
- Time Profiler
- Leaks
- Allocations
- Performance Optimization
- App Launch Performance

### Lab

- Debug a Broken App

### Challenge

- Performance Challenge

### Capstone

- Performance Optimization Project

---

## Module 7 — UIKit Essentials

### Goal

Understand UIKit well enough to work on existing production applications.

### Lessons

- UIViewController Lifecycle
- Auto Layout
- UITableView
- UICollectionView
- UINavigationController
- UITabBarController
- Storyboards (Reading Existing Projects)
- SwiftUI Interoperability
- UIViewRepresentable
- UIHostingController

### Lab

- UIKit Contacts App

### Challenge

- Legacy App Challenge

### Capstone

- Migrate UIKit Screen to SwiftUI

---

# Phase 4 — Software Engineering

> Goal: Learn to design maintainable software, make engineering decisions, and work effectively in professional teams.

---

## Module 1 — Clean Code

### Lessons

- Naming
- Functions
- Classes & Structures
- Comments
- Error Handling
- Code Smells
- Refactoring
- Readability

Capstone

- Refactor a Legacy Feature

---

## Module 2 — Design Patterns

### Lessons

- Strategy
- Factory
- Builder
- Adapter
- Decorator
- Observer
- Command
- Coordinator
- Repository
- Dependency Injection Pattern

Capstone

- Pattern Selection Project

---

## Module 3 — Clean Architecture

### Lessons

- Layers
- Entities
- Use Cases
- Interface Adapters
- Dependency Rule
- Feature Isolation
- Modular Design

Capstone

- Build a Clean Architecture Feature

---

## Module 4 — Domain-Driven Design

### Lessons

- Ubiquitous Language
- Entities
- Value Objects
- Aggregates
- Repositories
- Domain Services
- Application Services

Capstone

- Design a Business Domain

---

## Module 5 — Legacy Code & Refactoring

### Lessons

- Reading Unknown Code
- Safe Refactoring
- Characterization Tests
- Incremental Improvements
- Technical Debt

Capstone

- Modernize an Existing Project

---

## Module 6 — Team Engineering

### Lessons

- Code Reviews
- Git Workflows
- Pull Requests
- Technical Discussions
- Documentation
- Estimation
- Mentoring
- Communication

Capstone

- Simulated Team Project

---

# Phase 5 — Production Engineering

> Goal: Build applications that are ready for real users and the App Store.

---

## Module 1 — Production Apps

### Lessons

- Project Structure
- Configuration
- Build Settings
- Environment Management
- Feature Flags

---

## Module 2 — App Quality

### Lessons

- Accessibility
- Localization
- Error Reporting
- Analytics
- Logging
- Monitoring
- Privacy

---

## Module 3 — CI/CD

### Lessons

- GitHub Actions
- Fastlane
- Automated Testing
- Build Pipelines
- Release Pipelines

---

## Module 4 — App Store

### Lessons

- App Store Connect
- TestFlight
- Release Strategy
- Screenshots
- Metadata
- ASO Basics

---

## Module 5 — Open Source

### Lessons

- Reading Large Repositories
- Understanding Architecture
- Debugging Other People's Code
- First Contribution
- Creating Swift Packages
- Maintaining Open Source

Capstone

- Publish an Open Source Swift Package

---

## Module 6 — AI Engineering

### Lessons

- AI-Assisted Development
- Prompt Engineering for Developers
- Code Review with AI
- AI Limitations
- Building AI Features
- Local Models
- API-Based AI
- Responsible AI Usage

Capstone

- Add AI to an Existing App

---

# Phase 6 — Senior iOS Engineering

> Goal: Think like a senior engineer rather than simply writing code.

---

## Module 1 — System Design

### Lessons

- Scalability
- Caching
- Synchronization
- Offline Systems
- Push Notifications
- Background Processing
- Large Application Design

---

## Module 2 — Engineering Leadership

### Lessons

- Decision Making
- Technical Vision
- Trade-Off Analysis
- Risk Management
- Long-Term Thinking
- Architecture Reviews

---

## Module 3 — Product Thinking

### Lessons

- User Problems
- Product Discovery
- MVP Design
- Prioritization
- Metrics
- Feedback Loops

---

## Module 4 — Personal Engineering System

### Lessons

- Learning Systems
- Continuous Improvement
- Knowledge Management
- Building a Public Portfolio
- Technical Writing
- Career Planning

Capstone

- Build Your Own Engineering Playbook

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