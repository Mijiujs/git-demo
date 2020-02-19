# gittest
git 分布式版本控制系统

初始化
git config 查看git配置
gif config --global user.name <name>
git config --global user.email <email>
git init 创建git仓库
git clone <url> 从远程库克隆

提交撤销提交
git add <file1> <file2>工作区添加到暂存区
git add . 当前目录都提交
git commit -m <message> 暂存区提交到仓库
git commit --amend -m <message> 替代上次提交，改写上一次commit信息
git checkout -- <file> 丢弃工作区文件的修改
git reset HEAD 丢弃暂存区的修改 git reset HEAD <file>
git rm <file> 删除文件，加-f强制删除
git mv <name1> <name2> 文件换名字并且提交到暂存区

状态历史
git status 显示文件的变更信息
git diff 查看修改内容
git log 查看当前分支commit历史 --stat 以及每次发生变更的文件 
git log --oneline 
git reset --hard <commit_id> 回到某个版本 HEAD表示当前版本，HEAD^^表示上上个版本,HEAD~100回到上100个版本
git log --graph 查看分支合并图
git reflog 查看命令历史

分支
git branch 查看本地分支 -r查看远程分支 -a远程+本地
git branch <dev> 创建分支
git branch <dev> <commit> 新建一个分支指向指定commit
git branch -d <dev> 删除分支 -D强制
git checkout <dev> || git switch <dev> 切换分支
git checkout -b <dev> || git switch -c <dev> 创建并切换到分支
git merge <dev> 把分支合并到当前分支
git cherry-pick <c commit-id> <d commit-id> 把多个不同分支的提交合并到当前分支

储藏
git stash save <msg>储藏
git stash list 查看储藏区
git stash apply 恢复
git stash drop 删除
git stash pop 恢复+删除

远程仓库
git remote add origin <url> 关联远程库
git remote 查看远程库
git remote -v 更详细的查看远程库，可以知道哪些可以推拉

git push <远程主机名> <本地分支名>:<远程分支名> 推送某分支,若失败先git pull抓取远程的新提交
git push -u origin master 将本地master分支推送到origin主机，同时制定origin为默认主机
git push --set-upstream origin test
git push origin -d <remote-branch> 删除远程分支

git branch <branch> origin/branch-name 新建本地分支并和远程分支关联
git branch --set-upstream <branch> origin/branch-name 使本地已有分支和远程分支关联

标签
git tag <tag> 为当前commit打标签
git tag <tag> <commit> 为指定cimmit打标签
git tag -d <tag> 删除分支
git tag 查看历史
git show <tag> 看具体标签的详情

git push origin <tagname> 推送一个本地标签
git push origin --tags 推送全部未推送过的本地标签
git push origin :refs/tags/<tagname> 删除一个远程标签

远程创建分支,本地看不到最新分支
git remote update origin --prune

11
22