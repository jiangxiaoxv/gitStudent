
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

ls -al
cp ./readme.md  ./readme2.md
# 建Git仓库
1. git init
2. git init your_project