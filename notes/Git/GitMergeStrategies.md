# Git Merge Strategies

## Overview

Git has several ways to combine work from different branches:

- Fast-Forward Merge
- Three-Way Merge
- Squash Merge
- Rebase + Merge
- Octopus Merge
- Ours/Theirs Strategy

---

## 1. Fast-Forward Merge

A fast-forward merge happens when the target branch has not moved forward since the feature branch was created.

### Before

```text
A---B---C  main
         \
          D---E  feature
```

Git can simply move main forward.

### After

```text
A---B---C---D---E  main, feature
```

No merge commit is created.

### Command

```bash
git switch main
git merge feature
```

### Mental Model

"main is behind feature, so I can simply move main forward."

### Important

Fast-forward merge:

- Creates no merge commit.
- Keeps a linear history.
- Only works when the branches have not diverged.

---

## 2. Three-Way Merge

A three-way merge happens when both branches have new commits after they diverged.

### Before

```text
        D---E  feature
       /
A---B---C---F  main
```

Git uses three points:

- Common ancestor: B
- Tip of feature: E
- Tip of main: F

That is why it is called a three-way merge.

### After

```text
        D---E
       /     \
A---B---C---F---M  main
```

M is a merge commit.

### Command

```bash
git switch main
git merge feature
```

### Mental Model

"The branches diverged, so Git needs to combine their histories."

### Important

Three-way merge:

- Happens when branches have diverged.
- Usually creates a merge commit.
- Preserves the existing commits.
- Can produce conflicts.

---

## 3. Squash Merge

A squash merge combines all changes from a feature branch into one new commit on the target branch.

### Before

```text
A---B---C  main
     \
      D---E---F  feature
```

### After

```text
A---B---C---S  main
```

S contains the combined changes from:

```text
D + E + F
```

The individual commits D, E, and F are not added individually to main.

### Command

```bash
git switch main
git merge --squash feature
git commit
```

`git merge --squash` prepares the changes but does not create the commit automatically.

### Mental Model

"Take all the work from this branch and turn it into one commit."

### Advantages

- Keeps main history clean.
- Removes noisy development commits.
- Useful when a feature branch has many small commits.

### Disadvantage

The original feature commits are not preserved in the target branch history.

---

## 4. Rebase + Merge

Rebase and merge are different operations.

A common workflow is:

1. Rebase the feature branch onto main.
2. Merge the rebased branch into main.

### Before Rebase

```text
        D---E  feature
       /
A---B---C  main
```

Run:

```bash
git switch feature
git rebase main
```

Git recreates the feature commits on top of the latest main.

### After Rebase

```text
A---B---C---D'---E'  feature
```

Notice:

```text
D → D'
E → E'
```

The commits are recreated because their parent changed.

Now:

```bash
git switch main
git merge feature
```

The merge can be fast-forwarded:

```text
A---B---C---D'---E'  main
```

No merge commit is required.

### Mental Model

"Move my feature work on top of the latest main, then merge it as a straight line."

### Important

Rebase:

- Rewrites commit history.
- Creates new commit objects.
- Produces a cleaner linear history.
- Should be used carefully with commits other developers already have.

### Warning

Do not blindly rebase shared/public branches.

If other developers already based work on your commits, rewriting those commits can cause problems.

---

## 5. Octopus Merge

An octopus merge is an advanced merge that can combine multiple branches into one merge commit.

### Example

```text
        D---E  feature1
       /
A---B---C
       \
        F---G  feature2
       \
        H---I  feature3
```

You can merge multiple branches at once:

```bash
git merge feature1 feature2 feature3
```

The resulting merge commit can have multiple parents.

### Important Concept

An octopus merge commit can have more than two parents.

### Normal merge

```text
M
├── parent 1
└── parent 2
```

### Octopus merge

```text
M
├── parent 1
├── parent 2
├── parent 3
└── ...
```

### Why Is It Rare?

Octopus merges are most useful when the branches can be merged cleanly without conflicts.

For normal feature development, you will rarely need to use them manually.

### What You Need to Know

- Merges multiple branches at once.
- Creates one merge commit.
- The merge commit can have more than two parents.
- Mostly an advanced/overview topic.

---

## 6. Ours / Theirs Strategy

`ours` and `theirs` are mainly related to conflict resolution.

Suppose you are merging feature into main:

```bash
git switch main
git merge feature
```

If there is a conflict:

```text
CONFLICT
```

In this situation:

```text
ours   = main
theirs = feature
```

But do NOT memorize:

```text
ours = main
theirs = feature
```

That is not universally true.

Instead remember:

```text
ours = the branch you are currently on
theirs = the branch being merged in
```

### Ours

`ours` means:

Keep the version from the current branch.

For example:

```bash
git restore --ours file.swift
```

This chooses the current branch's version of the file.

### Theirs

`theirs` means:

Keep the version from the incoming branch.

For example:

```bash
git restore --theirs file.swift
```

This chooses the incoming branch's version of the file.

### Important

`ours`/`theirs` are not really alternative merge strategies like fast-forward or three-way merge.

They are mainly concepts/tools used during conflict resolution.

---

## Comparison

| Strategy | Main Idea | Merge Commit? | History |
| --- | --- | --- | --- |
| Fast-Forward | Move branch pointer forward | No | Linear |
| Three-Way Merge | Combine diverged branches | Usually yes | Preserves branches |
| Squash Merge | Combine feature commits into one commit | No traditional merge commit | Clean/linear |
| Rebase + Merge | Recreate commits on top of target branch | Usually no | Linear |
| Octopus Merge | Merge multiple branches at once | Yes | Multiple parents |
| Ours/Theirs | Choose one side during conflict resolution | Depends on merge | Conflict resolution |

---

## Fast-Forward vs Three-Way

This distinction is very important.

### Fast-Forward

#### Before

```text
A---B---C  main
         \
          D---E  feature
```

#### After

```text
A---B---C---D---E
```

#### Characteristics

- No divergence.
- No merge commit.
- Branch pointer moves forward.

### Three-Way

#### Before

```text
        D---E  feature
       /
A---B---C---F  main
```

#### After

```text
        D---E
       /     \
A---B---C---F---M
```

#### Characteristics

- Branches diverged.
- Merge commit is created.
- Existing commits are preserved.

---

## Squash vs Rebase

These are easy to confuse.

### Squash

Several commits become one new commit:

```text
D---E---F
    ↓
    S
```

Conceptually:

```text
D + E + F → S
```

### Rebase

Commits remain separate but are recreated on a new base:

```text
D---E
 ↓   ↓
D'--E'
```

### Simple Difference

#### Squash

Combine several commits into one.

#### Rebase

Recreate commits on top of a different base.

---

## The Most Important Mental Model

```text
Fast-Forward
    ↓
"Just move the pointer."
```

```text
Three-Way Merge
    ↓
"The branches diverged. Create a merge commit."
```

```text
Squash Merge
    ↓
"Take all feature work and make one commit."
```

```text
Rebase + Merge
    ↓
"Move/recreate feature commits on top of main."
```

```text
Octopus Merge
    ↓
"Merge several branches at once."
```

```text
Ours/Theirs
    ↓
"During a conflict, choose which side's version to keep."
```

---

## What You Should Master vs Just Understand

### Master These 🔴

- Fast-Forward Merge
- Three-Way Merge
- Squash Merge
- Rebase + Merge

You should be able to:

- Draw their commit graphs.
- Explain when each happens.
- Explain what happens to commits.
- Explain whether a merge commit is created.
- Explain the effect on history.

### Understand These 🟡⚪

- Ours/Theirs
- Octopus Merge

You do not need to become an expert in octopus merges right now.

---

## Interview-Level Questions

1. What is a fast-forward merge?

A merge where the target branch has not diverged, so Git can simply move the branch pointer forward without creating a merge commit.

2. What is a three-way merge?

A merge where Git uses the common ancestor and the tips of both branches to combine changes, usually creating a merge commit.

3. What is a squash merge?

A merge workflow that combines all feature-branch changes into one new commit on the target branch.

4. Does rebase create new commits?

Yes. Rebase recreates commits because their parent/ancestry changes.

5. What does ours mean?

The version from the branch currently checked out during the merge.

6. What does theirs mean?

The version from the branch being merged into the current branch.

7. What is an octopus merge?

A merge that combines multiple branches into a single merge commit with multiple parents.

---

## Final Mental Picture

```text
                         Git Merge Strategies
                                  |
          +-----------------------+-----------------------+
          |                       |                       |
      Fast-Forward          Three-Way                Squash
          |                       |                       |
    Move pointer             Merge histories        One new commit
          |                       |                       |
       No M commit             M commit              No M commit

                    Rebase + Merge
                          |
                 Recreate commits
                          |
                    Linear history

                  Advanced Topics
                          |
              +-----------+-----------+
              |                       |
          Octopus                 Ours/Theirs
              |                       |
      Multiple branches        Conflict resolution
```

---

## Key Takeaways

- Fast-forward moves a branch pointer.
- Three-way merge combines diverged histories and normally creates a merge commit.
- Squash merge turns multiple feature commits into one commit.
- Rebase recreates commits on a new base; it is not the same operation as merge.
- Octopus merge can merge multiple branches into one merge commit.
- Ours/Theirs helps decide which side to keep during conflict resolution.
- Never memorize `ours = main` and `theirs = feature`.

Remember:

```text
Current branch = ours
Incoming branch = theirs
```