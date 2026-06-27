# 📝 Git Add: Staging Changes

A complete reference for moving changes from your working directory into Git's staging area.

---

## 📂 What is `git add`?

`git add` moves changes — new files, edits, or deletions — into the **staging area** (also called the "index"), preparing them to be included in your next commit.

> 💡 **Pro-tip:** Staging is a deliberate checkpoint. It lets you build a commit piece by piece instead of committing *everything* you've changed at once.

---

## 🚀 Basic Usage

```bash
# Stage a single file
git add index.js

# Stage multiple specific files
git add index.js style.css

# Stage all changes in the current directory and subdirectories
git add .

# Stage all changes in the entire repository (run from anywhere inside it)
git add -A
```

---

## 🎯 Selective Staging

```bash
# Stage all files matching a pattern
git add *.js

# Stage an entire folder
git add src/

# Interactively choose which changes (hunks) to stage
git add -p
```

> 📝 **Note:** `git add -p` (patch mode) lets you stage **part** of a file's changes — perfect for splitting unrelated edits into separate, clean commits.

---

## 🔄 Staging Updates vs. New Files

```bash
# Stage only modified/deleted tracked files (ignores new untracked files)
git add -u

# Stage everything: new, modified, and deleted files
git add -A
```

> ⚠️ **Warning:** `git add .` (without `-A`) only stages files within the current directory and below — it won't catch changes elsewhere in the repo if you're in a subfolder.

---

## 🔍 Verifying What's Staged

```bash
# Check what's staged vs. unstaged
git status

# See the exact diff of staged changes
git diff --staged
```

---

## ↩️ Undoing a Stage

```bash
# Unstage a specific file (keeps your edits intact)
git restore --staged index.js

# Unstage everything
git restore --staged .
```

> 💡 **Pro-tip:** Older Git versions use `git reset HEAD <file>` to unstage — `git restore --staged` is the modern equivalent (Git 2.23+).

---

## 📋 Quick Reference

| Action | Command | Purpose |
|---|---|---|
| 📄 Stage one file | `git add <file>` | Adds a specific file to staging |
| 📁 Stage current dir | `git add .` | Stages all changes in the current directory |
| 🌐 Stage everything | `git add -A` | Stages all changes repo-wide |
| ✏️ Stage tracked only | `git add -u` | Stages modified/deleted files, skips new untracked ones |
| 🧩 Stage interactively | `git add -p` | Lets you pick specific hunks to stage |
| 🔍 Check staged diff | `git diff --staged` | Shows exact changes that will be committed |
| ↩️ Unstage a file | `git restore --staged <file>` | Removes file from staging without losing edits |

---