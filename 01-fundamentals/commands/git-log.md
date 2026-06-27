# 📜 Git Log: Viewing Commit History

A complete reference for exploring and navigating your repository's commit history.

---

## 📂 What is `git log`?

`git log` displays the commit history of your repository — author, date, message, and commit hash — in reverse chronological order (newest first).

> 💡 **Pro-tip:** `git log` opens in a pager (like `less`) by default. Press `q` to exit, and use arrow keys or `space` to scroll.

---

## 🚀 Basic Usage

```bash
# Show full commit history
git log

# Show a condensed, one-line-per-commit view
git log --oneline

# Limit to the last N commits
git log -5
```

---

## 🎨 Pretty & Visual Formats

```bash
# Show a compact, graphical branch history
git log --oneline --graph --all

# Customize the output format
git log --pretty=format:"%h - %an, %ar : %s"
```

> 📝 **Note:** `%h` = short hash, `%an` = author name, `%ar` = relative date, `%s` = subject line. Combine these freely to build your ideal log format.

---

## 🔍 Filtering History

```bash
# Show commits by a specific author
git log --author="Jane Doe"

# Show commits within a date range
git log --since="2 weeks ago" --until="yesterday"

# Show commits that touched a specific file
git log -- path/to/file.js

# Search commit messages for a keyword
git log --grep="bugfix"
```

---

## 🔬 Inspecting Changes

```bash
# Show the diff introduced by each commit
git log -p

# Show a summary of files changed per commit (added/removed lines)
git log --stat
```

> ⚠️ **Warning:** `git log -p` can produce very long output on large histories. Combine it with `-n` (e.g. `git log -p -3`) to limit scope.

---

## 🌳 Visualizing Branches

```bash
# Graph view across all branches with one-line commits
git log --graph --oneline --all --decorate
```

> 💡 **Pro-tip:** Add this as a Git alias for quick access:
> ```bash
> git config --global alias.tree "log --graph --oneline --all --decorate"
> ```
> Then just run `git tree`.

---

## 📋 Quick Reference

| Action | Command | Purpose |
|---|---|---|
| 📜 Full history | `git log` | Shows complete commit history |
| 📝 Compact view | `git log --oneline` | One line per commit |
| 🌳 Graph view | `git log --graph --oneline --all` | Visualizes branch structure |
| 👤 Filter by author | `git log --author="name"` | Shows commits from a specific person |
| 📅 Filter by date | `git log --since="date" --until="date"` | Limits history to a date range |
| 🔎 Search messages | `git log --grep="keyword"` | Finds commits matching a keyword |
| 🔬 Show diffs | `git log -p` | Displays the actual code changes per commit |
| 📊 Show stats | `git log --stat` | Shows file change summary per commit |

---