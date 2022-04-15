
# Git 初始化
1. 配置user信息
   git config --global user.name 'jxx'
   git config --global user.email '1043479536@qq.com'

   config的三个作用域
   git config --local 只对某个仓库有效(默认值)
   git config --global 对当前用户所有仓库有效
   git config --system 对系统所有登录的用户有效

   显示config的配置，加 --list
   git config --list --local
   git config --list --global
   git config --list --system


# 建Git仓库
1. git init
2. git init your_project

# 仓库文件
1. 版本历史
2. 暂存区
3. 工作目录


# mac 操作命令
ls -al
cp ./readme.md  ./readme2.md
mv readme readme.md

# 文件名变更
git reset --hard (暂存区, 工作区所有的东西都会被清除掉)
git mv readme.md readme2.md


# 查看版本历史
1. git log --oneline
2. git log -n4 --oneline  git log -n2 --oneline
3. git branch -v 查看本地分支
4. git checkout -b temp 7ad9f34 // 基于某次提交创建分支
5. git commit -am "feat: 注释"
6. git branch -av
7. git log --all
8. git log --all --graph
9. git log --oneline master
10. git help log


# .git目录探秘
cat .git/HEAD
cat .git/config

git cat-file -p 40e3d4e801c52
git cat-file -t 40e3d4e801c52

# commit -> tree -> blob

# 分离头指针


# 
git diff HEAD HEAD^1 | HEAD~2


# 删除不需要的分支
1. git branch -d demo
   git branch -D demo

# 修改最新commit的message
1. 