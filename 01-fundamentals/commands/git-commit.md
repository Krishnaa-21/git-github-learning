# ✅ Git Commit: Saving Your Changes

A complete reference for recording staged changes into your repository's history.

---

## 📂 What is `git commit`?

`git commit` takes everything in the staging area and saves it as a permanent snapshot in your repository's history, along with a message describing the change.

> 💡 **Pro-tip:** Commits are cheap and local. Commit often with small, focused changes rather than saving up one giant commit.

---

## 🚀 Basic Usage

```bash
# Commit staged changes with an inline message
git commit -m "Add user authentication endpoint"

# Commit with a longer, multi-line message (opens your default editor)
git commit
```

---

## ⚡ Shortcuts & Combos

```bash
# Stage all tracked, modified files AND commit in one step
# (does NOT include new untracked files)
git commit -am "Fix login validation bug"

# Add a more detailed commit message with a title and body
git commit -m "Fix login bug" -m "Validation failed on empty password field; added null check."
```

> ⚠️ **Warning:** `git commit -am` skips `git add` for *modified* and *deleted* files only — new untracked files will NOT be included. Use `git add -A` first if you need everything.

---

## ✏️ Amending Commits

```bash
# Fix the most recent commit's message
git commit --amend -m "Corrected commit message"

# Add forgotten changes to the previous commit (keeps same message)
git add forgotten-file.js
git commit --amend --no-edit
```

> ⚠️ **Warning:** Never amend a commit that's already been pushed and shared with others — it rewrites history and will cause conflicts for collaborators.

---

## 📜 Writing Good Commit Messages

```bash
# Recommended format:
# <type>: <short summary, 50 chars or less>
#
# <optional longer description, wrapped at 72 chars>

git commit -m "feat: add password reset flow"
git commit -m "fix: resolve race condition in payment webhook"
git commit -m "docs: update README with setup instructions"
```

> 📝 **Note:** Common prefixes: `feat`, `fix`, `docs`, `refactor`, `test`, `chore`. This is the basis of the widely-used [Conventional Commits](https://www.conventionalcommits.org/) standard.

---

## 🔍 Verifying a Commit

```bash
# View the most recent commit's details
git show HEAD

# Confirm the working directory is now clean
git status
```

---

## 📋 Quick Reference

| Action | Command | Purpose |
|---|---|---|
| ✅ Commit with message | `git commit -m "message"` | Saves staged changes with a description |
| ⚡ Stage tracked + commit | `git commit -am "message"` | Commits modified/deleted tracked files in one step |
| 📝 Title + body message | `git commit -m "title" -m "body"` | Adds a detailed multi-part commit message |
| ✏️ Edit last message | `git commit --amend -m "new message"` | Rewrites the most recent commit's message |
| ➕ Add to last commit | `git commit --amend --no-edit` | Adds staged changes to previous commit, keeps message |
| 🔍 View last commit | `git show HEAD` | Displays full details of the latest commit |

---