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

##

Practical Example

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

This confirms that the file has moved from the working directory to the staging area.