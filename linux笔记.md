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

* `文件目录的`  
  1、tree  
  tree 查看当前目录的内容，  
  tree dir 查看指定的目录  
  2、ls  
  功能：查看文件或者目录  
  语法：  
  参数：  
  　-a 显示所有文件  
  　　　隐藏文件：文件或目录名前有一个点  
  　


   


