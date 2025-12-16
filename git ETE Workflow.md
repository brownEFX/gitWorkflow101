# 📝 End-to-End Git Workflow Guide
**PROMPT:**  
Add existing project to a new repository using command line  
Give me a full end-to-end git workflow based on this diagram.  
Include explanations, descriptions and commands at each stage and what those commands do.  

**Source:** *[Medium - Git Workflow Diagram](https://medium.com/@Ariobarxan/git-workflow-7055c4354d92 )*.  
**Image Address:** *[Medium - Git Workflow Diagram Image](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*Ss4U-0Vci4dqBNL3v2PBHg.png)*
---

## 🧭 Workflow Stages Overview
| ***Stage***                | ***Purpose***                            | ***Key Commands***                                         |
|----------------------------|------------------------------------------|------------------------------------------------------------|
| 📌 Create Dir              | Create a project dir                     | mkdir "prjDir" + enter.                                    |
| 📌 Go to Dir               | Go to your project dir                   | cd "prjDir" + enter.                                       |
| 📌 Init new local Git repo | Add hidden .git in local                 | git init + enter.                                          |
| 📌 Add project setup files | Add boilerplate code                     | Code files                                                 |
| 📌 Stage                   | Add files to staging                     | git add . or git add <file_name>                           |
| 📌 Status                  | Review the staged changes:               | git status + enter                                         |  
| 📌 Commit                  | Save a snapshot of staged changes        | git commit -m "Initial project setup"                      | 
| 📌 Create Repo             | Create new repo on github.com            | New Repo, Name, Desc, Public and Hit Create Repo. Copy URL | 
| 📌 Add Remote URL          | Add remote repo named origin             | git remote add origin <repository_URL>                     |
| 📌 Set main branch         | Rename default branch to 'main'          | git branch -M main                                         |
| 📌 Push                    | Upload commits to remote repository      | git push -u origin HEAD / git push origin <branch-name>    | 
| 📌 Clone                   | Copy remote repo to local machine        | git clone <repo-url> OR git clone <repo-url> newDirNM      |
| 📌 Branch                  | Create a new branch for isolated changes | git checkout -b <branch-name>                              | 
| 📌 Pull Request            | Request to merge changes into main       | GitHub/GitLab UI or gh pr create                           | 
| 📌 Merge                   | Integrate branch changes into main       | git checkout main + git merge                              |
---
## 0️⃣ Existing Workspace - Steps to Set up a Repo
### 🎯 Create New Directory
      📌 Go to to root directory: c~ + enter.
      📌 Create new directory: $ mkdir "myWorkspace - Bookstore" + enter.
      📌 Go to your workspace: $ cd + "myWorkspace - Bookstore" path + enter.

### 🎯 Confirm Directory contents: 
      ✅️ Print Working Directory to display the full, absolute path of current location: pwd + enter
      ✅️ View files and sub-directory: dir + enter
      ✅️ View contents of directory: ls + enter
      ✅️ View directory with hidden files: Get-ChildItem -Force + enter
---
### 🎯 Initialize Git in your local project folder:
    📌 Initialize Git in your local project folder: git init + enter.
         💡 git init creates a hidden .git directory to track changes.
            📍 Confirm hidden .git directory: ls -a + enter 
---  
### 🎯 Add project files to Staging:
    📌 Stage all your project files for the initial commit: git add . OR git add <file_name>
         💡 git add . stage all changes (new, modified, and deleted files) in your local for the next commit.
         💡 git add <file_name> stages specified file in your local for the next commit.
            📍 Review the staged changes: git status + enter 
---
### 🎯 Commit staged files:
    📌 Commit files in staging: git commit -m "commit message" + enter
         💡 git commit -m "<message>" takes a permanent snapshot of files in staging and saves them in local repo.
         💡 -m flag specifies the commit message describing changes in the version.
            📍 -m flag generates uniqueID for the specific commit.
            📍 -m flag moves HEAD pointer of current branch to the new commit, making it latest version.
---

### ✍️  Create New Repo
#### 📌 Setup Repo Using gitHub UI
       1. Select New Repo from the + dropdown menu in GitHub
       2. Enter Repo name, description, select Public and Hit Create Repo

#### 📌  Setup Repo using CLI:
    1. Create a remote repo: git remote add origin https://github.com/brownEFX/Story.git
    2. Push local repo to remote repo: git push -u origin master. 
    3. Refresh repo in github to see your repo. Copy URL</li>

#### 📌 …or create a new repository on the command line
    echo "# theInternet-SeJavaPrj" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git branch -M main
    git remote add origin https://github.com/brownEFX/theInternet-SeJavaPrj.git
    git push -u origin main
    git push origin HEAD https://www.youtube.com/watch?v=bWLwktYhZh0

#### 📌 …or push an existing repository from the command line
    git remote add origin https://github.com/brownEFX/theInternet-SeJavaPrj.git
    git branch -M main
    git push -u origin main
---
## 1️⃣ CLONE: Get the Project Locally  
**Purpose:** Copy the remote repository to your local machine.  
**Command:**  
- git clone https://github.com/user/repo.git  
- git clone https://github.com/user/repo.git myNewDir [Clone with new dir name]  

**Outcome:**
- Downloads all files, branches, and history.
- Creates a local copy with a .git folder for tracking changes.
---

## 2️⃣ BRANCH: Create a Feature Branch
**Purpose:** Work in isolation without affecting the main branch.
**Command:** git checkout -b feature/my-branch
**Outcome:**
- Creates and switches to a new branch.
- Enables safe modification of files like DOG, CAT, BIRD, and addition of FISH.
---

## 3️⃣ STAGE: Prepare Changes for Commit
**Purpose:** Select which changes to include in the next commit.  

**Commands:**  
1. git add FISH.java       # Add a new file  
2. git add DAG.java        # Modified file  
3. git rm BIRD.java        # Deleted file
4. git add .               # Or to stage everything:
---

## 4️⃣ COMMIT: Save Changes to Local History
**Purpose:** Record a snapshot of staged changes.  
**Command:** git commit -m "Added FISH, modified DAG, removed BIRD"   
  
**Outcome:**  
- Creates a commit object with your changes.
- Adds it to your branch’s history.
- Packages changes into a "save point".
- Marks them for commit but doesn’t save yet.

**Purpose:** View branch history.  
**Command:** 
- View the history of the current branch: git log 
- View the history of a specific branch (without checking it out): git log <branch-name> e.g. git log master  
- View a concise summary of the history: git log --oneline
- Visualize the branch history as an ASCII graph: git log --graph --oneline --decorate --all

**Outcome:**  Example History:  
    COMMIT 2: Modified DAG  
    COMMIT 1: Added FISH, Removed BIRD  
    START
---

Last Wednesday

Give me a full end-to-end git workflow based on this diagram. Include explanations, descriptions and commands at each stage and what those commands do
Absolutely, Karabo — let’s walk through a full Git workflow based on your diagram, with clear explanations and commands at each stage. This will give you a reusable reference for teaching, documentation, or onboarding new collaborators.

🧭 Overview: Git Workflow Stages
Stage	Purpose	Key Commands
1. Clone	Copy remote repo to local machine	git clone
2. Branch	Create a new branch for isolated changes	git checkout -b
3. Stage	Mark files for commit	git add or git add .
4. Commit	Save a snapshot of staged changes	git commit -m "message"
5. Push	Upload commits to remote repository	git push origin
6. Pull Req	Request to merge changes into main	GitHub/GitLab UI or gh pr create
7. Merge	Integrate branch changes into main	git checkout main + git merge
   🔍 Step-by-Step Breakdown
   1️⃣ CLONE: Get the Project Locally
   Purpose: Copy the remote repository to your local machine.

Command:

bash
git clone https://github.com/user/repo.git
What it does:

Downloads all files, branches, and history.

Creates a local copy with a .git folder for tracking changes.

2️⃣ BRANCH: Create a Feature Branch
Purpose: Work in isolation without affecting the main branch.

Command:

bash
git checkout -b feature/my-branch
What it does:

Creates a new branch called feature/my-branch.

Switches your working directory to that branch.

🧠 Why? This allows you to safely modify files like DOG, CAT, BIRD, and add new ones like FISH.

3️⃣ STAGE: Prepare Changes for Commit
Purpose: Select which changes to include in the next commit.

Command:

bash
git add FISH.java       # Add a new file
git add DAG.java        # Modified file
git rm BIRD.java        # Deleted file
Or to stage everything:

bash
git add .
What it does:

Packages changes into a "save point".

Doesn’t actually save yet — just marks them for commit.

4️⃣ COMMIT: Save Changes to Local History
Purpose: Record a snapshot of staged changes.

Command: git commit -m "Added FISH, modified DAG, removed BIRD"
What it does: 
- Creates a commit object with your changes.
- Adds it to your branch’s history.

🧾 Example History:
Code
COMMIT 2: Modified DAG
COMMIT 1: Added FISH, Removed BIRD
START
---

5️⃣ PUSH: Upload Your Branch to Remote
Purpose: Share your changes with others or prepare for a pull request.
Command: 
- The first time you push a new local feature branch: git push -u origin HEAD: 
- If you have already set the upstream and just want to push to a specific remote: git push origin <branch-name>
What it does:
- Sends your local commits to the remote repository.
- Makes your branch visible on GitHub.
---

Last Wednesday

Give me a full end-to-end git workflow based on this diagram. Include explanations, descriptions and commands at each stage and what those commands do
Absolutely, Karabo — let’s walk through a full Git workflow based on your diagram, with clear explanations and commands at each stage. This will give you a reusable reference for teaching, documentation, or onboarding new collaborators.

🧭 Overview: Git Workflow Stages
Stage	Purpose	Key Commands
1. Clone	Copy remote repo to local machine	git clone
2. Branch	Create a new branch for isolated changes	git checkout -b
3. Stage	Mark files for commit	git add or git add .
4. Commit	Save a snapshot of staged changes	git commit -m "message"
5. Push	Upload commits to remote repository	git push origin
6. Pull Req	Request to merge changes into main	GitHub/GitLab UI or gh pr create
7. Merge	Integrate branch changes into main	git checkout main + git merge
   🔍 Step-by-Step Breakdown
   1️⃣ CLONE: Get the Project Locally
   Purpose: Copy the remote repository to your local machine.

Command:

bash
git clone https://github.com/user/repo.git
What it does:

Downloads all files, branches, and history.

Creates a local copy with a .git folder for tracking changes.

2️⃣ BRANCH: Create a Feature Branch
Purpose: Work in isolation without affecting the main branch.

Command:

bash
git checkout -b feature/my-branch
What it does:

Creates a new branch called feature/my-branch.

Switches your working directory to that branch.

🧠 Why? This allows you to safely modify files like DOG, CAT, BIRD, and add new ones like FISH.

3️⃣ STAGE: Prepare Changes for Commit
Purpose: Select which changes to include in the next commit.

Command:

bash
git add FISH.java       # Add a new file
git add DAG.java        # Modified file
git rm BIRD.java        # Deleted file
Or to stage everything:

bash
git add .
What it does:

Packages changes into a "save point".

Doesn’t actually save yet — just marks them for commit.

4️⃣ COMMIT: Save Changes to Local History
Purpose: Record a snapshot of staged changes.

Command:

bash
git commit -m "Added FISH, modified DAG, removed BIRD"
What it does:

Creates a commit object with your changes.

Adds it to your branch’s history.

🧾 Example History:

Code
COMMIT 2: Modified DAG
COMMIT 1: Added FISH, Removed BIRD
START
---

5️⃣ PUSH: Upload Your Branch to Remote
Purpose: Share your changes with others or prepare for a pull request.

Command: git push origin feature/my-branch
What it does:
- Sends your local commits to the remote repository.
- Makes your branch visible on GitHub/GitLab.

6️⃣ OPEN PULL REQUEST: Request a Merge
Purpose: Ask reviewers to approve your changes before merging.
Options: 
- Use GitHubUI → Click "New Pull Request"
- Use CLI: gh pr create --base main --head feature/my-branch --title "Feature update" --body "Added FISH, modified DAG"

What it does:
- Compares your branch to main.
- Allows reviewers to comment, approve, or request changes.
---

7️⃣ MERGE: Integrate Changes into Main
Purpose: Finalize the feature and update the main codebase.
Command:
    git checkout main
    git pull origin main          # Get latest main
    git merge feature/my-branch   # Merge your branch

What it does:
- Combines your branch into main.
- Resolves any conflicts if necessary.

***NOTE:***  
✅ Once approved and merged, your changes  are now part of the main project.  
✅ EXAMPLE: FISH added, DAG modified, BIRD removed

