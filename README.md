# gittest
测试git
git 分布式版本控制系统

git init 创建Git仓库
git add <filename> 工作区添加到暂存区
git commit -m <message> 暂存区提交到仓库

git status 查看工作区+暂存区状态
git diff 查看修改内容

git log 查看提交记录
git reset --hard <commit_id> 回到某个版本 HEAD表示当前版本，HEAD^^表示上上个版本,HEAD~100回到上100个版本
git reflog 查看命令历史

git checkout -- <filename> 丢弃工作区文件的修改
git reset HEAD <filename> 丢弃暂存区文件的修改
git rm <filename> 删除文件，加-f强制删除

远程仓库
git remote add origin <address> 关联远程库
git push -u origin master 第一次推送master分支的所有内容
git push origin master 推送最新修改
git clone <address> 从远程库克隆

git branch 查看分支
git branch <dev> 创建分支
git branch -d <dev> 删除分支
git checkout <dev> 或 git switch <dev> 切换分支
git checkout -b <dev> 或 git switch -c <dev> 创建并切换到分支
git merge <dev> 把分支合并到当前分支