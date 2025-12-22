# 🧭 Basic Git Workflow Diagram and Commands
| ***Area***              | ***Description***                        | ***Key Commands***                     |
|-------------------------|------------------------------------------|----------------------------------------|
| 📌 Working Directory    | For editing and managing files           | git status + enter.                    |
| 📌 Staging Area (Index) | Temp area for prepping before committing | git add <file> or git add .            |
| 📌 Local Repository     | Saved project history in local           | git commit -m "message"                |
| 📌 Remote Repository    | A shared version hosted on a git server  | git push, git pull, git clone + enter. |

## Git Command - AI Prompts
1. Working Directory:
   - What is git init?
   - What is echo "# Project Title" > README.md?
   - What is git Status?

2. Staging Area:
    - What is the difference between git add . and git add <file_name> [e.g. git add README.md]?
    - What is git add -p?
    - What is git add -u?

3. Move files from Staging Area to Local Repo history: 
  - What does git commit -m "Commit message" do?

4. Link local repo to remote:
  - What is git remote add origin [remote_repository_url]?
  - What is git remote -v?

5. Local Repo:
    - What is git log? 
    - What is git branch [branch-name]?
    - What is git checkout -b [branch-name]?
    - What is git switch -c [branch-name]?
    - What is git branch?
    - What is the difference between git checkout [branch-name] and git switch [branch-name]? Which one is recommended?
    - What is git merge [branch-name]?

6. Remote Repo - New Project
    - What is the difference between git push -u origin HEAD vs git push origin <branch-name>?
    - What is git push -u origin main or git push [remote] [branch]?
    - What is a pull request?
    - what is git pull?
    - What is git fetch?
    - What is git merge?

7. Remote Repo - Existing Project
   - What is git clone?

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
<caption style="font-weight: bold">📌Area: Working Directory - Local Machine</caption>
  <thead>
    <tr>
      <th>Commands</th>
      <th>CMD Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>git init</td>
      <td>Initializes a new Git repository in your current directory. Adds hidden .git directory</td>
    </tr>
    <tr>
      <td>git remote add origin [remote_repository_url]</td>
      <td>Link local repo to new remote:</td>
    </tr>
    <tr>
      <td>git status</td>
      <td>Shows untracked/modified files.</td>
    </tr>
  </tbody>
</table>

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
      <td>Initializes a new Git repository in your current directory. Adds hidden .git directory</td>
    </tr>
    <tr>
      <td>git remote add origin [remote_repository_url]</td>
      <td>Link local repo to new remote:</td>
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


