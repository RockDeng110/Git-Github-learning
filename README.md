# Git-Github-learning
## records for git & github learning
1. Create a new repo on github
1. move the repo created on web to your local machine by git clone 
   1. If the repo is private, you need input the account&password of the reop on the github.
   1. before this step, you may need to install git and set the global settings on your local machine.
1. Create a new branch and checkout to the branch on your terminal.
1. Make changes(adding files or edit) and commit.
1. Send the changes to github
   1. using:   git push -u origin <BRANCH-NAME>
1. Make a new Pull Request on github.
1. Merge your pull request on github.
   1. May you need to delete the branch you created it in step 3.
1. checkout to master branch on your local machine(terminal).
1. Refresh the reop:
   1. use :    git pull
   
## more details, please refer to [github tutorial](https://services.github.com/on-demand/github-cli/merge-pull-request-github)

提交： git commit -m 

跳过 stage 提交： git commit -m -a


## 对比working directory, staged and commits 相互之间的差异：

1，  查看不同提交版本之间有差异的文件

git diff --name-status HEAD~2 HEAD~3


2， 查看working directory 和 staged/commits 之间的差异

git diff  [HEAD~N] [--] [file directory]


3，查看 staged 和 commits 之间的差异

git diff  --cached [HEAD~N] [--] [file directory]


4，查看不同commit 之间的差异

git diff commit1 commit2 [--] [file directory]



## 回复历史文件：

1，三棵树同时恢复历史版本（会检查工作目录下的文件）：

 git checkout [commit]
 

2，恢复单个文件的历史版本(不动HEAD指针)：

 git reset (comit) -- file
 
 # svn learning
 ##  critical commands
 1, svn log -l 3 -v
 
   查看最近的3个revision, 以及相互之间有改动的文件。
   
   
 2，svn log -v -r88:90
 
   查看从revision 88 - 90的log, 以及每一次commit有改动的文件
   
   
 3, svn diff -r77:78 [file directory]   
 
   查看某个文件在版本77和78之间的改动
   
 
 4,  svn up -r 147 myfile.py
   
   恢复某个文件到历史版本
   
   
 5,  svn info 查看代码仓库的url等信息
   
   
   
# git-svn
## critical commands
1, git-svn rebase

This will download all new changesets from Subversion, apply them to the last checkout from Subversion, and then re-apply your local changes on top of that.Just like git pull.


2, git-svn dcommit

When you’re ready to commit back to Subversion, execute it. Just like git push.


3, git-svn clone [url]

Checking out a Subversion repository.


4, 当 git svn rebase 出现冲突时

可以按错误提示解决问题： 1， 先修改冲突文件解决冲突；
                     2， git add 修改好的冲突文件；
                     3， git rebase --continue 重新执行git pull
                     
5, checkout svn 仓库

git-svn clone [-s] http://example.com/my_subversion_repo

