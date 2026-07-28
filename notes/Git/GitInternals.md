# Git Internals (Practical Guide)

> **Goal:** Understand how Git works internally without going too deep. This is enough knowledge for most professional software developers.

---

# Git Object Model

Git stores everything as objects.

There are four object types:

1. Blob
2. Tree
3. Commit
4. Tag

---

# 1. Blob Object

## Definition

A **Blob (Binary Large Object)** stores **only the contents of a file**.

It does **NOT** store:

- Filename ❌
- File path ❌
- Folder ❌
- Permissions ❌

It stores only:

- File contents ✅

---

## Example

Project

```text
README.md
```

Contents

```text
Hello Git
```

Git creates

```text
Blob

Content:
Hello Git
```

---

## Important

Renaming a file does **not** create a new Blob.

Changing the file contents **does** create a new Blob.

---

## Mental Model

```
Blob = File Contents
```

---

# 2. Tree Object

## Definition

A **Tree** represents a directory (folder).

It stores:

- Filenames
- Folder structure
- File permissions
- Pointers to Blobs
- Pointers to other Trees

---

## Example

Project

```text
Project/

README.md
main.swift
```

Git stores

```text
Tree

README.md ─────► Blob A

main.swift ────► Blob B
```

---

## Nested Folders

```text
Project/

Sources/
    main.swift

Images/
    logo.png
```

Git creates multiple Trees.

```text
Root Tree

Sources ─────► Sources Tree

Images ──────► Images Tree
```

---

## Mental Model

```
Tree = Folder
```

---

# 3. Commit Object

## Definition

A Commit is a snapshot of your project.

It does **NOT** store files directly.

Instead, it stores:

- Tree Hash
- Parent Commit
- Author
- Date
- Commit Message

---

## Example

```text
Commit

Message:
"Add Login Screen"

↓

Root Tree

↓

Blobs
```

---

## Visual

```
Commit
   │
   ▼
Tree
   │
   ▼
Blobs
```

---

## Important

Every commit points to one Root Tree.

The Tree points to Blobs.

---

## Mental Model

```
Commit = Snapshot
```

---

# 4. Tag Object

## Definition

A Tag is a permanent name for a commit.

Example

```
v1.0
```

instead of remembering

```
a7d82c...
```

---

## Example

```
A ---- B ---- C ---- D
              ▲
              │
            v1.0
```

---

## Uses

- Releases
- Stable versions
- Production deployments

---

## Types

### Lightweight Tag

Simple pointer.

### Annotated Tag

Stores:

- Tag name
- Creator
- Date
- Message

---

## Mental Model

```
Tag = Permanent Bookmark
```

---

# References (Refs)

## Definition

A Reference is simply a named pointer to a commit.

Examples

```
main
feature/login
v1.0
origin/main
```

All of these point to commits.

---

## Visual

```
main
 │
 ▼
Commit D
```

---

## Types of References

```
refs/

heads/
    main
    feature

tags/
    v1.0

remotes/
    origin/main
```

---

## Important

A Branch is a movable reference.

A Tag is usually a fixed reference.

---

## Custom References

Git also allows custom references.

Example

```
refs/testing/my-ref
```

Create one

```bash
git update-ref refs/testing/my-ref HEAD
```

View all references

```bash
git show-ref
```

Delete

```bash
git update-ref -d refs/testing/my-ref
```

---

## Mental Model

```
Reference = Named Pointer
```

---

# HEAD

## Definition

HEAD tells Git

> "Where am I right now?"

Usually HEAD points to a branch.

```
HEAD
 │
 ▼
main
 │
 ▼
Commit D
```

---

## After a Commit

```
A ---- B ---- C ---- D
                    ▲
                    │
                  main
```

HEAD stays on **main**.

---

## Mental Model

```
HEAD = Your Current Location
```

---

# Detached HEAD

Normally

```
HEAD
 │
 ▼
main
 │
 ▼
Commit D
```

Checkout an old commit

```bash
git checkout <commit-hash>
```

Now

```
HEAD
 │
 ▼
Commit B
```

HEAD points directly to a commit instead of a branch.

This is called a **Detached HEAD**.

---

## Important

If you make commits while detached, no branch points to them.

Create a branch if you want to keep that work.

---

## Mental Model

```
Detached HEAD = Looking at History
```

---

# Working Tree

## Definition

The Working Tree is the files currently on your computer.

Example

```
Project/

README.md

main.swift
```

Editing these files changes the Working Tree.

Nothing is saved into Git yet.

---

## Mental Model

```
Working Tree = Your Files
```

---

# Index (Staging Area)

## Definition

The Index is Git's waiting room.

Changes stay here before becoming a commit.

---

## Flow

```
Working Tree

↓

git add

↓

Index

↓

git commit

↓

Commit
```

---

## Why?

Suppose you changed 20 files.

You only want to commit 5.

The Index lets you choose exactly what goes into the next commit.

---

## Mental Model

```
Index = Shopping Cart

Commit = Checkout
```

---

# Complete Git Flow

```
You Edit Files
      │
      ▼

Working Tree
      │
  git add
      ▼

Index
      │
 git commit
      ▼

Commit
      │
      ▼

Tree
      │
      ▼

Blob(s)
```

---

# Complete Git Object Model

```
                HEAD
                 │
                 ▼

              main (Reference)
                 │
                 ▼

              Commit
                 │
                 ▼

             Root Tree
          ┌──────┴──────┐
          ▼             ▼

     README.md      Sources/
          │             │
          ▼             ▼

      Blob A      Sources Tree
                        │
                        ▼

                   main.swift
                        │
                        ▼

                     Blob B
```

---

# Cheat Sheet

| Concept | Simple Meaning |
|----------|----------------|
| Blob | File contents |
| Tree | Folder structure |
| Commit | Snapshot of the project |
| Tag | Permanent bookmark to a commit |
| Reference (Ref) | Named pointer to a commit |
| Branch | Movable reference |
| HEAD | Your current location |
| Detached HEAD | HEAD points directly to a commit |
| Working Tree | Files on your computer |
| Index (Staging Area) | Selected changes waiting to be committed |

---

# One-Line Summary

- **Blob** → File contents
- **Tree** → Folder structure
- **Commit** → Snapshot
- **Tag** → Permanent bookmark
- **Reference** → Named pointer
- **Branch** → Movable reference
- **HEAD** → Current location
- **Detached HEAD** → HEAD on a commit instead of a branch
- **Working Tree** → Files you're editing
- **Index** → Staging area before commit

---

# What to Learn Next

Now that you understand Git Internals, the next topics should be:

1. Interactive Rebase
2. Merge vs Rebase
3. Cherry-pick
4. Reset (soft, mixed, hard)
5. Reflog
6. Stash
7. Bisect
8. Worktree
9. Hooks

These topics become much easier because you now understand what Git is actually moving internally.