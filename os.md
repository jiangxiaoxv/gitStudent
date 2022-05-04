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
        * -l（长格式显示文件） -a（隐藏） -r(逆向排序) -t -R(递归显示，包括子目录) -h 查看文件大小
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
2. \* 匹配当前目录下所有的文件与目录 cp file* / (以file开头)
3. cp file? /


# 文本查看命令
1. cat os.md 文本内容显示到终端
2. head -5 os.md  查看文本文件前五行(默认10行)
3. tail os.md 查看尾部
4. tail -r os.md 当文件发生变化时，不跟踪
5. wc -l os.md 查看文件有多少行
6. more os.md 分行显示 空格继续显示
7. tail -f os.md 当文件发生变化时，实时跟踪

# 打包压缩和解压缩
1. gzip 和bzip2 命令
2. tar -cvf datao/index.tar test 打包成文件
3. tar -czf datao/index.tar.zip test 打包并压缩
4. tar xf dabao.tar dabao 解包

# Vim的四种模式
在终端中输入vi，进入vim编辑器
1. 正常模式(i, I, a, A, o, O)
2. 插入模式
3. 命令模式
4. 可视模式(v)
5. 鼠标移动（h,j, k, l）
6. 复制（yy）
7. 粘贴（p）
8. 多行复制(2yy)
9. 特定行到尾部（y$）
10. 剪切命令(d$)
11. 撤销指令（u）
12. 取消撤销（ctrl + r）
13. 单个字符剪贴（x）
14. 单个字符替换（r）
15. 显示函数（:set nu）
16. 跳转到指定行 （11 + G）
17. 跳转到第一行（gg）
18. 跳转到最后一行(GG)
19. 跳转一行的头部（shift ^）
20. 跳转到一行的尾部(shift $)

# Vim 的命令模式
1. :w /root/a.txt 保存目录和文件
2. :wq 保存退出
3. :q! 退出，不保存
4. /x 查找字符x
5. n 向下查找到字符x
6. shift n 向上查找到字符x
7. :s/x/y 选中后所有x替换为y(针对光标当前行)
8. %s/x/y/g 整个文件的x替换为y
9. ：3，5s/x/y/g 特定行之间的替换
10. :set nu 显示行号
11. :set nonu 隐藏行号