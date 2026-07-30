# Git Recovery Notes

> Recovery is one of Git's strongest features. Most mistakes are recoverable because Git usually moves **references**, not the underlying **commit objects**. The first tool to use after almost any Git mistake is **`git reflog`**.

---

# 1. Reflog

## What is Reflog?

`git reflog` records the history of where **HEAD** and branch references have pointed over time.

Unlike `git log`, reflog includes commits that are no longer reachable from any branch.

Think of it as:

> Git's local diary.

---

## What Reflog Records

- Commits
- Checkouts
- Switches
- Resets
- Rebases
- Merges
- Pulls
- Branch movements

---

## View Reflog

```bash
git reflog
```

Example:

```text
28c8ff2 HEAD@{0}: commit: Added Login
ce4557d HEAD@{1}: reset: moving to HEAD~1
11b1cc9 HEAD@{2}: checkout: moving from feature to main
```

---

## Understanding `HEAD@{n}`

```
HEAD@{0} → Current HEAD

HEAD@{1} → Previous HEAD position

HEAD@{2} → Position before that
```

These represent **previous positions of HEAD**, not commit numbers.

---

## Recover Using Reflog

Create a recovery branch:

```bash
git switch -c recovered HEAD@{1}
```

Move current branch:

```bash
git reset --hard HEAD@{1}
```

Recover by commit hash:

```bash
git switch -c recovered <commit-hash>
```

---

## Important Notes

- Reflog is **local only**
- Not pushed to GitHub
- Usually keeps:
    - Reachable entries → ~90 days
    - Unreachable entries → ~30 days
- Eventually cleaned by Git Garbage Collection

---

# 2. Recover Lost Commits

## What is a Lost Commit?

A commit is considered "lost" when:

- No branch points to it
- No tag points to it

The commit object usually still exists.

Example:

Before

```text
A → B → C → D
```

After

```bash
git reset --hard B
```

History becomes

```text
A → B
```

Commits C and D are now unreachable but still recoverable.

---

## Common Causes

- Hard reset
- Deleted branch
- Bad rebase
- Force-moving a branch

---

## Recovery Steps

View reflog

```bash
git reflog
```

Recover safely

```bash
git switch -c recovered HEAD@{1}
```

Or

```bash
git switch -c recovered <commit-hash>
```

---

## Best Practice

Recover to a **new branch first**.

Inspect the recovered history before resetting any important branch.

---

# 3. Recover Deleted Branches

## Important Concept

A branch is only a **pointer**.

Deleting a branch deletes the pointer—not the commits.

---

## Safe Delete

```bash
git branch -d feature
```

Deletes only if the branch has already been merged.

---

## Force Delete

```bash
git branch -D feature
```

Deletes the branch even if it contains unmerged commits.

`-D` = Force delete

---

## Recover Deleted Branch

Find the last commit:

```bash
git reflog
```

Recreate the branch:

```bash
git switch -c feature <commit-hash>
```

or

```bash
git branch feature <commit-hash>
git switch feature
```

---

## Important Rule

Recover a branch from its **latest (tip) commit**, not its first commit.

Git automatically restores the earlier commits through the parent chain.

---

## Useful Command

View a branch's reflog:

```bash
git reflog show feature
```

If reflog is unavailable:

```bash
git fsck --lost-found
```

Searches for dangling commits.

---

# 4. Recover After Hard Reset

## What Does `git reset --hard` Change?

It resets three things:

1. Branch pointer (HEAD)
2. Staging Area (Index)
3. Working Directory

Everything becomes identical to the target commit.

---

## Example

Before

```text
A → B → C → D
```

Run

```bash
git reset --hard B
```

Result

```text
A → B
```

Commits C and D still exist until Garbage Collection removes them.

---

## Recover

View reflog

```bash
git reflog
```

Recover safely

```bash
git switch -c recovered HEAD@{1}
```

Or restore current branch

```bash
git reset --hard HEAD@{1}
```

---

## Very Important

Committed work:

✅ Usually recoverable

Uncommitted work:

❌ Usually lost forever after `git reset --hard`

Always commit or stash important changes before using `--hard`.

---

# 5. Recover After Bad Rebase

## What is a Bad Rebase?

Examples:

- Dropped wrong commit
- Squashed wrong commits
- Edited wrong commit
- Incorrect conflict resolution
- Finished rebase with incorrect history

---

## Important Concept

Rebase creates **new commits**.

Old commits usually still exist for some time.

Example

Before

```text
A → B → C → D → E
```

After dropping C

```text
A → B → D' → E'
```

`D'` and `E'` are new commits.

---

## If Rebase Is Still Running

Continue

```bash
git rebase --continue
```

Skip current commit

```bash
git rebase --skip
```

Abort

```bash
git rebase --abort
```

`--abort` works **only while the rebase is in progress**.

---

## If Rebase Has Finished

Use reflog.

```bash
git reflog
```

Recover safely

```bash
git switch -c recovered HEAD@{n}
```

Restore current branch

```bash
git reset --hard HEAD@{n}
```

---

# Common Recovery Workflow

Whenever you think you've lost work:

## Step 1

Don't panic.

---

## Step 2

View reflog.

```bash
git reflog
```

---

## Step 3

Find the commit before the mistake.

---

## Step 4

Recover safely.

```bash
git switch -c recovered HEAD@{n}
```

---

## Step 5

Inspect the recovered branch.

If everything looks correct:

- Continue working there
- Merge it
- Cherry-pick commits
- Reset your original branch

---

# Commands Cheat Sheet

## Reflog

```bash
git reflog
```

---

## Create recovery branch

```bash
git switch -c recovered HEAD@{1}
```

---

## Recover from commit hash

```bash
git switch -c recovered <commit-hash>
```

---

## Hard reset

```bash
git reset --hard HEAD~2
```

---

## Restore branch

```bash
git reset --hard HEAD@{1}
```

---

## Safe branch delete

```bash
git branch -d feature
```

---

## Force branch delete

```bash
git branch -D feature
```

---

## Create branch

```bash
git switch -c feature
```

---

## Create branch from commit

```bash
git switch -c feature <commit-hash>
```

---

## Continue rebase

```bash
git rebase --continue
```

---

## Skip current commit

```bash
git rebase --skip
```

---

## Abort rebase

```bash
git rebase --abort
```

---

## Find dangling commits

```bash
git fsck --lost-found
```

---

# Key Takeaways

- `git reflog` is your first recovery tool.
- Most Git mistakes move references rather than deleting commits.
- Recover to a **new branch first** whenever possible.
- A branch is only a pointer.
- `git reset --hard` changes the branch pointer, index, and working directory.
- Committed work is usually recoverable.
- Uncommitted work is usually **not** recoverable after a hard reset.
- `git rebase --abort` only works while a rebase is still running.
- After a completed rebase, use `git reflog` to recover.
- Don't panic—Git is designed to make many mistakes recoverable.