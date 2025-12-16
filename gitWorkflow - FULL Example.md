# 📝 End-to-End Git Workflow Example
1️⃣2️⃣3️⃣4️⃣5️⃣6️⃣7️⃣8️⃣9️⃣🔟 

**PROMPT:**  
Give me a full example from git init to pull requests and merge. Include concise comments

## Summary
This example demonstrates the full lifecycle of a feature, from starting a new project locally 
to merging a Pull Request (PR) on a remote server like GitHub as of 2025.

### 1️⃣ Setup & Initial Commit
Start by creating a local folder and initializing it as a Git repository.

    mkdir my-new-project && cd my-new-project  # Create and enter project folder
    git init                                   # Initialize local Git repository
    echo "# Project Title" > README.md         # Create an initial file
    git add README.md                          # Stage the file
    git commit -m "Initial commit"             # Save snapshot to local repo

### 2️⃣ Connect to Remote (GitHub/GitLab)
Once your local repo has its first commit, link it to a remote server.

    # Link local repo to a remote address (replace with your repo URL)
    git remote add origin [remote_repository_url]

    # Push the initial main branch to the remote server
    git push -u origin main

### 3️⃣ Feature Development (Branching)
Never work directly on the main branch.  
Create a feature branch to keep changes isolated.

    git checkout -b feature/login-page         # Create and switch to new branch
    # ... make changes to files ...
    git status                                 # Check which files were modified
    git add .                                  # Stage all modified files
    git commit -m "Add login form UI"          # Commit changes locally

### 4️⃣ Share the Branch (Pushing for PR)
Upload your feature branch to remote repo for review.

    git push origin feature/login-page         # Push local branch to remote

### 5️⃣ Create and Merge the Pull Request
The final steps move from your terminal to the remote server's web interface (e.g., GitHub).
1. Open PR: Navigate to your repository on GitHub. You will typically see a prompt to "Compare & pull request" for the branch you just pushed.
2. Review: Collaborators review your code, leave comments, and suggest changes.
3. Merge: Once approved, click "Merge pull request" on the web page to join your feature branch into main.
4. Clean Up: After merging, delete the remote branch on the website and update your local main branch.

         git checkout main                          # Switch back to local main branch
         git pull origin main                       # Pull the newly merged code from remote
         git branch -d feature/login-page           # Delete the local feature branch

# 🧭 Basic Git Workflow Diagram and Commands
| ***Area***              | ***Description***                        | ***Key Commands***                     |
|-------------------------|------------------------------------------|----------------------------------------|
| 📌 Working Directory    | For editing and managing files           | git status + enter.                    |
| 📌 Staging Area (Index) | Temp area for prepping before committing | git add <file> or git add .            |
| 📌 Local Repository     | Saved project history in local           | git commit -m "message"                |
| 📌 Remote Repository    | A shared version hosted on a git server  | git push, git pull, git clone + enter. |

## The Git Workflow Diagram with Commands
A Git workflow involves moving changes between three main areas: 
- the Working Directory
- the Staging Area (Index), and 
- Local Repository, before pushing them to a 
- Remote Repository.


## 📋Summary of the logical flow depicted:  
✅️ Initialization: init / remote add / clone.  
✅️ Development: status (check) → add (stage) → commit (save).  
✅️ Management: branch (create) → switch (move) → merge (combine).  
✅️ Collaboration: pull (receive) → push (send).  

<table>
<caption style="font-weight: bold">Basic Git Workflow</caption>
  <thead>
    <tr>
      <th>Area</th>
      <th>Area Description</th>
      <th>Commands</th>
      <th>CMD Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">📌 Working Directory </td>
      <td rowspan="3">Directory on your machine</td>
      <td>git init</td>
      <td>Initializes a new Git repository in your current directory</td>
    </tr>
    <tr>
      <td>git remote add origin [remote_repository_url]</td>
      <td>Link local repo to remote:</td>
    </tr>
    <tr>
      <td>git status</td>
      <td>	Shows untracked/modified files.</td>
    </tr>
    <tr>
      <td rowspan="2">📌 Staging Area </td>
      <td rowspan="2">Prep zone for next commit</td>
      <td>git add .</td>
      <td>Stages all current changes</td>
    </tr>
    <tr>
      <td>git add [filename]</td>
      <td>Stages specific file.</td>
    </tr>
    <tr>
      <td rowspan="6">📌 Local Repo </td>
      <td rowspan="6">Save version history </td>
      <td>git log</td>
      <td>Describes the state of the Local Repo</td>
    </tr>
    <tr>
      <td>git commit -m "commit message"</td>
     <td>Permanently saves staged snapshot into the local repository with a descriptive message.</td>
    </tr>
    <tr>
      <td>git branch [branch-name]</td>
      <td>Creates a new branch.</td>
    </tr>
    <tr>
      <td>git branch</td>
      <td>Lists branches</td>
    </tr>
    <tr>
      <td>git checkout [branch-name] or git switch [branch-name]</td>
      <td>Switches between different branches.</td>
    </tr>
    <tr>
      <td>git merge [branch-name]</td>
      <td>Combines changes from the specified branch into your current branch.</td>
    </tr>
    <tr>
      <td rowspan="3">📌 Remote Repo </td>
      <td rowspan="3">Shared version on GitHub server</td>
      <td>git clone [URL]</td>
      <td>Creates a local copy of a remote repository.</td>
    </tr>
    <tr>
      <td>git push [remote] [branch]</td>
     <td>Uploads local commits to the remote repository</td>
    </tr>
    <tr>
      <td>git pull</td>
      <td>One-step git fetch from remote + git merge into local branch.</td>
    </tr>
  </tbody>
</table>

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


