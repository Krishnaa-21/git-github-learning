# 📦 Git Add and Commit

<div align="center">

![Git](https://img.shields.io/badge/GIT-E44C30?style=for-the-badge&logo=git&logoColor=white)
![Markdown](https://img.shields.io/badge/Markdown-000000?style=for-the-badge&logo=markdown&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)

</div>

## 📖 Introduction

In Git, tracking changes is a two-step process. Before changes become part of the project history, they must first be **staged** and then **committed**.

The `git add` and `git commit` commands are fundamental to daily development workflows and are used in almost every Git-based project.

---

## ➕ Git Add

<div align="center">

![Git Add](https://img.shields.io/badge/Git-Add-orange?style=flat-square&logo=git)

</div>

The `git add` command is used to **stage changes**. Staging means selecting specific files or modifications that should be included in the next commit.

This gives developers control over what gets saved in project history.

### 📝 Syntax

```bash
git add <file-name>
```

Example:
```bash
git add README.md
```
To stage all current changes:
```bash

git add .
```

💡 Practical Example
```bash
# Create a new file:
touch app.py
```

# Check repository status:
```bash
git status
```

Expected output:

text

Untracked files:
  app.py
```bash
# Stage the file:
git add app.py

# Check status again:
git status
```
Expected output:

text

Changes to be committed:
  new file: app.py

# ✔️ Git Commit
<div align="center"><img src="https://img.shields.io/badge/Git-Commit-success?style=flat-square&logo=git" /></div>
The git commit command saves staged changes permanently in Git history.
📝 Syntax
```bash

git commit -m "commit message"
```
Example:

```bash

git commit -m "Add application entry file"
```
💡 Practical Example
```bash

# After staging files:
git add app.py

# Create a commit:
git commit -m "Add app.py file"
```
Expected output:

```text

1 file changed
create mode 100644 app.py
✅ This means Git has successfully recorded the changes.
```

# 🔄 Git Workflow
<div align="center"><img src="https://img.shields.io/badge/Git-Workflow-blue?style=for-the-badge&logo=git" /></div>
A standard Git workflow follows this sequence:

```text

📁 Working Directory → 📋 Staging Area → 📚 Repository History
🔍 Explanation:
📁 Working Directory: Where files are created or modified
📋 Staging Area: Where selected changes are prepared
📚 Repository History: Where committed changes are permanently stored
```