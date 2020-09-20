# Advanced Git Tutorial
Here are some git commands that come in handy. They are listed from easy -> hard. 

# 

    git status
check the status of current repo/branch

    git log
check the history of current repo/branch

    git clone <url>
clone the online repo into the local machine, if you want to name the local directory differently, you can do `git clone <url> <directory name>`

    git init
initialize a local directory to be a git repository

    git add <files>
add changes into the staging area, note that `git add .` will add all changes

    git commit -m <msg>
commit all changes in the staging area into the current branch

    git push <remote> <branch>
sync your changes onto a branch of an online repo(remote). note that sometimes when your local is behind online repo, you may need to do a `git pull` before `git push`. \<remote> will be `origin` most of the time, unless you have two or more remotes at the same time.  
*Note: Don't use `git push -f` unless you are absolutely sure what you are doing*

    git pull <remote> <branch>
sync the online changes onto your local repo. This is better than `git pull`, as a `git pull` command by itself varies its behavior in different git versions.  
*Note: A `git pull` is equivalent to a `git fetch` with a `git merge`*

    git branch

list all branched in the current local repo. `git branch -a` also lists all remote branches.

    git branch <branch-name>
will create a local branch with `branch-name`. 

    git checkout <branch>/<commit id>
will switch from the current branch/commit to another branch/commit. 

    git diff <branch A> <branch B>
will list the difference between the two branches. 

    git merge <branch>
say you are on branch `master`, a command of `git merge dev` will merge all commits on `dev` branch onto `master`. Sometimes a `merge` would result in a merge conflict, which requires developers to solve the conflict by hand. 

    git fetch
one of the very convenient command that you should learn to use. Let's say you have an `origin` remote that points to a Github address, `fetch` will update all online repo changes onto `origin/<branch-name>`, but not your local branches. You can then use for example `git merge origin/master` or `git pull origin master` to sync your local branch. `fetch` is good because you can always check the difference between origin and local, to prevent unwanted conflicts before your merge. 

    git reset (--soft/--mixed/--hard) <branch>/<commit id>
another very useful command. A common use case is when you want to discard every single change you've made to your working directory and restart, you can do `git reset --hard HEAD` or `git reset --hard origin/master` to reset your current working dir. A detailed discussion of the difference between soft/mixed/hard is discussed in https://stackoverflow.com/questions/3528245/whats-the-difference-between-git-reset-mixed-soft-and-hard