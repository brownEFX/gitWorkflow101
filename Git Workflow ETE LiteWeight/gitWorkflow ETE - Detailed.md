# GitWorkflow Command Prompt Suite
- This guide breaks down Git commands by workflow stage.  
- It offers AI-friendly prompts to explain each concept. 
- Ideal for onboarding, documentation, or interactive learning.  

# 🏁 Initialization: Working Directory  
1️⃣2️⃣3️⃣4️⃣5️⃣6️⃣7️⃣8️⃣9️⃣🔟
## 1️⃣ Setup Working Directory 

<table>
<caption style="font-weight: bold">📌Area: Working Directory - Local Machine</caption>
  <thead>
    <tr>
      <th>Commands</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>alt+f12</td>
      <td>open terminal in IntelliJ</td>
    </tr>
    <tr>
      <td>cd.. + enter</td>
      <td>Go to root C:\ </td>
    </tr>
    <tr>
      <td>C:\mkdir "myWorkspace gitWorkflow" + enter</td>
      <td>Create a working directory</td>
    </tr>
    <tr>
      <td>cd "myWorkspace gitWorkflow" + enter </td>
      <td>Navigate to Working Directory</td>
    </tr>
  </tbody>
</table>

## 2️⃣ Initialise Local Repo
<table>
<caption style="font-weight: bold">📌Area: Initialise Local Repo</caption>
  <thead>
    <tr>
      <th>Commands</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>git init</td>
      <td>
        <ol>
            <li>Creates & initializes a new Git repository in your current directory.</li>
            <li>Adds hidden .git subdirectory with necessary metadata and objects for Git to start tracking changes.</li>
            <li>Rerun git init to pick up new templates or move the repository path.</li>
            <li>Verify git init created hidden .git subdirectory: ls -Force + enter. </li>
        </ol> 
      </td>
    </tr> 
    <tr>
      <td>git init -b main</td>
      <td>
        <ol>
            <li>git init -b main sets the default branch name to main.</li>
            <li>Adds hidden .git subdirectory with necessary metadata and objects for Git to start tracking changes.</li>
            <li>Rerun git init to pick up new templates or move the repository path.</li>
            <li>Verify git init created hidden .git subdirectory: ls -Force + enter. </li>
        </ol> 
      </td>
    </tr> 
    <tr>
      <td>git status</td>
      <td>Shows new(untracked) and/or modified files.</td>
    </tr>
  </tbody>
</table>

## 3️⃣️ Add initial files
<table>
<caption style="font-weight: bold">📌Area: Working Directory - Initial Setup files</caption>
  <thead>
    <tr>
      <th>Commands</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>echo "# Project Title" > README.md </td>
      <td>
        <ul style="list-style-type:square;">
            <li>echo "# Project Title" > README.md creates/overwrites README.md with "# Project Title" content </li>
            <li>"# Project Title" is h1 in Markdown syntax</li> 
            <li>VERIFY:</li>
                <ul>
                    <li>View files and subdirectories: ls</li>
                    <li>View directory with hidden and Sys files: ls -Force + enter</li>
                </ul>
        </ul> 
      </td> 
    </tr>
    <tr>
      <td>git status </td>
      <td>Snapshot current state of local repository to monitor changes in your working directory and staging area.</td>
    </tr> 
  </tbody>
</table>
# 📤 Staging Area:
## 4️⃣ Add files to Staging Area for commit
<table>
<caption style="font-weight: bold">📌Action: Add files to the Staging</caption>
  <thead>
    <tr>
      <th>Commands</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">git add </td>
      <td>git add "fileName": Add specific file to the Staging Area.E.g. git add README.md </td>
    </tr> 
    <tr>
      <td>git add .: Add all changes in the current dir and subdirectories to the Staging Area.</td>
    </tr> 
    <tr>
      <td>git add -A: Repository-Wide, comprehensive staging of all new (untracked) files, modified files, and deleted files.</td>
    </tr> 
    <tr>
      <td>git status </td>
      <td>Snapshot current state of local repository to monitor changes in your working directory and staging area.</td>
    </tr> 
  </tbody>
</table>

# 🧠 Commit History: Local Repository 
- What does git commit -m "Commit message" do?
- What is git log?
- What is git branch <branch-name>?
- What is git checkout -b <branch-name>?
- What is git switch -c <branch-name>?
- What is git branch?
- What is git checkout <branch-name> vs git switch <branch-name>? Which one is recommended?
- What is git merge <branch-name>?

## 5️⃣ Commit work in Staging Area
<table>
<caption style="font-weight: bold">📌Area: Local Repo - Commit staged</caption>
  <thead>
    <tr>
      <th>Commands</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td> git commit -m "Commit message" </td>    
      <td>
        <ul>
            <li>Creates a snapshot of files in the Staging Area and saves it to Local Repo History</li>
            <li>Git creates unique 40-character SHA-1 string identifying the specific version.</li>
            <li>-m: provide a short summary of the changes.</li>
            <li>Use multiple -m flags for longer description: git commit -m "Title" -m "Detailed description"</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>git log</td> 
      <td>
        <ul>
            <li>Displays detailed commit history of your repository </li>
            <li>NOTE: Use arrows keys or space to scroll and q to exit log viewer.</li>
            <li>Common git log Commands:</li>
                <ul>
                    <li>git log --oneline: Condenses each commit into a single line for a high-level overview.</li>
                    <li>git log -n "number": Limits the output to a specific number of recent commits (e.g., git log -n 5</li>
                    <li>git log --stat: Shows statistics for files modified, including the number of lines added or deleted.</li>
                </ul>
        </ul>
      </td>
    </tr>
    <tr>
      <td>git status </td>
      <td>Snapshot current state of local repository to monitor changes in your working directory and staging area.</td>
    </tr> 
  </tbody>
</table>  

# 🌐 Remote Setup - Link local repo to remote:
- What is git remote add origin <remote_repository_url>?
- What is git remote -v?
- What is git remote show origin?
  1️⃣2️⃣3️⃣4️⃣5️⃣6️⃣7️⃣8️⃣9️⃣🔟
## 6️⃣ Connect to Remote (GitHub)
Once your local repo has its first commit, link it to a remote server.

2. 🔄 Remote Repo: Existing Project
    - What is git clone?
    - What is git fork?
    - git clone vs git fork?

    # Push the initial main branch to the remote server
    git push -u origin main


<table>
<caption style="font-weight: bold">📌Area: Link local repo to Remote</caption>
  <thead>
    <tr>
      <th>Commands</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>git remote add origin [remote_repository_url]</td>
      <td>
        <ol>
            <li>GitUI: Create new empty Repo. DON'T initialize it with a README or license file online</li>
            <li>Copy the remote repository's URL</li>
            <li>CLI: Link local repo to new remote: git remote add origin [remote_URL] + enter </li>
            <li>NOTE: Once configured, you can use remote shortname in commands like git fetch "remote", git pull "remote", and git push "remote" to exchange data with that repository.</li>
        </ol>
      </td>
     </tr>
    <tr>
    <tr>
      <td rowspan="3"> git remote </td>     
      <td>Lists shortnames/aliases of the remotes you have configured. </td>
    </tr>
    <tr>
        <td>
        Verify the Remote:
        <ul style="list-style-type:square;">
            <li>git remote -v: Lists existing remotes with their URLs</li>
            <li>git remote show origin: Displays detailed information about a specific remote, including fetch/push URLs and tracking branches.</li>
        </ul>
        </td>
    </tr>
    <tr>
      <td>
        <p>Managing Origin:</p>
        <ul style="list-style-type:square;">
            <li>git remote set-url origin [new_remote_URL]: Change Remote Repo URL to replace old with new URL</li>
            <li>git remote -v : Confirm change</li>
        </ul>
    </td>
    </tr>
  </tbody>
</table>

# 🚀🔄 Sync Local && Remote (GitHub)
    - What is git fetch? git fetch <remote>?
    - hat is git merge? git merge "remote"?
    - What is git pull? git pull <remote>?
    - What is git push? git push <remote>?
    - What is the difference between git push -u origin HEAD vs git push origin <branch-name>?
    - What is git push -u origin main or git push <remote> <branch>?
    - What is a pull request?

## 7️⃣ Download data from Remote (Don't merge)
<table>
<caption style="font-weight: bold">📌Area: Download from Remote</caption>
  <thead>
    <tr>
      <th>Commands</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td> git fetch </td>  
        <td>
            <ul>
             <li>Downloads data from the remote but does not merge it into your local work.</li>
             <li>Git connects to remote and downloads any new commits, branches, and tags</li>
             <li>Updates remote-tracking branches (e.g., origin/main or origin/develop)</li>
             <li>Local like main branch and your working directory remain unchanged.</li> 
             <li>BENEFIT: Ability to inspect the incoming changes before applying them. </li>
                <li>Common git fetch commands:</li>
                    <ul style="list-style-type:square;">
                        <li>git fetch origin: Fetches updates from the remote named "origin".</li>
                        <li>git fetch "remote-name": Fetches updates from a specific remote, such as upstream.</li>
                        <li>git fetch --all: Fetches updates from all configured remotes.</li>
                        <li>git fetch --prune: Removes references to branches that no longer exist on the remote repository</li>
                        <li>git fetch origin "branch-name": Fetches only a specific branch's updates. </li>
                    </ul>
            </ul>
        </td>
    </tr>
  </tbody>
</table>

## 8️⃣ Integrate changes from Data Downloaded from Remote
<table>
<caption style="font-weight: bold">📌Area: Integrate data from Remote</caption>
  <thead>
    <tr>
      <th>Commands</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Option 1: Integrate with git merge:</td> 
      <td>
        <ul>
            <li>git merge origin/"branch_name" (e.g., git merge origin/main).</li>
            <li>Integrates fetched changes into your current local branch.</li>
            <li>Brings work from one branch (e.g., a feature branch) into another (e.g., the main branch).</li>
            <li>If local and remote changes have diverged, it creates a "merge commit" to reconcile the histories.</li>
        </ul>
      </td>
    </tr>  
    <tr>
      <td>Option 2: Integrate with git rebase: </td> 
      <td>
        <ul>
            <li>git rebase origin/main</li>
            <li> For cleaner, linear project history, you can use git rebase instead of git merge</li>
            <li>git rebase moves local commits to sit on top of the latest fetched commits, rewriting the commit history.</li>
            <li> This process is effectively achieved by using git pull --rebase</li>
        </ul>
      </td>
    </tr>  
  </tbody>
</table> 


## 9️⃣ Download & Integrate changes Data from Remote
<table>
<caption style="font-weight: bold">📌Area: Pull from Remote</caption>
  <thead>
    <tr>
      <th>Commands</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td> git pull </td>     
      <td>
        <ul>
            <li>Updates local branch with the latest changes from a remote repository. Shorthand for fetch and integrate</li>
            <li>NB: git pull is a local command used on your machine to sync your own copy of the code.</li>
            <li>Core Mechanism - git pull command performs a two-step process in one command:</li>
                <ol>
                    <li>git fetch: Downloads new commits, files, and references from remote repo to your local machine without altering your current work.</li>
                    <li>git merge (default): Immediately integrates those downloaded changes into your active local branch.</li>
                </ol>
            <li>Common git pull commands:</li>
             <ul style="list-style-type:square;">
              <li>git pull: Fetches and merges changes from the default remote (e.g. origin) into your current branch.</li>
              <li>git pull "remote" "branch": Pulls changes from a specific remote and branch (e.g., git pull origin main).</li>
              <li>git pull --rebase: Fetches changes but uses git rebase instead of a merge, resulting in a cleaner, linear commit history.</li>
            </ul>
        </ul>
      </td>
    </tr>
</tbody>
</table>


<table>
<caption style="font-weight: bold">📌Area: Pull from Remote</caption>
  <thead>
    <tr>
      <th>Commands</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
      <td rowspan="4"> git rebase </td>     
      <td>
        <ul> 
            <li>git rebase integrates changes from one branch into another by rewriting commit history</li>
            <li>It "replays" your commits on top of a new base, creating a perfectly linear project history. </li>
        </ul>
      </td>
    </tr>
    <tr>
        <td>
        <p>How git rebase works:</p>
        <ul style="list-style-type:square;">
            <li>When you rebase a feature branch onto main, Git identifies the common ancestor of both branches.</li>
            <li>It temporarily sets aside your feature branch commits, updates your branch to the latest commit on main, and then reapplies your commits one by one on top.</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>
        <p>Key Benefits: git rebase:</p>
        <ul style="list-style-type:square;">
            <li>Linear History: Unlike git merge, which creates a "merge commit," rebasing avoids branching paths, making history easier to read and navigate.</li>
            <li>Cleanliness: It eliminates unnecessary merge commits that can clutter a shared repository.</li>
            <li>interactive Editing: With git rebase -i, you can squash multiple commits into one, reorder them, or edit old commit messages before they are merged.</li>
            <li>Golden Rule: Never rebase commits that have been pushed to a public repository.</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>
        <p>Common Commands: git rebase:</p>
        <ul style="list-style-type:square;">
            <li>git rebase main: Rebase your current branch onto the main branch.</li>
            <li>git rebase -i HEAD~3: Start an Interactive Rebase to modify the last three commits.</li>
            <li>git rebase --continue: Resume a rebase after manually resolving a conflict.</li>
            <li>git rebase --abort: Cancel the rebase and return your branch to its original state. </li>
        </ul>
        </td>
    </tr>
</tbody>
</table>

<table>
<caption style="font-weight: bold">📌Area: Pull from Remote</caption>
  <thead>
    <tr>
      <th>Commands</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="4"> git push </td>     
      <td>Uploads local commit history to a remote repository.</td>
    </tr>
    <tr>
        <td>
        <p><b>Key Functions:</b></p>
        <ul style="list-style-type:square;">
            <li>Uploads Commits: Transfers new commits, file changes, and directory snapshots from your local branch to its remote counterpart.</li>
            <li>Updates Remote References: Moves the pointer of the remote branch to match the latest commit you just uploaded.</li>
            <li>Creates New Branches: If you push a local branch that doesn't yet exist on the server, Git will create it for you there. </li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>
        <p><b>Common Usage and Syntax:</b></p>
        <ul style="list-style-type:square;">
            <li>Standard Push: git push "remote" "branch" e.g. git push origin main.</li>
            <li>First-Time Push: Use git push -u origin "branch-name" to set an upstream tracking relationship</li>
            <li>git push -u origin HEAD: to push your current local branch to a remote repository and simultaneously set it up for easier future use.</li>
            <ul>
                <li>git push: Sends your local commits to a remote repository.</li>
                <li>-u (or --set-upstream): Links your local branch to the remote branch you are pushing to.</li>
                <li>origin: The default name for your remote repository</li>
                <li>HEAD: A symbolic reference to the branch you currently have checked out.</li>
                <li>Using HEAD is a convenient way to refer to your current branch without having to type out its full name.</li>
            </ul>
            <li>Subsequent Push: Use git push for all future updates on that branch.</li>
            <li>Pushing All Branches: git push --all uploads every local branch to the remote repository at once.</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>
        <p><b>Crucial Safety Rules:</b></p>
        <ul style="list-style-type:square;">
            <li>Git only allows a push if your local branch is a direct descendant of the remote branch.</li>
            <li>First run git pull to integrate any pushed changes before pushing yours.</li>
            <li>git push --force (or -f) overwrites the remote history with your local history, can delete others' work</li>
            <li>Use --force-with-lease, which only proceeds if no new changes have been made to the remote since you last checked.</li>
        </ul>
        </td>
    </tr>
    <tr>
      <td rowspan="2"> Pull Request(PR)</td>     
      <td>
        <ul style="list-style-type:square;">
        <li>A PR is a formal proposal to merge code changes from one branch to another</li>
        <li>It requests the target branch to PULL your changes.</li>
        <li>It initiates collaborative process to review and test code before it can be officially integrated</li>
        <li>Key Components and Process</li>
        <ol>
            <li>Local Repo: Create new branch from main</li>
            <li>Code Changes: Add new feature or bug fix</li>
            <li>Push: Stage, commit and push your changes to remote repo</li>
            <li>Open PR: Create a PR requesting target branch to PULL  your changes</li> 
            <li>Review: Collaborators review the "diff" (differences), discuss, and suggest improvements.</li>
            <li>Merge: Approved changes are merged into the target branch, becoming part of the official codebase.</li>
            <li>Clean Up: After merging, delete the remote branch on the website and update your local main branch.</li>
        </ol>
        <li>RESOURCES: </li>
            <ul style="list-style-type:disc;">
                <li><a href="https://youtu.be/_HedItVFr5M?si=FD2OcFeKqo6pFHjE">Writing Great Pull Requests</a></li>
                <li><a href="https://youtu.be/FDXSgyDGmho?si=6A43wdX5Xukvojzz">Merging a pull request</a></li>
                <li><a href="https://github.com/LadyKerr/catch-the-cat-game">Git101 Repo</a></li> 
            </ul>
        </ul>
    </td>
    </tr>
    <tr>
        <td>
The final steps move from your terminal to the remote server's web interface (e.g., GitHub).
1. Open PR: 
   ❶ Navigate to your repository on GitHub.
   ❷ Select Pull Requests tab. 
   ❸ Click "Compare & pull request" for the branch you just pushed.
   ❹ Add a Title && Description
   ❺ Click Create Pull Request
   ❶❷❸❹❺❻❼ ❾❿
2. Review: Collaborators review your code, leave comments, and suggest changes.
3. Merge: Once approved, click "Merge pull request" on the web page to join your feature branch into main.
4. Clean Up: After merging, delete the remote branch on the website and update your local main branch.
        <p>Steps - Creating a Pull Request:</p>
        <ul style="list-style-type:none;">
            <li>❶ Navigate to your repository on GitHub.</li>
            <li>❷ Select Pull Requests tab.</li>
            <li>❸ Click "Compare & pull request" for the branch you just pushed.</li>
            <li>❹ Add a Title && Description</li>
            <li>❺ Click Create Pull Request</li>
        </ul>
        </td>
    </tr>
</tbody>
</table>  

7. Working with branches
<table>
<caption style="font-weight: bold">📌Area: Link Local Repo  to Remote</caption>
  <thead>
    <tr>
      <th>Commands</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="8">git branch</td>
      <td>git branch "branch-name" creates a new branch in your local repository but does not switch you to it.</td>
    </tr>
    <tr>
      <td>git switch "branch-name": to move to the new branch. </td>
    </tr>
    <tr>
      <td>git checkout "branch-name": to move to the new branch. </td>
    </tr>
    <tr>
      <td>git switch -c "branch-name": to create a new branch and switch to it immediately in one step. </td>
    </tr>
    <tr>
      <td>git checkout -b "branch-name": to create a new branch and switch to it immediately in one step. </td>
    </tr>
    <tr>
      <td>git branch -m "old-name" "new-name": to rename a branch. </td>
    </tr>
    <tr>
      <td>git branch -d "branch-name": standard delete. </td>
    </tr>
    <tr>
      <td>git branch -D "branch-name": forced delete if changes aren't merged </td>
    </tr>
  </tbody>
</table> 

7. 🧹 Optional Additions for Advanced Users
- What is git config --global user.name and user.email?
- What is git stash and git stash pop?
- What is the difference between git rebase and git merge?
- What is the difference between git reset and git revert?