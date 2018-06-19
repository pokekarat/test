# test
Create a test project.

wifi-17-1-12:Program ekaratrattagan$ git status
fatal: Not a git repository (or any of the parent directories): .git

wifi-17-1-12:Program ekaratrattagan$ mkdir test
wifi-17-1-12:Program ekaratrattagan$ cd test
wifi-17-1-12:test ekaratrattagan$ git init
Initialized empty Git repository in /Users/ekaratrattagan/Program/test/.git/

wifi-17-1-12:test ekaratrattagan$ touch "readme" > README.txt
wifi-17-1-12:test ekaratrattagan$ ls
README.txt	readme

wifi-17-1-12:test ekaratrattagan$ git add .
wifi-17-1-12:test ekaratrattagan$ git commit -m "test"
[master (root-commit) b77b72d] test
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.txt
 create mode 100644 readme

wifi-17-1-12:test ekaratrattagan$ git push
fatal: No configured push destination.
Either specify the URL from the command-line or configure a remote repository using

    git remote add <name> <url>

and then push using the remote name

    git push <name>

wifi-17-1-12:test ekaratrattagan$ git remote -v
wifi-17-1-12:test ekaratrattagan$ git remote add origin https://github.com/pokekarat/test.git

wifi-17-1-12:test ekaratrattagan$ git remote -v
origin	https://github.com/pokekarat/test.git (fetch)
origin	https://github.com/pokekarat/test.git (push)

wifi-17-1-12:test ekaratrattagan$ git status
On branch master
nothing to commit, working tree clean
wifi-17-1-12:test ekaratrattagan$ git commit -m "test"
On branch master
nothing to commit, working tree clean
wifi-17-1-12:test ekaratrattagan$ git status
On branch master
nothing to commit, working tree clean
wifi-17-1-12:test ekaratrattagan$ git status
On branch master
nothing to commit, working tree clean
wifi-17-1-12:test ekaratrattagan$ ls
README.txt	readme
wifi-17-1-12:test ekaratrattagan$ git add .
wifi-17-1-12:test ekaratrattagan$ git commit -a "test create a new repo"
fatal: Paths with -a does not make sense.
wifi-17-1-12:test ekaratrattagan$ git commit -m "test create a new repo"
On branch master
nothing to commit, working tree clean
wifi-17-1-12:test ekaratrattagan$ git push
fatal: The current branch master has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin master

wifi-17-1-12:test ekaratrattagan$ git add .
wifi-17-1-12:test ekaratrattagan$ git status
On branch master
nothing to commit, working tree clean
wifi-17-1-12:test ekaratrattagan$ git remote -v
origin	https://github.com/pokekarat/test.git (fetch)
origin	https://github.com/pokekarat/test.git (push)
wifi-17-1-12:test ekaratrattagan$ ls
README.txt	readme
wifi-17-1-12:test ekaratrattagan$ git add README.txt
wifi-17-1-12:test ekaratrattagan$ git status
On branch master
nothing to commit, working tree clean
wifi-17-1-12:test ekaratrattagan$ git log
commit b77b72ddfe5981dad6c23942e03f1f8c0847eb93 (HEAD -> master)
Author: ekarat <pokekarat@gmail.com>
Date:   Tue Jun 19 11:24:00 2018 +0700

    test
wifi-17-1-12:test ekaratrattagan$ git push origin master
To https://github.com/pokekarat/test.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/pokekarat/test.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
wifi-17-1-12:test ekaratrattagan$ git pull
warning: no common commits
remote: Counting objects: 12, done.
remote: Compressing objects: 100% (7/7), done.
remote: Total 12 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (12/12), done.
From https://github.com/pokekarat/test
 * [new branch]      master     -> origin/master
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> master

wifi-17-1-12:test ekaratrattagan$ ls
README.txt	readme
wifi-17-1-12:test ekaratrattagan$ git status
On branch master
nothing to commit, working tree clean
wifi-17-1-12:test ekaratrattagan$ git branch -u origin/master
Branch 'master' set up to track remote branch 'master' from 'origin'.
wifi-17-1-12:test ekaratrattagan$ git status
On branch master
Your branch and 'origin/master' have diverged,
and have 1 and 4 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)

nothing to commit, working tree clean
wifi-17-1-12:test ekaratrattagan$ git status
On branch master
Your branch and 'origin/master' have diverged,
and have 1 and 4 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)

nothing to commit, working tree clean
wifi-17-1-12:test ekaratrattagan$ git pull
fatal: refusing to merge unrelated histories
wifi-17-1-12:test ekaratrattagan$ ls
README.txt	readme
wifi-17-1-12:test ekaratrattagan$ git add .
wifi-17-1-12:test ekaratrattagan$ git commit -m "test create a new repo"
On branch master
Your branch and 'origin/master' have diverged,
and have 1 and 4 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)

nothing to commit, working tree clean
wifi-17-1-12:test ekaratrattagan$ git pull
fatal: refusing to merge unrelated histories
wifi-17-1-12:test ekaratrattagan$ git pull origin/master --allow-unrelated-histories
fatal: 'origin/master' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
wifi-17-1-12:test ekaratrattagan$ git pull origin master --allow-unrelated-histories
From https://github.com/pokekarat/test
 * branch            master     -> FETCH_HEAD
Merge made by the 'recursive' strategy.
 README.md | 2 ++
 hello.txt | 2 ++
 2 files changed, 4 insertions(+)
 create mode 100644 README.md
 create mode 100644 hello.txt
wifi-17-1-12:test ekaratrattagan$ git status
On branch master
Your branch is ahead of 'origin/master' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
wifi-17-1-12:test ekaratrattagan$ git pull
Already up to date.
wifi-17-1-12:test ekaratrattagan$ git push
Counting objects: 5, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (4/4), done.
Writing objects: 100% (5/5), 546 bytes | 546.00 KiB/s, done.
Total 5 (delta 0), reused 0 (delta 0)
To https://github.com/pokekarat/test.git
   28d6981..e1d54fb  master -> master
wifi-17-1-12:test ekaratrattagan$ 
