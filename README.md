1️⃣ GIT CONFIGURATION
```
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --global color.ui auto
git config --list
git config --global core.editor "code --wait"
```

2️⃣ INITIALIZING A REPOSITORY
```
git init
git init <directory>
```
3️⃣ CLONING
```
git clone <repo-url>
git clone <repo-url> <folder-name>
git clone -b <branch> <repo-url>
git clone --depth=1 <repo-url>     # shallow clone
```
4️⃣ CHECK STATUS
```
git status
git status -s        # short format
```
5️⃣ ADD FILES
```
git add <file>
git add .            # all files
git add -p           # add in patches
git add *.js
```

6️⃣ COMMIT
```
git commit -m "message"
git commit -am "message"      # adds + commits tracked files
git commit --amend            # modify last commit
git commit --amend -m "new message"
```

7️⃣ REMOVE FILES
```
git rm <file>
git rm -r <folder>
git rm --cached <file>      # remove from git, keep local
```

8️⃣ MOVE / RENAME FILE
```
git mv old_name new_name
```

9️⃣ BRANCH OPERATIONS
```
git branch                     # list
git branch -v                  # with latest commit
git branch <name>              # create
git branch -d <name>           # delete
git branch -D <name>           # force delete
git branch -m old new          # rename
git branch -a                  # all branches incl remotes
git branch -r                  # remote branches only
```

🔟 SWITCH / CHECKOUT
```
git checkout <branch>
git checkout -b <new-branch>
git checkout -- <file>         # discard changes

git switch <branch>
git switch -c <branch>          # create & switch
```

1️⃣1️⃣ MERGE
```
git merge <branch>
git merge --no-ff <branch>      # force merge commit
```
1️⃣2️⃣ REBASE
```
git rebase <branch>
git rebase -i HEAD~5    # interactive rebase last 5 commits
git rebase --continue
git rebase --abort
```
1️⃣3️⃣ LOG COMMANDS (VERY IMPORTANT)
```
git log
git log --oneline
git log --graph --oneline --decorate --all
git log -p                    # patch view
git log --stat
git log --author="Name"
git log --since="2 days ago"
git log -- <file>
```

1️⃣4️⃣ DIFF
```
git diff                     # unstaged
git diff --staged            # staged
git diff HEAD
git diff <branch1> <branch2>
git diff <commit1> <commit2>
git diff -- <file>
```

1️⃣5️⃣ REMOTE COMMANDS
```
git remote -v
git remote add origin <url>
git remote rename origin upstream
git remote remove origin
```
1️⃣6️⃣ PUSH
```
git push
git push origin <branch>
git push -u origin <branch>
git push --force
git push --force-with-lease   # safer force push
```

1️⃣7️⃣ PULL
```
git pull
git pull origin <branch>
git pull --rebase
```
1️⃣8️⃣ FETCH
```
git fetch
git fetch --all
git fetch origin
```
1️⃣9️⃣ RESET (VERY IMPORTANT)
```
SOFT (keeps changes)
git reset --soft HEAD~1

MIXED (unstaged, default)
git reset HEAD~1

HARD (dangerous)
git reset --hard HEAD~1
git reset --hard origin/main
```
2️⃣0️⃣ RESTORE
```
git restore <file>                 # discard changes
git restore --staged <file>        # unstage
git restore .                      # restore all
```
2️⃣1️⃣ REVERT
```
git revert <commit_id>
git revert -n <commit>   # no-commit revert
```
2️⃣2️⃣ STASH
```
git stash
git stash save "message"
git stash list
git stash show
git stash show -p
git stash apply stash@{0}
git stash pop
git stash drop stash@{0}
git stash clear
```

2️⃣3️⃣ TAGS
```
Create tag
git tag v1.0
git tag -a v1.0 -m "Release 1.0"

List tags
git tag
git tag -l "v1.*"

Push tags
git push origin --tags
git push origin v1.0

Delete tags
git tag -d v1.0
git push origin :refs/tags/v1.0
```

2️⃣4️⃣ CHERRY-PICK (it merge master with a specific commit of an any branch)
```
git cherry-pick <commit>
git cherry-pick <commit1> <commit2>
git cherry-pick --continue
git cherry-pick --abort
```

2️⃣5️⃣ GIT CLEAN (remove untracked)
```
git clean -n    # preview
git clean -f    # delete
git clean -fd   # delete directories
```

2️⃣6️⃣ GIT SHOW
```
git show <commit>
git show HEAD
git show HEAD~1
git show <tag>
```

2️⃣7️⃣ GIT DESCRIBE
```
git describe
git describe --tags
git describe --all
```

2️⃣8️⃣ GIT GREP (search inside repo)
```
git grep "keyword"
git grep -n "function"
git grep -i "error"
git grep "main" -- *.js
```
2️⃣9️⃣ GIT ARCHIVE (zip repo)
```
git archive --format=zip HEAD > project.zip
```

3️⃣0️⃣ GIT BISECT (find bug commit)
```
git bisect start
git bisect bad
git bisect good <commit-id>
git bisect reset
```

3️⃣1️⃣ GIT SUBMODULE
```
git submodule add <repo-url>
git submodule update --init
git submodule update --recursive
```

3️⃣2️⃣ GIT HOOKS
```
.git/hooks/pre-commit
.git/hooks/post-commit
.git/hooks/pre-push
```

3️⃣3️⃣ GIT ALIASES (Shortcuts)
```
git config --global alias.st "status"
git config --global alias.co "checkout"
git config --global alias.br "branch"
```

⭐ BEST PRACTICE SHORT COMMAND SET (SUPER USEFUL)
```
git log --oneline --graph --decorate --all
git status -s
git diff HEAD~1
git restore .
git reset HEAD~
git stash pop
git push --force-with-lease
git rebase -i HEAD~5
```
