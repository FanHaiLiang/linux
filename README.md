# touch 创建文字
# p 复制 -a目录包括目录下文件或子目录
# cd 切换目录
# mv 移动或重命名
# rm 删除 -rf强制删除目录在机起子目录
# pwd 显示绝对路径
# cat 列出当前文件内容
# ls 的列出当前目录的文件
  * -a 列出目录内隐藏文件
  * -l 列出文件详细内容
# man 查看命令手册
# mkdir 创建目录
# gzip 压缩
# gunzip 解压
# bzip2 压缩
# bunzip2 解压
# tar -czvf 压缩后文件名 压缩前文件名 压缩
#      -xzvf 压缩文件名    解压
    * -czvf (c:创建一个压缩 z:压缩格式.gz 随压缩格式字幕改变 v:压缩过程 f:压缩文件名)
    * -xzvf (x 解压命令) -xvf 解压所有类型
# shell通配符   
##  *用于匹配任意长度的字符
##  ？用于匹配任意一个字符
##  【】用于匹配指定的一个字符
##   ^用于在【】中进行字符过滤
# home 目录下都是普通目录
# root 超级目录
# /etc目录下哦都是配置文件
# exit 退出root
# liunx组的分类：1.主组 2.附属组
# vi /ect/passwd 查看用户下配置信息 
# vi /etc/group 查看分组信息
# sudo adduser username 创建一个新的用户
# sudo useradd -s /bin/bash -m -g username 设置密码 sudo passwd username
# su username 登录一个用户
# sudo userrmod -s /bin/bash -G group1,group2 username 更改用户组
# sudo gpasswd -a username groupname 添加一个用户到一个组
# sudo gpasswd -d username groupname 测删除组中用户
# sudo passwd username 修改用户密码
# sudo passwd root 修改root密码
# sudo deluser username 删除一个用户不善目录
# sudo deluser username --remove-home 删除组中的用户连同目录一起
# shutdown -r 重启
# shutdown -h 关机
# shutdown -k 通知其他用户我要关机
# shutdown -c 取消关机
# df -a 查看所有磁盘空间
# df -h 可读的方式查看磁盘空间
# df -T 查看使用了多少空间
# du -h 文件名 查看文件站磁盘的大小 大于等于文件大小 
# du -sh 目录名 查看目录大小 
# ps 显示当前所有运行的层程序快照
# ps -ajx 列出所有进程数据 带+的是前台运行的
# ps -aux 比ajx多一个用户
# pstree 产生一个进程树
# top (动态)列出所有进程的cpu和内存使用情况 shift+<>换页 q 退出
# kill -9 pid 杀死pid号的进程 
# kill -9 -1 杀死一切进程
# 应用软件包 后缀都是.deb
# amd64 在64位操作系统上运行的
# 本地安装命令
# sudo dpkg -i 软件包全称.deb 本地安装命令
# sudo apt-get install -f 解决依赖关系
# dpkg -s 软件包名称 查看软件包安装状态
# dpkg -L 软件包名称 查看软件包装到哪个目录里
# dpkg -r 软件包名称 卸载软件
# sudo dpkg -P 软件包名称 卸载软件 包括软件相关包
# 在线安装命令
# sudo apt-get update 更新本地软件源
# sudo apt-get install 软件包名称 在线安装命令
# sudo apt-cache policy 软件包名称 查看软件包安装状态
# sudo apt-cache show 软件包名称 查看软件包信息（无论有没有安装） 
# sudo apt-get- remove --purge 软件包名   
# 卸载软件包 sudo apt-get download 软件包名称        
# 下载软件包 不安装 sudo apt-get source  软件包名称     


