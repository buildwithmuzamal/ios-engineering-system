# Git — Large Projects & Performance/Maintenance

# Large Projects

## 1. Git Worktree 🟡

Git Worktree allows you to have **multiple working directories from the same Git repository**.

Normally:

```text
Repository
   ↓
One working directory
   ↓
One checked-out branch
```

With worktrees:

```text
Repository
 ├── Worktree 1 → main
 ├── Worktree 2 → feature/login
 └── Worktree 3 → bugfix/crash
```

### Why use it?

Useful when you want to work on multiple branches at the same time without constantly switching branches.

---

# 2. Git Hooks 🟡

Git Hooks are scripts that Git automatically runs when specific Git actions happen.

Example:

```text
git commit
    ↓
pre-commit hook
    ↓
Run checks
    ↓
Success → Commit continues
Failure → Commit stops
```

Useful for:

- Running linting
- Running formatting checks
- Running tests
- Validating commit messages
- Preventing bad code from being committed or pushed
- Automating team rules

---

## Where Are Git Hooks?

Git stores local hooks inside:

```text
.git/hooks/
```

Check them:

```bash
ls .git/hooks
```

Typical sample hooks include:

```text
pre-commit.sample
commit-msg.sample
pre-push.sample
```

---

## Creating a `pre-commit` Hook

Create it:

```bash
touch .git/hooks/pre-commit
```

Make it executable:

```bash
chmod +x .git/hooks/pre-commit
```

Example:

```sh
#!/bin/sh

echo "Running pre-commit checks..."

echo "Commit is allowed."

exit 0
```

Now:

```bash
git add .
git commit -m "Test git hook"
```

The hook automatically runs before the commit.

---

## Exit Codes

The most important Git Hook concept:

```text
exit 0 → SUCCESS → Git continues
exit 1 → FAILURE → Git stops
```

### `exit 0`

Allows the Git operation to continue:

```sh
exit 0
```

Example:

```text
git commit
    ↓
pre-commit
    ↓
exit 0
    ↓
Commit created
```

### `exit 1`

Stops the Git operation:

```sh
exit 1
```

Example:

```text
git commit
    ↓
pre-commit
    ↓
exit 1
    ↓
Commit blocked
```

### Important

`echo` only prints text.

This does NOT block a commit:

```sh
echo "Commit is blocked."
```

This blocks it:

```sh
exit 1
```

---

## Blocking a Commit

Example:

```sh
#!/bin/sh

echo "Running pre-commit checks..."

echo "Commit is blocked."

exit 1
```

Now:

```bash
git add .
git commit -m "Test git hook"
```

The commit should be blocked because the hook exits with status `1`.

---

## Common Git Hooks

You don't need to memorize every Git Hook.

Focus on these three.

### `pre-commit`

Runs before a commit is created.

Useful for:

- Formatting
- Linting
- Quick tests
- Simple validation

```text
git commit
    ↓
pre-commit
```

### `commit-msg`

Runs after entering the commit message.

Useful for enforcing commit-message rules.

For example:

```text
feat: add login
fix: resolve crash
refactor: simplify networking
```

A hook can reject invalid commit messages.

### `pre-push`

Runs before Git pushes to a remote.

Useful for:

- Running tests
- Running lint
- Checking important conditions

```text
git push
   ↓
pre-push
   ↓
Checks
   ↓
Pass → Push
Fail → Stop
```

---

## Practical iOS Example

A team might want to prevent pushing code when tests fail.

Example `pre-push` hook:

```sh
#!/bin/sh

echo "Running tests before push..."

xcodebuild test \
    -scheme MyApp \
    -destination 'platform=iOS Simulator,name=iPhone 16'

if [ $? -ne 0 ]; then
    echo "Tests failed. Push aborted."
    exit 1
fi

echo "Tests passed. Continuing push."
exit 0
```

Workflow:

```text
git push
   ↓
Run tests
   ↓
 ┌───────────────┐
 │               │
Pass             Fail
 │               │
 ↓               ↓
Push          Stop push
```

---

## Important Limitation of `.git/hooks`

Hooks inside:

```text
.git/hooks/
```

are local to your repository.

They are normally not committed and pushed to the remote.

Therefore:

```text
Developer A
.git/hooks/pre-commit

Developer B
does NOT automatically get it
```

---

## Sharing Hooks With a Team

A common approach is to create a tracked directory:

```text
.githooks/
├── pre-commit
└── pre-push
```

Example:

```text
MyApp/
├── .githooks/
│   ├── pre-commit
│   └── pre-push
├── Sources/
├── Tests/
└── README.md
```

Configure Git:

```bash
git config core.hooksPath .githooks
```

Now Git uses:

```text
.githooks/
```

instead of:

```text
.git/hooks/
```

Because `.githooks/` is part of the repository, it can be committed and shared.

---

## Don't Put Huge Tests in `pre-commit`

Avoid making every commit take several minutes.

A better strategy:

```text
pre-commit
    ↓
Fast checks
- Formatting
- Lint
- Simple validation
```

Then:

```text
pre-push
    ↓
More expensive checks
- Unit tests
- Integration tests
```

And:

```text
Push
 ↓
CI
 ↓
Full test suite
```

---

## Git Hooks vs CI

### Git Hooks

Run on the developer's machine:

```text
Your Mac
   ↓
Git Hook
```

They provide:

- Fast feedback
- Local automation
- Developer convenience

### CI

Runs on a CI server:

```text
GitHub
   ↓
CI Server
   ↓
Build / Tests / Lint
```

CI should perform the authoritative checks.

Why?

Because local hooks can be bypassed.

For example:

```bash
git commit --no-verify
```

can bypass client-side commit hooks.

Therefore:

```text
Git Hooks
→ Convenience + early feedback

CI
→ Authoritative verification
```

---

## Git Hooks Practice

### Practice 1 — Allow a Commit

Create a `pre-commit` hook:

```sh
#!/bin/sh

echo "Running pre-commit checks..."
echo "Commit is allowed."

exit 0
```

Run:

```bash
git add .
git commit -m "Test git hook"
```

Understand that `exit 0` allows the commit.

### Practice 2 — Block a Commit

Change:

```sh
exit 0
```

to:

```sh
exit 1
```

Run:

```bash
git add .
git commit -m "Test git hook"
```

Understand that `exit 1` blocks the commit.

### Practice 3 — Pre-Push Hook

Create:

```text
.git/hooks/pre-push
```

Make it executable:

```bash
chmod +x .git/hooks/pre-push
```

Add:

```sh
#!/bin/sh

echo "Running before push..."
```

Then push and observe that the hook runs before the push.

### Practice 4 — Shared Hooks

Create:

```text
.githooks/
```

Move your hooks there and configure:

```bash
git config core.hooksPath .githooks
```

Commit the `.githooks` directory so the team can share the hooks.

---

# 3. Git LFS ⚪

**Git Large File Storage (LFS)** is used for large files that don't work well with normal Git.

Examples:

- Large images
- Videos
- Audio
- Design files
- Large binary files

Instead of storing the large file directly in normal Git history:

```text
Normal Git
Git → Large file
```

Git LFS uses:

```text
Git → Pointer → Large file storage
```

### Mental model

```text
Git LFS
→ Large binary files
```

You only need to understand the purpose initially.

---

# 4. Sparse Checkout ⚪

Sparse Checkout allows you to clone a repository but only check out specific folders/files.

Useful when a repository is huge and you only need part of it.

Example:

```text
Huge Repository
├── iOS/
├── Android/
├── Backend/
├── Docs/
└── Tools/
```

You might only check out:

```text
iOS/
```

### Mental model

```text
Sparse Checkout
→ Only check out the part of a large repository you need
```

It is especially useful with large monorepos.

---

# 5. Submodules ⚪

A Git repository can contain another Git repository as a dependency.

Example:

```text
Main Repository
├── App
├── Sources
└── ExternalLibrary ← separate Git repository
```

The main repository tracks a **specific commit** of the external repository.

### Mental model

```text
Main Repository
      ↓
References another Git repository
```

Useful when an external project needs to remain an independent Git repository.

---

# 6. Subtree ⚪

Git Subtree has a similar goal to Submodules: include another repository inside your repository.

The important difference:

```text
Submodule
Main repo
   ↓
Reference another repository

Subtree
Main repo
   ↓
Contains another repository's code
```

The external code becomes part of the main repository's working tree/history.

For now, understand the concept rather than memorizing commands.

---

# Performance & Maintenance

These topics deal with how Git stores objects and keeps repositories efficient.

---

# 7. Garbage Collection ⚪

Git can have objects that are no longer needed.

Garbage collection cleans up and optimizes the repository.

```text
Unused Git objects
       ↓
Garbage Collection
       ↓
Cleanup + Optimization
```

Command:

```bash
git gc
```

You generally don't need to run it manually often because Git can perform maintenance automatically.

### Mental model

```text
Garbage Collection
→ Clean and optimize Git storage
```

---

# 8. Pack Files ⚪

Git does not necessarily store every object as an independent file forever.

Git can compress many Git objects together into pack files.

Instead of:

```text
Object
Object
Object
Object
Object
```

Git can store them efficiently as:

```text
Pack File
 ├── Object
 ├── Object
 ├── Object
 └── Object
```

This saves disk space and improves performance.

### Mental model

```text
Pack Files
→ Efficiently store many Git objects together
```

---

# 9. Pruning ⚪

Pruning removes Git objects that are no longer reachable and are safe to delete.

Example:

```text
Deleted / unreachable objects
          ↓
       Pruning
          ↓
       Removed
```

Be careful:

```text
Unreachable
≠
Immediately safe to delete in every situation
```

Git can sometimes use unreachable objects for recovery before they are permanently removed.

### Mental model

```text
Pruning
→ Remove old unreachable Git objects
```

---

# 10. Repository Maintenance ⚪

Repository Maintenance is the broader concept of keeping a Git repository:

- Fast
- Compact
- Healthy
- Efficient

It can involve:

- Garbage collection
- Packing objects
- Pruning
- Updating maintenance data
- Optimizing repository storage

Mental model:

```text
Repository Maintenance
        │
        ├── Garbage Collection
        ├── Pack Files
        ├── Pruning
        └── Other optimization
```

---

# Quick Reference

| Topic | Main Idea |
|---|---|
| Git Worktree | Multiple working directories from one repository |
| Git Hooks | Automatically run scripts during Git actions |
| Git LFS | Store large binary files efficiently |
| Sparse Checkout | Check out only part of a large repository |
| Submodules | Reference another Git repository |
| Subtree | Include another repository's code in your repository |
| Garbage Collection | Clean and optimize Git objects |
| Pack Files | Efficiently store Git objects |
| Pruning | Remove unreachable Git objects |
| Repository Maintenance | Keep the repository healthy and efficient |

---

# What You Need to Know

## Understand Well

### Git Worktree

```text
One repository
    ↓
Multiple working directories
    ↓
Multiple branches at the same time
```

### Git Hooks

```text
Git action
    ↓
Hook
    ↓
Script
    ↓
exit 0 → Continue
exit 1 → Stop
```

Especially understand:

```text
pre-commit
commit-msg
pre-push
```

---

## Understand Conceptually

### Git LFS

```text
Large binary files
```

### Sparse Checkout

```text
Only part of a huge repository
```

### Submodules

```text
Repository inside/reference from another repository
```

### Subtree

```text
Another repository's code becomes part of your repository
```

### Garbage Collection

```text
Clean / optimize Git objects
```

### Pack Files

```text
Efficiently store Git objects
```

### Pruning

```text
Remove unreachable objects
```

### Repository Maintenance

```text
Overall Git optimization and cleanup
```

---

# Final Mental Model

## Large Projects

```text
How do I work efficiently with a huge or complex repository?

        ├── Worktree
        ├── Hooks
        ├── LFS
        ├── Sparse Checkout
        ├── Submodules
        └── Subtree
```

## Performance & Maintenance

```text
How does Git store and maintain all that data efficiently?

        ├── Garbage Collection
        ├── Pack Files
        ├── Pruning
        └── Repository Maintenance
```

The goal at this stage is **not** to memorize every command.

You should know:

```text
Worktree
→ Multiple branches/workspaces

Hooks
→ Automatic checks

LFS
→ Large files

Sparse Checkout
→ Partial checkout

Submodules
→ Separate repository dependency

Subtree
→ Repository code included in main repository

Garbage Collection
→ Cleanup

Pack Files
→ Efficient storage

Pruning
→ Remove unreachable objects

Maintenance
→ Keep Git healthy
```

That level of understanding is enough before moving deeper into Git internals.
