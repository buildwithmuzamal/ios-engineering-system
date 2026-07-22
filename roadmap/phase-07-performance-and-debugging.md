# Phase 07 — Performance & Debugging

> **Purpose:** Learn to find, understand, and fix performance, memory, > rendering, and runtime issues using professional engineering tools.

---

# Goal

Build applications that are not only correct, but fast, responsive, memory efficient, and easy to debug.

---

# Learning Outcomes

By the end of this phase you should be able to:

- Profile apps with Instruments.
- Diagnose memory leaks.
- Optimize SwiftUI rendering.
- Debug complex production issues.
- Measure before optimizing.

---

# Module 1 — Debugging Mindset

## Core Topics

- Reproduce bugs
- Isolate root cause
- Form hypotheses
- Verify fixes

---

## Learning Objectives

After completing this module you should be able to:

- Understand Reproduce bugs and recognize when it is the right tool.
- Understand Isolate root cause and recognize when it is the right tool.
- Understand Form hypotheses and recognize when it is the right tool.
- Understand Verify fixes and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.
- Builds on Phase 00 Debugging Basics and Phase 02 Performance. Focus on professional debugging process.

---

## Parallel Learning Layers

### Git

- Use git bisect to find performance regressions.
- Branch for profiling experiments.
- Document measured improvements in commit messages.

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

- Prefer clarity when working with Reproduce bugs.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Reproduce bugs solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Read a performance-related pull request

### AI

- Ask AI to explain Reproduce bugs after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Reproduce bugs in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Reproduce bugs, Isolate root cause, Form hypotheses, Verify fixes.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Reproduce bugs to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Build a small focused exercise that proves you understand Reproduce bugs.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Reproduce bugs correctly in a realistic scenario and explain the trade-offs.
- Use Isolate root cause correctly in a realistic scenario and explain the trade-offs.
- Use Form hypotheses correctly in a realistic scenario and explain the trade-offs.
- Use Verify fixes correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 2 — Instruments

## Core Topics

- Time Profiler - Allocations - Leaks - Memory Graph - Signposts

---

## Learning Objectives

After completing this module you should be able to:

- Understand Time Profiler - Allocations - Leaks - Memory Graph - Signposts and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use git bisect to find performance regressions.
- Branch for profiling experiments.
- Document measured improvements in commit messages.

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

- Prefer clarity when working with Time Profiler - Allocations - Leaks - Memory Graph - Signposts.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Time Profiler - Allocations - Leaks - Memory Graph - Signposts solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Read a performance-related pull request

### AI

- Ask AI to explain Time Profiler - Allocations - Leaks - Memory Graph - Signposts after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Time Profiler - Allocations - Leaks - Memory Graph - Signposts in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Time Profiler - Allocations - Leaks - Memory Graph - Signposts.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Time Profiler - Allocations - Leaks - Memory Graph - Signposts to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Profile an existing app.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Time Profiler - Allocations - Leaks - Memory Graph - Signposts correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 3 — Memory Management

## Core Topics

- Retain cycles - Heap vs Stack review - ARC review - Memory Graph

---

## Learning Objectives

After completing this module you should be able to:

- Understand Retain cycles - Heap vs Stack review - ARC review - Memory Graph and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use git bisect to find performance regressions.
- Branch for profiling experiments.
- Document measured improvements in commit messages.

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

- Prefer clarity when working with Retain cycles - Heap vs Stack review - ARC review - Memory Graph.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Retain cycles - Heap vs Stack review - ARC review - Memory Graph solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Read a performance-related pull request

### AI

- Ask AI to explain Retain cycles - Heap vs Stack review - ARC review - Memory Graph after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Retain cycles - Heap vs Stack review - ARC review - Memory Graph in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Retain cycles - Heap vs Stack review - ARC review - Memory Graph.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Retain cycles - Heap vs Stack review - ARC review - Memory Graph to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Remove leaks.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Retain cycles - Heap vs Stack review - ARC review - Memory Graph correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 4 — SwiftUI Performance

## Core Topics

- View identity - Lazy containers - Equatable - Rendering - State

---

## Learning Objectives

After completing this module you should be able to:

- Understand View identity - Lazy containers - Equatable - Rendering - State and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.
- Deepens Phase 02 Performance with Instruments-backed SwiftUI optimization.

---

## Parallel Learning Layers

### Git

- Use git bisect to find performance regressions.
- Branch for profiling experiments.
- Document measured improvements in commit messages.

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

- Prefer clarity when working with View identity - Lazy containers - Equatable - Rendering - State.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does View identity - Lazy containers - Equatable - Rendering - State solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Read a performance-related pull request

### AI

- Ask AI to explain View identity - Lazy containers - Equatable - Rendering - State after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of View identity - Lazy containers - Equatable - Rendering - State in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document View identity - Lazy containers - Equatable - Rendering - State.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach View identity - Lazy containers - Equatable - Rendering - State to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Optimize a scrolling screen.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use View identity - Lazy containers - Equatable - Rendering - State correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 5 — Performance Optimization

## Core Topics

- Startup time - Image loading - Network efficiency - Background

---

## Learning Objectives

After completing this module you should be able to:

- Understand Startup time - Image loading - Network efficiency - Background and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use git bisect to find performance regressions.
- Branch for profiling experiments.
- Document measured improvements in commit messages.

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

- Prefer clarity when working with Startup time - Image loading - Network efficiency - Background.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Startup time - Image loading - Network efficiency - Background solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Read a performance-related pull request

### AI

- Ask AI to explain Startup time - Image loading - Network efficiency - Background after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Startup time - Image loading - Network efficiency - Background in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Startup time - Image loading - Network efficiency - Background.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Startup time - Image loading - Network efficiency - Background to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Improve a real feature.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Startup time - Image loading - Network efficiency - Background correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 6 — Crash Analysis

## Core Topics

- Crash logs - Symbolication - Assertions - Preconditions

---

## Learning Objectives

After completing this module you should be able to:

- Understand Crash logs - Symbolication - Assertions - Preconditions and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Use git bisect to find performance regressions.
- Branch for profiling experiments.
- Document measured improvements in commit messages.

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

- Prefer clarity when working with Crash logs - Symbolication - Assertions - Preconditions.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Crash logs - Symbolication - Assertions - Preconditions solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Read a performance-related pull request

### AI

- Ask AI to explain Crash logs - Symbolication - Assertions - Preconditions after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Crash logs - Symbolication - Assertions - Preconditions in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Crash logs - Symbolication - Assertions - Preconditions.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Crash logs - Symbolication - Assertions - Preconditions to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Build a small focused exercise that proves you understand Crash logs - Symbolication - Assertions - Preconditions.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Crash logs - Symbolication - Assertions - Preconditions correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Phase Project

Take one previous application and: - Profile with Instruments - Remove memory leaks - Improve launch time - Optimize one SwiftUI screen - Fix at least three real bugs - Document every optimization and its measured impact

---

# Exit Criteria

You are ready for the next phase when you can:

- Debug confidently.
- Use Instruments effectively.
- Explain performance bottlenecks.
- Optimize based on evidence.
- Read crash reports.

---

# Next Phase

➡️ Phase 08 — Security
