# 🧭 The Existing Project gitWorkflow (Clone to Merge)
| ***Area***       | ***Area Description***  	                       | ***Commands***                                    | ***CMD Description***                                     |
|------------------|:------------------------------------------------|---------------------------------------------------|-----------------------------------------------------------|
| 📌 Remote Repo 	 | The source of truth (GitHub/GitLab)             | 	git clone [URL]	                                 | Downloads the entire project and history to your machine. |
| 📌 Local Repo	   | Your local copy of the history	                 | git switch -c feature-name                        | 	Creates and switches to a new feature branch.            |
| 📌 Working Dir   | 	Where you edit the code	                       | git status	                                       | Verifies which files you have changed.                    |
| 📌 Staging Area	 | Preparation for commit                          | 	git add .	                                       | Groups your changes together.                             |
| 📌 Local Repo    | 	Saving your work                               | 	git commit -m "message"	                         | Saves the changes into your local history.                |
| 📌 Remote Repo   | 	Sharing your work                              | 	git push -u origin HEAD	                         | Uploads your branch and sets it to track the remote.      |
| 📌 Web UI        | 	Pull Request (PR) Phase	N/A (Web Browser)	     | Open a Pull Request on GitHub to request a merge. |
| 📌 Local Repo    | 	Syncing after Merge	                           | git pull origin main	                             | Updates your local machine with the newly merged code.    |

# 🚀Step-by-Step Execution Example
## 📌 Setup New Project
### 🎯  Area: Working Directory && Local Repo
| ***Commands***                       | ***CMD Description***                      |
|--------------------------------------|--------------------------------------------|
| alt+f12 && cd.. to go to root [C:\]  | Open terminal and navigate to root dir.    |
| mkdir "myWorkspace - prjDir" + enter | Create working dir.                        |
| cd "myWorkspace - prjDir" + enter    | Navigate to Working Directory              |
| git init                             | Initialize local Git repository            |
| echo "# Project Title" > README.md   | Create an initial file                     |
| git add README.md                    | Stage the file                             |
| git commit -m "Initial commit"       | Save snapshot to local repo                |
| git remote add origin                | Link local repo to a remote server         |
| git push -u origin main              | Push initial main branch to remote server  |

### 🎯  Area: Remote Repo: gitUI
| ***Commands***      | ***CMD Description***                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------|
| Open PR             | Click "Compare & pull request" for the branch you just pushed                                    |
| Create PR           | Add PR Title and PR Description, then click Create Pull Request                                  |
| Review Code updates | Collaborators review your code, leave comments, and suggest changes                              |
| Merge               | Once approved, click "Merge pull request" on the web page to join your feature branch into main. |
| Review Code updates | Collaborators review your code, leave comments, and suggest changes                              |

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

   ### 🎯 Existing Project  
✍️ Open terminal: alt+f12 and cd.. to go to root [C:\]  
✍️ Create Dir: mkdir "myWorkspace - prjDir" + enter  
✍️ Navigate to Working Directory: cd "myWorkspace - prjDir" + enter  
✍️ Clone Project: `git clone repository-url`  
- 📝 The `git clone repository-url` command:
  - 💡 `git clone repository-url` creates a new directory named after the repository in your current location
  - 💡 The command downloads the entire project history and files into it.  

***Cloning Options:***
- Name directory after Repository Name: `git clone repository-url` + enter  
- Clone to current Directory: `git clone repository-url .` + enter
- Specify Directory Name: `git clone <repository-url> <directory-name>` + enter
- Clone a specific branch: 
  - By default, `git clone` checks out the default branch (usually main or master). 
  - To clone a different branch, use the -b option: `git clone -b <branch-name> <repository-url>`  
    

***Shallow Clone:***
***BENEFITS:***
- Useful for large repositories
- Saves time and disk space by limiting the download to a specific number of recent commits  

***Commands:***  
***SYNTAX:*** `git clone --depthdepth_value repository-url`
- `depth_value` is the positive integer specifying the number of commits you want to retrieve.  
- `repository-url` is the URL of the remote Git repository.  
  
***EXAMPLES:***
  - Clone most recent commit: `git clone --depth 1 repository-url`
  - Clone latest 5 commits: `git clone --depth 5 repository-url`
  - Clone latest commit of specific branch, using the `-b` (or `--branch`) option: `git clone --depth 1 -b branch_name URL`  

***Clone with SSH:***
***BENEFITS:***
- Using SSH keys provides a more secure authentication method
- Avoids entering credentials repeatedly. 

***Commands:***  
***SYNTAX:*** `git clone git@github.com:user/repository.git`
- `depth_value` is the positive integer specifying the number of commits you want to retrieve.
- `repository-url` is the URL of the remote Git repository.


✍️ Navigate to new Directory: cd `repository-name` + enter


| 📌 Create Dir              | Create a project dir                     | mkdir "prjDir" + enter.                                    |
| 📌 Go to Dir               | Go to your project dir                   | cd "prjDir" + enter.                                       |
