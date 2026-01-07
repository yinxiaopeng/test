# 1. 进入项目文件夹
cd ~/Documents/my-project

# 2. 初始化 Git 仓库
git init

# 3. 查看状态（应该是红色，表示未跟踪的文件）
git status

# 4. 添加所有文件到暂存区
git add .

# 5. 提交到本地仓库
git commit -m "初次提交：项目初始化"

# 6. 查看提交历史
git log

# 7.回滚到上一个提交
<!-- commit cf437aa7eb837b03ffbd343d60017fb9bc37945a -->
git reset --hard cf437aa7eb837b03ffbd343d60017fb9bc37945a

# 8.如果看不到回滚后的提交记录，需要查看历史记录
git reflog

# 9.查看当前分支
git branch

# 10.创建新分支
git branch new-feature

# 11.切换到新分支
git checkout new-feature

# 12.创建并切换到新分支
git checkout -b new-feature

# 13.合并新分支到主分支 将new-feature分支的变更合并到master分支
git checkout master
git merge new-feature