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
