# 🔍 Git Status: Checking Your Repository State

A complete reference for understanding and using `git status` to inspect the current state of your working directory and staging area.

---

## 📂 What is `git status`?

`git status` shows you the current state of your repository — which branch you're on, which files are staged, modified, or untracked, and whether you're ahead/behind the remote.

> 💡 **Pro-tip:** `git status` is a **read-only** command. It never changes your repository, so run it as often as you like to stay oriented.

---

## 🚀 Basic Usage

```bash
# Show the full status of the working directory
git status
```

Typical output:

On branch main

Your branch is up to date with 'origin/main'.
Changes not staged for commit:

(use "git add <file>..." to update what will be committed)

modified:   index.js
Untracked files:

(use "git add <file>..." to include in what will be committed)

notes.txt

---

## 📝 Short Format Output

For a more compact, scannable view:

```bash
# Show status in short format
git status -s
```

```bash
# Short format with branch info included
git status -sb
```

Example output:
main...origin/main
M index.js

?? notes.txt

> 📝 **Note:** Status codes explained — `M` = modified, `A` = added, `D` = deleted, `R` = renamed, `??` = untracked, `!!` = ignored.

---

## 🧹 Filtering and Customizing Output

```bash
# Show status but ignore untracked files
git status --untracked-files=no

# Show status including ignored files
git status --ignored

# Show status for a specific file or folder only
git status -- path/to/file.js
```

> ⚠️ **Warning:** `--ignored` can produce a lot of noise in projects with large `node_modules` or build folders. Use it only when you specifically need to debug your `.gitignore` rules.

---

## 🔎 Understanding the Three States

| State | Meaning |
|---|---|
| **Untracked** | File exists but Git isn't tracking it yet |
| **Staged** (added) | File is marked to be included in the next commit |
| **Modified** (unstaged) | Tracked file has changes not yet staged |

```bash
# Example workflow showing state transitions
echo "hello" > file.txt   # Untracked
git add file.txt          # Now staged
echo "more" >> file.txt   # Now both staged AND modified
git status                # Shows file in both sections
```

---

## 🌳 Checking Branch & Sync Status

`git status` also tells you how your branch compares to its remote counterpart:
Your branch is ahead of 'origin/main' by 2 commits.

(use "git push" to publish your local commits)

```bash
# Refresh remote tracking info first for accurate comparison
git fetch
git status
```

> 💡 **Pro-tip:** Run `git fetch` before `git status` if you want an up-to-date comparison against the remote — `git status` alone only checks against your last fetched data, not live remote state.

---

## 📋 Quick Reference

| Action | Command | Purpose |
|---|---|---|
| 🔍 Full status check | `git status` | Shows branch, staged, modified, and untracked files |
| 📝 Compact view | `git status -s` | Shows a short, symbol-based summary |
| 🌿 Compact + branch info | `git status -sb` | Short format including branch/tracking info |
| 🚫 Hide untracked files | `git status --untracked-files=no` | Limits output to tracked file changes only |
| 🗑️ Show ignored files | `git status --ignored` | Reveals files excluded via `.gitignore` |
| 📁 Check specific path | `git status -- path/to/file` | Limits status check to a file or folder |
| 🔄 Sync before checking | `git fetch && git status` | Ensures accurate ahead/behind comparison with remote |

---