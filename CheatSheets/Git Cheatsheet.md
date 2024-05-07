## Configuration

- `git config --global user.name "Your Name"`: Set your username globally.
- `git config --global user.email "youremail@example.com"`: Set your email globally.
- `git config --list`: List your Git configurations.

## Basic Commands

- `git init`: Initialize a new Git repository.
- `git clone <repository>`: Clone a remote repository.
- `git status`: View the status of your working directory.
- `git add <file>`: Stage a file for commit.
- `git commit -m "Commit message"`: Commit staged changes.
- `git commit -a -m "Commit message"`: Commit all tracked changes.
- `git log`: View commit history.

## Branching

- `git branch`: List all branches (current branch highlighted with an asterisk).
- `git branch <branch-name>`: Create a new branch.
- `git checkout <branch-name>`: Switch to an existing branch.
- `git checkout -b <branch-name>`: Create and switch to a new branch.
- `git merge <branch-name>`: Merge changes from another branch.
- `git branch -d <branch-name>`: Delete a merged branch.
- `git branch -D <branch-name>`: Force delete an unmerged branch.

## Remote Repositories

- `git remote add <name> <url>`: Add a remote repository.
- `git remote -v`: List remote repositories with URLs.
- `git push <remote> <branch>`: Push changes to a remote repository.
- `git pull <remote> <branch>`: Pull changes from a remote repository.
- `git fetch <remote>`: Fetch remote changes without merging.

## Stashing

- `git stash`: Stash changes in a temporary area.
- `git stash list`: List stashed changes.
- `git stash apply`: Apply the latest stashed changes.
- `git stash pop`: Apply and remove the latest stashed changes.
- `git stash drop`: Discard the latest stashed changes.

## Undoing

- `git reset <file>`: Unstage a file.
- `git reset --hard HEAD`: Discard all local changes.
- `git revert <commit>`: Create a new commit that undoes a previous commit.
- `git commit --amend`: Modify the latest commit message or content.

## Tagging

- `git tag`: List all tags.
- `git tag <tag-name>`: Create a lightweight tag at the current commit.
- `git tag -a <tag-name> -m "Tag message"`: Create an annotated tag.
- `git push --tags`: Push tags to a remote repository.

## Advanced

- `git cherry-pick <commit>`: Apply a specific commit to the current branch.
- `git rebase <base-branch>`: Reapply commits on top of another branch.
- `git reflog`: View a log of all Git references (useful for undoing mistakes).
- `git remote show <remote>`: Display detailed information about a remote repository.
- `git clean -n`: Preview untracked files and directories that will be removed.
- `git clean -f`: Remove untracked files and directories forcefully.
- `git blame <file>`: Show who last modified each line of a file.
- `git bisect start`: Start a binary search to find the commit that introduced a bug.
- `git bisect bad`: Mark the current commit as bad in the binary search.
- `git bisect good <commit>`: Mark a specific commit as good in the binary search.
- `git rebase -i <base-branch>`: Interactively rebase and edit commits before applying.
- `git log --graph`: Display a visual commit history graph.
- `git submodule add <repository>`: Add a submodule to your repository.
- `git submodule update --init`: Initialize and update submodules.
- `git stash branch <branch-name>`: Create a new branch from a stash.

## Collaboration

- `git remote rename <old-name> <new-name>`: Rename a remote repository.
- `git remote remove <remote>`: Remove a remote repository.
- `git remote set-url <remote> <url>`: Change the URL of a remote repository.
- `git fetch --prune`: Fetch and remove remote branches that no longer exist.
- `git push <remote> --delete <branch>`: Delete a remote branch.
- `git push <remote> --tags --force`: Force push tags to a remote repository.
- `git pull --rebase <remote> <branch>`: Pull changes and rebase them onto your branch.

## Customization

- `git config --global alias.<shortcut> <command>`: Create a custom Git shortcut.
- `git config --global core.excludesfile <file>`: Specify global ignore patterns.

## Troubleshooting

- `git fsck --full`: Check the integrity of your Git objects.
- `git clean -df`: Remove untracked files and directories forcefully, including ignored ones.
- `git reset --hard <commit>`: Reset the branch and working directory to a specific commit.
- `git revert --no-commit <commit>..HEAD`: Revert a range of commits without committing.
- `git cherry-pick --abort`: Abort a cherry-pick in progress.