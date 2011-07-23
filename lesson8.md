#编码风格（）

###tab和空格不能混用

###tab设置
	akaedu@akaedu-desktop:~$ vim .vimrc
	set autoindent    //自动换行
	set tabstop=4     //tab跳跃4个空格
	set expandtab     //tab和空格的作用相同（可跳四个但删除时是一个个的）
	set shiftwidth=4  //可视行左右移动是四个空格
    在插入模式下处理不对齐的缩进：ctrl+t(后)  ctrl+d(前) 
###vim 小设置
    用打开一个文件在插入模式下"h q(要查找项)"即可进入帮助文件
    akaedu@akaedu-desktop:~$ vimdiff .bashrc barccc
    可以查看两个文件的不同（红色高亮）注：事先两个文件都没被打开
###使用小词典
    虽然电脑已安装但是默认不可用
    akaedu@akaedu-desktop:~$ vim .vimrc
    set dictionary=/usr/share/dict/words
    此后用vim打开一个文件在写单词的时候若忘记咋写则 he（想写hello）->ctrl+x+k
###登录别人服务器
    akaedu@akaedu-desktop:~$ ifconfig 查看自己的IP地址   
    akaedu@akaedu-desktop:~$ psjicfh openssh-server //安装软件（被登录电脑上装）
                                     ssh-client     //此软件系统默认安装（主机）
    akaedu@akaedu-desktop:~$ ssh peter@192.168.1.17 //要登录的用户名密码
    ctrl+d 退出 
    复制peter的东西到自己的目录
    akaedu@akaedu-desktop:~$ scp -r peter@192.168.1.17:~/happycasts .
    从机关闭服务:sudo service ssh stop
    从机开启服务:sudo service ssh start

