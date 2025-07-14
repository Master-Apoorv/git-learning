# 🚀 Git Learning Journey Report

This document summarizes my progress, insights, challenges, and technical learnings from the comprehensive Git Fundamentals assignment. It spans setting up Git, mastering local and remote operations, branching strategies, collaboration workflows, conflict resolution, and repository management.

---

## 📝 1. Progress Report

### Week Overview
The assignment was divided into thematic sections, each focusing on a different aspect of Git. Through hands-on tasks in VS Code and Git Bash, I transitioned from basic usage to advanced Git operations such as rebasing, branching strategy design, remote integrations, and troubleshooting.

### Key Accomplishments

- **Environment Setup**: Installed Git, configured user identity, and set up VS Code as the default editor.
- **Local Repository Initialization**: Initialized `git_learning` repository with folder structure (`src/`, `docs/`, `tests/`, `README.md`).
- **Staging & Committing**: Learned granular staging, meaningful commit messaging, and inspection using `git status`, `git diff`, and `git log`.
- **Branch Management**: Created feature and bugfix branches, followed naming conventions, and managed merges including conflict resolution.
- **Remote Integration**: Linked local repository to GitHub, pushed branches, and practiced multi-device workflows using fetch and pull.
- **Collaboration Simulation**: Practiced pull request workflow, reviews, branch protection, and etiquette.
- **Advanced Operations**: Used rebase interactively to squash and reorder commits, created aliases for productivity, and cleaned up large repositories.
- **Troubleshooting**: Simulated detached HEAD, binary merge conflicts, and used `git reflog` and `git bisect` for recovery and debugging.
- **Documentation**: Created cheat sheets, branching strategy guides, troubleshooting manuals, and daily summaries.

---

## ⚙️ 2. Git Command Log (with Explanations)

| Command | Purpose |
|--------|---------|
| `git init` | Create a new repository |
| `git config --global user.name "Your Name"` | Set global username |
| `git config --global user.email "email@example.com"` | Set global email |
| `git config --global core.editor "code --wait"` | Set VS Code as editor |
| `git add <file>` | Stage changes |
| `git add -p` | Selectively stage changes |
| `git commit -m "message"` | Save staged changes |
| `git status` | Check current state of working directory |
| `git diff` | View unstaged differences |
| `git log` | Show commit history |
| `git log --oneline --graph --decorate` | Visual summary of history |
| `git branch` | List local branches |
| `git branch -a` | List all branches including remotes |
| `git checkout <branch>` | Switch branches |
| `git checkout -b <new-branch>` | Create and switch to new branch |
| `git merge <branch>` | Merge changes |
| `git revert <commit>` | Undo a commit safely (creates a new one) |
| `git reset --hard HEAD~1` | Remove last commit forcefully |
| `git rm <file>` | Delete file from working directory and stage removal |
| `git clean -n` | Preview which untracked files will be removed |
| `git clean -f` | Delete untracked files |
| `git remote add origin <URL>` | Link local repo to GitHub |
| `git push -u origin main` | Push main branch to GitHub |
| `git fetch` | Get updates from remote without merging |
| `git pull` | Fetch + merge updates from remote |
| `git rebase -i HEAD~n` | Interactively rebase last n commits |
| `git reflog` | Recover lost commits and branches |
| `git bisect start` | Begin binary search for bugs |
| `git bisect bad` / `git bisect good` | Mark commits during bisect |
| `git alias.st status` | Alias for `status` |
| `git fsck` | Check repository integrity |
| `git gc --prune=now` | Garbage collection of unused data |
| `git blame <file>` | Show commit history per line |
| `git show <commit>` | Display commit details |

---

## 🧩 3. Problem Log

### Problem: Merge Conflict During Feature Merge
**Context**: While merging `feature/footer` into `main`, both branches had modified the same lines in `style.css`.

**Solution**:
- Used CLI to manually resolve conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`).
- Verified resolution using `git status`, then committed fix.
- Documented fix in `docs/merge-conflicts.md`.

---

### Problem: Detached HEAD State
**Context**: Accidentally checked out a previous commit instead of a branch.

**Solution**:
- Verified detached state with `git status`.
- Recovered changes using `git checkout -b temp-fix`.

---

### Problem: Committed Sensitive `.env` File
**Context**: `.env` was added and pushed unintentionally.

**Solution**:
- Removed using `git filter-branch --force` (experimented locally).
- Updated `.gitignore` to include `.env`.
- Documented safety protocols in `docs/security-best-practices.md`.

---

### Problem: Accidental `git reset`
**Context**: Used `reset --hard` on wrong branch, lost recent commits.

**Solution**:
- Used `git reflog` to find lost commit.
- Restored using `git checkout <commit>` and `git checkout -b recovered-work`.

---

### Problem: Binary Conflict During Image Merge
**Context**: Modified binary `.png` in two branches and attempted a merge.

**Solution**:
- Replaced with one version manually.
- Committed fix and added note to avoid simultaneous binary edits.

---

### Problem: Repository Bloated by Log Files
**Context**: Git tracked `.log` files growing in size.

**Solution**:
- Added `*.log` to `.gitignore`.
- Removed tracked logs using `git rm --cached`.
- Run `git gc --prune=now` to clean repo.

---

## 🪞 4. Reflection

### Challenges Faced

- **Understanding Reset vs Revert**: Differentiating destructive vs non-destructive undo methods was tricky initially.
- **Conflict Resolution**: My first merge conflict felt intimidating, especially dealing with multiple versions of the same file.
- **Remote Collaboration**: Simulating multiple users across machines required careful branch syncing and pull request workflows.
- **Rebase vs Merge**: It was challenging to determine when to rebase for cleaner history vs when to merge for traceability.
- **Performance Optimization**: Learning tools like `git fsck`, pruning, and garbage collection demanded patience and experimentation.

### Skills Mastered

- **Clean and Semantic Commit Practices**: I adopted conventional commit messages (`feat`, `fix`, `chore`, `docs`) which helped maintain clarity.
- **Branching Strategies**: I now consistently use `feature/`, `bugfix/`, and `hotfix/` prefixes to organize work efficiently.
- **Conflict Navigation**: Conflicts became opportunities to understand collaborative dynamics and code ownership.
- **Troubleshooting Confidence**: Tools like `reflog` and `bisect` empowered me to recover and debug confidently.
- **Documentation Mindset**: Writing markdown guides and summaries not only reinforced my learning but also laid the foundation for team knowledge sharing.

---

## 📚 Final Thoughts

This assignment transformed Git from a checklist into a mindset. It’s not just about commands—it’s about habits, clarity, collaboration, and precision. Whether managing solo projects or contributing to open source, Git now feels like a natural extension of my coding workflow. I’m more confident not only in using Git but also in teaching and troubleshooting it.

I'm proud of the structured, documented, and recoverable journey I’ve built using Git. The road was full of forks—literally and figuratively—and I’m ready for whatever branching path comes next.
