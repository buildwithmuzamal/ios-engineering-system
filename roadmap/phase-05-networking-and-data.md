# Phase 05 — Networking & Data

> **Purpose:** Learn how production iOS applications communicate with servers, store data, and provide a reliable user experience even without an internet connection.

---

# Goal

Build robust data-driven applications using Apple's networking and persistence technologies while understanding the engineering decisions behind them.

---

# Learning Outcomes

By the end of this phase you should be able to:

- Build networking layers using URLSession.
- Consume REST APIs.
- Decode and encode JSON using Codable.
- Design reusable networking services.
- Persist local data with SwiftData.
- Implement caching strategies.
- Build offline-first experiences.
- Handle authentication and token refresh.

---

# Module 1 — Networking Fundamentals

## Core Topics

- Client--Server Architecture
- HTTP
- HTTPS
- Request & Response
- Status Codes
- REST APIs

---

## Learning Objectives

After completing this module you should be able to:

- Understand Client--Server Architecture and recognize when it is the right tool.
- Understand HTTP and recognize when it is the right tool.
- Understand HTTPS and recognize when it is the right tool.
- Understand Request & Response and recognize when it is the right tool.
- Understand Status Codes and recognize when it is the right tool.
- Connect the remaining core topics into one coherent mental model.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.
- Builds on Phase 03 Networking Foundation. Focus on production HTTP fundamentals and client-server design.

---

## Parallel Learning Layers

### Git

- Commit networking and persistence layers separately.
- Resolve merge conflicts in model files carefully.
- Link commits to API contract changes.

### Xcode

- Network Link Conditioner awareness
- Console logging
- Breakpoint on failing requests

### Apple Documentation

- URL Loading System
- Codable
- relevant persistence docs

### WWDC

- Networking and data sessions when relevant

### Best Practices

- Prefer clarity when working with Client--Server Architecture.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Client--Server Architecture solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Read a networking client in an open-source iOS project

### AI

- Ask AI to explain Client--Server Architecture after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Client--Server Architecture in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Client--Server Architecture, HTTP, HTTPS, Request & Response.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Client--Server Architecture to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Build a small focused exercise that proves you understand Client--Server Architecture.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Client--Server Architecture correctly in a realistic scenario and explain the trade-offs.
- Use HTTP correctly in a realistic scenario and explain the trade-offs.
- Use HTTPS correctly in a realistic scenario and explain the trade-offs.
- Use Request & Response correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 2 — URLSession

## Core Topics

- URLSession
- URLRequest
- GET
- POST
- PUT
- DELETE

---

## Learning Objectives

After completing this module you should be able to:

- Understand URLSession and recognize when it is the right tool.
- Understand URLRequest and recognize when it is the right tool.
- Understand GET and recognize when it is the right tool.
- Understand POST and recognize when it is the right tool.
- Understand PUT and recognize when it is the right tool.
- Connect the remaining core topics into one coherent mental model.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Commit networking and persistence layers separately.
- Resolve merge conflicts in model files carefully.
- Link commits to API contract changes.

### Xcode

- Network Link Conditioner awareness
- Console logging
- Breakpoint on failing requests

### Apple Documentation

- URL Loading System
- Codable
- relevant persistence docs

### WWDC

- Networking and data sessions when relevant

### Best Practices

- Prefer clarity when working with URLSession.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does URLSession solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Read a networking client in an open-source iOS project

### AI

- Ask AI to explain URLSession after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of URLSession in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document URLSession, URLRequest, GET, POST.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach URLSession to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Build a small focused exercise that proves you understand URLSession.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use URLSession correctly in a realistic scenario and explain the trade-offs.
- Use URLRequest correctly in a realistic scenario and explain the trade-offs.
- Use GET correctly in a realistic scenario and explain the trade-offs.
- Use POST correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 3 — Codable & JSON

## Core Topics

- Codable
- Decodable
- Encodable
- Custom Coding Keys
- Nested JSON

---

## Learning Objectives

After completing this module you should be able to:

- Understand Codable and recognize when it is the right tool.
- Understand Decodable and recognize when it is the right tool.
- Understand Encodable and recognize when it is the right tool.
- Understand Custom Coding Keys and recognize when it is the right tool.
- Understand Nested JSON and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Commit networking and persistence layers separately.
- Resolve merge conflicts in model files carefully.
- Link commits to API contract changes.

### Xcode

- Network Link Conditioner awareness
- Console logging
- Breakpoint on failing requests

### Apple Documentation

- URL Loading System
- Codable
- relevant persistence docs

### WWDC

- Networking and data sessions when relevant

### Best Practices

- Prefer clarity when working with Codable.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Codable solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Read a networking client in an open-source iOS project

### AI

- Ask AI to explain Codable after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Codable in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Codable, Decodable, Encodable, Custom Coding Keys.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Codable to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Build a small focused exercise that proves you understand Codable.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Codable correctly in a realistic scenario and explain the trade-offs.
- Use Decodable correctly in a realistic scenario and explain the trade-offs.
- Use Encodable correctly in a realistic scenario and explain the trade-offs.
- Use Custom Coding Keys correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 4 — Error Handling

## Core Topics

- Network errors
- API errors
- Retry strategies
- User-friendly error messages

---

## Learning Objectives

After completing this module you should be able to:

- Understand Network errors and recognize when it is the right tool.
- Understand API errors and recognize when it is the right tool.
- Understand Retry strategies and recognize when it is the right tool.
- Understand User-friendly error messages and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Commit networking and persistence layers separately.
- Resolve merge conflicts in model files carefully.
- Link commits to API contract changes.

### Xcode

- Network Link Conditioner awareness
- Console logging
- Breakpoint on failing requests

### Apple Documentation

- URL Loading System
- Codable
- relevant persistence docs

### WWDC

- Networking and data sessions when relevant

### Best Practices

- Prefer clarity when working with Network errors.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Network errors solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Read a networking client in an open-source iOS project

### AI

- Ask AI to explain Network errors after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Network errors in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Network errors, API errors, Retry strategies, User-friendly error messages.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Network errors to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Build a small focused exercise that proves you understand Network errors.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Network errors correctly in a realistic scenario and explain the trade-offs.
- Use API errors correctly in a realistic scenario and explain the trade-offs.
- Use Retry strategies correctly in a realistic scenario and explain the trade-offs.
- Use User-friendly error messages correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 5 — Authentication

## Core Topics

- API Keys
- Bearer Tokens
- JWT (Concept)
- Token Refresh
- Secure Storage with Keychain

---

## Learning Objectives

After completing this module you should be able to:

- Understand API Keys and recognize when it is the right tool.
- Understand Bearer Tokens and recognize when it is the right tool.
- Understand JWT (Concept) and recognize when it is the right tool.
- Understand Token Refresh and recognize when it is the right tool.
- Understand Secure Storage with Keychain and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Commit networking and persistence layers separately.
- Resolve merge conflicts in model files carefully.
- Link commits to API contract changes.

### Xcode

- Keychain debugging caution
- Scheme environment variables
- Console redaction habits

### Apple Documentation

- Security overview
- Keychain Services
- App Privacy details

### WWDC

- Security and privacy sessions relevant to the module

### Best Practices

- Prefer clarity when working with API Keys.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does API Keys solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study how an open-source app stores credentials

### AI

- Ask AI to explain API Keys after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of API Keys in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document API Keys, Bearer Tokens, JWT (Concept), Token Refresh.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach API Keys to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Build a small focused exercise that proves you understand API Keys.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use API Keys correctly in a realistic scenario and explain the trade-offs.
- Use Bearer Tokens correctly in a realistic scenario and explain the trade-offs.
- Use JWT (Concept) correctly in a realistic scenario and explain the trade-offs.
- Use Token Refresh correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 6 — Local Persistence

## Core Topics

- SwiftData
- UserDefaults
- FileManager
- Choosing the right storage

---

## Learning Objectives

After completing this module you should be able to:

- Understand SwiftData and recognize when it is the right tool.
- Understand UserDefaults and recognize when it is the right tool.
- Understand FileManager and recognize when it is the right tool.
- Understand Choosing the right storage and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.
- Builds on Phase 03 Persistence. Focus on choosing storage and designing a persistence layer for production apps.

---

## Parallel Learning Layers

### Git

- Commit networking and persistence layers separately.
- Resolve merge conflicts in model files carefully.
- Link commits to API contract changes.

### Xcode

- Navigator
- Quick Help
- Breakpoints
- Documentation viewer

### Apple Documentation

- Official docs related to SwiftData, UserDefaults, FileManager, Choosing the right storage

### WWDC

- Only sessions that directly strengthen this module

### Best Practices

- Prefer clarity when working with SwiftData.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does SwiftData solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Find a small open-source example related to SwiftData

### AI

- Ask AI to explain SwiftData after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of SwiftData in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document SwiftData, UserDefaults, FileManager, Choosing the right storage.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach SwiftData to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Build a small focused exercise that proves you understand SwiftData.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use SwiftData correctly in a realistic scenario and explain the trade-offs.
- Use UserDefaults correctly in a realistic scenario and explain the trade-offs.
- Use FileManager correctly in a realistic scenario and explain the trade-offs.
- Use Choosing the right storage correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 7 — Caching & Offline-First

## Core Topics

- Memory Cache
- Disk Cache
- Cache Policies
- Offline-first design
- Data Synchronization

---

## Learning Objectives

After completing this module you should be able to:

- Understand Memory Cache and recognize when it is the right tool.
- Understand Disk Cache and recognize when it is the right tool.
- Understand Cache Policies and recognize when it is the right tool.
- Understand Offline-first design and recognize when it is the right tool.
- Understand Data Synchronization and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Commit networking and persistence layers separately.
- Resolve merge conflicts in model files carefully.
- Link commits to API contract changes.

### Xcode

- Network Link Conditioner awareness
- Console logging
- Breakpoint on failing requests

### Apple Documentation

- URL Loading System
- Codable
- relevant persistence docs

### WWDC

- Networking and data sessions when relevant

### Best Practices

- Prefer clarity when working with Memory Cache.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Memory Cache solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Read a networking client in an open-source iOS project

### AI

- Ask AI to explain Memory Cache after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Memory Cache in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Memory Cache, Disk Cache, Cache Policies, Offline-first design.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Memory Cache to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Build a small focused exercise that proves you understand Memory Cache.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Memory Cache correctly in a realistic scenario and explain the trade-offs.
- Use Disk Cache correctly in a realistic scenario and explain the trade-offs.
- Use Cache Policies correctly in a realistic scenario and explain the trade-offs.
- Use Offline-first design correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 8 — Repository Pattern

## Core Topics

- Repository Pattern
- Data Sources
- Remote vs Local Data
- Single Source of Truth

---

## Learning Objectives

After completing this module you should be able to:

- Understand Repository Pattern and recognize when it is the right tool.
- Understand Data Sources and recognize when it is the right tool.
- Understand Remote vs Local Data and recognize when it is the right tool.
- Understand Single Source of Truth and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.
- Applies the repository idea from architecture thinking to networking and persistence data sources.

---

## Parallel Learning Layers

### Git

- Commit networking and persistence layers separately.
- Resolve merge conflicts in model files carefully.
- Link commits to API contract changes.

### Xcode

- Network Link Conditioner awareness
- Console logging
- Breakpoint on failing requests

### Apple Documentation

- URL Loading System
- Codable
- relevant persistence docs

### WWDC

- Networking and data sessions when relevant

### Best Practices

- Prefer clarity when working with Repository Pattern.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Repository Pattern solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Read a networking client in an open-source iOS project

### AI

- Ask AI to explain Repository Pattern after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Repository Pattern in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Repository Pattern, Data Sources, Remote vs Local Data, Single Source of Truth.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Repository Pattern to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Build a small focused exercise that proves you understand Repository Pattern.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Repository Pattern correctly in a realistic scenario and explain the trade-offs.
- Use Data Sources correctly in a realistic scenario and explain the trade-offs.
- Use Remote vs Local Data correctly in a realistic scenario and explain the trade-offs.
- Use Single Source of Truth correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Phase Project

Build a production-style application that includes: - REST API integration - URLSession - Codable - Authentication - SwiftData - Local caching - Offline-first support - Repository Pattern Document: - Data flow - Networking architecture - Persistence decisions - Offline strategy - Trade-offs ------------------------------------------------------------------------

---

# Exit Criteria

You are ready for the next phase when you can:

- Design a reusable networking layer.
- Consume REST APIs confidently.
- Decode complex JSON.
- Store and synchronize local data.
- Build offline
- capable applications.
- Explain networking and persistence trade
- offs.

---

# Next Phase

➡️ Phase 06 — Testing
