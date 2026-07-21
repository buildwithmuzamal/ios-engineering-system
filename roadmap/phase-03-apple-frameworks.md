# Phase 03 — Apple Frameworks

> **Purpose:** Master Apple's frameworks by understanding not only how they work individually, but how they work together to build production-quality applications.

---

# Goal

Develop the ability to confidently select, integrate, and use Apple's frameworks while understanding their responsibilities, limitations, and trade-offs.

---

# Learning Outcomes

By the end of this phase you should be able to:

- Choose the correct framework for a problem.
- Read Apple framework documentation efficiently.
- Integrate multiple frameworks into one application.
- Understand framework dependencies.
- Design applications around Apple's ecosystem.
- Continue learning newly released frameworks independently.

---

# Module 1 — Foundation Frameworks

## Core Topics

- Foundation
- URL
- Date
- Calendar
- TimeZone
- Locale
- Measurement
- UUID
- Data
- JSON
- Codable
- FileManager
- UserDefaults
- Bundle
- ProcessInfo

---

## Learning Objectives

After completing this module you should understand:

- Why Foundation is the backbone of nearly every Apple application.
- How Foundation simplifies common development tasks.
- How data is represented, stored, and transformed.
- How to work with files, dates, and user preferences.
- When to use each Foundation type.

---

## Parallel Learning Layers

### Git

Learn:

- Organize utility classes separately.
- Commit Foundation exercises independently.
- Practice meaningful commit history.

Practice:

Create one commit for every major Foundation topic.

---

### Xcode

Learn:

- Debug Console
- File System inspection
- Breakpoints
- Playground experiments

Practice:

Prototype Foundation APIs inside Playgrounds before integrating them into applications.

---

### Apple Documentation

Read:

- Foundation Overview
- Codable
- FileManager
- UserDefaults
- URL
- Date
- Calendar

Goal

Become comfortable navigating Foundation documentation without tutorials.

---

### WWDC

Recommended Topics

- What's New in Foundation
- Meet Foundation Improvements
- Modern Swift APIs

Goal

Understand Apple's evolution of Foundation.

---

### Best Practices

Learn:

- Prefer Codable over manual parsing.
- Store only lightweight preferences in UserDefaults.
- Use FileManager for documents.
- Avoid force-unwrapping URLs.
- Handle dates using Calendar and Locale.

Avoid:

- Storing sensitive data in UserDefaults.
- Hardcoded date formats.
- Manual JSON parsing.

---

### Design Thinking

Questions to ask:

- Which Foundation type best represents this data?
- Is there an existing Apple API instead of writing custom code?

---

### Architecture Thinking

Understand:

Foundation belongs to the infrastructure layer.

Business logic should depend on abstractions—not directly on implementation details whenever possible.

---

### Open Source

Study:

Production projects using:

- Codable
- FileManager
- UserDefaults
- URLSession support classes

Observe:

- Utility organization.
- Extensions.
- Helpers.
- Error handling.

---

### AI

Use AI to:

- Explain Foundation APIs.
- Compare serialization approaches.
- Review persistence decisions.

Avoid:

- Depending on AI instead of reading Apple's documentation.

---

### English

Vocabulary

- Serialization
- Persistence
- Locale
- Time Zone
- Bundle
- Encoding
- Decoding
- Resource

Practice:

Explain when each Foundation API should be used.

---

### Notes

Document:

- Foundation APIs.
- Codable rules.
- Date handling.
- File system notes.
- Common mistakes.

---

### Reflection

Ask yourself:

- Why is Foundation imported almost everywhere?
- Could I build this feature without reinventing existing APIs?
- Which Foundation types am I using most often?

---

## Mini Project

Build a Personal Journal application that includes:

- JSON import/export
- Local file storage
- User preferences
- Date formatting
- Search by date
- Codable models

---

## Exit Criteria

✓ Understand Foundation.

✓ Use Codable confidently.

✓ Work with files.

✓ Handle dates correctly.

✓ Use UserDefaults appropriately.

---

# Module 2 — Data Persistence

## Core Topics

- SwiftData
- Core Data (Concepts)
- ModelContainer
- ModelContext
- @Model
- Relationships
- FetchDescriptor
- Predicates
- Migrations (Introduction)
- Data Modeling

---

## Learning Objectives

After completing this module you should understand:

- How local persistence works.
- When SwiftData should be used.
- How to model relationships.
- How data flows between storage and UI.
- How persistence affects architecture.

---

## Parallel Learning Layers

### Git

Learn:

- Track schema changes.
- Separate migration commits.
- Document model evolution.

Practice:

Commit every model change independently.

---

### Xcode

Learn:

- SwiftData debugging.
- Preview with sample data.
- Inspect persistent stores.

Practice:

Create sample databases for testing.

---

### Apple Documentation

Read:

- SwiftData Overview
- @Model
- ModelContext
- FetchDescriptor
- Relationships

Goal

Understand Apple's modern persistence framework.

---

### WWDC

Recommended Topics

- Meet SwiftData
- Dive deeper into SwiftData
- Model your data

Goal

Learn directly from the engineers who built SwiftData.

---

### Best Practices

Learn:

- Keep models simple.
- Normalize relationships.
- Use lightweight models.
- Separate persistence from UI.

Avoid:

- Massive models.
- Business logic inside models.
- Tight UI coupling.

---

### Design Thinking

Questions to ask:

- What information truly needs persistence?
- What data is temporary?

---

### Architecture Thinking

Understand:

Persistence belongs to the data layer.

Views should never directly own persistence logic.

---

### Open Source

Study:

SwiftData projects.

Observe:

- Folder organization.
- Repository pattern.
- Model structure.

---

### AI

Use AI to:

- Review data models.
- Compare persistence approaches.
- Explain migrations.

Avoid:

- Generating complete database schemas.

---

### English

Vocabulary

- Persistence
- Entity
- Relationship
- Migration
- Predicate
- Context

Practice:

Explain your data model to another developer.

---

### Notes

Document:

- Data models.
- Relationships.
- Common fetch patterns.
- Migration notes.

---

### Reflection

Ask yourself:

- Does this model represent the business domain?
- Can this schema evolve without major rewrites?

---

## Mini Project

Build a Notes application featuring:

- SwiftData
- Relationships
- Search
- Filtering
- Sorting
- Categories
- Favorites

---

## Exit Criteria

✓ Design data models.

✓ Use SwiftData confidently.

✓ Build scalable persistence layers.

---
# Module 3 — Networking & Web

## Core Topics

- URLSession
- URLRequest
- URLResponse
- HTTP
- HTTPS
- REST APIs
- JSON
- Async/Await
- Download Tasks
- Upload Tasks
- Multipart Requests (Introduction)
- WebSockets (Introduction)
- Network Monitoring
- URLCache

---

## Learning Objectives

After completing this module you should understand:

- How applications communicate with servers.
- How HTTP works.
- How URLSession performs requests.
- How to build a reusable networking layer.
- How networking fits into application architecture.

---

## Parallel Learning Layers

### Git

Learn:

- Separate networking commits from UI changes.
- Track API evolution.
- Write meaningful commit messages for networking features.

Practice:

Create one commit for every completed networking feature.

---

### Xcode

Learn:

- Network Debugger
- Console Logging
- Debug Network Requests
- Breakpoints in async code

Practice:

Inspect every API request while developing.

---

### Apple Documentation

Read:

- URLSession
- URLRequest
- URLCache
- URLComponents
- Async/Await

Goal

Understand Apple's networking APIs before using third-party libraries.

---

### WWDC

Recommended Topics

- Use Async/Await
- Meet URLSession
- Modern Networking

Goal

Learn Apple's recommended networking architecture.

---

### Best Practices

Learn:

- Build reusable networking clients.
- Centralize request creation.
- Handle errors consistently.
- Decode responses safely.
- Cache when appropriate.

Avoid:

- Networking inside Views.
- Duplicate API logic.
- Force-unwrapping decoded data.
- Ignoring HTTP status codes.

---

### Design Thinking

Questions to ask:

- Does this request improve the user's experience?
- Should this data be cached?
- Does the user really need this network call?

---

### Architecture Thinking

Understand:

Networking belongs in the infrastructure layer.

Views communicate through:

View → ViewModel → Repository → Network Client

---

### Open Source

Study:

Production networking layers.

Observe:

- API Client
- Request builders
- Error handling
- Dependency Injection

---

### AI

Use AI to:

- Review networking architecture.
- Compare request implementations.
- Explain HTTP behavior.

Avoid:

- Copying networking code without understanding it.

---

### English

Vocabulary

- Request
- Response
- Endpoint
- Header
- Payload
- Authentication
- Timeout
- Cache

Practice:

Explain the complete lifecycle of an API request.

---

### Notes

Document:

- HTTP methods.
- Status codes.
- Error handling.
- Async/Await patterns.
- Networking architecture.

---

### Reflection

Ask yourself:

- Could another project reuse this networking layer?
- Is networking independent of UI?
- How would this scale to dozens of endpoints?

---

## Mini Project

Build a reusable Networking Package supporting:

- GET
- POST
- PUT
- DELETE
- JSON Decoding
- Error Handling
- Authentication Headers
- Request Logging

---

## Exit Criteria

✓ Understand HTTP fundamentals.

✓ Build reusable networking layers.

✓ Decode JSON confidently.

✓ Use Async/Await effectively.

✓ Debug networking issues.

---

# Module 4 — Media Frameworks

## Core Topics

- PhotosPicker
- Photos Framework
- AVFoundation
- AVAudioPlayer
- AVPlayer
- Camera
- Video Playback
- Audio Recording
- Image Processing (Introduction)
- ShareLink

---

## Learning Objectives

After completing this module you should understand:

- How media is captured, displayed, and managed.
- How to integrate the camera and photo library.
- How audio and video playback work.
- How to respect user privacy when accessing media.

---

## Parallel Learning Layers

### Git

Learn:

- Separate media features into isolated branches.
- Track permission-related changes independently.

Practice:

Commit after each media integration.

---

### Xcode

Learn:

- Simulator limitations.
- Physical device testing.
- Privacy permission debugging.

Practice:

Test camera and microphone functionality on a real device.

---

### Apple Documentation

Read:

- PhotosPicker
- Photos Framework
- AVFoundation
- ShareLink

Goal

Understand Apple's media APIs and permission model.

---

### WWDC

Recommended Topics

- Meet PhotosPicker
- AVFoundation sessions
- Modern media APIs

Goal

Learn Apple's recommended media workflows.

---

### Best Practices

Learn:

- Request permissions only when needed.
- Compress media when appropriate.
- Handle unavailable hardware gracefully.
- Respect user privacy.

Avoid:

- Requesting every permission at launch.
- Blocking the main thread.
- Loading full-resolution media unnecessarily.

---

### Design Thinking

Questions to ask:

- Does the user understand why permission is requested?
- Is media capture optional?
- Can the task be completed without the camera?

---

### Architecture Thinking

Understand:

Separate:

- Media Services
- Permissions
- UI
- Business Logic

---

### Open Source

Study:

Camera and media applications.

Observe:

- Permission handling.
- Media caching.
- Service organization.

---

### AI

Use AI to:

- Explain AVFoundation.
- Review media architecture.
- Compare image loading strategies.

Avoid:

- Generating complex AVFoundation code without understanding it.

---

### English

Vocabulary

- Capture
- Playback
- Permission
- Compression
- Recording
- Streaming
- Library

Practice:

Explain your media pipeline.

---

### Notes

Document:

- Permission flow.
- AVFoundation basics.
- Photos APIs.
- Common mistakes.

---

### Reflection

Ask yourself:

- Is media handling independent from UI?
- Are permissions requested responsibly?
- Does this respect user privacy?

---

## Mini Project

Build a Media Journal featuring:

- Camera
- Photo Library
- Video Playback
- Audio Notes
- Share functionality

---

## Exit Criteria

✓ Integrate camera.

✓ Handle permissions correctly.

✓ Play audio and video.

✓ Work with photos confidently.

---

# Module 5 — Location & Maps

## Core Topics

- Core Location
- CLLocationManager
- Authorization
- Location Updates
- Significant Location Changes
- Geocoding
- Reverse Geocoding
- MapKit
- Map
- Annotations
- Overlays
- Directions (Introduction)
- Region Monitoring (Introduction)

---

## Learning Objectives

After completing this module you should understand:

- How location services work.
- How to request location permissions responsibly.
- How to display maps.
- How to convert coordinates into addresses.
- How location integrates with real-world applications.

---

## Parallel Learning Layers

### Git

Learn:

- Separate location features into dedicated branches.
- Keep permission changes isolated.

Practice:

Commit after every completed location feature.

---

### Xcode

Learn:

- Simulated Locations.
- GPX files.
- Debugging Location Services.

Practice:

Test multiple geographic locations using the simulator.

---

### Apple Documentation

Read:

- Core Location
- CLLocationManager
- MapKit
- Geocoder
- Map

Goal

Understand Apple's complete location ecosystem.

---

### WWDC

Recommended Topics

- What's New in MapKit
- Core Location sessions
- Designing Location Experiences

Goal

Learn Apple's recommendations for location-based apps.

---

### Best Practices

Learn:

- Request permissions only when necessary.
- Use the minimum location accuracy required.
- Stop updates when not needed.
- Respect battery life.
- Explain why location is required.

Avoid:

- Continuous tracking unnecessarily.
- Background location without justification.
- Requesting Always permission first.

---

### Design Thinking

Questions to ask:

- Does this feature really require location?
- Can the user manually enter a location?
- Is permission timing appropriate?

---

### Architecture Thinking

Separate:

- Location Service
- Permission Manager
- Map Presentation
- Business Logic

Avoid tightly coupling maps to application logic.

---

### Open Source

Study:

Location-based applications.

Observe:

- Permission flow.
- Service organization.
- Map interactions.
- Error handling.

---

### AI

Use AI to:

- Explain authorization states.
- Compare MapKit APIs.
- Review location architecture.

Avoid:

- Copying complex map implementations without understanding them.

---

### English

Vocabulary

- Coordinate
- Latitude
- Longitude
- Region
- Annotation
- Geocoding
- Authorization

Practice:

Explain how a location is obtained and displayed.

---

### Notes

Document:

- Authorization states.
- MapKit APIs.
- Location accuracy.
- Common permission issues.

---

### Reflection

Ask yourself:

- Is location essential?
- Am I respecting user privacy?
- Is battery usage reasonable?

---

## Mini Project

Build a Nearby Places application featuring:

- Current Location
- Search
- Pins
- Place Details
- Reverse Geocoding
- Favorite Locations

---

## Exit Criteria

✓ Work with Core Location.

✓ Display interactive maps.

✓ Handle permissions correctly.

✓ Convert coordinates into addresses.

---

# Module 6 — Device Hardware

## Core Topics

- Haptic Feedback
- Core Motion
- Device Orientation
- Clipboard
- Drag & Drop
- Share Sheet
- Contacts (Introduction)
- Calendar (Introduction)
- PencilKit (Overview)
- Vision Framework (Overview)

---

## Learning Objectives

After completing this module you should understand:

- How applications interact with hardware.
- Which device capabilities improve user experience.
- How hardware APIs should be abstracted.
- When hardware integration is appropriate.

---

## Parallel Learning Layers

### Git

Learn:

- Separate hardware integrations.
- Track permission changes.

Practice:

Commit after every hardware feature.

---

### Xcode

Learn:

- Device testing.
- Simulator limitations.
- Debug hardware capabilities.

Practice:

Test on physical hardware whenever required.

---

### Apple Documentation

Read:

- Core Haptics
- Core Motion
- UIPasteboard
- Drag and Drop
- Contacts
- EventKit

Goal

Understand Apple's hardware-related APIs.

---

### WWDC

Recommended Topics

- Core Haptics
- Device interactions
- Modern hardware APIs

Goal

Learn how hardware enhances applications.

---

### Best Practices

Learn:

- Use haptics sparingly.
- Respect privacy.
- Request permissions only when necessary.
- Gracefully handle unsupported hardware.

Avoid:

- Excessive haptic feedback.
- Assuming hardware availability.

---

### Design Thinking

Questions to ask:

- Does this hardware improve the experience?
- Is there a simpler solution?
- Is hardware essential?

---

### Architecture Thinking

Separate:

- Hardware Services
- Permissions
- Business Logic
- UI

Hardware APIs should never dominate application architecture.

---

### Open Source

Study:

Applications using hardware capabilities.

Observe:

- Service abstraction.
- Permission handling.
- Error recovery.

---

### AI

Use AI to:

- Compare hardware APIs.
- Explain Core Motion.
- Review service architecture.

Avoid:

- Treating AI as hardware documentation.

---

### English

Vocabulary

- Haptic
- Motion
- Sensor
- Clipboard
- Permission
- Orientation

Practice:

Explain why a hardware feature improves UX.

---

### Notes

Document:

- Hardware APIs.
- Permission requirements.
- Device limitations.

---

### Reflection

Ask yourself:

- Is this hardware feature valuable?
- Can the application function without it?

---

## Mini Project

Build a Smart Notes application featuring:

- Clipboard support
- Drag & Drop
- Haptics
- Device orientation
- Share Sheet

---

## Exit Criteria

✓ Integrate hardware responsibly.

✓ Understand device capabilities.

✓ Handle permissions professionally.

---

# Module 7 — Background Processing

## Core Topics

- BackgroundTasks
- App Lifecycle
- Scene Lifecycle
- Background Refresh
- Background URLSession
- Task Scheduling
- Background Fetch (Concepts)
- Energy Efficiency

---

## Learning Objectives

After completing this module you should understand:

- How applications continue limited work in the background.
- Apple's restrictions on background execution.
- How to schedule background tasks correctly.
- Why battery efficiency matters.

---

## Parallel Learning Layers

### Git

Learn:

- Track lifecycle changes separately.
- Keep background-task commits isolated.

Practice:

Document lifecycle changes clearly.

---

### Xcode

Learn:

- Simulate Background Fetch.
- Debug Lifecycle Events.
- Energy diagnostics.

Practice:

Verify background behavior on real devices.

---

### Apple Documentation

Read:

- BackgroundTasks
- App Lifecycle
- Scene Lifecycle
- Background URLSession

Goal

Understand Apple's lifecycle model.

---

### WWDC

Recommended Topics

- Background execution
- Efficient apps
- App lifecycle

Goal

Learn Apple's battery-efficient development practices.

---

### Best Practices

Learn:

- Perform minimal background work.
- Schedule responsibly.
- Respect system resources.
- Handle interruptions gracefully.

Avoid:

- Long-running background work.
- Fighting the operating system.
- Battery-intensive operations.

---

### Design Thinking

Questions to ask:

- Does this task truly need background execution?
- Would users expect this behavior?

---

### Architecture Thinking

Separate:

- Lifecycle Management
- Background Services
- UI
- Networking

---

### Open Source

Study:

Applications with offline synchronization.

Observe:

- Background scheduling.
- Data synchronization.
- Retry mechanisms.

---

### AI

Use AI to:

- Explain lifecycle events.
- Review scheduling decisions.
- Compare synchronization strategies.

Avoid:

- Using AI instead of Apple's lifecycle documentation.

---

### English

Vocabulary

- Lifecycle
- Background Task
- Refresh
- Synchronization
- Scheduling
- Energy

Practice:

Describe the complete application lifecycle.

---

### Notes

Document:

- Lifecycle states.
- Background limitations.
- Scheduling APIs.
- Battery considerations.

---

### Reflection

Ask yourself:

- Is background execution justified?
- Does this respect battery life?
- What happens if the task is interrupted?

---

## Mini Project

Build an Offline News Reader supporting:

- Background Refresh
- Offline Cache
- Automatic Synchronization
- Lifecycle Handling

---

## Exit Criteria

✓ Understand the application lifecycle.

✓ Schedule background tasks.

✓ Design battery-efficient applications.

---

# Module 8 — Notifications & Communication

## Core Topics

- UserNotifications
- Local Notifications
- Push Notifications (Concepts)
- Notification Categories
- Notification Actions
- Notification Permissions
- Deep Linking from Notifications
- Background Notification Handling

---

## Learning Objectives

After completing this module you should understand:

- How notifications work on Apple platforms.
- The difference between Local and Push Notifications.
- How notification permissions affect user experience.
- How notifications integrate with application workflows.
- How to build respectful notification systems.

---

## Parallel Learning Layers

### Git

Learn:

- Separate notification features into dedicated branches.
- Keep permission changes isolated.

Practice:

Commit after implementing each notification feature.

---

### Xcode

Learn:

- Notification testing.
- Push notification simulation.
- Background notification debugging.

Practice:

Test notification flows on a physical device.

---

### Apple Documentation

Read:

- UserNotifications
- NotificationCenter
- Notification Categories
- Notification Actions

Goal

Understand Apple's notification framework completely.

---

### WWDC

Recommended Topics

- UserNotifications
- Push Notifications
- Notification best practices

Goal

Learn how Apple recommends communicating with users.

---

### Best Practices

Learn:

- Request permission at the right moment.
- Send meaningful notifications.
- Group related notifications.
- Respect user preferences.
- Allow users to control notification settings.

Avoid:

- Spamming users.
- Requesting permission at launch without context.
- Sending unnecessary reminders.

---

### Design Thinking

Questions to ask:

- Does this notification provide value?
- Is this interruption justified?
- Would users appreciate this notification?

---

### Architecture Thinking

Separate:

- Notification Service
- Scheduling Logic
- Business Rules
- User Interface

Notifications should trigger actions—not contain business logic.

---

### Open Source

Study:

Applications with well-designed notification systems.

Observe:

- Scheduling.
- Categories.
- Deep linking.
- User settings.

---

### AI

Use AI to:

- Review notification strategy.
- Suggest scheduling improvements.
- Compare notification workflows.

Avoid:

- Using AI to replace user research.

---

### English

Vocabulary

- Notification
- Category
- Permission
- Reminder
- Scheduling
- Badge
- Action

Practice:

Explain when a notification should be delivered.

---

### Notes

Document:

- Notification APIs.
- Permission flow.
- Scheduling patterns.
- User experience guidelines.

---

### Reflection

Ask yourself:

- Would I enjoy receiving these notifications?
- Is each notification solving a real problem?
- Am I respecting the user's attention?

---

## Mini Project

Build a Task Reminder application featuring:

- Local Notifications
- Notification Categories
- Reminder Scheduling
- Custom Actions
- Deep Linking into Tasks

---

## Exit Criteria

✓ Schedule Local Notifications.

✓ Understand Push Notification concepts.

✓ Build respectful notification experiences.

✓ Handle notification permissions correctly.

---

# Module 9 — Authentication & Security

## Core Topics

- Authentication
- Authorization
- Sign in with Apple
- Keychain
- LocalAuthentication
- Face ID
- Touch ID
- App Attest (Introduction)
- DeviceCheck (Overview)

---

## Learning Objectives

After completing this module you should understand:

- How authentication differs from authorization.
- How credentials should be stored securely.
- How biometric authentication works.
- How Apple protects user identity.
- How authentication fits into application architecture.

---

## Parallel Learning Layers

### Git

Learn:

- Keep security-related commits isolated.
- Never commit secrets.
- Use environment configurations.

Practice:

Review repositories for accidental secret exposure.

---

### Xcode

Learn:

- Keychain debugging.
- Face ID simulation.
- Environment configuration.

Practice:

Test authentication on supported devices.

---

### Apple Documentation

Read:

- AuthenticationServices
- LocalAuthentication
- Security Framework
- Keychain Services

Goal

Understand Apple's authentication ecosystem.

---

### WWDC

Recommended Topics

- Sign in with Apple
- Authentication Services
- Security sessions

Goal

Learn Apple's identity best practices.

---

### Best Practices

Learn:

- Use Sign in with Apple when appropriate.
- Store secrets in Keychain.
- Use biometrics as convenience—not as the only security layer.
- Respect user privacy.

Avoid:

- Storing passwords in UserDefaults.
- Creating custom password storage.
- Hardcoding API keys.

---

### Design Thinking

Questions to ask:

- Is authentication actually required?
- What is the simplest secure experience?
- Can friction be reduced safely?

---

### Architecture Thinking

Separate:

- Authentication Service
- Credential Storage
- Session Management
- User Interface

Authentication should remain independent from presentation.

---

### Open Source

Study:

Authentication implementations.

Observe:

- Session handling.
- Token management.
- Dependency Injection.

---

### AI

Use AI to:

- Review authentication architecture.
- Compare authentication approaches.
- Explain Keychain usage.

Avoid:

- Sharing secrets with AI.

---

### English

Vocabulary

- Authentication
- Authorization
- Credential
- Token
- Session
- Biometrics
- Identity

Practice:

Explain the complete authentication flow.

---

### Notes

Document:

- Authentication flow.
- Keychain usage.
- Session lifecycle.
- Security recommendations.

---

### Reflection

Ask yourself:

- Is user data protected?
- Are credentials stored securely?
- Could this authentication scale?

---

## Mini Project

Build a Secure Notes application supporting:

- Sign in with Apple
- Face ID / Touch ID
- Keychain storage
- Session management
- Automatic logout

---

## Exit Criteria

✓ Implement secure authentication.

✓ Use Keychain correctly.

✓ Understand biometric authentication.

✓ Protect sensitive information.

---

# Module 10 — App Services & Integrations

## Core Topics

- App Groups
- Widgets (Overview)
- App Intents (Overview)
- Share Extensions
- Universal Links
- Deep Links
- Siri Shortcuts (Introduction)
- CloudKit (Overview)
- StoreKit (Overview)

---

## Learning Objectives

After completing this module you should understand:

- How applications integrate with the Apple ecosystem.
- How apps communicate with extensions.
- How users interact with apps outside the main application.
- How Apple services expand application capabilities.

---

## Parallel Learning Layers

### Git

Learn:

- Organize integrations by feature.
- Track extension development independently.

Practice:

Commit each integration separately.

---

### Xcode

Learn:

- Targets
- App Extensions
- Capabilities
- Entitlements

Practice:

Create and configure extension targets.

---

### Apple Documentation

Read:

- App Extensions
- App Groups
- Universal Links
- Widgets
- CloudKit
- StoreKit

Goal

Understand Apple's ecosystem integration points.

---

### WWDC

Recommended Topics

- App Intents
- WidgetKit
- CloudKit
- StoreKit
- App Extensions

Goal

Understand how modern Apple apps extend beyond a single executable.

---

### Best Practices

Learn:

- Integrate only when valuable.
- Keep extensions lightweight.
- Share data safely.
- Respect user privacy.

Avoid:

- Building unnecessary extensions.
- Duplicating business logic.

---

### Design Thinking

Questions to ask:

- Does this integration improve the user's workflow?
- Is an extension better than another screen?
- Would users actually discover this feature?

---

### Architecture Thinking

Separate:

- Shared Business Logic
- Extension Logic
- Main Application
- Shared Storage

Design for reuse across targets.

---

### Open Source

Study:

Applications using Widgets, Extensions, or Universal Links.

Observe:

- Target organization.
- Shared code.
- App Group usage.

---

### AI

Use AI to:

- Compare integration options.
- Review extension architecture.
- Explain capability requirements.

Avoid:

- Blindly enabling capabilities you don't understand.

---

### English

Vocabulary

- Extension
- Widget
- Capability
- Entitlement
- Integration
- Universal Link
- Target

Practice:

Explain how different Apple services communicate.

---

### Notes

Document:

- Extension lifecycle.
- Shared storage.
- Capabilities.
- Integration checklist.

---

### Reflection

Ask yourself:

- Which integrations add real value?
- Is shared code organized properly?
- Can future platforms reuse this architecture?

---

## Mini Project

Extend one of your previous applications with:

- Widget
- Universal Links
- Share Extension
- App Groups
- Basic App Intent

---

## Exit Criteria

✓ Understand Apple's ecosystem integrations.

✓ Build extensions confidently.

✓ Configure capabilities correctly.

✓ Share code between targets.

---

# Module 11 — Framework Selection & Engineering Decisions

## Core Topics

- Choosing the Right Framework
- Trade-offs
- Framework Dependencies
- Native vs Third-party
- Maintenance
- Scalability
- Future-proofing

---

## Learning Objectives

After completing this module you should understand:

- How to evaluate Apple frameworks.
- How to avoid unnecessary dependencies.
- How to make long-term engineering decisions.
- How to continue learning new frameworks independently.

---

## Parallel Learning Layers

### Git

Document Architecture Decision Records (ADRs) explaining why a framework was chosen.

### Xcode

Understand project capabilities and framework linking.

### Apple Documentation

Practice reading documentation before searching for tutorials.

### WWDC

Watch "What's New" sessions every year to stay current.

### Best Practices

- Prefer Apple's native frameworks when they meet requirements.
- Add third-party libraries only when they provide clear value.
- Keep dependencies minimal.

### Design Thinking

Choose frameworks that solve user problems—not because they're popular.

### Architecture Thinking

Evaluate every framework based on maintainability, scalability, and long-term cost.

### Open Source

Study why mature projects adopt (or avoid) specific frameworks.

### AI

Use AI to compare frameworks and discuss trade-offs—not to make decisions for you.

### English

Practice explaining **why** one framework was chosen over another.

### Notes

Maintain a personal "Framework Decision Journal."

### Reflection

Ask yourself:

- Why did I choose this framework?
- What alternatives exist?
- What are the trade-offs?

---

## Mini Project

Review three existing applications you've built and justify every Apple framework used.

---

## Exit Criteria

✓ Select frameworks confidently.

✓ Explain engineering trade-offs.

✓ Continue learning future Apple frameworks independently.

---

# Phase Project

Build a production-style application that combines multiple Apple frameworks.

Suggested features:

- SwiftData persistence
- URLSession networking
- Camera & Photos
- Maps & Location
- Local Notifications
- Background Refresh
- Sign in with Apple
- Face ID / Touch ID
- Widget or Share Extension

Document:

- Why each framework was selected.
- Alternatives considered.
- Architecture decisions.
- Privacy considerations.
- Performance considerations.

---

# Exit Criteria

You can confidently:

✓ Choose the appropriate Apple framework.

✓ Combine multiple frameworks in one application.

✓ Read Apple framework documentation independently.

✓ Integrate frameworks into a clean architecture.

✓ Explain the responsibilities and trade-offs of every framework you use.

---

# Phase Reflection

Before moving to Phase 04, answer these questions:

1. Can I choose the correct Apple framework without guessing?
2. Can I integrate multiple frameworks into one application?
3. Do I understand Apple's documentation well enough to learn new frameworks on my own?
4. Can I justify why I selected a framework?
5. Am I depending on third-party libraries unnecessarily?

If the answer to any question is **No**, revisit the relevant module before continuing.

---

# Next Phase

➡️ **Phase 04 — Professional App Architecture**
