
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
1. git commit --amend
   i wq!

# 修改历史commit的message
1. git rebase -i 40e3d4e801c52ddd43fa9 // 40e3d4e801c52ddd43fa9是要修改的信息的父提交
   r

# 把连续的多个commit整理成1个
1. git rebase -i 
   s

# 把间隔的多个commit整理成一个
1. git rebase -i 
   
# 怎么比较暂存区和HEAD所含文件的差异
1. git diff --cached 暂存区与历史文件的差异，此时工作区的文件变化没有体现

# 工作区与暂存区的差异
1. git diff
2. git diff -- readme.md

# 让暂存区恢复成和head一样
1. git reset HEAD(废弃暂存区，恢复到工作区)

# 让暂存区恢复到和工作区一样
1. git checkout -- .

# 取消暂存区部分文件的更改
1. git reset HEAD -- readme.md index.html

# 回退前几个commit
1. git reset --hard HEAD(工作区，暂存区，提交历史都没有了)

# 删除文件
1. rm readme.md
2. git rm readme.md
3. git reset --hard HEAD（恢复）

# 临时修复bug
1. git stash
2. git stash list
3. git stash pop
4. git stash apply


# .gitignore

# git 备份
1. 哑协议(传输进度不可见)
2. 智能协议（传输可见）
3. 平时接触到的都是智能协议（http/https）
4. ssh

5. git clone --bare 仓库1            name1
6. git clone --bare file://         name2
7. git clone --bare https://git.vue name3
8. git remote -v
9. git remove add zhineng file://
10. git push --set-upstream zhineng 

# github 远端分支
1. git remote -v
2. git remote add remotename git@github.com:git....
3. git push remotename --all // 把本地的分支都push到远程re

实例
git add remote origin git@github.com:jiangxiaoxv/gitStudent.git
git push origin --all

# 变基停止
git rebase --abort
=======
4. git 


