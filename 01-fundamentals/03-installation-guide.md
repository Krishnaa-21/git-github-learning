# 🛠️ Git Installation Guide

Welcome! 🎉

Before we start learning Git, we need to install it on our machine.

Don't worry — the process is simple and takes only a few minutes.

---

# 🎯 What You'll Achieve

After completing this guide, you'll be able to:

✅ Install Git

✅ Verify the installation

✅ Configure your identity

✅ Check that Git is working correctly

---

# 💻 Installing Git on Windows

### Step 1: Download Git

Visit the official Git website:

https://git-scm.com/downloads

Git will usually detect your operating system automatically.

Download the latest stable version.

---

### Step 2: Run the Installer

Double-click the downloaded installer.

During installation:

✅ Keep most options as default

✅ Click **Next** until installation completes

✅ Click **Install**

For beginners, the default settings are perfectly fine.

---

### Step 3: Verify Installation

Open:

```text
Command Prompt
```

or

```text
PowerShell
```

Run:

```bash
git --version
```

Example output:

```bash
git version 2.50.1
```

🎉 Congratulations! Git is installed successfully.

---

# 🐧 Installing Git on Linux (Ubuntu/Debian)

Update package information:

```bash
sudo apt update
```

Install Git:

```bash
sudo apt install git -y
```

Verify installation:

```bash
git --version
```

Example:

```bash
git version 2.50.1
```

---

# 🍎 Installing Git on macOS

Using Homebrew:

```bash
brew install git
```

Verify:

```bash
git --version
```

Example:

```bash
git version 2.50.1
```

---

# 👤 Configure Your Identity

Git needs to know who is making commits.

Set your username:

```bash
git config --global user.name "Your Name"
```

Example:

```bash
git config --global user.name "Krishna Prajapat"
```

---

Set your email:

```bash
git config --global user.email "your-email@example.com"
```

Example:

```bash
git config --global user.email "krishna@example.com"
```

---

# 🔍 Verify Configuration

Check your settings:

```bash
git config --list
```

You should see something similar:

```text
user.name=Krishna Prajapat
user.email=krishna@example.com
```

---

# 📁 Create Your First Git Workspace

Create a practice directory:

```bash
mkdir git-playground
cd git-playground
```

Initialize Git:

```bash
git init
```

Expected output:

```text
Initialized empty Git repository
```

🎉 Your first Git repository is ready.

---

# 🧪 Quick Health Check

Run:

```bash
git status
```

Expected output:

```text
On branch main

No commits yet

nothing to commit
```

If you see this message, Git is working correctly.

---

# 🚨 Common Beginner Problems

### ❌ git: command not found

Cause:

Git is not installed or not added to PATH.

Solution:

* Restart terminal
* Reinstall Git
* Verify installation again

---

### ❌ Wrong Username or Email

Check current values:

```bash
git config --global user.name
git config --global user.email
```

Update them if needed:

```bash
git config --global user.name "New Name"
git config --global user.email "new@email.com"
```

---

### ❌ Terminal Doesn't Recognize Git

Try:

```bash
git --version
```

If it fails:

* Restart your machine
* Reinstall Git
* Ensure Git is added to PATH

---

# 📌 Pro Tip

Many beginners install Git and immediately start memorizing commands.

Don't do that.

First understand:

* Why Git exists
* What problem it solves
* How the Git workflow works

Commands become much easier when the concepts are clear.

---

# ✅ Checklist

Before moving to the next chapter, make sure:

* [ ] Git Installed
* [ ] Git Version Verified
* [ ] Username Configured
* [ ] Email Configured
* [ ] Practice Folder Created
* [ ] First Repository Initialized
* [ ] `git status` Working

If all boxes are checked, you're ready to start your Git journey 🚀
