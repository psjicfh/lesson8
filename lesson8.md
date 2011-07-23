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
    使用小词典虽然电脑已安装但是默认不可用
###akaedu@akaedu-desktop:~$ vim .vimrc
    set dictionary=/usr/share/dict/words
    此后用vim打开一个文件在写单词的时候若忘记咋写则 he（想写hello）->ctrl+x+k
    
