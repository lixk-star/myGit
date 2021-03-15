# git命令

git config 配置   /etc/gitconfig --systemxit       ~/.gitconfig --global用户   .git/config --local当前

 git config --local user.email 'lixiankai@broadtree.cn'

 git config --global user.email 'lixiankai@broadtree.cn'

git sastus 状态

 rm -rf test.txt 删除文件

vi text.txt 编辑文件

cat text.txt 查看文件

pwd 当前目录

 :wq 保存退出

shift+A 插入内容

git checkout -- text.txt 去掉之前编辑的内容

echo 'welcome' > text.txt 覆盖之前内容

 git commit -m 'second commit'

git rm text2.txt



git rm:（执行两个操作）

1.删除了一个文件  

2.将被删除的文件纳入暂存区

恢复（执行两个动作）

（ git reset HEAD text2.txt 暂存区 回到工作区）

（git checout -- text2.txt工作区撤销之前的修改）



rm :

将文件删除，这时，被删除的文件未被纳入暂存区中

执行git add 文件



文件重命名

git mv text.txt text2.txt



git commit --amend -m '修正过后的消息'    （描述消息修改）

git log --pretty=oneline 以行显示 

git log -n  指定显示消息

git branch

git branch mew_branch

git checkout new_branch 



分支

git branch（查看）

git branch 文件名（创建）

git checkout 文件名 （切换分支）

git checkout -b 文件名  （创建并切换）

git branch -d 文件名 删除分支

git merge 文件名 （合并分支）



git log --graph

git merge --no-ff 分支名（保留分支信息）



git reset --hard HEAD^  版本回退rgit reset --hard HEAD~n

git reset --hard HEAD_id

git relog 全部历史记录



git checkout commit_id  游离状态

git add

git chechout mycommit 61e5936 

 

git checkout -- file 从工作区中移除修改（相对于暂存区最后一次修改）



git checkout -m file newfile  修改名



保存现场

git stash

git stash list

恢复现场

git stash apply(stash内容需要通过git stash drop stash @{n})手动删除

git stash pop (恢复同时，删除)

git stash apply stash @{n} 恢复指定stash



标签

git tag 查看 git tag -l "v1.0"

git tag v1.0

git tag -a -m '2.0 released'

git tag -d v1.0 删除

git blame <file>  文件相关作者信息



git diff：(比较的是工作区与暂存区的差别)

git diff HEAD:(比较的是最新提交与工作区的差别)

git diff --cached commit_id:(比较的是最新提交与暂存区的差别)

'

git remote show （与远程仓库相关联是）

git remote show  origin  （远程仓库详尽信息）

git branch -a (远程分支和本地分支)

git branch -av

：2,4d 删除多行

dd删除一行



git pull == git fetch + git merge



stackoverflow.com

git config --global alias.br branch

、

git push --set-upstreom origin develop  增加远程分支 == git push -u origin test

git checkout -b develop origin/develop  拉取  增加远程分支 创建对应本地分支==git checkout --track develop origin/develop



git branch -d file 删除本地分支

git push = git push origin srcBranch(本地）:destBranch（远程）

git pull = git pull origin srcBranch(远程）:destBranch（本地）

git push = git push origin   :dest（远程） 删除远程分支 == git push origin --delete develop



git push --set-upstream origin develop:develop2 (推送去远程，对应另一个名)

git pushi origin HEAD :develop2  (将当前分支推送到远程分支)

标签

git tag 查看

git tag v1.0

git tag -a v2.0 -m 'v2.0 released'

git push origin v1.0 v2.0 ..  (推送远程分支)

git  push origin --tags(推送全部标签)

gie pull 

git push origin :refs/tag/v6.0 删除标签

it push origin --delete tag v6.0删除标签

git tag -d v5.0 删除本地的标签

git fetch origin tag v7.0 拉取远程一个分支



git remote prune origin 删除远程已经删除的分支

git log origin/master 查看远程分支记录

git refspec

 git push --set-upstream origin dev 推送至远程并创建一样的分支

git checkout -b dev origin/dev  本地创建并关联远程

git checkout --track origin/dev 本地创建并关联远程 

git push origin src(源):dev（目标）  

git pull origin src(源):dev（目标）

git push origin --detele dev 删除远程分支

git 裸库（没有工作区）

git init --bare 建裸库

子模块

git submodule

git submodule add 路径  目录

git clone submodule add 路径  目录 --recursive  包括git clone子模块

git submodule foreach git pull  更新全部子模块

git submodule  init 单个更新1

git sumodule updatae  --recursive  单个更新2

git rebase -i cmmit_id 合并

git cherry-pick commit_id



git mergr dev

git rebase dev

