# Git Branch Management

## 1. What Is a Branch Strategy?

A branch strategy is a set of rules for how a team uses Git branches.
It answers questions like:

- Where does new work start?
- Where should developers merge their work?
- How long should branches live?
- How are releases prepared?
- How are production bugs fixed?

Think of it this way:

```text
Git = gives us branches
Branch Strategy = tells the team how to use those branches
```

The three major strategies you should understand are:

1. GitHub Flow
2. Trunk-Based Development
3. Git Flow

Important: Release branches and hotfix branches are NOT separate strategies. They are branch types/patterns, mainly associated with Git Flow.

---

## 2. GitHub Flow

GitHub Flow is a simple branch strategy based around main and short-lived feature branches.

### Basic structure

```text
main
 ├── feature/login
 ├── feature/profile
 └── feature/payment
```

### Typical workflow

```text
main
  ↓
create feature branch
  ↓
develop
  ↓
push branch
  ↓
Pull Request
  ↓
code review
  ↓
merge into main
  ↓
delete feature branch
```

### Example

```bash
git switch main
git pull

git switch -c feature/login

# Work on the feature
git add .
git commit -m "Add login screen"

git push -u origin feature/login
```

Then open a Pull Request.
After review:

```text
feature/login
      ↓
Pull Request
      ↓
main
```

Then delete the feature branch.

### Main idea

main should normally remain in a state that can be released/deployed.

### Characteristics

- Simple
- Few long-lived branches
- Feature branches are temporary
- Pull Requests are commonly used
- Good for continuous delivery
- Easy to understand

### Example

You need to add Dark Mode:

```text
main
  \
   feature/dark-mode
```

After development:

```text
feature/dark-mode
        ↓
       PR
        ↓
      review
        ↓
       main
```

---

## 3. Trunk-Based Development

In Trunk-Based Development, the main branch is called the trunk.
Usually:

```text
main = trunk
```

The central idea is:
Integrate changes into main very frequently.
Branches, if used, are extremely short-lived.

### Example

```text
main
  \
   small-change
       ↓
      main
```

Then another change:

```text
main
  \
   another-small-change
          ↓
         main
```

Instead of keeping a branch for weeks:

```text
feature/dark-mode

Monday
Tuesday
Wednesday
Thursday
Friday

        ↓

      merge
```

developers try to integrate small changes quickly.

### Main idea

Stay close to main.

### Characteristics

- Very short-lived branches
- Frequent integration
- Small changes
- Requires good automated testing
- Often used with CI/CD
- Helps reduce large merge conflicts

### Feature Flags

Trunk-Based Development often uses feature flags.
For example:

```text
Dark Mode code exists
        ↓
Feature Flag = OFF
        ↓
Users don't see it
```

Later:

```text
Feature Flag = ON
        ↓
Users see Dark Mode
```

This allows incomplete or partially developed functionality to exist in the codebase without necessarily exposing it to users.

### Important distinction

GitHub Flow and Trunk-Based Development can look similar because both use short-lived feature branches.
The main difference is the philosophy:

```text
GitHub Flow:
feature → PR → main

Trunk-Based:
small change → main as frequently as possible
```

Trunk-Based Development emphasizes very frequent integration into the trunk.

---

## 4. Git Flow

Git Flow is a more structured branch strategy.
It uses multiple types of branches.
The classic structure is:

```text
main
  ↑
release
  ↑
develop
  ↑
feature
```

There are two important long-lived branches:

```text
main
develop
```

And several temporary branch types:

```text
feature/*
release/*
hotfix/*
```

### 4.1 Feature Branches

Feature branches are used to develop individual features.

#### Example

```text
develop
   \
    feature/login
```

After the feature is complete:

```text
feature/login
      ↓
    develop
```

Multiple features can exist:

```text
             feature/login
            /
develop ---- feature/payment
            \
             feature/profile
```

### 4.2 Develop Branch

develop represents the current development state.
Features are normally merged into:

```text
feature/*
      ↓
develop
```

The next release is prepared from develop.

### 4.3 Release Branches

A release branch is created when a particular version is ready to be prepared and tested.

#### Example

```text
develop
   ↓
release/2.0
```

Now QA can test version 2.0.
Only release-related fixes should normally be added to the release branch.
Meanwhile, developers can continue working on the next version in develop.

```text
release/2.0
    ↓
QA / bug fixes

develop
    ↓
Version 3.0 work
```

When version 2.0 is ready:

```text
release/2.0
      ↓
     main
      ↓
 production
```

The release is also normally merged back into develop so release fixes are not lost.

#### Conceptually

```text
             → main → production
            /
release/2.0
            \
             → develop
```

### Main idea

A release branch is:
A temporary branch used to stabilize and prepare a specific release.

---

## 5. Hotfix Branches

A hotfix branch is used for an urgent production bug.
Imagine:

```text
main
 ↓
production
 ↓
CRITICAL BUG
```

You cannot wait for the next normal release.
Create:

```text
hotfix/payment-crash
```

Fix the bug:

```text
main
  \
   hotfix/payment-crash
          ↓
        fix
          ↓
         main
          ↓
      production
```

In classic Git Flow, the hotfix is also merged into develop so the fix exists in future development.

### Conceptually

```text
              → main → production
             /
hotfix/bug
             \
              → develop
```

### Main idea

A hotfix branch is:
A temporary branch for an urgent production fix.

---

## 6. Release Branch vs Hotfix Branch

This distinction is extremely important.

### Release Branch

Used for:

```text
Preparing a planned release
```

#### Example

```text
release/2.0
```

#### Situation

"Version 2.0 is almost ready. QA needs to test and stabilize it."

### Hotfix Branch

Used for:

```text
Fixing an urgent production problem
```

#### Example

```text
hotfix/payment-crash
```

#### Situation

"Version 2.0 is already live, but there is a critical crash."

Remember:

```text
Release = planned
Hotfix  = emergency
```

---

## 7. Comparing the Three Strategies

| Strategy | Main Idea | Branch Lifetime | Complexity |
| --- | --- | --- | --- |
| GitHub Flow | Feature → PR → main | Short | Low |
| Trunk-Based | Integrate into main very frequently | Very short | Medium |
| Git Flow | Structured development with develop/release/hotfix | Longer | High |

---

## 8. Visual Comparison

### GitHub Flow

```text
main
  \
   feature
      ↓
     PR
      ↓
    main
```

Simple.

### Trunk-Based Development

```text
main
 ↓
small change
 ↓
main
 ↓
small change
 ↓
main
 ↓
small change
 ↓
main
```

Very frequent integration.

### Git Flow

```text
                 feature
                /
develop -------- feature
                \
                 feature
                    ↓
               release/2.0
                    ↓
                   main
                    ↓
                production
```

More structured.

---

## 9. Where Release and Hotfix Branches Fit

Do NOT think:

```text
GitHub Flow
Trunk-Based
Git Flow
Release Branch
Hotfix Branch
```

are five different strategies.
Instead:

```text
Branch Strategies
│
├── GitHub Flow
│
├── Trunk-Based Development
│
└── Git Flow
     │
     ├── Feature Branch
     ├── Release Branch
     └── Hotfix Branch
```

Release and hotfix branches are branch patterns/types, not separate major strategies.

---

## 10. The Most Important Mental Model

Ask three questions when looking at a branch strategy.

### Question 1: Where does normal development happen?

#### GitHub Flow:

```text
feature → main
```

#### Trunk-Based:

```text
small changes → main
```

#### Git Flow:

```text
feature → develop
```

### Question 2: How long do branches live?

#### GitHub Flow:

```text
short
```

#### Trunk-Based:

```text
very short
```

#### Git Flow:

```text
can be longer
```

### Question 3: How are releases handled?

#### GitHub Flow:

```text
main → production
```

#### Trunk-Based:

```text
main → production
```

#### Git Flow:

```text
develop
   ↓
release
   ↓
main
   ↓
production
```

---

## 11. Easy Way to Remember

```text
GitHub Flow
    ↓
Simple
```

```text
Trunk-Based Development
    ↓
Fast + frequent integration
```

```text
Git Flow
    ↓
Structured + multiple branch types
```

And:

```text
Release Branch
    ↓
Planned release
```

```text
Hotfix Branch
    ↓
Emergency production fix
```

---

## 12. What You Should Practice

Don't just memorize the diagrams.
Create a small Git repository and practice these scenarios.

### Practice 1 — GitHub Flow

```text
main
  ↓
feature/login
  ↓
commit
  ↓
merge
  ↓
main
```

### Practice 2 — Trunk-Based Development

Make several tiny changes and integrate them into main frequently.

```text
main
 ↓
small change
 ↓
main
 ↓
small change
 ↓
main
```

### Practice 3 — Release Branch

Simulate:

```text
develop
   ↓
release/1.0
   ↓
bug fix
   ↓
main
```

### Practice 4 — Hotfix

Simulate:

```text
main
 ↓
production bug
 ↓
hotfix/crash
 ↓
main
 ↓
production
```

### Practice 5 — Git Flow

Finally practice the complete model:

```text
main
develop
feature/*
release/*
hotfix/*
```

---

## 13. One-Sentence Summary

GitHub Flow keeps things simple, Trunk-Based Development keeps integration extremely frequent, and Git Flow adds more structure around development, releases, and production fixes.
