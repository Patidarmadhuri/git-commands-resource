1. Beginner Git Commands

1.1 git init

Purpose: Initializes a new Git repository in the current directory.Usage:

git init

Explanation: This command creates a .git directory in your project folder, which Git uses to track version history.

1.2 git clone <repo>

Purpose: Clones an existing repository from a URL.Usage:

git clone https://github.com/username/repository.git

Explanation: This command copies the entire repository (with history and all branches) to your local machine.

1.3 git status

Purpose: Shows the status of changes in your working directory.Usage:

git status

Explanation: It shows which files are staged, modified, or untracked.

1.4 git add <file>

Purpose: Adds files to the staging area to prepare them for a commit.Usage:

git add index.html
git add .  # Adds all files

Explanation: Stages the changes you want to commit. The . stages all modified files.

1.5 git commit -m "message"

Purpose: Commits the staged changes with a descriptive message.Usage:

git commit -m "Add new homepage layout"

Explanation: This command saves your changes in the local repository with a message describing what was done.

1.6 git log

Purpose: Displays the commit history.Usage:

git log

Explanation: Shows a list of all commits with the commit hashes, dates, and messages.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

2. Intermediate Git Commands

2.1 git diff

Purpose: Shows the differences between files or commits.Usage:

git diff
git diff --staged  # Shows staged changes

Explanation: git diff shows changes in your working directory that are not staged. --staged compares staged changes to the last commit.

2.2 git branch

Purpose: Lists, creates, or deletes branches.Usage:

git branch  # List all local branches
git branch <branch-name>  # Create a new branch
git branch -d <branch-name>  # Delete a branch

Explanation: Use git branch to create and manage branches, which help in working on different features independently.

2.3 git checkout <branch>

Purpose: Switches between branches.Usage:

git checkout develop

Explanation: Switches to the specified branch. It's necessary to be on the correct branch to work on a specific feature.

2.4 git merge <branch>

Purpose: Merges changes from one branch into another.Usage:

git checkout main
git merge feature-branch

Explanation: Combines changes from the feature-branch into the main branch. Conflicts might arise if changes overlap.

2.5 git remote -v

Purpose: Displays the URLs of the remote repositories.Usage:

git remote -v

Explanation: This command is useful to verify where your local repository is connected and which remote repository it will push to or pull from.

2.6 git push

Purpose: Pushes commits from your local repository to a remote repository.Usage:

git push origin main

Explanation: This uploads your changes to the remote repository. You must specify the branch you're pushing to (e.g., main).

2.7 git pull

Purpose: Fetches changes from the remote repository and merges them into your local repository.Usage:

git pull origin main

Explanation: Pulls down the latest changes from the remote main branch and merges them with your local copy.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

3. Advanced Git Commands

3.1 git rebase <branch>

Purpose: Re-applies commits on top of another branch to maintain a clean history.Usage:

git checkout feature-branch
git rebase main

Explanation: Rebasing allows you to place your changes on top of another branch, eliminating unnecessary merge commits and keeping the history linear.

3.2 git reset

Purpose: Resets your repository to a previous commit or state.Usage:

git reset --hard HEAD~1  # Reset to the previous commit
git reset <file>  # Unstage a file

Explanation: git reset can undo commits or unstage changes. --hard discards changes completely.

3.3 git cherry-pick <commit>

Purpose: Applies a specific commit from another branch.Usage:

git cherry-pick abc1234  # Apply commit abc1234 to the current branch

Explanation: You can pick a commit from one branch and apply it to your current branch.

3.4 git stash

Purpose: Stashes your changes to temporarily save them without committing.Usage:

git stash
git stash pop  # Apply stashed changes

Explanation: If you need to switch tasks but don't want to commit your changes, git stash saves your work temporarily, and git stash pop re-applies them when needed.

3.5 git reflog

Purpose: Displays the history of HEAD and recent changes to it.Usage:

git reflog

Explanation: git reflog helps you track where HEAD and other references have been, allowing you to recover lost commits or references.
