linux笔记
====
## day1  
* `快捷键`  
    1.遍历历史记录：  
    向上：UP  
    向下：DOWN  
    2.删除：  
    删除光标前边的字符：backspace ctrl + h  
    删除光标后边的字符：ctrl+d  
    删除光标前边的字符串：ctrl+u  
    删除光标后边的字符串：ctrl+k  
    3.移动  
    向前：ctrl+b  
    向后：ctrl+f  
    光标移动到头部：ctrl+a
    光标移动到尾部：ctrl+e  
    
* `目录结构`  
  根目录的表示方式：/  
  常见目录：  
  /bin: binary,二进制文件，可执行程序，shell命令  
  /dev: device,设备目录,在linux下一切皆文件 硬盘，显卡，显示器。。。都被抽象成一个文件，放在/dev：目录下。 
  /lib：linux系统运行时候需要加载的一些动态库  
  /mnt: 手动的挂载目录  
  /media：外设的自动挂载目录  
  /root：linux的超级用户的家目录  
  /usr：unix system resource 资源目录  
  　　头文件  -stdio.h stdlib.h  
  　　游戏  
  　　用户安装的应用程序 /usr/local  
  /etc: 存放配置文件  
  　　/etc/passed  
  　　/etc/group  
  /opt: 安装第三方的应用程序   
  /home: 操作系统的所有用户的家目录 /home/qiaoguan  
  /temp: 存放临时文件  

* `.和..`  
  .是当前目录，..是当前目录的上一级目录  

* `文件目录`  
  #### 1、tree  
  tree 查看当前目录的内容，  
  tree dir 查看指定的目录  
  #### 2、ls  
  功能：查看文件或者目录  
  语法：  
  参数：  
  　-a 显示所有文件  
  　　　隐藏文件：文件或目录名前有一个点  
  　-l  
  　　　-rwxrw-r-- 1 kevin kevin 3231145 11月 23 23:08 vimplus.tar.gz  
     第一个字符：文件类型，有七种，普通文件: -;目录：d; 符号链接：l；管道：p;套接字：s;字符设备：c(键盘鼠标);块设备：b(U盘，鼠标)；  
     三种类型的用户：文件所有者：user;文件所属组用户：group;其他人:other.  
     rwx:文件所有者 rw-:文件所属组用户 r--:其他人  
     "1" 代表硬链接计数  
     kevin:代表文件所有者  第二个kevin文件所属组得名字  
     3231145：文件的大小。如果是目录，永远是4k（）  
  #### 3、cd -- 切换目录  
  + cd目录　　
  + 如何进入家目录：cd绝对路径(/home/kevin);cd ~; cd　　
  + 在两个临近目录之间切换 cd -  
  #### 4、pwd   
  当前的路径 print work directory  
  #### 5、mkdir   
  + 名字或者路径： 创建目录 mkdir aa/bb/cc/ -p ;　　-p创建多级目录　  
  #### 6、touch:  
  touch file.c  
  #### 7、rmdir  
  只能删除空目录不常用  
  #### 8、rm  
  + 删除目录
    + rm 目录名 -r
    + 递归的方法删除 rm aa - r  
    + 删除之后，很难恢复 可以使用 -ri 会有信息提示  
  + 删除文件
    + rm 文件名 -i
  #### 9、cp 拷贝
  + cp  要拷贝的文件 file (file不存在自动创建)
  + cp  要拷贝的文件 file (file若存在会被新文件覆盖)
  + cp  要拷贝的文件 dir (存在)
  + cp  dir1(存在)  dir2(存在) -r
    + 将dir1 拷贝到dir2中 ,-r 是指递归拷贝
  + cp dir(存在)  dir2(不存在) -r
    + 创建dir2 将dir1中的内容拷贝到dir2中，不包括dir1的目录
  #### 10、mv 改名或者移动
    mv file1 file2
  + 改名
    + mv file(存在) file1(不存在)  --file是文件 
    + mv dir(存在)  dir(不存在)  --dir是目录
  + 移动
    + mv file(文件) dir(存在的目录) filr-->dir
    + mv dir(目录存在) dir1(目录存在) dir-->dir1
  + 覆盖操作(谨慎操作)
    + mv file(存在) file2(存在)
* `查看文件`
  #### 命令
  + cat , more , less , head , tail 

* `软硬连接ln`
  #### 软连接 -- 快捷方式
  + ln -s 文件名 快捷方式的名字 ln -s home/qiaoguan/program s.sorft  
    + 文件名使用绝对路径，可以保证快捷方式在移动后仍能使用
  + 目录也可以创建软连接
  #### 硬链接
  + ln 文件名 硬链接的名字
  #### chmod
  修改权限 具体百度
  #### chown ,chgrp
  不想写了，具体百度