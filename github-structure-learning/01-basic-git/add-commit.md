# Git Add and Commit

## Introduction

In Git, tracking changes is a two-step process. Before changes become part of the project history, they must first be staged and then committed.

The `git add` and `git commit` commands are fundamental to daily development workflows and are used in almost every Git-based project.

## Git Add

The `git add` command is used to stage changes. Staging means selecting specific files or modifications that should be included in the next commit.

This gives developers control over what gets saved in project history.

### Syntax

```bash
git add <file-name>

Example:

git add README.md

To stage all current changes:

git add .

```

Practical Example

```bash

Create a new file:

touch app.py

Check repository status:

git status

Expected output:

Untracked files:
  app.py

Stage the file:

git add app.py

Check status again:

git status

Expected output:

Changes to be committed:
  new file: app.py

  ```

This confirms that the file has moved from the working directory to the staging area.


## Git Commit

The git commit command saves staged changes permanently in Git history.

Think of a commit as a project checkpoint or snapshot.

Syntax
```bash

git commit -m "commit message"

Example:

git commit -m "Add application entry file"
Practical Example

After staging files:

git add app.py

Create a commit:

git commit -m "Add app.py file"

Expected output:

1 file changed
create mode 100644 app.py
 ```

This means Git has successfully recorded the changes.

## Git Workflow

A standard Git workflow follows this sequence:
```bash
Working Directory → Staging Area → Repository History
```
Explanation:

Working Directory: Where files are created or modified
Staging Area: Where selected changes are prepared
Repository History: Where committed changes are permanently stored

## Difference Between Git Add and Git Commit

| Command      | Purpose                                         |
| ------------ | ----------------------------------------------- |
| `git add`    | Selects and stages changes for the next commit  |
| `git commit` | Saves staged changes permanently in Git history |

## Common Commands

Stage a single file:
```bash
git add README.md
```
Stage all changes:
```bash
git add .
```
Commit staged changes:
```bash
git commit -m "Add project documentation"
```
View commit history:
```bash
git log
```