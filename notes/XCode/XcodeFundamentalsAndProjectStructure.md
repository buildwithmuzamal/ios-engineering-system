# Xcode Fundamentals

## Topics

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

---

# 1. Workspace

## What is a Workspace?

A **Workspace** is a container that allows Xcode to manage multiple projects and packages together.

```
Workspace
│
├── MyApp.xcodeproj
├── UI.xcodeproj
└── Networking Package
```

A workspace does not mean that all projects must depend on each other. It simply provides a single environment where related projects and packages can be managed together.

> **Note:** Workspace membership ≠ Dependency
>
> Having two projects in the same workspace does NOT automatically mean that one depends on the other.

## 2. Project

### What is a Project?

An Xcode Project contains the configuration and structure needed to build one or more targets.

It manages things such as:

- Files
- Targets
- Build settings
- Build phases
- Build rules
- Dependencies
- Project configuration

### Example

```
MyApp.xcodeproj
│
├── MyApp Target
├── MyAppTests Target
└── MyAppUITests Target
```

**Mental model:**
```
Project
   ↓
Contains
   ↓
Targets + Files + Configuration
```

## 3. Target

### What is a Target?

A Target tells Xcode what to build and how to build it.

A project can contain multiple targets.

### Example

```
MyApp.xcodeproj
│
├── MyApp Target
├── MyAppTests Target
└── MyAppUITests Target
```

Each target can produce a different build product.

```
MyApp Target
    ↓
MyApp.app

MyAppTests Target
    ↓
MyAppTests.xctest

MyAppUITests Target
    ↓
MyAppUITests.xctest
```

**Important mental model:**
```
Target
   ↓
Instructions for producing a build product
```

A target can also represent different platforms/products.

For example:

```
MyApp Project
│
├── iOS Target
└── macOS Target
```

Common logic can be shared between targets, while platform-specific files can belong to only one target.

## 4. Target Membership

### What is Target Membership?

Target Membership determines which targets a particular file participates in.

### Example

**User.swift**

Target Membership:
- ☑ MyApp
- ☑ macOS
- ☐ MyAppTests

This means the file is included in the MyApp and macOS targets, but not the test target.

### Example Table

| File | iOS | macOS |
|------|-----|-------|
| NetworkManager | ✓ | ✓ |
| User | ✓ | ✓ |
| Database | ✓ | ✓ |
| HomeView | ✓ | ✗ |
| MacHomeView | ✗ | ✓ |

> **Note:** Seeing a file in the Project Navigator does not necessarily mean that the file is included in a target. Target Membership determines which targets compile/include the file.

## 5. Workspace vs Project vs Target

The basic hierarchy is:

```
Workspace
    │
    └── Projects
          │
          └── Targets
                │
                └── Build Products
```

### Example

```
MyAppWorkspace
│
├── MyApp.xcodeproj
│   │
│   ├── MyApp Target
│   │      ↓
│   │    MyApp.app
│   │
│   ├── MyAppTests Target
│   │      ↓
│   │    MyAppTests.xctest
│   │
│   └── MyAppUITests Target
│          ↓
│        MyAppUITests.xctest
│
└── UI.xcodeproj
    │
    └── UI Target
           ↓
       UI.framework
```

## 6. Scheme

### What is a Scheme?

A Scheme tells Xcode which target/action/configuration to use.

### Common Scheme actions

- Run
- Test
- Profile
- Analyze
- Archive

A scheme is not the same thing as a target.

| | |
|--------|--------|
| **Target** | What can Xcode build? |
| **Scheme** | What should Xcode do with it? |

### Scheme Actions

#### Run

Run is used during normal development.

**Shortcut:** ⌘R

**Conceptually:**
```
Source Code
    ↓
Build
    ↓
MyApp.app
    ↓
Simulator/Device
    ↓
Debugger
```

Use Run when you want to launch and manually test the app.

**Mental model:** Run = "Let's use the app."

#### Test

Test executes automated tests.

**Shortcut:** ⌘U

**Example:**
```
MyApp Scheme
      ↓
     Test
      ↓
MyAppTests Target
      ↓
Execute Tests
      ↓
Pass / Fail
```

**Mental model:** Test = "Let's verify the app automatically."

#### Profile

Profile is used to investigate runtime performance using Instruments.

**Example:**
```
MyApp Scheme
      ↓
   Profile
      ↓
Build
      ↓
Launch App
      ↓
Instruments
      ↓
Runtime Analysis
```

**Examples of things you might investigate:**

- CPU usage
- Memory usage
- Leaks
- Allocations
- Energy
- Performance

**Mental model:** Profile = "Let's measure the running app."

#### Analyze

Analyze performs static analysis of the source code.

Static means Xcode analyzes the code without actually running the application.

It can detect things such as:

- Potential memory problems
- Suspicious code
- Resource problems
- Certain unreachable/suspicious paths
- Other potential issues

> **Note:** Xcode Analyze is not a complete dead-code detector. For specialized unused/dead Swift code detection, tools such as Periphery can be used.

**Profile vs Analyze:**

```
Profile
   ↓
Runtime
   ↓
Running application

Analyze
   ↓
Source code
   ↓
Static analysis
```

**Mental model:** Analyze = "Let's inspect the code."

#### Archive

Archive is used to prepare a build for distribution.

**Conceptually:**
```
MyApp
   ↓
Archive
   ↓
Release Build
   ↓
MyApp.xcarchive
   ↓
Organizer
   ↓
TestFlight / App Store / Distribution
```

You don't normally archive every time you develop a feature. You archive when you want a distributable build.

**Mental model:** Archive = "Let's prepare a distributable build."

### Scheme Summary

| Action | Purpose |
|--------|---------|
| Run | Use the app |
| Test | Execute automated tests |
| Profile | Analyze runtime performance |
| Analyze | Analyze source code |
| Archive | Prepare a distributable build |

## 7. Project Navigator

### What is Project Navigator?

The Project Navigator is the left-side Xcode panel used to navigate project files and resources.

**Shortcut:** ⌘1

### Example

```
MyApp
│
├── App
│   └── MyAppApp.swift
│
├── Views
│   └── ContentView.swift
│
├── Models
│   └── User.swift
│
└── Assets.xcassets
```

> **Note:** The Project Navigator is not necessarily the same as your physical folder structure on disk.
>
> Xcode can use groups to organize files. For example:
> ```
> Views
> ├── HomeView.swift
> └── SettingsView.swift
> ```
>
> The Views group may not necessarily correspond to a physical Views folder on disk. Therefore, moving something in Project Navigator does not always mean moving the actual file on your Mac.

## 8. Build Phases

### What are Build Phases?

Build Phases define the major steps/resources involved in building a target.

**Go to:** Target → Build Phases

### Common sections include

- Dependencies
- Compile Sources
- Link Binary With Libraries
- Copy Bundle Resources
- Embed Frameworks / Libraries

### Compile Sources

Compile Sources tells Xcode which source files should be compiled for this target.

**Example:**
```
Compile Sources
├── MyAppApp.swift
├── ContentView.swift
├── User.swift
└── NetworkManager.swift
```

**Connection to Target Membership:**
```
Target Membership
       ↓
Which target gets the file?
       ↓
Build Phases
       ↓
Compile Sources
       ↓
Compile the file
```

### Link Binary With Libraries

This tells Xcode which libraries/frameworks should be linked into the target.

**Example:**
```
Link Binary With Libraries
├── SwiftUI.framework
├── Foundation.framework
└── Networking.framework
```

> **Note:** Linking and target dependency are related but different concepts.
> ```
> Target Dependency → Build order
> Linking → Which binary/library is linked
> ```

### Copy Bundle Resources

Resources that need to be included in the app bundle can appear here.

**Examples:**

- Assets.xcassets
- Localizable.strings
- JSON files
- Fonts
- Images

**Mental model:**
```
Compile Sources → Code
Copy Bundle Resources → Resources
```

### Embed Frameworks / Libraries

Some frameworks need to be embedded in the application bundle so they are available at runtime.

You may see:

- Embed & Sign
- Do Not Embed

Don't go deeply into static vs dynamic linking yet.

### Build Phases Summary

Remember these questions:

- **Compile Sources** → What code do I compile?
- **Link Binary With Libraries** → What libraries/frameworks do I link?
- **Copy Bundle Resources** → What resources go into my app?
- **Dependencies** → What targets must be built first?

## 9. Build Rules

### What are Build Rules?

Build Rules tell Xcode how particular types of source files should be processed during a build.

**For example:**
```
.swift
   ↓
Swift compiler
   ↓
Compile
```

**Another source type:**
```
.m
   ↓
Objective-C compiler
   ↓
Compile
```

### Build Phases vs Build Rules

- **Build Phases** → What steps should happen during the build?
- **Build Rules** → How should a particular type of file be processed?

Build Rules are rarely customized in a normal Swift/SwiftUI project.

They are more commonly encountered in:

- Legacy projects
- Mixed-language projects
- Generated source code
- Custom build pipelines
- Specialized tooling

> **Note:** Understand Build Rules, but don't spend much time customizing them at this stage.

## 10. Target Dependencies

### What is a Target Dependency?

A Target Dependency tells Xcode that one target needs another target to be built first.

**Example:**
```
MyApp Target
      ↓
depends on
      ↓
Networking Target
```

Xcode can then build:
```
1. Networking
        ↓
2. MyApp
```

### Workspace ≠ Dependency

Having projects inside the same workspace does not automatically mean they depend on each other.

```
Workspace
│
├── MyApp
└── Networking
```

Means: Both projects are managed by the workspace.

It does not necessarily mean:
```
MyApp
  ↓
Networking
```

### Target Dependency vs Linking

These are related but different.

**Target Dependency:**
```
MyApp Target
      ↓
Networking Target
```
Means: Build Networking before MyApp when required.

**Linking:**
```
MyApp Target
      ↓
Networking.framework
```
Means: Link the Networking binary into MyApp.

Therefore:
```
Build order ≠ Linking
```

### Target Dependencies Are Directional

If:
```
A → B
```

It means: A depends on B.

It does not mean B depends on A.

**Example:**
```
App
 ↓
Networking
 ↓
Core
```

This is a normal dependency direction.

Avoid unnecessary circular dependencies such as:
```
App
 ↔
Core
```

### Important Xcode Dependency Models

**Swift Package:**
```
MyApp
  ↓
Swift Package Dependency
  ↓
Networking Package
```
Swift Package Manager manages the dependency.

**Xcode Framework Project:**
```
MyApp Target
      ↓
UI Target
```
The UI target produces UI.framework, which MyApp can link against.

### Workspace and Cross-Project Dependencies

A workspace can contain:
- MyApp.xcodeproj
- UI.xcodeproj

The projects themselves aren't simply "dependent projects." Instead, the dependency relationship is between their targets/products.

**Conceptually:**
```
Workspace
│
├── MyApp Project
│   └── MyApp Target
│
└── UI Project
    └── UI Target
```

Then:
```
MyApp Target
      ↓
uses
      ↓
UI.framework
      ↓
produced by
      ↓
UI Target
```

Xcode can infer the build dependency when the framework/product relationship is correctly established.

## 11. Project Settings vs Target Settings

A project can contain multiple targets.

**Example:**
```
MyApp Project
│
├── MyApp Target
├── MyAppTests Target
└── MyAppUITests Target
```

There are therefore two levels of configuration:

```
Project Settings
       ↓
Common/default configuration
       ↓
Target Settings
       ↓
Target-specific configuration
```

### Project Settings

Project settings provide common/default configuration for the targets in that project.

**Example:**
```
MyApp Project
    ↓
Common settings
    ↓
Targets
```

### Target Settings

Target settings configure a specific product.

**Example:**
```
MyApp Target
├── General
├── Signing & Capabilities
├── Build Settings
├── Build Phases
└── Build Rules
```

The target settings answer: How should this particular product be built?

### Project vs Target Override

Suppose:
```
Project:
iOS Deployment Target = iOS 17
```

Targets can inherit this:
```
MyApp       → iOS 17
MyAppTests  → iOS 17
```

But if:
```
MyApp Target:
iOS Deployment Target = iOS 18
```

Then:
```
MyApp       → iOS 18
MyAppTests  → iOS 17
```

Because the MyApp target overrides the project value.

**Mental model:**
```
Project
   ↓
Defaults
   ↓
Target
   ↓
Target-specific override
   ↓
Final setting
```

### Build Setting Inheritance

You may see: `$(inherited)`

It allows settings from a higher level to flow into the current configuration.

**Conceptually:**
```
Project
   ↓
inherited
   ↓
Target
   ↓
Final Build Setting
```

Build-setting inheritance will be studied more deeply later.

## 12. .xcodeproj

### What is .xcodeproj?

`.xcodeproj` is the Xcode project package that stores the configuration and structure of a project.

**Example:** `MyApp.xcodeproj`

It contains information about things such as:

- Targets
- Build settings
- Build phases
- Build rules
- File references
- Target dependencies
- Project configuration

> **Note:** The `.xcodeproj` does not simply contain your Swift source code. Your source files are separate:
> ```
> MyApp/
> ├── ContentView.swift
> ├── User.swift
> └── Assets.xcassets
> ```
> 
> While `MyApp.xcodeproj` stores information about how Xcode organizes and builds those files.

### .xcodeproj Internal Structure

An `.xcodeproj` is actually a package.

You can use: Right click → Show Package Contents

You may see:

- project.pbxproj
- project.xcworkspace
- xcshareddata
- xcuserdata

The important file is: `project.pbxproj`

It contains project configuration information such as:

- File references
- Targets
- Build phases
- Build settings
- Dependencies

> **Warning:** Don't manually edit `project.pbxproj` at this stage. Use Xcode's UI.

### .xcodeproj and Git

The `.xcodeproj` is normally committed to Git because it is part of the project's configuration.

**Example:**
```
MyProject/
├── MyApp/
├── MyApp.xcodeproj/
└── README.md
```

However, user-specific generated data such as `xcuserdata` is commonly excluded from Git.

## 13. .xcworkspace

### What is .xcworkspace?

`.xcworkspace` is a workspace file that allows Xcode to manage multiple projects and packages together.

**Example:**
```
MyAppWorkspace.xcworkspace
│
├── MyApp.xcodeproj
├── UI.xcodeproj
└── Networking Package
```

### Why use a Workspace?

Without a workspace:

- `MyApp.xcodeproj` is one project.
- `UI.xcodeproj` is another project.

A workspace allows them to be managed together:

```
Workspace
│
├── MyApp Project
├── UI Project
└── Other Project
```

### .xcodeproj vs .xcworkspace

| Aspect | .xcodeproj | .xcworkspace |
|--------|-----------|-----------------|
| Purpose | Represents a project | Represents a workspace |
| Content | Contains project configuration | Organizes multiple projects/packages |
| Structure | Contains targets | Can contain multiple .xcodeprojs |
| Level | Project-level structure | Workspace-level structure |
| Usage | Can be opened independently | Used to manage related projects together |

**Mental model:**
```
.xcworkspace
      ↓
   Workspace
      ↓
┌─────┴─────┐
↓           ↓
.xcodeproj  .xcodeproj
↓           ↓
Project     Project
```

## Complete Xcode Project Structure

The overall mental model:

```
.xcworkspace
      │
      ├── .xcodeproj
      │      │
      │      ├── Project Settings
      │      │
      │      ├── Target
      │      │    │
      │      │    ├── Build Settings
      │      │    ├── Build Phases
      │      │    ├── Build Rules
      │      │    └── Target Dependencies
      │      │
      │      └── Target
      │
      └── .xcodeproj
             │
             └── Target
```

## Complete Mental Model

Remember these definitions:

- **Workspace** → Manages multiple projects/packages together.
- **Project** → Contains files, targets, and project configuration.
- **Target** → Defines what Xcode builds and how that product is built.
- **Target Membership** → Determines which targets include a file.
- **Scheme** → Tells Xcode which target/action/configuration to use.
- **Project Navigator** → Provides a view for navigating project files/resources.
- **Build Phases** → Defines major steps/resources involved in building a target.
- **Build Rules** → Defines how particular file types are processed.
- **Target Dependencies** → Defines which targets need to be built before another target.
- **Project Settings** → Common/default configuration for targets.
- **Target Settings** → Configuration specific to a particular target.
- **.xcodeproj** → Project configuration package.
- **.xcworkspace** → Workspace configuration that manages multiple projects/packages.

## Important Relationships

**Workspace → Project**
```
Workspace
   ↓
contains
   ↓
Projects
```

**Project → Target**
```
Project
   ↓
contains
   ↓
Targets
```

**Target → Product**
```
Target
   ↓
builds
   ↓
Product
```

**File → Target**
```
File
   ↓
Target Membership
   ↓
Target
```

**Scheme → Target**
```
Scheme
   ↓
selects/configures
   ↓
Target + Action + Build Configuration
```

**Target → Dependency**
```
App Target
   ↓
depends on
   ↓
Framework Target
```

## Practical Example

Suppose we have:

```
MyAppWorkspace
│
├── MyApp.xcodeproj
│   └── MyApp Target
│
├── UI.xcodeproj
│   └── UI Target
│
└── Networking Package
```

The relationships could be:

```
MyApp Target
│
├── uses → UI.framework
│             ↑
│             │
│         UI Target
│
└── uses → Networking Package
```

And the workspace manages all of them:

```
MyAppWorkspace
       │
       ├── MyApp Project
       ├── UI Project
       └── Networking Package
```

## Practice Exercises

### Exercise 1 — Workspace

Create or use a workspace containing:

- MyApp.xcodeproj
- UI.xcodeproj

**Understand:** Both projects can be managed from one workspace.

### Exercise 2 — Target Membership

Create: `Shared.swift`

Set:
- ☑ MyApp
- ☐ MyAppTests

Then create: `TestHelper.swift`

Set:
- ☐ MyApp
- ☑ MyAppTests

**Understand:** Each file participates in different targets.

### Exercise 3 — Build Phases

Open: MyApp Target → Build Phases

Inspect:
- Compile Sources
- Link Binary With Libraries
- Copy Bundle Resources
- Target Dependencies

**Ask:**
- What code is compiled?
- What libraries are linked?
- What resources are copied?
- What targets are dependencies?

### Exercise 4 — Project vs Target Settings

Compare:
- Project → Build Settings
- MyApp Target → Build Settings

Find: iOS Deployment Target

**Understand:** Which value is inherited and which value is overridden.

### Exercise 5 — Framework Project Dependency

Create: `UI.xcodeproj` with `UI Target`

Add it to your workspace.

Then link the UI framework to MyApp:
- MyApp Target → General → Frameworks, Libraries & Embedded Content → UI.framework

**Understand:**
```
MyApp Target
      ↓
uses
      ↓
UI.framework
      ↓
produced by
      ↓
UI Target
```

## Xcode Fundamentals — Final Mental Model

```
                    WORKSPACE
                       │
             ┌─────────┴─────────┐
             ↓                   ↓
          PROJECT             PROJECT
             │                   │
        ┌────┴────┐              │
        ↓         ↓              ↓
      TARGET    TARGET         TARGET
        │
        ├── Target Membership
        ├── Build Settings
        ├── Build Phases
        ├── Build Rules
        └── Dependencies
        │
        ↓
    BUILD PRODUCT


                    SCHEME
                       │
                       ↓
          Target + Action + Configuration
                       │
          ┌────────────┼────────────┐
          ↓            ↓            ↓
         Run          Test       Profile
          ↓            ↓            ↓
       App/Debug     Tests      Instruments

          Analyze → Static Code Analysis

          Archive → Distribution Build
```

## What You Should Know Before Moving On

You don't need to memorize every Xcode screen.

You should be able to explain these without looking them up:

- What is a Workspace?
- What is a Project?
- What is a Target?
- What is Target Membership?
- What is a Scheme?
- What does Run do?
- What does Test do?
- What does Profile do?
- What does Analyze do?
- What does Archive do?
- What is the Project Navigator?
- What are Build Phases?
- What are Build Rules?
- What is a Target Dependency?
- Project Settings vs Target Settings?
- What is .xcodeproj?
- What is .xcworkspace?
- What's the difference between a Swift Package dependency and an Xcode target dependency?