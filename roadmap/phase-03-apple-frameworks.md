# Phase 03 — Apple Frameworks

> **Purpose:** Learn Apple's frameworks by solving real-world problems instead of studying APIs in isolation.

---

# Goal

Understand when, why, and how to use Apple's frameworks while developing production-quality applications.

---

# Learning Outcomes

By the end of this phase you should be able to:

- Select the right framework for a problem.
- Read framework documentation confidently.
- Integrate Apple frameworks into SwiftUI apps.
- Understand framework trade-offs.
- Build apps using multiple Apple technologies.

---

# Module 1 — Foundation Framework

## Core Topics

- Date
- URL
- URLComponents
- JSON
- FileManager
- UserDefaults
- Measurement
- Locale

---

## Learning Objectives

After completing this module you should be able to:

- Understand Date and recognize when it is the right tool.
- Understand URL and recognize when it is the right tool.
- Understand URLComponents and recognize when it is the right tool.
- Understand JSON and recognize when it is the right tool.
- Understand FileManager and recognize when it is the right tool.
- Connect the remaining core topics into one coherent mental model.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Rebase a short feature branch onto main.
- Separate framework experiments into clear commits.
- Tag a working integration checkpoint.

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

- Prefer clarity when working with Date.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Date solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Read a networking client in an open-source iOS project

### AI

- Ask AI to explain Date after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Date in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Date, URL, URLComponents, JSON.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Date to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Build a small focused exercise that proves you understand Date.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Date correctly in a realistic scenario and explain the trade-offs.
- Use URL correctly in a realistic scenario and explain the trade-offs.
- Use URLComponents correctly in a realistic scenario and explain the trade-offs.
- Use JSON correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 2 — Persistence

## Core Topics

- UserDefaults
- FileManager
- SwiftData
- Core Data (legacy understanding)

---

## Learning Objectives

After completing this module you should be able to:

- Understand UserDefaults and recognize when it is the right tool.
- Understand FileManager and recognize when it is the right tool.
- Understand SwiftData and recognize when it is the right tool.
- Understand Core Data (legacy understanding) and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.
- This introduces Apple persistence options. Production offline-first design is deepened in Phase 05.

---

## Parallel Learning Layers

### Git

- Rebase a short feature branch onto main.
- Separate framework experiments into clear commits.
- Tag a working integration checkpoint.

### Xcode

- Navigator
- Quick Help
- Breakpoints
- Documentation viewer

### Apple Documentation

- Official docs related to UserDefaults, FileManager, SwiftData, Core Data (legacy understanding)

### WWDC

- Only sessions that directly strengthen this module

### Best Practices

- Prefer clarity when working with UserDefaults.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does UserDefaults solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Find a small open-source example related to UserDefaults

### AI

- Ask AI to explain UserDefaults after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of UserDefaults in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document UserDefaults, FileManager, SwiftData, Core Data (legacy understanding).
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach UserDefaults to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Create a simple notes application with SwiftData.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use UserDefaults correctly in a realistic scenario and explain the trade-offs.
- Use FileManager correctly in a realistic scenario and explain the trade-offs.
- Use SwiftData correctly in a realistic scenario and explain the trade-offs.
- Use Core Data (legacy understanding) correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 3 — Networking Foundation

## Core Topics

- URL
- URLRequest
- URLSession
- JSONDecoder
- JSONEncoder

---

## Learning Objectives

After completing this module you should be able to:

- Understand URL and recognize when it is the right tool.
- Understand URLRequest and recognize when it is the right tool.
- Understand URLSession and recognize when it is the right tool.
- Understand JSONDecoder and recognize when it is the right tool.
- Understand JSONEncoder and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.
- This is an introduction to networking APIs. Production networking architecture is deepened in Phase 05.

---

## Parallel Learning Layers

### Git

- Rebase a short feature branch onto main.
- Separate framework experiments into clear commits.
- Tag a working integration checkpoint.

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

- Prefer clarity when working with URL.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does URL solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Read a networking client in an open-source iOS project

### AI

- Ask AI to explain URL after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of URL in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document URL, URLRequest, URLSession, JSONDecoder.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach URL to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Fetch and display remote data with URLSession and Codable.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use URL correctly in a realistic scenario and explain the trade-offs.
- Use URLRequest correctly in a realistic scenario and explain the trade-offs.
- Use URLSession correctly in a realistic scenario and explain the trade-offs.
- Use JSONDecoder correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 4 — Media Frameworks

## Core Topics

- PhotosPicker
- AVFoundation
- Camera basics
- Sharing

---

## Learning Objectives

After completing this module you should be able to:

- Understand PhotosPicker and recognize when it is the right tool.
- Understand AVFoundation and recognize when it is the right tool.
- Understand Camera basics and recognize when it is the right tool.
- Understand Sharing and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Rebase a short feature branch onto main.
- Separate framework experiments into clear commits.
- Tag a working integration checkpoint.

### Xcode

- Navigator
- Quick Help
- Breakpoints
- Documentation viewer

### Apple Documentation

- Official docs related to PhotosPicker, AVFoundation, Camera basics, Sharing

### WWDC

- Only sessions that directly strengthen this module

### Best Practices

- Prefer clarity when working with PhotosPicker.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does PhotosPicker solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Find a small open-source example related to PhotosPicker

### AI

- Ask AI to explain PhotosPicker after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of PhotosPicker in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document PhotosPicker, AVFoundation, Camera basics, Sharing.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach PhotosPicker to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Create a media picker feature with PhotosPicker and sharing.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use PhotosPicker correctly in a realistic scenario and explain the trade-offs.
- Use AVFoundation correctly in a realistic scenario and explain the trade-offs.
- Use Camera basics correctly in a realistic scenario and explain the trade-offs.
- Use Sharing correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 5 — Location & Maps

## Core Topics

- CoreLocation
- MapKit
- Permissions

---

## Learning Objectives

After completing this module you should be able to:

- Understand CoreLocation and recognize when it is the right tool.
- Understand MapKit and recognize when it is the right tool.
- Understand Permissions and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Rebase a short feature branch onto main.
- Separate framework experiments into clear commits.
- Tag a working integration checkpoint.

### Xcode

- Navigator
- Quick Help
- Breakpoints
- Documentation viewer

### Apple Documentation

- Official docs related to CoreLocation, MapKit, Permissions

### WWDC

- Only sessions that directly strengthen this module

### Best Practices

- Prefer clarity when working with CoreLocation.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does CoreLocation solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Find a small open-source example related to CoreLocation

### AI

- Ask AI to explain CoreLocation after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of CoreLocation in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document CoreLocation, MapKit, Permissions.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach CoreLocation to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Display user location on a map with proper permissions.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use CoreLocation correctly in a realistic scenario and explain the trade-offs.
- Use MapKit correctly in a realistic scenario and explain the trade-offs.
- Use Permissions correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 6 — Notifications

## Core Topics

- Local Notifications
- Notification Permissions
- Background delivery basics

---

## Learning Objectives

After completing this module you should be able to:

- Understand Local Notifications and recognize when it is the right tool.
- Understand Notification Permissions and recognize when it is the right tool.
- Understand Background delivery basics and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Rebase a short feature branch onto main.
- Separate framework experiments into clear commits.
- Tag a working integration checkpoint.

### Xcode

- Navigator
- Quick Help
- Breakpoints
- Documentation viewer

### Apple Documentation

- Official docs related to Local Notifications, Notification Permissions, Background delivery basics

### WWDC

- Only sessions that directly strengthen this module

### Best Practices

- Prefer clarity when working with Local Notifications.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Local Notifications solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Find a small open-source example related to Local Notifications

### AI

- Ask AI to explain Local Notifications after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Local Notifications in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Local Notifications, Notification Permissions, Background delivery basics.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Local Notifications to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Schedule local notification reminders with permission handling.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Local Notifications correctly in a realistic scenario and explain the trade-offs.
- Use Notification Permissions correctly in a realistic scenario and explain the trade-offs.
- Use Background delivery basics correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 7 — Background Work

## Core Topics

- BackgroundTasks
- App lifecycle
- Scene phase

---

## Learning Objectives

After completing this module you should be able to:

- Understand BackgroundTasks and recognize when it is the right tool.
- Understand App lifecycle and recognize when it is the right tool.
- Understand Scene phase and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Rebase a short feature branch onto main.
- Separate framework experiments into clear commits.
- Tag a working integration checkpoint.

### Xcode

- Navigator
- Quick Help
- Breakpoints
- Documentation viewer

### Apple Documentation

- Official docs related to BackgroundTasks, App lifecycle, Scene phase

### WWDC

- Only sessions that directly strengthen this module

### Best Practices

- Prefer clarity when working with BackgroundTasks.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does BackgroundTasks solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Find a small open-source example related to BackgroundTasks

### AI

- Ask AI to explain BackgroundTasks after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of BackgroundTasks in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document BackgroundTasks, App lifecycle, Scene phase.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach BackgroundTasks to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Refresh cached data using BackgroundTasks and scene phase awareness.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use BackgroundTasks correctly in a realistic scenario and explain the trade-offs.
- Use App lifecycle correctly in a realistic scenario and explain the trade-offs.
- Use Scene phase correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 8 — Widgets & App Intents

## Core Topics

- WidgetKit
- App Intents
- Interactive Widgets

---

## Learning Objectives

After completing this module you should be able to:

- Understand WidgetKit and recognize when it is the right tool.
- Understand App Intents and recognize when it is the right tool.
- Understand Interactive Widgets and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.
- Widgets appear again in Phase 12 with multiplatform depth. Here focus on building a first widget for an existing app.

---

## Parallel Learning Layers

### Git

- Rebase a short feature branch onto main.
- Separate framework experiments into clear commits.
- Tag a working integration checkpoint.

### Xcode

- Navigator
- Quick Help
- Breakpoints
- Documentation viewer

### Apple Documentation

- Official docs related to WidgetKit, App Intents, Interactive Widgets

### WWDC

- Only sessions that directly strengthen this module

### Best Practices

- Prefer clarity when working with WidgetKit.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does WidgetKit solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Find a small open-source example related to WidgetKit

### AI

- Ask AI to explain WidgetKit after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of WidgetKit in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document WidgetKit, App Intents, Interactive Widgets.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach WidgetKit to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Build a widget for an existing project using WidgetKit.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use WidgetKit correctly in a realistic scenario and explain the trade-offs.
- Use App Intents correctly in a realistic scenario and explain the trade-offs.
- Use Interactive Widgets correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 9 — Cloud & Purchases

## Core Topics

- CloudKit (Introduction)
- StoreKit (Introduction)

---

## Learning Objectives

After completing this module you should be able to:

- Understand CloudKit (Introduction) and recognize when it is the right tool.
- Understand StoreKit (Introduction) and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Rebase a short feature branch onto main.
- Separate framework experiments into clear commits.
- Tag a working integration checkpoint.

### Xcode

- Navigator
- Quick Help
- Breakpoints
- Documentation viewer

### Apple Documentation

- Official docs related to CloudKit (Introduction), StoreKit (Introduction)

### WWDC

- Only sessions that directly strengthen this module

### Best Practices

- Prefer clarity when working with CloudKit (Introduction).
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does CloudKit (Introduction) solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Find a small open-source example related to CloudKit (Introduction)

### AI

- Ask AI to explain CloudKit (Introduction) after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of CloudKit (Introduction) in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document CloudKit (Introduction), StoreKit (Introduction).
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach CloudKit (Introduction) to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Prototype a CloudKit or StoreKit decision memo and a minimal proof-of-concept.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use CloudKit (Introduction) correctly in a realistic scenario and explain the trade-offs.
- Use StoreKit (Introduction) correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Phase Project

Build a production-ready application that includes: - SwiftData - URLSession - Photos - Notifications - Background Tasks - Widget - MapKit Document: - Framework selection - Trade-offs - Apple recommendations ------------------------------------------------------------------------

---

# Exit Criteria

You are ready for the next phase when you can:

- Choose the correct Apple framework.
- Read framework documentation independently.
- Integrate multiple frameworks into one app.
- Understand common framework trade
- offs.

---

# Next Phase

➡️ Phase 04 — Professional App Architecture
