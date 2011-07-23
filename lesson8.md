#编码风格（）

###tab和空格不能混用

###tab设置
	akaedu@akaedu-desktop:~$ vim .vimrc
	set autoindent    //自动换行
	set tabstop=4     //tab跳跃4个空格
	set expandtab     //tab和空格的作用相同（可跳四个但删除时是一个个的）
	set shiftwidth=4  //可视行左右移动是四个空格
    在插入模式下处理不对齐的缩进：ctrl+t(后)  ctrl+d(前) 
