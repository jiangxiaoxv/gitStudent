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
新建目录
1. mkdir /demo 在根目录下建立demo目录
2. mkdir demo 在当前目录，建立目录
3. mkdir b c d 建立多个目录
4. mkdir /a/b 建立多极目录
删除目录
1. rmdir /demo 删除目录 (只能删除空白目录)
2. rm -r /a/b 删除目录和文件

# 复制和移动目录
1. cp -r  src srcCopy 复制目录,里面的文件不重命名，文件也复制过来了
2. cp -r src/http.js src/httpCopy.js 复制文件
3. cp -a 复制权限，等相关属性
文件的移动与重命名
1. mv src/http.js src/httpRename.js
2. * 匹配当前目录下所有的文件与目录 cp file* / (以file开头)
3. cp file? /