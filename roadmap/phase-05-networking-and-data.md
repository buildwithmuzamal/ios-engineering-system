# Phase 05 --- Networking & Data

> **Purpose:** Learn how production iOS applications communicate with
> servers, store data, and provide a reliable user experience even
> without an internet connection.

------------------------------------------------------------------------

# Goal

Build robust data-driven applications using Apple's networking and
persistence technologies while understanding the engineering decisions
behind them.

------------------------------------------------------------------------

# Learning Outcomes

By the end of this phase you should be able to:

-   Build networking layers using URLSession.
-   Consume REST APIs.
-   Decode and encode JSON using Codable.
-   Design reusable networking services.
-   Persist local data with SwiftData.
-   Implement caching strategies.
-   Build offline-first experiences.
-   Handle authentication and token refresh.

------------------------------------------------------------------------

# Module 1 --- Networking Fundamentals

## Core Topic

-   Client--Server Architecture
-   HTTP
-   HTTPS
-   Request & Response
-   Status Codes
-   REST APIs

### Parallel Learning Layers

**Git** - Pull latest changes - Resolve simple merge conflicts

**Xcode** - Network Console - Debug Console

**Apple Documentation** - URL Loading System

**Best Practices** - Never hardcode URLs - Separate networking logic

**Design Thinking** - Why REST? - Why separate networking from UI?

**AI** - Review networking design instead of generating requests

**English** - Request, Response, Endpoint, Payload, Header

**DSA** - Hash Maps for response caching (concept)

**Practice** - Explore a public REST API.

------------------------------------------------------------------------

# Module 2 --- URLSession

## Core Topic

-   URLSession
-   URLRequest
-   GET
-   POST
-   PUT
-   DELETE

### Practice

Build reusable API request functions.

------------------------------------------------------------------------

# Module 3 --- Codable & JSON

## Core Topic

-   Codable
-   Decodable
-   Encodable
-   Custom Coding Keys
-   Nested JSON

### Best Practices

-   Keep models simple
-   Separate API models from domain models when appropriate

### Practice

Decode complex JSON responses.

------------------------------------------------------------------------

# Module 4 --- Error Handling

## Core Topic

-   Network errors
-   API errors
-   Retry strategies
-   User-friendly error messages

### Design Thinking

-   Fail gracefully
-   Don't expose technical errors to users

------------------------------------------------------------------------

# Module 5 --- Authentication

## Core Topic

-   API Keys
-   Bearer Tokens
-   JWT (Concept)
-   Token Refresh
-   Secure Storage with Keychain

### Practice

Authenticate against a demo API.

------------------------------------------------------------------------

# Module 6 --- Local Persistence

## Core Topic

-   SwiftData
-   UserDefaults
-   FileManager
-   Choosing the right storage

### Best Practices

-   Store only what you need
-   Separate persistence layer

### Practice

Persist application data locally.

------------------------------------------------------------------------

# Module 7 --- Caching & Offline-First

## Core Topic

-   Memory Cache
-   Disk Cache
-   Cache Policies
-   Offline-first design
-   Data Synchronization

### Design Thinking

-   What should happen when the internet is unavailable?
-   How do professional apps stay usable offline?

### Practice

Build an app that loads cached data when offline.

------------------------------------------------------------------------

# Module 8 --- Repository Pattern

## Core Topic

-   Repository Pattern
-   Data Sources
-   Remote vs Local Data
-   Single Source of Truth

### Practice

Refactor networking and persistence behind repositories.

------------------------------------------------------------------------

# Phase Project

Build a production-style application that includes:

-   REST API integration
-   URLSession
-   Codable
-   Authentication
-   SwiftData
-   Local caching
-   Offline-first support
-   Repository Pattern

Document: - Data flow - Networking architecture - Persistence
decisions - Offline strategy - Trade-offs

------------------------------------------------------------------------

# Exit Criteria

You can:

-   Design a reusable networking layer.
-   Consume REST APIs confidently.
-   Decode complex JSON.
-   Store and synchronize local data.
-   Build offline-capable applications.
-   Explain networking and persistence trade-offs.

------------------------------------------------------------------------

# Next Phase

➡️ Phase 06 --- Testing
