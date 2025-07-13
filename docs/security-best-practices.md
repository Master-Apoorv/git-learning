# 🛠️ Git Troubleshooting Guide

A practical reference for navigating Git's quirks and complexities. This guide covers common problems, emergency recovery steps, performance tips, and essential security practices.

---

## 🧩 Common Problems and Solutions

### 1. Merge Conflicts
**Problem**: Conflicting changes between branches.
**Solution**:
- Use `git status` to locate conflicted files.
- Edit files to resolve conflicts manually.
- Mark files as resolved: `git add <file>`
- Continue with `git merge --continue` or `git rebase --continue`.

### 2. Detached HEAD
**Problem**: You're in a state where HEAD points to a commit instead of a branch.
**Solution**:
- Create a branch to keep changes: `git checkout -b temp-fix`
- Avoid working without branching in the future.

### 3. Accidentally Committed Sensitive Info
**Problem**: Secrets added in a commit.
**Solution**:
- Remove the file from history:
```bash
git filter-branch --force --index-filter \
"git rm --cached --ignore-unmatch path/to/secret.txt" \
--prune-empty --tag-name-filter cat -- --all