# Git Add & Commit — Professional Learning Notes

## Overview

In Git, saving work happens in two important stages:

1. **git add** → moves changes to the staging area
2. **git commit** → permanently saves staged changes in Git history

These are among the most frequently used Git commands in daily development workflows.

---

# 1. Git Add

## Definition

`git add` moves modified, new, or deleted files into Git’s **staging area**.

The staging area acts like a preparation zone before creating a commit.

Think of it as:

> "Select exactly what should be included in the next save point."

---

## Syntax

### Add specific file

```bash
git add filename