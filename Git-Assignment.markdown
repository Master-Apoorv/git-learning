# This is Git Assignment

# Section 1: Foundation & Local Repository

## Task 1.1: Environment Setup & Configuration
![Setup and repo creation-1](image.png)

![Setup and repo creation-2](image-1.png)

## Task 1.2: Basic File Operations
![alt text](image-2.png)
![alt text](image-3.png)

### Git Status

![alt text](image-4.png)

### Git Diff

![alt text](image-5.png)


![alt text](image-6.png)

## Task 1.3: History and Undoing Changes

### 1. git log --oneline
![git_log](image-7.png)

### 2. git log --graph
![git log --graph](image-8.png)

### 3. git log --decorate
![alt text](image-9.png)

### Undoing Changes

Command - git revert head
![git revert](image-10.png)

## Task 1.4 - File Management

#### Creating .gitignore file
![alt text](image-12.png)

#### File Removal

##### a. Added Temp File
![alt text](image-13.png)
##### b. Remove Via Git
![alt text](image-14.png)
##### c. Clean untracked files
![alt text](image-15.png)

## Task 1.5 : Document `git cheat sheet` created and saved in `docs`

## My Learning in Task 1
### In this task I learned basic Git oprations like creating repository. Challenging thing for me was to learn these commands but I managed it my practicing and making a cheat sheet to look again and again and praticing it.

-----------------------------
------------------------
# Section 2: Branching & Merging Mastery

## Task 2.1: Branch Creation & Management

![alt text](image-19.png)
![alt text](image-16.png)
![alt text](image-17.png)
![alt text](image-18.png)


![alt text](image-20.png)
### A. Feature/navigation Branch

#### Changing branch and editing index.html
![alt text](image-21.png)
![alt text](image-22.png)
#### Editing and commint style.css
![alt text](image-23.png)

### B. feature/footer branch
#### Commit 1 - Editing footer
![alt text](image-16.png)
#### Commit 2 - Editing index.html again
![alt text](image-17.png)

### C. feature/contact-form Branch
#### Commit 1 - Editing Header
![alt text](image-18.png)
#### Commit 2 - Updating spelling
![alt text](image-19.png)

### D. bugfix/styling-issues Branch
#### Commit 1 - Edited style.css
![alt text](image-20.png)
#### Commit 2 - Modifying Padding
![alt text](image-24.png)

### Listing all branches
#### Using command `git branch -a`
![alt text](image-25.png)

## Task 2.2 Branching
### Process
#### 1. Find a commit from three commits ago on main
![alt text](image-26.png)
#### 2. Create a hotfix branch at that point
![alt text](image-27.png)
#### 3. Rename a poorly named branch and delete old branches
Renaming
![alt text](image-28.png)
Deleting Branch
A. Creation
![alt text](image-29.png)
B. Delete
![alt text](image-30.png)

## Task 2.3 Merging
### A. Merge feature/navigation into main
![alt text](image-34.png)
### B. Create two branches that both modify `src/style.css`
![alt text](image-30.png)
### C. Merge and observe conflict
#### Below is the message while merging
![alt text](image-35.png)
#### Merge Successful
![alt text](image-36.png)


## Task 2.4 Merging conflict
### Resolved the merging conflict
![alt text](image-31.png)
![alt text](image-32.png)
![alt text](image-33.png)

## Task 2.5 Git-Branching document in `docs` folder

##
### In this task I majorly learned about Branching and Merging. Branches have pattern and I learned its very imp. to be cautious while working on branching . I made a mistake that some of my work was not saved in main branch. So I quickly searched where that work is saved and because rest of work was same I overcome this challenge by merging the 2 branches this was I got my worka back.


---------------------------------
------------------------------------

# Section 3: Remote Repositories & GitHub Integration

## Task 3.1 - GitHub Repository Setup and Pushing all work
![alt text](image-37.png)
![alt text](image-38.png)

## Task 3.2: Cloning & Forking

### A. Clone to a fresh folder
![alt text](image-40.png)
![alt text](image-39.png)

### B. Fork and clone an open-source project

![alt text](image-51.png)
![alt text](image-49.png)


## Task 3.3: Collaboration Simulation

### Simulate multi-device workflow
#### On machine A
```
git checkout -b feature/deviceA
# make change, commit, push
git push origin feature/deviceA
```

#### On Machine B
```
git fetch origin
git checkout feature/deviceA
```

### Fetch v/s Pull
```
git fetch origin
git log HEAD..origin/main --oneline
git pull   # fetch + merge by default
```

## Task 3.4: Pull Request Workflow

### A. 
### Step 1: Create and switch to a new feature branch
`git checkout -b feature/my-enhancement`

### Step 2: Add and commit changes
`git add .`
`git commit -m "Implement feature: my enhancement"`

### Step 3: Push branch to origin
`git push origin feature/my-enhancement`

### B. Document etiquette in docs/pr-etiquette.md

## Task 3.5 --> Completed Same/Full Challenge in Task 5.2

## Learning in Section 3
### In this section I learned a lot about Remote repository and how to work with them. From setting up the repository to pushing to origin each and every step was full of learning.

-------------------------------------------------------------

# Section 4: Rebase & Productivity

## Task 4.1: Git Rebase
![alt text](image-52.png)

recently made branch -> indicated with green color code
![alt text](image-54.png)

`git rebase -i HEAD~4`
![alt text](image-53.png)


![alt text](image-55.png)
```
git checkout main
git merge feature/some-work --no-ff -m "merge with no-ff"
git checkout main
git reset --hard origin/main
git rebase feature/some-work
git log --oneline --graph

```

#### B. Rebase vs Merge document in `docs` named `rebase-vs-merge.md`.

## Task 4.2: Aliases & Productivity
![alt text](image-56.png)
![alt text](image-57.png)

## My Learnings
### This section taught me how to use git rebase to keep branch history clean and neat. I learned to manage rebase steps and saw how Git shows branch info with colors. Using no-ff merge helps track changes. I also used aliases to work faster and write commands more easily.


----------------------------------------------------------
-----------------------------------------------------------

# Section 5: Large Repository Management

## Task 5.1 - Simulate a Large Project
![alt text](image-58.png)

### Generate directories/files
![alt text](image-59.png)
![alt text](image-60.png)

### Extend .gitignore for IDE, OS files

### Selective staging
![alt text](image-61.png)

![alt text](image-62.png)
### A. Run garbage collection
![alt text](image-63.png)

### B. Prune unreachable objects and check health
![alt text](image-64.png)

## Task 5.2 - Team Collaboration Scenario

![alt text](image-65.png)
![alt text](image-42.png)
![alt text](image-43.png)
![alt text](image-44.png)
![alt text](image-45.png)
![alt text](image-46.png)
![alt text](image-47.png)
![alt text](image-48.png)

### File Structure
![alt text](image-41.png)

### Work Commited By Me
![alt text](image-67.png)

### Pull Request Accepted
![alt text](image-66.png)

## My Learning from this section
### In this section I learned about working in a team to manage a repository on github using git. Here I implemented the git concepts of remote repository , pushing code and creating a pull reqest which I learned in previous sections. It was a very good learning experience.

--------------------------------------------------------------
--------------------------------------------------------------

# Section 6 : Troubleshooting & Problem Solving

## Task 6.1 - Common Git Problems
![alt text](image-68.png)
### I used AI to know about this and this is what I can summarize.
![alt text](image-69.png)

## Task 6.2 - Data Recovery & Forensics

### A. Recover deleted commit with reflog
`git reflog`
![alt text](image-70.png)
![alt text](image-71.png)
![alt text](image-72.png)
![alt text](image-73.png)
![alt text](image-74.png)
![alt text](image-75.png)
![alt text](image-76.png)

### B. Track file history
#### i. `git blame src/index.html`

![alt text](image-77.png)
![alt text](image-78.png)

#### ii. `git log --follow -- src/index.html`

![alt text](image-79.png)

## Task 6.3 - Security & Best Practices

### 1. Remove sensitive data

`git filter-branch --force --index-filter \
  "git rm --cached --ignore-unmatch path/to/secret.txt" \
  --prune-empty --tag-name-filter cat -- --all`

  ```
This command forcefully rewrites Git history across all branches and tags to remove path/to/secret.txt from the index, cleaning up empty commits and preserving tag names.
  ```

  ![alt text](image-80.png)

### 2. Enable signed commits

`git config --global user.signingkey <GPG_KEY_ID>
git config --global commit.gpgSign true`

```
These commands configure Git to sign all commits globally using your specified GPG key (<GPG_KEY_ID>), helping verify your identity and ensuring commit integrity. 🔐 It's a solid step toward trusted, secure version control. Let me know if you want help setting up your GPG key too!
```

## Task 6.4 
### Document guidelines in `docs/security-best-practices.md` on security best practices.

## My Learnings
### This Section taught me troubleshooting problems and I learned the importance of logs in git. I also came to know about security best pratices which we should follow.

-------------------------------------------------------------
------------------------------------------------------------------

# Section 7

## Task 7.1: Build Demo Project
### Step 1: Set up a Local Project with Git
```
mkdir git-demo-project
cd git-demo-project
git init
```
![alt text](image-81.png)

### Step 2: Create Basic App (e.g., a simple Python app)
```
touch main.py
echo 'print("Hello from Git Demo!")' > main.py
git add main.py
git commit -m "Initial commit: Add base app"
```
![alt text](image-82.png)

### Step 3 : Create Feature Branches
`Let’s add two features: logging and math function.`
![alt text](image-83.png)

![alt text](image-84.png)

#### Merge the branches
![alt text](image-85.png)
![alt text](image-86.png)

### Step 4: Documentation and README

Commands I followed
```
touch README.md
echo "# Git Demo Project\n\n## Features\n- Logging\n- Math operations\n\n## How to Run\npython main.py" > README.md
git add README.md
git commit -m "Add README documentation"
```
![alt text](image-87.png)

### Step 5: Simulate Code Review (on GitHub)

#### A. Push to GitHub
Commands I followed
```
git remote add origin https://github.com/YOUR_USERNAME/git-demo-project.git
git push -u origin main
```
![alt text](image-88.png)
![alt text](image-89.png)
![alt text](image-90.png)
![alt text](image-91.png)

## Task 7.2: Create Learning Docs

### Structure
```
docs/
│
├── daily_summaries.md
├── Git_Assignments.md
├── commands_reference.md
├── problem_solving.md
└── personal_workflow.md
```

## Task 7.3 - Knowledge Sharing
 ### `created markdown file on git hub concepts named` ```git-concepts.md```


# Deliverables
![alt text](image-92.png)

## Created a markdown document named `deliverables.md` in `docs` folder.

----------------------------------------------------
-----------------------------------------------------
# The End
----------------------------------------------------




