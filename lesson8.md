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
    用vim打开一个文件要写一段英语想检查有没有单词错误
    在普通模式下“:set spell”  亦可在.vimrc中设置
    akaedu@akaedu-desktop:~$ vim .vimrc 
    “map ,ss :set spell<cr>”
    即：在以后检查错误的时候在普通模式下按“,ss”就行
    用vim打开多个文件默认是“:bn”查看下一个文件
    若在“.vimrc”中设置  “map <tab> :bn<cr>” 此后按tab就可以换
    在插入模式下想回到普通模式按“esc”
    在".vimrc"中设置 “imap jj <esc>”此后按“jj”即可从插入模式回到普通模式
    注：在“.vimrc”中“map”是设置在普通模式下的 “imap”是设置在插入模式下的
    默认的回车：cannage return 即 '\r'  换行： '\n'
    在unix下 '\n'='\n'+ '\r'   在windows下 '\n'='n'
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
###快速查找main函数中调用的子函数
    kaedu@akaedu-desktop:~$ psjicfh ctags //安装软件
    akaedu@akaedu-desktop:~/work/lesson7/lesson7_project$ ctags lesson7.c
    （若一个工程中有多个文件则格式是“ctags *”）
    akaedu@akaedu-desktop:~/work/lesson7/lesson7_project$ ls
    a.out  lesson7.c  tags     //生成tags文件夹
    akaedu@akaedu-desktop:~/work/lesson7/lesson7_project$ vim lesson7.c
    把光标指到待查看的子函数名然后 “ctrl+]:查找下一个，ctrl+t:查找上一个”
###查看标准库(下面的我也不知道啥意思！)
    akaedu@akaedu-desktop:~/work/lesson7/lesson7_project$ ldd a.out
            linux-gate.so.1 =>  (0x00d1b000)
            libc.so.6 => /lib/tls/i686/cmov/libc.so.6 (0x00ae0000)
            /lib/ld-linux.so.2 (0x001d7000)
