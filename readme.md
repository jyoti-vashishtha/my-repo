```bash
git -v        
git config --global user.name"jyoti-vashishtha"
git config --global user.email jyotivashishtha110@gmail.com
git config --list
```
git -v                                                                                                                                           

```bash
PS D:\git-repo> git init
Initialized empty Git repository in D:/git-repo/.git/
PS D:\git-repo> ls

PS D:\git-repo> git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html
        readme.md
```bash
nothing added to commit but untracked files present (use "git add" to track)```PS D:\git-repo> git add readme.md
PS D:\git-repo> git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   index.html
        new file:   readme.md
`PS D:\git-repo> git commit -m "first v1 of index.html"
[master (root-commit) 400d100] first v1 of index.html
 2 files changed, 17 insertions(+)
 create mode 100644 index.html
 create mode 100644 readme.md
PS D:\git-repo> git branch
* master
PS D:\git-repo> git log
commit 400d100dc2b91331e16368c3d6ca25b8f551bbc8 (HEAD -> master)
Author: jyotivashishtha110@gmail.com <jyotivashishtha110@gmail.com>
Date:   Mon Jun 15 22:57:00 2026 -0700

    first v1 of index.html``bash
