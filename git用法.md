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

# 14.删除分支
git branch -d new-feature
git branch -D new-feature 不做任何检查，强制删除


# 15.配置SSH公钥
# 生成SSH密钥对
ssh-keygen -t rsa
# 查看公钥内容
cat ~/.ssh/id_rsa.pub
# 验证是否配置成功
ssh -T git@github.com





# 16.添加远程仓库
git remote add origin git@github.com:your-username/my-project.git
# 查看远程仓库
git remote -v

# 17.将本地仓库推送到远程仓库
git push origin main
git push [-f][--set-upstream] origin main
git push --set-upstream origin main:main
git branch -vv 
# 后续推送可以简单使用
git push

# 18.克隆远程仓库到本地
git clone git@github.com:your-username/my-project.git “保存在本地的文件夹名，如果不写就用默认my-project”

# 19.从远程仓库抓取变更（把更新的变更拉取到本地，但不合并，合并还需要merge命令）
git fetch origin main
# 合并远程变更到本地分支
git merge origin/main
# 查看抓取的变更
git log --oneline origin/main

# 20.拉取远程变更到本地分支(fetch+merge)
git pull origin main

# 21. 查看远程分支
git branch -r
# 22. 查看本地分支和远程分支的关联关系
git branch -vv
# 23. git log --oneline --graph 查看分支合并历史




