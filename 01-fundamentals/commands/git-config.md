# ⚙️ Git Config: Configuring Git Settings

A complete reference for setting up and managing your Git identity and preferences.

---

## 📂 What is `git config`?

`git config` lets you get and set configuration values that control Git's behavior — your identity, default editor, aliases, and more — at the **system**, **global**, or **local (repo)** level.

> 📝 **Note:** Configuration levels override in this order: **local** > **global** > **system**. Local (per-repo) settings always take priority.

---

## 🚀 Essential First-Time Setup

```bash
# Set your name (used in commits)
git config --global user.name "Jane Doe"

# Set your email (must match your GitHub account for contributions to count)
git config --global user.email "jane@example.com"

# Verify your settings
git config --global user.name
git config --global user.email
```

> ⚠️ **Warning:** Always run this before your first commit. Commits made without identity config will use generic system defaults and may not attribute properly on GitHub.

---

## 🌐 Configuration Levels

```bash
# System-wide config (applies to all users on the machine)
git config --system user.name "Jane Doe"

# Global config (applies to all repos for the current user)
git config --global user.name "Jane Doe"

# Local config (applies only to the current repository)
git config user.name "Jane Doe"
```

---

## 🎨 Useful Preferences

```bash
# Set your default branch name for new repos
git config --global init.defaultBranch main

# Set your default text editor for commit messages
git config --global core.editor "code --wait"   # VS Code
git config --global core.editor "vim"           # Vim

# Enable colored output in the terminal
git config --global color.ui auto

# Set default pull behavior to avoid merge commit ambiguity
git config --global pull.rebase false
```

---

## ⚡ Creating Aliases

```bash
# Shorten common commands
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.st status
git config --global alias.cm "commit -m"

# Now you can use:
git st        # instead of git status
git cm "fix"  # instead of git commit -m "fix"
```

> 💡 **Pro-tip:** Aliases are stored in your `~/.gitconfig` file and can be as simple or complex as you like — even chaining multiple Git commands together.

---

## 🔍 Viewing & Editing Config

```bash
# List all current settings and where they come from
git config --list --show-origin

# Open your global config file directly in your editor
git config --global --edit

# Remove a specific setting
git config --global --unset user.name
```

---

## 📋 Quick Reference

| Action | Command | Purpose |
|---|---|---|
| 👤 Set name | `git config --global user.name "Name"` | Sets commit author name |
| 📧 Set email | `git config --global user.email "email"` | Sets commit author email |
| 🌿 Set default branch | `git config --global init.defaultBranch main` | Sets default branch for new repos |
| 📝 Set editor | `git config --global core.editor "editor"` | Sets default editor for commit messages |
| ⚡ Create alias | `git config --global alias.<name> "<command>"` | Creates a shortcut for a Git command |
| 🔍 List all settings | `git config --list --show-origin` | Shows all config values and their source files |
| ❌ Remove a setting | `git config --global --unset <key>` | Deletes a specific configuration value |

---