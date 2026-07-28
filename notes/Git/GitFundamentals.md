> **Purpose**
>
> Store permanent engineering knowledge that can be revisited and improved over time.

> **Use When**
>
> Learning a concept that will remain useful long-term.

> **Do Not Use**
>
> Daily logs, temporary thoughts, or progress updates.

# Git Fundamentals

## Overview

Git is a distributed version control system that tracks changes made to files over time. It allows developers to collaborate, maintain history, restore previous versions, and safely experiment using branches.

Git stores snapshots of your project instead of creating complete copies every time.

---

## Why

Git solves several software development problems:

- Tracks every change made to a project.
- Allows multiple developers to work simultaneously.
- Makes it easy to restore previous versions.
- Enables safe experimentation using branches.
- Keeps a complete project history.
- Simplifies collaboration through remote repositories.

---

## Key Concepts

### Version Control

A system that records changes to files over time.

---

### Repository

A project managed by Git.

Contains:

- Source code
- Commit history
- Branches
- Tags
- Git configuration

Stored in the hidden `.git` directory.

---

### Working Directory

The files currently visible on your computer.

---

### Staging Area (Index)

A temporary area where changes are prepared before creating a commit.

```
Working Directory
        ↓
   Staging Area
        ↓
      Commit
```

---

### Commit

A snapshot of the staged changes.

Each commit contains:

- Changes
- Author
- Timestamp
- Commit message
- Parent commit reference

---

### Branch

An independent line of development.

Allows multiple features to be developed without affecting the main branch.

---

### Merge

Combines another branch into the current branch.

Usually creates a merge commit when both branches have changed.

---

### Rebase (Basic)

Moves your branch onto another branch by replaying your commits on top of it.

Unlike merge, rebase rewrites commit history to create a cleaner, linear history.

Only rebase commits that have not been shared with others.

---

### Cherry-pick

Copies a specific commit from another branch without merging the entire branch.

---

### Reset

Moves the current branch to another commit.

Depending on the mode (`--soft`, `--mixed`, `--hard`), it may also modify the staging area and working directory.

---

### Revert

Creates a new commit that undoes the changes introduced by an earlier commit.

Unlike reset, history is preserved.

---

### Stash

Temporarily saves uncommitted changes so you can return to a clean working directory.

---

### Tag

A permanent label pointing to a specific commit.

Typically used for releases such as:

- v1.0
- v2.1.3

---

### Remote

Another copy of the repository stored elsewhere (GitHub, GitLab, Bitbucket).

---

### Pull Request

A collaboration feature provided by platforms like GitHub.

Allows developers to:

- Review code
- Discuss changes
- Run CI/CD
- Merge branches

---

### Conflict Resolution

Occurs when Git cannot automatically combine changes.

The developer manually decides which changes to keep.

---

### GitHub

A cloud platform that hosts Git repositories and provides collaboration tools such as Pull Requests, Issues, Discussions, Actions, and Wikis.

---

## Best Practices

- Commit small, focused changes.
- Write meaningful commit messages.
- Create feature branches.
- Pull frequently from the main branch.
- Resolve conflicts carefully.
- Never commit generated files unless required.
- Rebase only local, unpublished commits.
- Prefer Pull Requests over pushing directly to the main branch.

---

## Common Mistakes

- Working directly on `main`.
- Creating very large commits.
- Writing vague commit messages.
- Rebasing commits already shared with teammates.
- Forgetting to pull before pushing.
- Using `git reset --hard` without understanding its effects.

---

## Apple Documentation

- None (Git is not an Apple technology.)

---

## Related Notes

- Git Internals
- Interactive Rebase
- Merge Strategies
- GitHub
- CI/CD
- Xcode Source Control

---

## Revision Questions

1. What problem does Git solve?
2. What is the difference between the Working Directory, Staging Area, and Repository?
3. Why do we create commits?
4. When should you create a branch?
5. What is the difference between Merge and Rebase?
6. When should you use Cherry-pick?
7. What is the difference between Reset and Revert?
8. Why is Rebase considered history rewriting?
9. When should you use Stash?
10. What is the purpose of a Pull Request?
11. What causes merge conflicts?
12. Why should you avoid rebasing shared commits?

---

## Last Updated

2026-07-24