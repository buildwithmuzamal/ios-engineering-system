# Phase 06 --- Testing

> **Purpose:** Learn to build reliable, maintainable software through
> automated testing. Testing is a core engineering skill, not an
> afterthought.

------------------------------------------------------------------------

# Goal

Develop the confidence to change code safely by writing effective
automated tests and designing software that is easy to test.

------------------------------------------------------------------------

# Learning Outcomes

By the end of this phase you should be able to:

-   Write unit, integration, and UI tests.
-   Understand what should and should not be tested.
-   Design testable code.
-   Use TDD when appropriate.
-   Debug failing tests.
-   Build confidence before shipping features.

------------------------------------------------------------------------

# Module 1 --- Testing Fundamentals

## Core Topic

-   Why testing matters
-   Types of tests
-   XCTest
-   Test pyramid
-   Test lifecycle

### Parallel Learning Layers

**Git** - Create small commits before writing tests. - Review changes
with `git diff`.

**Xcode** - Test Navigator - Run individual tests - Debug failing tests

**Apple Documentation** - XCTest documentation

**WWDC** - Testing sessions relevant to XCTest

**Best Practices** - Test behavior, not implementation. - Keep tests
independent.

**Design Thinking** - What makes code easy to test?

**AI** - Review test quality instead of generating all tests.

**English** - Test Case - Assertion - Fixture - Failure - Mock

**DSA** - Use simple deterministic data structures for tests.

**Practice** - Write your first XCTest cases.

**Notes** - Document testing terminology.

**Reflection** - Why do professional teams invest heavily in testing?

------------------------------------------------------------------------

# Module 2 --- Unit Testing

## Core Topic

-   XCTest
-   Assertions
-   Arrange--Act--Assert
-   Test naming
-   Edge cases

### Parallel Learning Layers

**Git** - Commit after each passing test.

**Best Practices** - One behavior per test.

**Practice** - Test ViewModels and business logic.

------------------------------------------------------------------------

# Module 3 --- Test Doubles

## Core Topic

-   Mock
-   Stub
-   Fake
-   Spy
-   Dummy

### Design Thinking

-   Why isolate dependencies?

### Practice

Replace real networking with mocks.

------------------------------------------------------------------------

# Module 4 --- Testable Architecture

## Core Topic

-   Dependency Injection
-   Protocols
-   Repository Pattern
-   Separation of concerns

### Practice

Refactor existing code to improve testability.

------------------------------------------------------------------------

# Module 5 --- Integration Testing

## Core Topic

-   Testing multiple components together
-   Repository + Networking
-   Repository + SwiftData

### Practice

Verify data flows through your application correctly.

------------------------------------------------------------------------

# Module 6 --- UI Testing

## Core Topic

-   XCUITest
-   Launching applications
-   UI interactions
-   Accessibility identifiers

### Xcode Layer

-   Record UI tests
-   Debug UI tests

### Practice

Automate common user flows.

------------------------------------------------------------------------

# Module 7 --- Test-Driven Development (TDD)

## Core Topic

-   Red
-   Green
-   Refactor

### Design Thinking

-   When is TDD valuable?
-   When is it unnecessary?

### Practice

Build a small feature using TDD.

------------------------------------------------------------------------

# Module 8 --- Snapshot & Performance Testing

## Core Topic

-   Snapshot Testing
-   Performance Tests
-   Measuring execution time

### Best Practices

-   Only snapshot stable UI.
-   Measure meaningful scenarios.

------------------------------------------------------------------------

# Phase Project

Improve one of your previous applications by adding:

-   Unit Tests
-   Integration Tests
-   UI Tests
-   Test Doubles
-   Dependency Injection
-   Performance Tests

Document:

-   Testing strategy
-   Coverage decisions
-   Trade-offs
-   Lessons learned

------------------------------------------------------------------------

# Exit Criteria

You can:

-   Write reliable automated tests.
-   Design software for testability.
-   Use test doubles correctly.
-   Apply TDD when appropriate.
-   Debug failing tests confidently.
-   Explain the trade-offs between different testing strategies.

------------------------------------------------------------------------

# Next Phase

➡️ Phase 07 --- Performance & Debugging
