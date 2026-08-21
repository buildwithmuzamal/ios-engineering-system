# iOS Engineering Knowledge Map (Zero → Top 1% iOS Engineer)

> **Purpose:** This is a master list of topics to learn. It is **not** a learning order. Pick one topic at a time and study it deeply.

---

# 00. Computer Science Fundamentals

- How Computers Work
- Binary
- CPU
- RAM
- Storage
- Operating Systems
- Processes
- Threads
- Networking Basics
- Internet
- HTTP
- HTTPS
- DNS
- IP Address
- TCP
- UDP
- Data Structures
- Algorithms
- Time Complexity
- Space Complexity

---

# 01. macOS

- Finder
- File System
- Terminal
- Shell
- Environment Variables
- Homebrew
- Permissions
- Keyboard Shortcuts

---

# 02. Git
- Git Fundamentals
    - Version Control
    - Repository
    - Clone
    - Commit
    - Branch
    - Merge
    - Rebase
    - Cherry Pick
    - Reset
    - Revert
    - Stash
    - Tag
    - Remote
    - Pull Request
    - Conflict Resolution
    - GitHub
> ### Legend
>
> 🔴 **Must Know** — Essential for daily professional iOS development. Master these.
>
> 🟡 **Should Know** — Important topics you'll encounter regularly. Learn after the essentials.
>
> ⚪ **Nice to Have** — Advanced or specialized topics. Learn when the need arises or out of curiosity.


# Advanced Git

## Git Internals

- 🔴 Git Object Model
- 🔴 Blob
- 🔴 Tree
- 🔴 Commit Object
- 🟡 Tag Object
- 🟡 SHA-1 / SHA-256 Hashes
- 🔴 HEAD
- 🔴 Detached HEAD
- 🔴 References (refs)
- 🔴 Index (Staging Area)
- 🔴 Working Tree


## History Manipulation

- 🔴 Interactive Rebase
- 🔴 Squash
- 🔴 Fixup
- 🟡 Autosquash
- 🔴 Reword
- 🔴 Edit
- 🔴 Drop
- 🟡 Split Commits
- 🔴 Rebase vs Merge (Deep Dive)
- 🔴 Force Push vs `--force-with-lease`


## Recovery

- 🔴 Reflog
- 🔴 Recover Lost Commits
- 🟡 Recover Deleted Branches
- 🔴 Recover After Hard Reset
- 🔴 Recover After Bad Rebase


## Investigation

- 🔴 Git Bisect
- 🟡 git blame
- 🔴 git log (advanced)
- 🟡 git show
- 🔴 git diff (advanced)
- ⚪ git range-diff


## Branch Management

- 🔴 Branch Strategies
- ⚪ Git Flow
- 🔴 GitHub Flow
- 🔴 Trunk-Based Development
- 🟡 Release Branches
- 🟡 Hotfix Branches



## Merge Strategies

- 🔴 Fast Forward
- 🔴 Three-Way Merge
- 🔴 Squash Merge
- 🔴 Rebase Merge
- ⚪ Octopus Merge (overview)
- 🟡 Ours/Theirs Strategy



## Remote Collaboration

- 🔴 Fetch vs Pull
- 🔴 Upstream Branches
- 🔴 Tracking Branches
- 🟡 Fork Workflow
- 🔴 Pull Request Best Practices
- 🔴 Code Review Workflow



## Large Projects

- 🟡 Git Worktree
- 🟡 Git Hooks
- ⚪ Git LFS
- ⚪ Sparse Checkout
- ⚪ Submodules
- ⚪ Subtree (overview)



## Performance & Maintenance

- ⚪ Garbage Collection
- ⚪ Pack Files
- ⚪ Pruning
- ⚪ Repository Maintenance




# 03. Xcode

### 🟢 Xcode Fundamentals
- Xcode Interface & Navigation
- Workspace
- Project
- Target
- Scheme
- Project Navigator
- Target Membership

### 🔴 Project Structure
- Build Phases
- Build Rules
- Target Dependencies
- Project vs Target Settings
- `.xcodeproj`
- `.xcworkspace`

### 🔴 Build Fundamentals
- Xcode Build System
- Build Process
- Compile
- Link
- Build Products
- Derived Data
- Clean Build Folder
- Incremental Builds
- Build Logs

### 🔴 Build Configurations
- Build Configurations
- Debug vs Release
- Build Settings
- `.xcconfig`
- User-Defined Build Settings
- Environment Variables
- Build Settings Inheritance

### 🔴 App Configuration
- Info.plist
- Bundle Identifier
- Version
- Build Number
- Entitlements
- Capabilities

### 🔴 Code Signing Fundamentals
- Code Signing
- Certificates
- Provisioning Profiles
- Automatic Signing
- Manual Signing
- Team
- App ID
- Signing Identity

### 🟡 Devices & Simulator
- Simulator
- Physical Devices
- Device Management
- Running on a Physical Device
- Device Logs
- Console

### 🔴 Basic Debugging
- Debugger
- Breakpoints
- Conditional Breakpoints
- Step Over
- Step Into
- Step Out
- Continue
- Variables
- Call Stack
- Debug Console
- Debug View Hierarchy
- Memory Graph Debugger

### 🟡 Swift Package Manager
- Package Dependencies
- Package Resolution
- `Package.swift`
- `Package.resolved`
- Local Packages
- Remote Packages

### 🟡 Source Control in Xcode
- Git Integration
- Source Control Navigator
- Diff
- Commit
- Branch
- Merge
- Conflict Resolution

### 🟡 Xcode Developer Tools
- Quick Help
- Jump to Definition
- Find References
- Find in Workspace
- Code Completion
- Refactoring
- Documentation
- Code Snippets
- Assistant Editor

### 🟡 Archive Basics
- Archive
- Organizer
- Build for Distribution
- Archive vs Build

---

# 04. Swift

## Language Basics

- Variables
- Constants
- Data Types
- Operators
- Control Flow
- Functions
- Closures
- Optionals
- Strings
- Arrays
- Sets
- Dictionaries
- Tuples

## Object-Oriented Programming

- Structures
- Classes
- Enumerations
- Protocols
- Extensions
- Initializers
- Deinitializers
- Properties
- Methods
- Access Control
- Inheritance
- Polymorphism

## Advanced Swift

- Generics
- Associated Types
- Opaque Types
- Existentials
- Result Type
- Error Handling
- Pattern Matching
- Key Paths
- Property Wrappers
- Result Builders
- Macros
- Regular Expressions

---

# 05. Memory Management

- Stack
- Heap
- Value Types
- Reference Types
- ARC
- Retain Cycle
- Weak References
- Unowned References
- Copy-on-Write
- Ownership
- Lifetime
- Allocation
- Deallocation
- Memory Graph

---

# 06. Swift Concurrency

- Async/Await
- Tasks
- Task Groups
- Actors
- MainActor
- Sendable
- Isolation
- Structured Concurrency
- Cancellation
- AsyncSequence
- Continuations
- Task Priorities

---

# 07. SwiftUI

## Fundamentals

- Views
- View Lifecycle
- View Modifiers
- Containers
- Layout System

## State Management

- State
- Binding
- Environment
- Observation
- Observable
- PreferenceKey

## Navigation

- NavigationStack
- NavigationPath
- TabView
- Sheets
- Popovers
- Alerts

## UI

- Lists
- Grids
- Forms
- Menus
- Toolbars
- Gestures
- Animations
- Transitions
- Canvas
- Shapes
- Charts

## Advanced

- GeometryReader
- Accessibility
- Localization
- Performance
- Custom Layout
- UIKit Integration

---

# 08. UIKit

- UIView
- UIViewController
- View Lifecycle
- Auto Layout
- Storyboards
- XIB
- TableView
- CollectionView
- NavigationController
- TabBarController
- ScrollView
- Gestures
- Animations
- UIKit + SwiftUI

---

# 09. Architecture

- MVC
- MVP
- MVVM
- VIPER
- Clean Architecture
- Coordinator Pattern
- Dependency Injection
- SOLID Principles
- Design Patterns
- Modularization

---

# 10. Persistence

- UserDefaults
- FileManager
- Keychain
- SQLite
- Core Data
- SwiftData
- Realm

---

# 11. Networking

- URLSession
- HTTP
- HTTPS
- REST API
- GraphQL
- JSON
- Codable
- Authentication
- Authorization
- OAuth
- JWT
- Cookies
- Sessions
- Multipart Upload
- Download
- WebSockets
- Retry
- Pagination
- Caching
- Network Monitoring

---

# 12. Security

- Keychain
- Encryption
- Hashing
- Secure Enclave
- Biometrics
- Certificate Pinning
- App Transport Security
- Code Signing

---

# 13. Testing

- XCTest
- Unit Testing
- UI Testing
- Integration Testing
- Snapshot Testing
- Performance Testing
- Mocking
- Test Doubles
- Test-Driven Development (TDD)

---

# 14. Performance

- Instruments
- Time Profiler
- Memory Graph
- Leaks
- Allocations
- CPU Optimization
- Memory Optimization
- Rendering
- Startup Time
- Energy Usage

---

# 15. Apple Frameworks

- Foundation
- SwiftUI
- UIKit
- Observation
- Combine
- Core Animation
- Core Graphics
- AVFoundation
- Vision
- Core ML
- Core Image
- Core Location
- MapKit
- WidgetKit
- ActivityKit
- App Intents
- UserNotifications
- Background Tasks
- CloudKit
- StoreKit
- HealthKit
- Photos Framework

---

# 16. Package Management

- Swift Package Manager
- CocoaPods
- Carthage
- Binary Frameworks

---

# 17. Project Structure

- Tuist
- Modular Architecture
- Feature Modules
- Shared Modules
- Resource Management
- Environment Management
- Build Configurations

---

# 18. Debugging

- Breakpoints
- Conditional Breakpoints
- Symbolic Breakpoints
- LLDB
- Logging
- Assertions
- Memory Debugging
- Crash Analysis

---

# 19. CI/CD

- Fastlane
- GitHub Actions
- Xcode Cloud
- Bitrise
- Build Automation
- Automated Testing
- Deployment

---

# 20. App Store

- App Store Connect
- TestFlight
- Certificates
- Provisioning Profiles
- Privacy Manifest
- App Review
- App Analytics
- In-App Purchases
- Subscriptions

---

# 21. UI/UX Design

- Apple Human Interface Guidelines
- Typography
- Color Theory
- Layout
- Spacing
- SF Symbols
- Icons
- Dark Mode
- Accessibility

---

# 22. System Design

- Scalability
- Offline First
- Caching
- Synchronization
- Repository Pattern
- Dependency Graph
- State Management
- Background Processing

---

# 23. Software Engineering

- Requirements Gathering
- Planning
- Estimation
- Documentation
- Code Review
- Refactoring
- Technical Debt
- Agile
- Scrum
- Kanban
- Release Management
- Monitoring
- Maintenance

---

# 24. Backend Knowledge

- APIs
- SQL
- NoSQL
- Databases
- Authentication
- Authorization
- Server Architecture
- Microservices
- Webhooks

---

# 25. DevOps Basics

- Linux
- Docker
- Nginx
- Reverse Proxy
- DNS
- SSL
- CDN
- Cloud Storage

---

# 26. Product Engineering

- Product Thinking
- MVP
- User Research
- Analytics
- A/B Testing
- Feature Flags
- Crash Reporting
- Logging
- Metrics

---

# 27. Business

- App Store Optimization (ASO)
- Marketing
- Branding
- Pricing
- Subscription Models
- Revenue Models
- Customer Support

---

# 28. Soft Skills

- Communication
- Technical Writing
- Mentoring
- Leadership
- Interview Skills
- Time Management
- Problem Solving

---

# Continuous Learning

- Apple Documentation
- WWDC Videos
- Swift Evolution Proposals
- Open Source Projects
- Reverse Engineering Apps
- Reading Source Code
- Building Side Projects
- Code Reviews
- System Design Practice
- DSA Practice




# Module Connections Guide

> **Purpose:** Software engineering is not linear. Every module depends on previous knowledge and unlocks future topics. Use this guide to understand how everything connects.

---

# Module 00 — Software Engineering Mindset

### Depends On
- Nothing

### Unlocks
- Every other module

### Real-World Usage
Everything you build starts with understanding the problem before writing code.

---

# Module 01 — Computer Science Fundamentals

### Depends On
- Module 00

### Unlocks
- Swift
- Memory Management
- Concurrency
- Networking
- Performance
- System Design

### Real-World Usage
Understanding CPU, memory, networking, and algorithms helps explain why code behaves the way it does.

---

# Module 02 — Development Environment

### Depends On
- Module 01

### Unlocks
- Every coding module

### Real-World Usage
Git and Xcode become your daily tools. Every feature starts here.

---

# Module 03 — Swift Foundations

### Depends On
- Module 01
- Module 02

### Unlocks
- Advanced Swift
- SwiftUI
- UIKit
- Architecture

### Real-World Usage
Swift is the language used everywhere in your app.

---

# Module 04 — Advanced Swift

### Depends On
- Module 03

### Unlocks
- Architecture
- SwiftUI
- Modern API Design

### Real-World Usage
Generics, protocols, and result builders are heavily used in Apple's frameworks.

---

# Module 05 — Memory & Concurrency

### Depends On
- Module 03
- Module 04

### Unlocks
- SwiftUI
- Networking
- Performance
- Debugging

### Real-World Usage
Know where your code runs, avoid memory leaks, prevent data races, and update UI safely using `@MainActor`.

---

# Module 06 — SwiftUI

### Depends On
- Module 03
- Module 04
- Module 05

### Unlocks
- Real App Development
- Apple Frameworks
- Performance

### Real-World Usage
SwiftUI is where users interact with your application. State management depends on understanding memory and concurrency.

---

# Module 07 — UIKit

### Depends On
- Module 03
- Module 05

### Unlocks
- Legacy Projects
- UIKit Integration
- Advanced UI

### Real-World Usage
Many production apps still contain UIKit.

---

# Module 08 — Architecture

### Depends On
- Module 03
- Module 04
- Module 05

### Unlocks
- Persistence
- Networking
- Testing
- Modularization
- System Design

### Real-World Usage
Architecture determines how easy your app is to maintain, test, and scale.

---

# Module 09 — Persistence

### Depends On
- Module 08

### Unlocks
- Offline Support
- Caching
- System Design

### Real-World Usage
Store user data, cache API responses, and support offline experiences.

---

# Module 10 — Networking

### Depends On
- Module 05
- Module 08

### Unlocks
- Authentication
- Cloud Features
- System Design

### Real-World Usage
Networking should work together with persistence, security, concurrency, and architecture.

---

# Module 11 — Project Organization

### Depends On
- Module 08

### Unlocks
- Large Applications
- Team Development
- CI/CD

### Real-World Usage
Large apps are divided into modules for faster builds and better maintainability.

---

# Module 12 — Testing

### Depends On
- Module 08
- Module 10
- Module 11

### Unlocks
- CI/CD
- Safe Refactoring

### Real-World Usage
Dependency Injection and clean architecture make testing simple and reliable.

---

# Module 13 — Debugging & Performance

### Depends On
- Module 05
- Module 06
- Module 10

### Unlocks
- Production Optimization

### Real-World Usage
Use Instruments, LLDB, and Memory Graph to diagnose and fix performance issues.

---

# Module 14 — Apple Frameworks

### Depends On
- Module 06
- Module 08
- Module 10

### Unlocks
- Advanced iOS Features

### Real-World Usage
Frameworks should integrate naturally into your app's architecture rather than being used in isolation.

---

# Module 15 — Security

### Depends On
- Module 09
- Module 10

### Unlocks
- Production Apps

### Real-World Usage
Protect user data, secure API communication, and store sensitive information safely.

---

# Module 16 — Release

### Depends On
- Modules 00–15

### Unlocks
- App Store Distribution

### Real-World Usage
Prepare, sign, test, and publish production applications.

---

# Module 17 — CI/CD

### Depends On
- Module 11
- Module 12
- Module 16

### Unlocks
- Team Automation

### Real-World Usage
Automate builds, tests, and deployments for reliable releases.

---

# Module 18 — System Design

### Depends On
- Almost Every Previous Module

### Unlocks
- Senior Engineer Thinking

### Real-World Usage
System design combines architecture, networking, persistence, concurrency, performance, and security into scalable solutions.

---

# Module 19 — Backend Knowledge

### Depends On
- Module 10

### Unlocks
- Better API Design
- Full-Stack Communication

### Real-World Usage
Understand how servers work to collaborate effectively with backend engineers.

---

# Module 20 — Product Engineering

### Depends On
- Module 16

### Unlocks
- Better Products

### Real-World Usage
Measure user behavior, analyze crashes, and improve features based on real-world data.

---

# Module 21 — Business

### Depends On
- Module 20

### Unlocks
- Sustainable Apps

### Real-World Usage
Learn how great products generate revenue and reach users.

---

# Module 22 — Leadership & Professional Growth

### Depends On
- All Previous Modules

### Unlocks
- Senior & Staff Engineer Skills

### Real-World Usage
Leadership is about multiplying the impact of your technical skills through communication, mentoring, and sound engineering practices.