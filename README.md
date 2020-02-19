# gittest
git 分布式版本控制系统

初始化

git init 创建git仓库
git config 查看git配置
gif config --global user.name <name>
git config --global user.email <email>
git clone <url> 从远程库克隆

提交撤销提交
git add <file1> <file2>工作区添加到暂存区
git add . 当前目录都提交
git commit -m <message> 暂存区提交到仓库
git checkout -- <file> 丢弃工作区文件的修改
git reset HEAD <file> 丢弃暂存区文件的修改
git rm <file> 删除文件，加-f强制删除
git mv <name1> <name2>

状态历史
git status 查看工作区+暂存区状态
git diff 查看修改内容
git log 查看提交记录
git reset --hard <commit_id> 回到某个版本 HEAD表示当前版本，HEAD^^表示上上个版本,HEAD~100回到上100个版本
git log --graph 查看分支合并图
git reflog 查看命令历史

分支
git branch 查看分支
git branch <dev> 创建分支
git branch -d <dev> 删除分支
git branch -D <name> 强制删除分支
git checkout <dev> 或 git switch <dev> 切换分支
git checkout -b <dev> 或 git switch -c <dev> 创建并切换到分支
git merge <dev> 把分支合并到当前分支
git cherry-pick <c commit-id> <d commit-id> 把多个不同分支的提交合并到当前分支

储藏
git stash 储藏
git stash list 查看储藏区
git stash apply 恢复
git stash drop 删除
git stash pop 恢复+删除

远程仓库
git remote add origin <address> 关联远程库
git remote 查看远程库
git remote -v 更详细的查看远程库，可以知道哪些可以推拉
git push -u origin master 第一次推送master分支的所有内容
git push origin <branch-name> 推送某分支,若失败先git pull抓取远程的新提交

git checkout -b branch-name origin/branch-name 新建本地分支并和远程分支关联
git branch --set-upstream branch-name origin/branch-name 使本地已有分支和远程分支关联

标签
git tag <tagname> 为当前commit_id打标签
git tag <tagname> <commit_id> 为指定cimmit_id打标签
git tag -d <tagname> 删除分支
git tag 查看历史
git show <tagname> 看具体标签的详情

git push origin <tagname> 推送一个本地标签
git push origin --tags 推送全部未推送过的本地标签
git push origin :refs/tags/<tagname> 删除一个远程标签