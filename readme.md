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
                                                                             