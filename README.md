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
###  *用于匹配任意长度的字符
###  ？用于匹配任意一个字符
###  【】用于匹配指定的一个字符
##3   ^用于在【】中进行字符过滤
# home 目录下都是普通目录
# root 超级目录
# /etc目录下哦都是配置文件
# exit 退出root
# 用户和组方面
### liunx组的分类：1.主组 2.附属组
### vi /ect/passwd 查看用户下配置信息 
### vi /etc/group 查看分组信息
### sudo adduser username 创建一个新的用户
### sudo useradd -s /bin/bash -m -g username 设置密码 sudo passwd username
### su username 登录一个用户
### sudo userrmod -s /bin/bash -G group1,group2 username 更改用户组
### sudo gpasswd -a username groupname 添加一个用户到一个组
### sudo gpasswd -d username groupname 测删除组中用户
### sudo passwd username 修改用户密码
### sudo passwd root 修改root密码
### sudo deluser username 删除一个用户不善目录
### sudo deluser username --remove-home 删除组中的用户连同目录一起
# 开关机
### shutdown -r 重启
### shutdown -h 关机
### shutdown -k 通知其他用户我要关机
### shutdown -c 取消关机
# 查看磁盘空间
### df -a 查看所有磁盘空间
### df -h 可读的方式查看磁盘空间
### df -T 查看使用了多少空间
# 查看文件目录大小
### du -h 文件名 查看文件站磁盘的大小 大于等于文件大小 
### du -sh 目录名 查看目录大小
# 查看进程
### ps 显示当前所有运行的层程序快照
### ps -ajx 列出所有进程数据 带+的是前台运行的
### ps -ajx | grep 想查找内容  得到想找内容的编号
### ps -aux 比ajx多一个用户
### pstree 产生一个进程树
### top (动态)列出所有进程的cpu和内存使用情况 shift+<>换页 q 退出
### kill -9 pid 杀死pid号的进程 
##3 kill -9 -1 杀死一切进程
# 本地和在线安装
## 应用软件包 后缀都是.deb
## amd64 在64位操作系统上运行的
## 本地安装命令
### sudo dpkg -i 软件包全称.deb 本地安装命令
### sudo apt-get install -f 解决依赖关系
### dpkg -s 软件包名称 查看软件包安装状态
### dpkg -L 软件包名称 查看软件包装到哪个目录里
### dpkg -r 软件包名称 卸载软件
### sudo dpkg -P 软件包名称 卸载软件 包括软件相关包
## 在线安装命令
### sudo apt-get update 更新本地软件源
### sudo apt-get install 软件包名称 在线安装命令
### sudo apt-cache policy 软件包名称 查看软件包安装状态
### sudo apt-cache show 软件包名称 查看软件包信息（无论有没有安装） 
### sudo apt-get- remove --purge 软件包名   
### 卸载软件包 sudo apt-get download 软件包名称        
### 下载软件包 不安装 sudo apt-get source  软件包名称    
# sudo passwd root 修改root密码     
# 进入root最大权利方法 su -
# tftp
### TFTP:端口号69
### ip地址区分区域网的身份
### 端口号：区分同一台电脑的不同程序
## 环境配置
### 修改配置文件sudo vi /etc/default/tftpd-hpa
#### 第一行文件的名称
#### 第三行 环境变量 
#### 第四行 fttpboot 上传下载目录 
#### 第五行 端口号
#### 第六行 安全  改成"--secure -c -l"
### chmod 777 /var/lib/tftpvoot
## tftp操作步骤：
### sudo service tftpd-hpa start 启动服务器
### tftp 127.0.0.1（自己ip地址）
### put     上传
### get     下载
### quit    退出
### sudo service tftpd-hpa restart 重启服务
### sudo service tftpd-hpa stop
# ifconfig 产看自己ip在地址 
# 127.0.0.1 带边自己ip
# chomd 777 目录 修改权限 777表示对所有用户公开（r 4 w 2 x 1）
# NFS服务器
### 安装nfs服务端 和 客户端
### dpkg -s nfs-kernel-server 检查NFS服务器的安装状态
## 修改环境变量
### sudo vi /etc/exports 
### 在最后一行加入/被挂载目录  *(rw,sync,no_subtree_check,no_root_squash)
## 操作步骤
### sudo service nfs-kernel-server start  开启客户端
### sudo service nfs-kernel-server restart  重启客户端
### sudo service 。 。 。 。 。 。 stop  关闭客户端
### mount -t nfs ip地址:/被挂载目录   挂载目录名
### umount 挂载目录                   取消挂载
# 网络文件系统NFS  
# hostname   主机名    
# /srv/homes 共享目录
# SSH
### 安装openssh-server(ssh) 服务端 opensh-clien(sshd) 客户端
### 配置文件目录 /etc/ssh/sshd_config
### 带#的 去掉#就可以使用 仔细看好内容在去掉
#### port 设施sshd监听口
#### ListenAddress 设置sshd服务器绑定的IP地址
#### HostKey 设置包含计算机私人密匙的文件
#### ServerKeyBits 定义服务器密匙的位数
#### LoginGraceTime 设置如果用户不能登录，在切断连接之前服务器需要等待的时间（以秒为单位）
#### KeyRegenerationInterval 设置在多少秒之后自动重新生成服务器的密匙（如果使用密匙）。重生密匙
#### PermiRootLogin 设置root能不能用ssh登录。选择yes 最高权限登录他人计算机 危险
#### X11Forwarding 设置是否允许X11转发
# ssh操作步骤
### sudo service sshd start 启动服务
### sudo service sshd restast 重启服务
### sudo service sshd stop   
### ssh 用户名@ip地址或主机名  远程登录别人服务器
### scp 文件名 用户名@ip地址或主机名:  复制自己文件到别人用户主目录
### scp -r 用户名@ip地址或主机名:/路径/文件名 . 复制别人目录到自己目录
# wc的使用
### wc 输出行的俄个数 单词的个数 字节的个数
### ls | wc   输出目录下文件   -l  就输出文件个数
### wc  文件名 输出文件的  行数 单词数  字节个数
# grep的使用
### grep 关键字 文件名  查找关键字
### grep -n 关键字 文件名 找到关键字并显示行号
### grep -R -n 关键字 .    查找当前目录中包括子目录的所有关键字
### ps ajx | grep 想查找内容  得到想找内容的编号
# tree 目录名 以树状显示目录
# ll  相当于ls -al（不是所有系统都通用）
# apache web服务器的应用软件
## 安装 apache的步骤
### 安装 apache
### 安装tasksel
### 输入tasksel
### 找到 LAMP server 安空格键选中 
## /etc  配置文件目录 /etc/apache2/ 






