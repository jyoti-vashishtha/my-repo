PS D:\git-repo> git --version
git version 2.54.0.windows.1
PS D:\git-repo> git config --global user.name"jyoti-vashishtha"
PS D:\git-repo> git config --global user.email jyotivashishtha110@gmail.com
git config --list :- for user name or email verification 
git init :- for initialization for which git repo track files
.git/ :- hidden file that is present on git 

steps for git commit:- 1 git status :- use to check the status at first we se repo is empty so we add files on it. {working area}
                       2 git add file name :- ex:- git add index.html for all we add *. for adding the files in repo {staging area}
                       3 git status:- for checking 
                       4 git commit -m" this is version 1" :- local area for sending messige staging to local area.
                       5 git branch :- check which branch we are working 

                       gitcommit;- creating a permanent record in repository history .
                       6:- git log :- use to check commit is done.
1:- git diff;- check the past and present file difference.
  if some changes in file again put commit steps on it.                     
2;- view files from old commit :- git show fileid:file name
            step1;- git log
            step2;- git show fileid:filename
 3:- get old version with git checkout;- git checkout fileid --file name
 4:-1  undo the changes:- git restore .(. mean for all files) for specific:- git restore filename
    2  we added the changes using git :- git restore --staged<filename> to unstage.
                                         git restore filename   <undo changes in working directory>
    3:- to get the staged changes:- git restore --worktree filename
     4:-if we did commit also wrong file:-  git reset --soft HEAD^(uncommit and keep the changes)
                                            git reset --hard HEAD^(uncommit amd discard the change)
   log options :-git log -p -2(last two commit with diff)
   git log --stat(summary of changes)
   git log --pretty=oneline(commit ki information one line me ho )
   git log --pretty=format:"%h - %an,%ar : %s"
   git log -S function_name

git remote or git remote -v ;- check ki local repo or remote repo linked  or not
git push ;- local to remote repo 
git pull;- remote to local repo 

PS D:\my-repo> git branch
* main
PS D:\my-repo> git branch design       syntax:-git branch newbranchname
PS D:\my-repo> git branch
  design
* main
PS D:\my-repo> git checkout design
M       readme.md
Switched to branch 'design'
PS D:\my-repo> git branch 
* design
  main

  PS D:\my-repo> git status
On branch main

nothing to commit, working tree clean
PS D:\my-repo> git add index.html
PS D:\my-repo> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   index.html

PS D:\my-repo> git commit -m"this is v4"
[main e042964] this is v4
 1 file changed, 1 insertion(+), 1 deletion(-)
PS D:\my-repo> git log
Author: jyotivashishtha110@gmail.com <jyotivashishtha110@gmail.com>
Date:   Mon Jun 22 01:50:27 2026 -0700

    this is v4

commit f775bb9a0f8a0bf6c53644693798cf2e10427dfa (origin/main, origin/HEAD)
Author: jyoti-vashishtha <jyotivashishtha110@gmail.com>
Date:   Mon Jun 22 01:16:48 2026 -0700


Date:   Mon Jun 22 01:03:02 2026 -0700
PS D:\my-repo> git push
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Writing objects: 100% (3/3), 348 bytes | 348.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/jyoti-vashishtha/my-repo.git
   f775bb9..e042964  main -> main
PS D:\my-repo> git branch
* main
PS D:\my-repo> git branch design
PS D:\my-repo> git branch
  design
* main
PS D:\my-repo> git checkout design
M       readme.md
Switched to branch 'design'
PS D:\my-repo> git branch 
PS D:\my-repo> git status
On branch design
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html
        modified:   readme.md
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        style.css
no changes added to commit (use "git add" and/or "git commit -a")
PS D:\my-repo> git add *
PS D:\my-repo> git status
On branch design
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   index.html
        modified:   readme.md
        new file:   style.css

PS D:\my-repo> git commit -m"added design for website"
[design bacafc1] added design for website
 3 files changed, 79 insertions(+), 3 deletions(-)
 create mode 100644 style.css
PS D:\my-repo> git log
Author: jyotivashishtha110@gmail.com <jyotivashishtha110@gmail.com>
Date:   Mon Jun 22 02:52:17 2026 -0700
    added design for website

Author: jyotivashishtha110@gmail.com <jyotivashishtha110@gmail.com>
Date:   Mon Jun 22 01:50:27 2026 -0700

    this is v4

commit f775bb9a0f8a0bf6c53644693798cf2e10427dfa
Author: jyoti-vashishtha <jyotivashishtha110@gmail.com>
Date:   Mon Jun 22 01:16:48 2026 -0700
PS D:\my-repo> git branch
* design
  main
PS D:\my-repo> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS D:\my-repo> git checkout design
Switched to branch 'design'

PS D:\my-repo> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS D:\my-repo> git merge design       git merge branch name

Updating e042964..47c759b
Fast-forward
 index.html |  12 +++++--
 readme.md  | 108 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++-
 style.css  |  54 +++++++++++++++++++++++++++++++
 3 files changed, 171 insertions(+), 3 deletions(-)
 create mode 100644 style.css
