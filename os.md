# 操作系统查看目录
1. ls / 根目录
2. / 目录
3. /root root用户的家目录
4. /home/username 普通用户的家目录
5. /etc 配置文件目录
6. /bin 命令目录
7. /sbin 管理命令目录
8. /usr/bin /usr/sbin系统预装的其他命令

# 万能的帮助命令
1. man是manual的缩写
   # man ls
   # ls --help  |  help cd
   # info ls

2. pwd和ls命令（一切皆文件）
   # pwd 当前工作目录
   # cd 更改当前的操作目录
   # ls 查看当前目录下的文件
        * -l（长格式显示文件） -a（隐藏） -r(逆向排序) -t -R(递归显示，包括子目录)
        * ls filename
        * ls /root /
        * ctrl + l

# cd 命令
1. cd - 回到之前的目录
2. cd /etc

# 创建和删除目录
        