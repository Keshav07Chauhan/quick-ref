> **Source & Credit**
>
> This Git cheat sheet is derived from the official Git documentation  
> provided by **The Git Project** at https://git-scm.com.
>
> Original cheat sheet: https://git-scm.com/cheat-sheet
>
> Git is a trademark of Software Freedom Conservancy.

---

# Git Cheat Sheet

## Getting Started

### Start a new repo

```bash
git init
```

### Clone an existing repo

```bash
git clone <url>
```



---

## Prepare to Commit

### Add untracked file or unstaged changes

```bash
git add <file>
```

### Add all untracked files and unstaged changes

```bash
git add .
```

### Choose which parts of a file to stage

```bash
git add -p
```

### Move file

```bash
git mv <old> <new>
```

### Delete file

```bash
git rm <file>
```

### Tell Git to forget about a file without deleting it

```bash
git rm --cached <file>
```

### Unstage one file

```bash
git reset <file>
```

### Unstage everything

```bash
git reset
```

### Check what you added

```bash
git status
```



---

## Make Commits

### Make a commit (and open text editor to write message)

```bash
git commit
```

### Make a commit

```bash
git commit -m 'message'
```

### Commit all unstaged changes

```bash
git commit -am 'message'
```



---

## Move Between Branches

### Switch branches

```bash
git switch <name>
# OR
git checkout <name>
```

### Create a branch

```bash
git switch -c <name>
# OR
git checkout -b <name>
```

### List branches

```bash
git branch
```

### List branches by most recently committed to

```bash
git branch --sort=-committerdate
```

### Delete a branch

```bash
git branch -d <name>
```

### Force delete a branch

```bash
git branch -D <name>
```



---

## Diff Staged/Unstaged Changes

### Diff all staged and unstaged changes

```bash
git diff HEAD
```

### Diff just staged changes

```bash
git diff --staged
```

### Diff just unstaged changes

```bash
git diff
```



---

## Diff Commits

### Show diff between a commit and its parent

```bash
git show <commit>
```

### Diff two commits

```bash
git diff <commit> <commit>
```

### Diff one file since a commit

```bash
git diff <commit> <file>
```

### Show a summary of a diff

```bash
git diff <commit> --stat
git show <commit> --stat
```



---

## Ways to Refer to a Commit

Every time we say `<commit>`, you can use any of these:

* a branch (e.g., `main`)
* a tag (e.g., `v0.1`)
* a commit ID (e.g., `3e887ab`)
* a remote branch (e.g., `origin/main`)
* current commit (`HEAD`)
* 3 commits ago (`HEAD^^^` or `HEAD~3`)
  

---

## Discard Your Changes

### Delete unstaged changes to one file

```bash
git restore <file>
# OR
git checkout <file>
```

### Delete all staged and unstaged changes to one file

```bash
git restore --staged --worktree <file>
# OR
git checkout HEAD <file>
```

### Delete all staged and unstaged changes

```bash
git reset --hard
```

### Delete untracked files

```bash
git clean
```

### “Stash” all staged and unstaged changes

```bash
git stash
```



---

## Edit History

### “Undo” the most recent commit (keep your working directory the same)

```bash
git reset HEAD^
```

### Squash last 5 commits into one

```bash
git rebase -i HEAD~6
```

*(Then change “pick” to “fixup” for any commit you want to combine with the previous one)*

### Undo a failed rebase

```bash
git reflog BRANCHNAME
# find the right commit in reflog
git reset --hard <commit>
```

### Change a commit message (or add a file you forgot)

```bash
git commit --amend
```



---

## Code Archaeology

### Look at a branch’s history

```bash
git log main
git log --graph main
git log --oneline
```

### Show every commit that modified a file

```bash
git log <file>
```

### Show every commit that modified a file, even before rename

```bash
git log --follow <file>
```

### Find every commit that added or removed some text

```bash
git log -G banana
```

### Show who last changed each line of a file

```bash
git blame <file>
```



---

## Combine Diverged Branches

### Combine with rebase

```bash
git switch banana
git rebase main
```

### Combine with merge

```bash
git switch main
git merge banana
```

### Combine with squash merge

```bash
git switch main
git merge --squash banana
git commit
```

### Bring a branch up to date (fast-forward)

```bash
git switch main
git merge banana
```

### Copy one commit onto current branch

```bash
git cherry-pick <commit>
```



---

## Restore an Old File

### Get the version of a file from another commit

```bash
git checkout <commit> <file>
# OR
git restore <file> --source <commit>
```



---

## Add a Remote

```bash
git remote add <name> <url>
```



---

## Push Your Changes

### Push `main` to remote `origin`

```bash
git push origin main
```

### Push current branch to its remote tracking branch

```bash
git push
```

### Push a branch you’ve never pushed before

```bash
git push -u origin <name>
```

### Force push

```bash
git push --force-with-lease
```

### Push tags

```bash
git push --tags
```



---

## Pull Changes

### Fetch changes (but don’t change local branches)

```bash
git fetch origin main
```

### Fetch and rebase

```bash
git pull --rebase
```

### Fetch and merge

```bash
git pull origin main
# OR
git pull
```



---

## Configure Git

### Set a config option

```bash
git config user.name 'Your Name'
```

### Set option globally

```bash
git config --global ...
```

### Add an alias

```bash
git config alias.st status
```

### See all config options

```bash
man git-config
```



---

## Important Files

* Local git config:

  ```text
  .git/config
  ```
* Global git config:

  ```text
  ~/.gitconfig
  ```
* List of files to ignore:

  ```text
  .gitignore
  ```

---

## Learn Git Properly (Recommended Resources)

If this cheat sheet feels cryptic, that’s normal.  
Git is not intuitive — it’s a graph database with a CLI.

### Official Documentation (Authoritative)
- Git Book (free, official):  
  https://git-scm.com/book/en/v2

### Interactive Learning (Best for beginners)
- Learn Git Branching (visual + hands-on):  
  https://learngitbranching.js.org/

### Practical Workflow Guides
- GitHub Git Handbook:  
  https://docs.github.com/en/get-started/using-git

### Reference-Level Depth
- `man git` (installed locally)
- `man git-rebase`, `man git-reset`, `man git-commit`


---

## License & Attribution Notice

This document aggregates and reformats material from the official  
Git documentation available at https://git-scm.com.

All credit for original content belongs to **The Git Project**.  
This file is provided for educational and reference purposes only.
