> **Purpose**
>
> Store permanent engineering knowledge that can be revisited and improved over time.

> **Use When**
>
> Learning a concept that will remain useful long-term.

> **Do Not Use**
>
> Daily logs, temporary thoughts, or progress updates.

# Processes, Threads & Process Communication

## Overview

A **process** is a running instance of a program. It has its own memory, resources, and at least one thread.

A **thread** is the smallest unit of execution inside a process. Multiple threads within the same process work together and share the process's memory.

Modern operating systems use processes for **isolation and security**, while threads provide **concurrency and responsiveness**.

---

## Why

Understanding processes and threads is essential because almost every iOS concept builds on them.

Topics that depend on this knowledge include:

* Swift Concurrency (`async/await`)
* Actors
* Grand Central Dispatch (GCD)
* URLSession
* Memory Management
* App Performance
* XPC Services
* App Extensions

---

# Key Concepts

## Program vs Process

A **program** is a file stored on disk.

Example:

```text
Safari.app
```

When the operating system launches it, the program becomes a **process**.

```text
Safari.app
        │
        ▼
Safari Process
```

A process only exists while the program is running.

---

## What Does a Process Contain?

Each process owns its own resources.

```text
Safari Process
├── Memory
├── Threads
├── Variables
├── Open Files
├── Network Connections
└── System Resources
```

Each process has its own private memory that other processes cannot access directly.

---

## Why Do Processes Exist?

Processes provide:

* Security
* Stability
* Isolation

If every application shared the same memory:

* One app could overwrite another app's data.
* A crashing app could crash every other app.
* Malware could easily steal data.

Process isolation prevents these problems.

---

## Process Lifecycle

```text
Program (SSD)

↓

Operating System loads it into RAM

↓

Creates Process

↓

CPU executes instructions

↓

Process Ends

↓

Memory is released
```

---

## Multiple Processes from One Program

One program can create multiple processes.

Example: Google Chrome

```text
Chrome

├── Browser Process
├── GPU Process
├── Renderer Process (Tab 1)
├── Renderer Process (Tab 2)
└── Extension Process
```

If one tab crashes, the other processes continue running.

---

# Threads

A thread is the smallest unit of execution inside a process.

Every process has at least one thread.

```text
Process
└── Main Thread
```

Most applications create additional threads.

```text
Music App Process

├── Main Thread
├── Network Thread
├── Database Thread
└── Image Loading Thread
```

---

## Why Multiple Threads?

Without multiple threads:

```text
Download Image

↓

Wait

↓

Update UI
```

The UI freezes.

With multiple threads:

```text
Main Thread
↓

Draw UI

Background Thread
↓

Download Image
```

The user interface remains responsive while background work continues.

---

## Main Thread

On iOS, the Main Thread is responsible for:

* Drawing the UI
* Handling touch events
* Animations

Heavy work should never run on the Main Thread.

---

## Threads Share Memory

Unlike processes, all threads inside the same process share memory.

```text
Process

├── Main Thread
├── Background Thread
└── Worker Thread

Shared Memory
```

This allows fast communication but introduces the possibility of race conditions.

---

## Process vs Thread

| Process             | Thread                 |
| ------------------- | ---------------------- |
| Running program     | Unit of execution      |
| Owns memory         | Shares process memory  |
| Heavyweight         | Lightweight            |
| Expensive to create | Cheap to create        |
| Isolated            | Works inside a process |

---

# Process Communication (IPC)

## Why Can't Processes Access Each Other's Memory?

Every process has its own private memory.

Example:

```text
Safari Process

Memory
---------
Tabs
Cookies
---------

Spotify Process

Memory
---------
Songs
Volume
---------
```

Safari cannot directly read or modify Spotify's memory.

This isolation is enforced by the operating system.

---

## How Do Processes Communicate?

Processes communicate through **Inter-Process Communication (IPC)**.

Common IPC methods:

* Pipes
* Sockets
* Shared Memory
* Message Queues
* XPC (Apple)
* URL Schemes
* Notifications

Instead of sharing memory directly, they exchange messages through the operating system.

---

## Swift Example (URL Scheme)

Suppose you have two applications.

```text
Notes App

Calculator App
```

The Notes app wants to open the Calculator app.

It cannot call:

```swift
CalculatorApp.open()   // ❌ Impossible
```

Instead it asks the operating system:

```swift
UIApplication.shared.open(
    URL(string: "calculator://")!
)
```

The operating system launches the Calculator application.

Communication flow:

```text
Notes Process

↓

Operating System

↓

Calculator Process
```

The two applications never access each other's memory directly.

---

## Apple XPC

On macOS, Apple commonly uses **XPC**.

Example:

```text
Finder

↓

"Compress this folder"

↓

Compression Service

↓

Returns Success
```

Instead of sharing memory, the processes exchange messages.

---

# Memory Management Between Processes

## What Happens When One Process Uses Too Much RAM?

Suppose a Mac has:

```text
16 GB RAM
```

Running applications:

```text
Safari      2 GB

Spotify     500 MB

Xcode       6 GB

Photos      3 GB
```

Everything works normally.

Now another application needs 10 GB.

Total required memory becomes larger than available RAM.

The operating system manages memory automatically.

---

## Step 1 — Memory Compression

Unused memory is compressed to create more available RAM.

```text
Old Memory

↓

Compressed

↓

More Free RAM
```

---

## Step 2 — Swap Memory

If compression is not enough:

```text
RAM

↓

SSD (Swap)
```

Less frequently used memory is moved to disk.

This is called **swap**.

The application continues working but becomes slower because SSDs are much slower than RAM.

---

## Step 3 — Process Termination

If memory is still exhausted, the operating system may terminate processes.

On iOS this commonly happens to background applications.

---

# Virtual Memory

One of the most important operating system concepts.

Processes do **not** own fixed physical RAM locations.

Instead, every process has its own **virtual address space**.

Example:

```text
Safari

0x1000
```

Spotify:

```text
Spotify

0x1000
```

Both processes appear to own address `0x1000`.

However, the operating system maps those virtual addresses to completely different physical RAM locations.

This allows:

* Memory isolation
* Better security
* Easier memory management

---

# Can Processes Access Each Other's Memory?

Normally,

**No.**

The CPU uses a hardware component called the **Memory Management Unit (MMU)**.

Every memory access is checked.

```text
CPU

↓

MMU

↓

Physical RAM
```

If Safari tries to access Spotify's memory:

```text
Safari

↓

Spotify Memory

↓

Access Denied
```

The operating system prevents it.

---

# Creating Multiple Processes in Swift

## iOS

You cannot create additional processes.

Each iOS application runs as a single process.

```text
My App

↓

One Process
```

Inside that process you can create many threads or Swift Concurrency tasks.

Example:

```swift
Task {
    await downloadImage()
}

Task {
    await loadDatabase()
}

Task {
    await uploadFile()
}
```

These are **not** separate processes.

---

## macOS

macOS allows one application to launch another executable.

Example:

```swift
let process = Process()
process.executableURL = URL(fileURLWithPath: "/bin/ls")
try process.run()
```

This creates a new operating system process.

---

# Questions & Answers

## Q: How do processes communicate with each other?

Processes communicate using **Inter-Process Communication (IPC)**.

They never access each other's memory directly.

Instead, they exchange messages through operating system services such as:

* XPC
* Sockets
* Pipes
* URL Schemes
* Shared Memory

---

## Q: When one process uses too much memory, how do other processes continue working?

The operating system manages memory automatically.

It typically follows these steps:

1. Compress memory.
2. Move less-used memory to SSD (swap).
3. Terminate processes if memory is exhausted.

Applications do not manage this themselves.

---

## Q: Is one process stored next to another process in RAM?

No.

Processes use **virtual memory**.

They are not guaranteed to be stored next to each other in physical RAM.

The operating system decides where memory is placed.

---

## Q: Can an iOS app create multiple processes?

No.

An iOS application runs as a single process.

You create concurrency using:

* Threads
* Grand Central Dispatch (GCD)
* Swift Concurrency (`Task`, `async/await`)

---

## Q: Can a macOS app create multiple processes?

Yes.

Using the `Process` API (formerly `NSTask`), a macOS application can launch another executable as a separate process.

---

## Best Practices

* Think of a process as an independent running application.
* Think of a thread as a worker inside that application.
* Never block the Main Thread.
* Use background threads or Swift Concurrency for heavy work.
* Remember that threads share memory but processes do not.
* Prefer message passing over shared mutable state.

---

## Common Mistakes

* Thinking a program and a process are the same thing.
* Assuming threads have separate memory.
* Assuming processes can directly access each other's memory.
* Believing an iOS app can create multiple processes.
* Thinking physical memory is allocated sequentially to processes.

---

## Apple Documentation

* Process
* Threading Programming Guide
* Concurrency Programming Guide
* Swift Concurrency
* Grand Central Dispatch
* XPC Services
* Process (Foundation)

---

## WWDC

* Explore Structured Concurrency in Swift
* Protect Mutable State with Swift Actors
* Meet Async/Await in Swift
* Modern Concurrency in Swift

---

## Related Notes

* Operating Systems
* CPU
* RAM
* Virtual Memory
* Swift Concurrency
* Actors
* Grand Central Dispatch (GCD)
* URLSession
* Memory Management

---

## Revision Questions

1. What is the difference between a program and a process?
2. Why does every process have its own memory?
3. What is the difference between a process and a thread?
4. Why do threads share memory?
5. What problems can shared memory create?
6. What is Inter-Process Communication (IPC)?
7. Why can't one process directly access another process's memory?
8. What happens when RAM becomes full?
9. What is swap memory?
10. What is virtual memory?
11. Why can two processes both use address `0x1000`?
12. Why can an iOS app not create multiple processes?
13. How can a macOS application launch another process?
14. Why should heavy work never run on the Main Thread?

---

## Last Updated

2026-07-23
