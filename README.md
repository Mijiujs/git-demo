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