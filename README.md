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

git diff --name-status HEAD~/2 HEAD~/3


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
