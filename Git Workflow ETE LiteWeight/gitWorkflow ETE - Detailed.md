# GitWorkflow Command Prompt Suite
- This guide breaks down Git commands by workflow stage.  
- It offers AI-friendly prompts to explain each concept. 
- Ideal for onboarding, documentation, or interactive learning.  

1. 🏁 Initialization: Working Directory
    - What is git init?
    - How do you create a README file using shell commands before committing with Git?
      - What is echo "# Project Title" > README.md?
    - What is git Status?

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
    <tr>
      <td>git init</td>
      <td>Initializes a new Git repository in your current directory. Adds hidden .git directory</td>
    </tr>
    <tr>
      <td>Shell Command: echo "# Project Title" > README.md </td>
      <td>Create an initial file</td>
    </tr>
    <tr>
      <td>git commit -m "Initial commit"</td>
      <td>Save snapshot to local repo</td>
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

2. 🔄 Remote Repo: Existing Project
    - What is git clone?
    - What is git fork?
    - git clone vs git fork?

3. 📤 Staging Area:
    - What is the difference between git add . and git add <file_name> (e.g. git add README.md)?
    - What is git add -p?
    - What is git add -u?

<table>
<caption style="font-weight: bold">📌Area: Staging Area</caption>
  <thead>
    <tr>
      <th>Commands</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>git add . </td>
      <td>Stage ALL files. Stages changes within your current directory and its subdirectories</td>
    </tr>
    <tr>
      <td>git add -A</td>
      <td>
        <ul>
            <li>git add -A (or its equivalent --all) stages all changes to the Git index/staging area for the next commit.</li> 
            <li>Key Features: git add -A:</li>
              <ul>
                <li>Comprehensive Staging: Includes all new (untracked) files, modified files, and deleted files.</li>
                <li>Repository-Wide Scope: git add -A stages changes from the entire repository, regardless of which folder you are currently in.</li>
            </ul>
            <li>Common Workflow: git add -A:</li>
                <ul>
                    <li>git status: Check status to see which files are untracked or modified.</li>
                    <li>git add -A: Stage changes to prepare everything for a snapshot.</li>
                    <li>git commit -m "commit message": save staged changes into the local project history.</li>
                </ul>
        </ul>
      </td>
    </tr>
    <tr>
      <td>git add "file_name"</td>
      <td>Stage specific file e.g. README.md </td>
    </tr>
    <tr>
      <td>git add -p</td>
      <td>
        <ul>
            <li>git add -p (short for --patch) is used for interactive staging.</li>
            <li>Lets you choose portions/specific "hunks"/parts) of modified files to add to Staging for next commit. </li>
            <li>Presents you with a chunk of changes and prompt you for a command:</li>
            <li>How git add -p works:</li>
              <ul>
                <li>Git divides your changes into chunks and asks you what to do with each one.</li>
                <li>This helps separate unrelated changes (e.g., a bug fix and a formatting update) into different, focused commits.</li>
            </ul>
            <li>Common git add -p commands:</li>
                <ul>
                    <li>Use n(no) to ignore the chunk, do not stage this hunk</li>
                    <li>Use d(do not stage) Do not stage this hunk or any of the remaining hunks in this file.</li>
                    <li>Use y(yes) to stage the chunk, stage this hunk for the next commit</li> 
                    <li>Use s(split) to split it into smaller hunks if they are separated by unchanged lines</li>
                    <li>Use e(edit) to manually edit the hunk in your default text editor</li>
                    <li>Use q(quit) to exit interactive session without staging any more hunks (already staged hunks remain staged).</li>
                    <li>Use ?(help) to display a summary of all available commands.</li>
                </ul>
        </ul>
      </td>
    </tr>
    <tr>
      <td>git add -u</td>
      <td>
       <ul>
        <li>git add -u (short for --update) stages changes for all files that Git is already tracking.</li>
        <li>Key Characteristics:</li>
            <ul>
                <li>Only Tracked Files: It specifically stages modifications and deletions of files already in the Git index.</li>
                <li>Ignores Untracked Files: Will not stage new files that have been created but are not yet being tracked by Git</li>
                <li>Project-Wide Scope: Identifies changes across entire repository, regardless of which subdirectory you are currently in.</li>
            </ul>
        <li>When to use it:</li>
            <ul>
                <li>Cleaning up file deletions from the repo in the next commit.</li>
                <li>Incremental updates to stage every change made to existing code while explicitly leaving out files you aren't ready to track yet.</li>
            </ul>
        </ul> 
      </td>
    </tr>
  </tbody>
</table>

4. 🧠 Commit History: Local Repository (Move files from Staging Area to Local Repo history:)
- What does git commit -m "Commit message" do?
- What does git commit -m "Commit message" do?
- What is git log?
- What is git branch <branch-name>?
- What is git checkout -b <branch-name>?
- What is git switch -c <branch-name>?
- What is git branch?
- What is git checkout <branch-name> vs git switch <branch-name>? Which one is recommended?
- What is git merge <branch-name>?

<table>
<caption style="font-weight: bold">📌Area: Local Repo</caption>
  <thead>
    <tr>
      <th>Commands</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="4"> git commit -m "Commit message" </td>     
      <td>Creates a snapshot of files in the Staging Area and saves it to Local Repo History</td>
    </tr>
    <tr>   
      <td>-m flag allows you to provide a short summary of the changes directly in the terminal.</td>
    </tr>
    <tr>   
      <td>Multiple -m flags to longer description: git commit -m "Title" -m "Detailed description"</td>
    </tr>
    <tr>   
      <td>Git creates unique 40-character SHA-1 string identifying the specific version.</td>
    </tr>
    <tr>
      <td rowspan="9">git log</td>
      <td>Displays detailed commit history of your repository </td>
    </tr>
    <tr>   
      <td>NOTE: Use arrows keys or space to scroll and q to exit log viewer.</td>
    </tr>
    <tr>   
      <td>git log --oneline: Condenses each commit into a single line for a high-level overview.</td>
    </tr>
    <tr>   
      <td>git log --graph: Displays a visual ASCII graph showing how branches diverge and merge.</td>
    </tr>
    <tr>   
      <td>git log -n "number": Limits the output to a specific number of recent commits (e.g., git log -n 5)</td>
    </tr>
    <tr>   
      <td>git log -p (or --patch): Shows the full "diff" or actual code changes for each commit.</td>
    </tr>
    <tr>   
      <td>git log --stat: Shows statistics for files modified, including the number of lines added or deleted.</td>
    </tr>
    <tr>   
      <td>git log --author="Name": Filters the history to only show commits from a specific person.</td>
    </tr>
    <tr>   
      <td>git log --grep="keyword": Searches commit messages for a specific word or phrase.</td>
    </tr>
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
    <tr>
      <td rowspan="3">git merge</td>
      <td>Integrates independent lines of development into a single branch. </td>
    </tr>
    <tr>
      <td>Brings work from one branch (e.g., a feature branch) into another (e.g., the main branch).</td>
    </tr>
    <tr> 
          <td>
            <p>git merge Workflow: merge a feature branch into main:</p>
            <ol type="a">
                <li>Switch to the target: git checkout main.</li>
                <li>Update it: git pull origin main (to ensure you have the latest changes).</li>
                <li>Merge the feature: git merge feature-branch-name.</li>
                <li>Finish: If there were conflicts, resolve them and then git commit to finalize.</li>
            </ol>
          </td>
    </tr>
  </tbody>
</table>  
  
5. 🌐 Remote Setup - Link local repo to remote:
- What is git remote add origin <remote_repository_url>?
- What is git remote -v?
- What is git remote show origin?

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
      <td rowspan="2"> git remote add origin "remote_repository_url" </td>     
      <td>Creates a create a link between your local Git repository and a remote server</td>
    </tr>
    <tr>
        <td>
        <p>git merge Workflow: merge a feature branch into main:</p>
        <ul style="list-style-type:square;">
            <li>git remote add: Instructs Git to create a new connection record to a remote repository.</li>
            <li>origin: An industry standard shorthand name (or alias) for the remote URL.</li>
            <li>remote_repository_url: Remote Repo URL (e.g., https://github.com/user/repo.git).</li>
        </ul>
        <p> Once a remote is configured, you can use its shortname in commands like git fetch "remote", git pull "remote", and git push "remote" to exchange data with that repository. </p>
        </td>
    </tr>
    <tr>
      <td rowspan="2"> git remote </td>     
      <td>Lists shortnames/aliases of the remotes you have configured. </td>
    </tr>
    <tr>
        <td>
        <p>Other common git remote commands:</p>
        <ul style="list-style-type:square;">
            <li>git remote -v: Lists existing remotes with their URLs</li>
            <li>git remote show origin: Displays detailed information about a specific remote, including fetch/push URLs and tracking branches.</li>
        </ul>
        </td>
    </tr>
  </tbody>
</table>

6. 🚀 Remote Repo: New Project
    - What is git fetch? git fetch <remote>?
    - hat is git merge? git merge "remote"?
    - What is git pull? git pull <remote>?
    - What is git push? git push <remote>?
    - What is the difference between git push -u origin HEAD vs git push origin <branch-name>?
    - What is git push -u origin main or git push <remote> <branch>?
    - What is a pull request?

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
      <td rowspan="3"> git fetch </td>     
      <td>Downloads data from the remote but does not merge it into your local work.</td>
    </tr>
    <tr>
        <td>
        <p>How git fetch works:</p>
        <ul style="list-style-type:square;">
            <li>Git connects to the specified remote repository (usually origin by default).</li>
            <li>It downloads any new commits, branches, and tags that you don't have locally.</li>
            <li>Updates remote-tracking branches (e.g., origin/main or origin/develop), which are local mirrors of the remote branches' state.</li>
            <li>Local like main branch and your working directory remain unchanged.</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>
        <p>Common git fetch commands:</p>
        <ul style="list-style-type:square;">
            <li>git fetch origin: Fetches updates from the remote named "origin".</li>
            <li>git fetch "remote-name": Fetches updates from a specific remote, such as upstream.</li>
            <li>git fetch --all: Fetches updates from all configured remotes.</li>
            <li>git fetch --prune: Removes references to branches that no longer exist on the remote repository</li>
            <li>git fetch origin "branch-name": Fetches only a specific branch's updates. </li>
        </ul>
        </td>
    </tr>
    <tr>
      <td rowspan="4"> git pull </td>     
      <td>Updates your local branch with the latest changes from a remote repository. Shorthand for fetch and integrate</td>
    </tr>
    <tr>
        <td>
        <p>NB: git pull is a local command used on your machine to sync your own copy of the code. </p>
        <p>Core Mechanism - git pull command performs a two-step process in one command:</p>
        <ul style="list-style-type:square;">
            <li>git fetch: Downloads new commits, files, and references from remote repo to your local machine without altering your current work.</li>
            <li>git merge (default): Immediately integrates those downloaded changes into your active local branch.</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>
        <p>Common git pull commands:</p>
        <ul style="list-style-type:square;">
            <li>git pull: Fetches and merges changes from the default remote (e.g. origin) into your current branch.</li>
            <li>git pull "remote" "branch": Pulls changes from a specific remote and branch (e.g., git pull origin main).</li>
            <li>git pull --rebase: Fetches changes but uses git rebase instead of a merge, resulting in a cleaner, linear commit history.</li>
            <ul>
                <li>Integrates changes from one branch onto another by moving or reapplying a series of commits to a new base commit</li>
                <li>It is an alternative to git merge that results in a cleaner, linear project history, free of unnecessary merge commits. </li>
            </ul> 
            <li>git pull --ff-only: Only updates if it can "fast-forward" without creating a new merge commit; it fails if your local branch has diverged.</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>
        <p>Common git pull - Key Considerations commands:</p>
        <ul style="list-style-type:square;">
            <li>Action - 	Downloads and merges changes.</li>
            <li>Safety: Risk of merge conflicts.</li> 
            <li>Use Case: Quick synchronization when you trust the remote.</li>
        </ul>
        </td>
    </tr>
    <tr>
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

7. 🧹 Optional Additions for Advanced Users
- What is git config --global user.name and user.email?
- What is git stash and git stash pop?
- What is the difference between git rebase and git merge?
- What is the difference between git reset and git revert?