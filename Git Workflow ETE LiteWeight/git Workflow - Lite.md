# Git Workflow Overview
This page provides a comprehensive Git workflow guide designed for onboarding, documentation, and interactive learning. It covers essential Git commands and best practices across different workflow stages, including initialization, staging, committing, branching, remote repository management, collaboration, and advanced topics.

# 1. Repository Initialization
- `git init`: Create a new Git repository locally.
- `git clone <repo_url>`: Clone an existing remote repository.

Example
    # Initializes a new Git repository in the current directory
    `git init`

# Cloning a remote repository
`git clone https://github.com/user/repo.git`

# 2. Staging Changes
`git status`: Check the status of files in the working directory.
`git add <file>`: Stage specific files for commit.
`git add .`: Stage all changed files.

Example
`git status` # Shows modified and untracked files
`git add README.md` # Stages the README.md file for commit
`git add .` # Stage all changes

# 3. Committing Changes
`git commit -m "<message>"`: Commit staged changes with a descriptive message.

Best practice: Write clear, concise commit messages explaining the "why" behind changes.

Example
`git commit -m "Add user authentication feature"`

# 4. Branching and Merging
`git branch`: List all branches.
`git branch <branch_name>`: Create a new branch.
`git checkout <branch_name>`: Switch to a different branch.
`git checkout -b <branch_name>`: Create and switch to a new branch.
`git merge <branch_name>`: Merge another branch into the current branch.
Use branches to isolate features, bug fixes, or experiments.

Example
`git checkout -b feature/login` # Create and switch to a new branch
`git checkout main`
`git merge feature/login` # Merge feature branch into main branch

Diagram
main ---o---o---o---o---o
feature/login ---o---o---o

# 5. Remote Repository Management
`git remote add origin <repo_url>`: Link local repo to remote.
`git push -u origin <branch_name>`: Push local branch to remote and set upstream.
`git pull`: Fetch and merge changes from remote.

Example
# Add remote repository
`git remote add origin https://github.com/user/repo.git`
# Push branch to remote
`git push -u origin main`

# Pull latest changes
`git pull`

# 6. Collaboration Workflow
- Use feature branches for development.
- Regularly pull changes from the main branch to stay updated.
- Open pull requests for code review before merging.
- Resolve merge conflicts carefully by reviewing conflicting files.

Tips
- Commit frequently with meaningful messages.
- Keep branches focused and short-lived.
- Regularly sync with remote to avoid conflicts.
- Review code thoroughly during pull requests.

# 7. Advanced Topics
- `git rebase`: Reapply commits on top of another base tip for a cleaner history.
- `git stash`: Temporarily save changes without committing.
- `git log --oneline --graph --all`: Visualize commit history.
- Git hooks: Automate tasks like pre-commit checks.

Example
# Rebase feature branch onto main
`git checkout feature/login`
`git rebase main`

# Stash changes temporarily
`git stash`

# View commit history graph
`git log --oneline --graph --all`

Visual Aids and Resources
- Diagram illustrating branching and merging included above.
- For more detailed diagrams and workflows, see Gitflow Diagram Explained.
- Official Git documentation: https://git-scm.com/doc

This page now includes detailed examples, a simple branching diagram, and practical tips for best practices throughout the Git workflow stages.