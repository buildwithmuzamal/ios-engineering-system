# Git Remote Collaboration

## 1. Fetch vs Pull

### `git fetch`

Fetch downloads the latest information from the remote repository without changing your current local branch.

```bash
git fetch
```

Example:

Before:

```text
A---B---C
        ↑
       main
```

Remote has:

```text
A---B---C---D
            ↑
        origin/main
```

After:

```bash
git fetch
```

Your local branch is still at `C`, but Git now knows about `D`.

```text
A---B---C---D
    ↑       ↑
   main  origin/main
```

### `git pull`

Pull downloads remote changes and integrates them into your current branch.

Conceptually:

```bash
git pull
```

is approximately:

```bash
git fetch
git merge
```

Mental model:

```text
git fetch
Remote → Local knowledge

git pull
Remote → Local knowledge → Integrate
```

### Why use `fetch`?

`fetch` gives you more control.

You can first inspect the changes:

```bash
git fetch origin
git log main..origin/main
git diff main..origin/main
```

Then decide whether to merge or rebase.

---

# 2. Upstream Branches

An upstream branch is the remote branch that your local branch is connected to.

Example:

```text
local branch:
feature/login

        ↓ tracks

remote-tracking branch:
origin/feature/login
```

You normally establish this relationship when pushing a new branch:

```bash
git push -u origin feature/login
```

The `-u` means:

```text
Set this remote branch as the upstream branch.
```

After that, you can simply use:

```bash
git push
git pull
```

instead of repeatedly specifying:

```bash
git push origin feature/login
git pull origin feature/login
```

Check upstream relationships:

```bash
git branch -vv
```

Example:

```text
* feature/login abc123 [origin/feature/login] Add login
  main          def456 [origin/main] Update README
```

---

# 3. Tracking Branches

A tracking relationship tells Git which remote branch a local branch is associated with.

Example:

```text
local branch
feature/login
      ↓
tracks
      ↓
origin/feature/login
```

This allows Git to tell you whether your branch is ahead or behind.

For example:

```text
Your branch is ahead of 'origin/feature/login' by 2 commits.
```

or:

```text
Your branch is behind 'origin/feature/login' by 3 commits.
```

Check tracking information:

```bash
git branch -vv
```

## Important distinction

These are different:

```text
feature/login
```

Your local branch.

```text
origin/feature/login
```

A remote-tracking branch.

`origin/feature/login` is Git's local record of what the remote branch looked like the last time Git updated it, usually through `fetch`.

Mental model:

```text
LOCAL
feature/login
      ↓
REMOTE-TRACKING
origin/feature/login
      ↓
REMOTE
GitHub feature/login
```

---

# 4. Fork Workflow

A fork is your own copy of someone else's repository on GitHub.

It is useful when you do not have permission to push directly to the original repository.

Typical structure:

```text
Original Repository
        ↓
       Fork
        ↓
Your GitHub Repository
        ↓
Your Local Repository
```

Usually you configure two remotes:

```text
origin   → your fork
upstream → original repository
```

Check them:

```bash
git remote -v
```

Example:

```text
origin    https://github.com/you/project.git
upstream  https://github.com/company/project.git
```

## Typical fork workflow

Get the latest changes from the original repository:

```bash
git fetch upstream
```

Create your feature branch:

```bash
git switch -c feature/login upstream/main
```

Work on the feature.

Push the branch to your fork:

```bash
git push -u origin feature/login
```

Then create a Pull Request:

```text
Your fork
    ↓
Pull Request
    ↓
Original repository
```

## Why use a fork?

You can contribute to a project without having direct write access to the original repository.

---

# 5. Pull Request Best Practices

A Pull Request (PR) is a request to merge your changes into another branch.

A PR is not simply:

```text
"I finished my code. Please merge it."
```

A good PR communicates:

* What changed?
* Why was it changed?
* How was it implemented?
* How was it tested?

## Good PR description

### What changed?

```text
Added password reset flow.
```

### Why?

```text
Users were unable to reset their password after their session expired.
```

### How?

```text
Added a dedicated password-reset flow and updated the authentication service.
```

### Testing

```text
- Tested successful password reset
- Tested invalid token
- Tested expired token
```

---

# Keep PRs Small

Avoid huge PRs containing unrelated work.

Bad:

```text
PR:
- Add login
- Rename 20 files
- Reformat the project
- Upgrade dependencies
- Fix unrelated bug
- Rewrite networking
```

This makes code review difficult.

Better:

```text
PR #1
Add login functionality

PR #2
Add password reset

PR #3
Fix unrelated networking bug
```

The exact splitting depends on the project, but the principle is:

```text
One PR → One clear purpose
```

---

# Avoid Unrelated Changes

If you are implementing a login feature, don't include unrelated formatting, refactoring, or dependency changes unless they are necessary.

Bad:

```text
Feature:
Add login

Also:
- Rename files
- Reformat everything
- Upgrade a dependency
- Rewrite networking
- Fix another bug
```

Keep unrelated changes in separate commits or PRs.

---

# 6. Code Review Workflow

Code review is the process where other developers examine your changes before they are merged.

Typical workflow:

```text
Task
 ↓
Create branch
 ↓
Implement
 ↓
Commit
 ↓
Push
 ↓
Create Pull Request
 ↓
Code Review
 ↓
Changes requested?
 ├── Yes → Fix → Commit → Push → Review again
 │
 └── No → Approve
              ↓
             Merge
```

---

## Step 1 — Start from Updated Main

```bash
git switch main
git fetch origin
git pull --ff-only
```

Then create your feature branch:

```bash
git switch -c feature/login
```

---

## Step 2 — Implement the Feature

Make your changes and create commits.

Example:

```text
A---B---C---D
        ↑
   feature/login
```

---

## Step 3 — Push

```bash
git push -u origin feature/login
```

---

## Step 4 — Create Pull Request

The PR represents:

```text
feature/login
      ↓
     main
```

The PR description should explain:

```text
What changed?
Why?
How was it implemented?
How was it tested?
```

---

## Step 5 — Code Review

A reviewer examines your changes.

Example review comment:

```text
Can you move this validation into the authentication service?
```

You make the requested change:

```bash
git add .
git commit -m "Move validation to auth service"
git push
```

The existing Pull Request automatically updates.

You do NOT need to create another PR.

---

## Step 6 — Approval and Merge

After the reviewer approves:

```text
Reviewer
   ↓
Approve
   ↓
Merge
   ↓
main
```

---

# Complete Remote Collaboration Model

```text
                  GitHub
                    │
          ┌─────────┴─────────┐
          │                   │
       upstream              origin
       company               your fork
          │                   │
          └─────────┬─────────┘
                    │
                  fetch
                    ↓
          Remote-tracking branches
                    │
                    ↓
             Local branches
                    │
                    ↓
                 Commits
                    │
                    ↓
                  Push
                    │
                    ↓
             Pull Request
                    │
                    ↓
              Code Review
                    │
              ┌─────┴─────┐
              ↓           ↓
           Changes     Approved
              ↓           ↓
            Push         Merge
                          ↓
                         main
```

---

# Important Mental Models

## Fetch vs Pull

```text
FETCH
Remote → Update local knowledge

PULL
Remote → Update local knowledge → Integrate
```

## Tracking

```text
local branch
      ↓
remote-tracking branch
```

Example:

```text
feature/login
      ↓
origin/feature/login
```

## Fork

```text
Original repository
        ↓
       Fork
        ↓
Your repository
        ↓
Feature branch
        ↓
Pull Request
        ↓
Original repository
```

## Code Review

```text
Branch
  ↓
Push
  ↓
PR
  ↓
Review
  ↓
Fix if needed
  ↓
Approval
  ↓
Merge
```

---

# Practice Exercises

## Exercise 1 — Fetch vs Pull

Use two clones of the same repository:

```text
repo-A
repo-B
```

In `repo-A`:

```bash
git commit ...
git push
```

In `repo-B`:

```bash
git fetch
```

Then inspect:

```bash
git log main..origin/main
```

Then:

```bash
git pull
```

Understand exactly what changed.

---

## Exercise 2 — Tracking

Create a branch:

```bash
git switch -c feature/test
```

Push it:

```bash
git push -u origin feature/test
```

Check:

```bash
git branch -vv
```

Understand which branch is being tracked.

---

## Exercise 3 — Fork Workflow

Practice:

```text
Original repository
        ↓
Fork
        ↓
Your repository
        ↓
Clone
        ↓
Feature branch
        ↓
Push
        ↓
Pull Request
```

---

## Exercise 4 — Code Review

Create a PR in a practice repository.

Review it as if you were another developer.

Ask:

* Is the PR focused?
* Is the code understandable?
* Are the commits meaningful?
* Is there unnecessary code?
* Are tests included?
* Does the PR description explain the change?
* Can another developer understand why the change exists?

Then leave review comments, fix them, push again, and review the updated PR.

---

# Core Takeaway

Do not memorize GitHub buttons.

Understand this model:

```text
LOCAL REPOSITORY
       ↕
REMOTE-TRACKING BRANCHES
       ↕
REMOTE REPOSITORY
```

And this workflow:

```text
Branch
  ↓
Commit
  ↓
Push
  ↓
Pull Request
  ↓
Code Review
  ↓
Fix if needed
  ↓
Approval
  ↓
Merge
```

Once this model is clear, remote collaboration becomes much easier to understand.
