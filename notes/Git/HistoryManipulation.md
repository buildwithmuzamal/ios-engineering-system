# Git History Manipulation

> Goal: Learn how to clean, organize, and safely manage Git history before sharing your work.

---

# 1. Interactive Rebase

## What is it?

Interactive Rebase allows you to **rewrite commit history** by replaying commits one by one while giving you control over each commit.

Unlike a normal rebase, you can:

- Change commit messages
- Combine commits
- Remove commits
- Edit commit contents
- Reorder commits
- Split commits

## Command

```bash
git rebase -i HEAD~N
```

Example:

```bash
git rebase -i HEAD~5
```

Git opens:

```text
pick a1b2c3 Commit 1
pick d4e5f6 Commit 2
pick g7h8i9 Commit 3
```

Change `pick` to another action if needed.

---

# Interactive Rebase Commands

| Command | Purpose |
|---------|----------|
| pick | Keep commit |
| reword | Change commit message |
| edit | Change commit contents |
| squash | Merge commits and edit message |
| fixup | Merge commits and discard second message |
| drop | Delete commit |

---

# 2. Reword

## Purpose

Change only the commit message.

The code remains unchanged.

### Before

```text
Add Login
```

### After

```text
Implement Login Screen
```

### Steps

```bash
git rebase -i HEAD~1
```

Change

```text
pick
```

to

```text
reword
```

Save.

Git opens the commit message.

Edit it.

Save.

Done.

---

# 3. Squash

## Purpose

Combine multiple commits into one.

Allows editing the final commit message.

### Before

```text
Add Login

Fix Login

Improve Login
```

### After

```text
Add Login
```

(with one combined commit)

### Steps

```bash
git rebase -i HEAD~3
```

Example:

```text
pick   Add Login
squash Fix Login
squash Improve Login
```

Git asks for the final commit message.

---

# 4. Fixup

## Purpose

Combine commits while automatically keeping the first commit message.

Use when the second commit is just a small correction.

### Before

```text
Add Login

Fix Typo
```

### After

```text
Add Login
```

### Steps

```bash
git rebase -i HEAD~2
```

Example:

```text
pick   Add Login
fixup  Fix Typo
```

Git does not ask for a commit message.

---

# 5. Autosquash

## Purpose

Automatically arrange fixup commits.

Instead of manually changing

```text
pick
```

to

```text
fixup
```

Git does it for you.

### Create Fixup Commit

```bash
git commit --fixup=<commit-hash>
```

Example

```bash
git commit --fixup=06a50ab
```

Git creates

```text
fixup! Learn MVVM
```

### Run

```bash
git rebase -i --autosquash HEAD~N
```

Git automatically changes

```text
pick fixup! Learn MVVM
```

to

```text
fixup fixup! Learn MVVM
```

---

# 6. Edit

## Purpose

Modify the contents of an existing commit.

Useful when:

- forgot a file
- need to remove debug code
- want cleaner history

### Steps

Start

```bash
git rebase -i HEAD~N
```

Change

```text
pick
```

to

```text
edit
```

Git stops.

Make changes.

Stage:

```bash
git add .
```

Amend:

```bash
git commit --amend
```

Continue:

```bash
git rebase --continue
```

---

# 7. Drop

## Purpose

Delete a commit completely.

### Before

```text
Login

Temporary Debug

Profile
```

### After

```text
Login

Profile
```

### Steps

```bash
git rebase -i HEAD~3
```

Change

```text
pick
```

to

```text
drop
```

or remove the line entirely.

---

# 8. Split Commits

## Purpose

Break one large commit into several smaller commits.

Example

### Before

```text
Add Login + Profile + Settings
```

### After

```text
Add Login

Add Profile

Add Settings
```

### Steps

Start

```bash
git rebase -i HEAD~1
```

Change

```text
pick
```

to

```text
edit
```

Git stops.

Undo the commit while keeping all changes:

```bash
git reset HEAD^
```

Now create smaller commits:

```bash
git add login.txt
git commit -m "Add Login"

git add profile.txt
git commit -m "Add Profile"

git add settings.txt
git commit -m "Add Settings"
```

Continue

```bash
git rebase --continue
```

---

# 9. Rebase vs Merge

## Merge

Command

```bash
git merge main
```

Creates a merge commit.

### Before

```text
A---B---C (main)
     \
      D---E (feature)
```

After

```text
A---B---C------F (main)
     \         /
      D---E---M
```

Advantages

- preserves history
- safe for shared branches
- no commit rewriting

---

## Rebase

Command

```bash
git rebase main
```

Replays feature commits on top of main.

### Before

```text
A---B---C---F---G (main)
     \
      D---E (feature)
```

After

```text
A---B---C---F---G---D'---E'
```

Advantages

- linear history
- cleaner commit graph
- great before Pull Requests

Disadvantage

- rewrites commit history

---

# Interactive Rebase vs Rebase

## Normal Rebase

```bash
git rebase main
```

Purpose

Move your branch onto another branch.

Example

```text
feature
   D
   E

↓

main
A-B-C-F-G

↓

A-B-C-F-G-D'-E'
```

---

## Interactive Rebase

```bash
git rebase -i HEAD~5
```

Purpose

Replay commits while allowing you to edit them.

You can

- reword
- squash
- fixup
- edit
- drop
- reorder

Interactive Rebase is simply **Rebase with user control**.

---

# 10. Force Push vs --force-with-lease

## Normal Push

```bash
git push
```

Use when history has **not** been rewritten.

Example

```text
A-B-C

↓

A-B-C-D
```

---

## Force Push

```bash
git push --force
```

Purpose

Overwrite remote history with local history.

Danger

Can overwrite other developers' work.

---

## Force With Lease

```bash
git push --force-with-lease
```

Purpose

Force push **only if the remote hasn't changed** since your last fetch.

If someone pushed new commits:

Git rejects your push.

Safer than

```bash
git push --force
```

---

# When to Use Which Push Command

| Situation | Command |
|-----------|----------|
| Added new commit | `git push` |
| Used amend | `git push --force-with-lease` |
| Squashed commits | `git push --force-with-lease` |
| Rebased branch | `git push --force-with-lease` |
| Reworded commit | `git push --force-with-lease` |
| Dropped commit | `git push --force-with-lease` |

Avoid

```bash
git push --force
```

unless you fully understand the consequences.

---

# Quick Cheat Sheet

| Task | Command |
|------|----------|
| Interactive Rebase | `git rebase -i HEAD~N` |
| Rebase onto main | `git rebase main` |
| Reword | `reword` |
| Edit | `edit` |
| Squash | `squash` |
| Fixup | `fixup` |
| Autosquash | `git rebase -i --autosquash HEAD~N` |
| Create fixup commit | `git commit --fixup=<hash>` |
| Drop | `drop` |
| Split commit | `edit` + `git reset HEAD^` |
| Continue rebase | `git rebase --continue` |
| Abort rebase | `git rebase --abort` |
| Force push safely | `git push --force-with-lease` |

---

# Best Practices

- Make each commit represent one logical change.
- Reword unclear commit messages before sharing.
- Squash or fixup small correction commits.
- Use `edit` to fix old commits.
- Split large commits into smaller logical commits.
- Rebase your feature branch before opening a Pull Request.
- Prefer `git push --force-with-lease` over `git push --force`.
- Never rewrite history on shared branches unless your team agrees.