# git-cheatsheet

| Command | Purpose | Description |
| :-- | :-- | :-- |
| `git init <dir>` | Basics | Create empty Git repo in specified directory |
| `git clone <repo>` | Basics | Create repo located at <repo> onto local machine |
| `git config user.name` | Basics | Define author name used for all commits in the current repo. use with `--global` flag for global tit config controls settings for the currently logged in user and all repositories|
|`git commit -m "<commit_message>"` | Basics | Commit the staged snapshot using <commit_message> as the commit message |
|`git status` | Basics | List which files are staged, unstaged and untracked |
|`git log` | Basics | Display entire commit history using the default format |
|`git diff` | Basics | Show unstaged changes between your index and working directory |
|`git revert <commit>` | Undo Change | Creates new commit that undoes all changes made in <commit> and apply to current branch |
|`git reset` | Undo Change | Reset staged changes to match most recent commit and leave working directory unchanged |
|`git reset --hard` | Undo Change | Reset staged changes to match most recent commit and overwrites all changes in working directory |
|`git reset <commit>` | Undo Change | Move current branch tip backwards to <commit>, reset staged changes to match and leave working directory unchanged |
|`git reset --hard <commit>` | Undo Change | Move current branch tip backwards to <commit> and resets staged changes and working directory to match. Uncommitted changes and all commits after <commit> will be DELETED |
|`git reset <file>` | Undo Change | Remove <file> from staged files and leave working directory unchanged. Unstages a file without overwriting any change |
|`git clean -n` | Undo Change | Shows files to be removed from working directory |
|`git cherry-pick <commit>` | Rewrite Git History | Apply the changes introduced by some existing commits |
|`git commit --amend` | Rewrite Git History | Replace last commit with staged changes and last commit combined. Use with nothing staged to edit last commit's message |
|`git rebase <base>` | Rewrite Git History | Rebase current branch onto <base>. <base> can be one of: commit ID, branch name, tag or a relative reference to HEAD |
|`git rebase -i <base>` | Rewrite Git History | Interactively rebase current base onto <base>. Editor would be launched interactively to view how the commits will be transferred to new base |
|`git reflog` | Rewrite Git History | Shows logs of changes to local repository's HEAD |
|`git branch` | Git branches | List all branches in repo |
|`git checkout -b <branch_name>` | Git branches | Create and check out on new branch <branch_name>. Run without `-b` flag to checkout an existing branch |
|`git merge <branch_name>` | Git branches | Merge <branch_name> into current branch |
|`git remote add <name> <url>` | Remote Repository | Creates a new connection to a remote repository. |
|`git fetch <remote> <branch>` | Remote Repository | Fetches a specific <branch> from the repository |
|`git pull <remote>` | Remote Repository | Fetches the specific <branch> remote's copy of current branch and immediately merge it into the local copy |
|`git pull --rebase <remote>` | Remote Repository | Fetches remote's copy of current branch and rebases it into the local copy. Uses git rebase instead of merge to integrate the branches |
|`git push <remote> <branch>` | Remote Repository | Pushes the branch to <remote> with committed commits |
|`git push <remote> --force` | Remote Repository | Forces the push to remote even if it results in a non-fast-forward merge (do not use unless you know what is happening here) |
|`git push <remote> --tags` | Remote Repository | Pushes local tags to the remote repository since tags are not automatically pushed when you push a branch |