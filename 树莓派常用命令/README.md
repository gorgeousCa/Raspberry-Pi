# 树莓派常用命令
 
- 导航命令：  
 1、ls   查看当前目录内容  
 2、cd   <name>   切换工作目录   
 3、pwd  查看当前路径  
- 目录操作命令:    
1、mkdir   <name>   创建目录  
2、rmdir  <name> 删除空目录（只能删除空目录）  
3、 rm  <name>   删除目录  

- 文件操作命令:
1、touch   <name>    创建空文件
2、file  <filename>      查看文件类型
3、more /less  <name>   查看文件内容 （more 和 less 两个命令都可用来浏览文本文件，可以分页查看文件内容，空格翻页。文 件浏览完毕，按键盘 q 退出。相比来说 less 命令更加灵活，支持键盘的 Page Up 和 Page Down 键，可任意向前向后翻 页浏览，并且还支持文本搜索。使用 less 打开文件后，输入/abc 可在文本中搜索字符串 abc， 匹配的字符串高亮显示）
4、head/tail    <name>  查看文件内容 （head 和 tail 这两个命令可分别查看文件头部和文件尾部，一般用于查看 ASCII 文件。默 认显示 10 行。）
5、cat      <name>      查看文件内容 （可以将一个或者多个文件输出到标准输出上）
6、tar      <name>     文件压缩/解压
7、mv       < 源文件/目录目的文件/目录 >      文件改名和移动 
8、cp       [选项] <源文件/目录目的文件/目录 > 复制文件
9、 ln      < 选项源文件/目录目标文件 >        创建链接
10、chmod [参数] <文件/目录  >                改变或者设置文件/目录的权限
11、find   <name> /  grep<  选项   >                   查找文件

**-网络配置命令:**
 1、ifconfig   网络接口 [选项] 地址/参数     查看和更改网络接口的地址和参数
 2、ping              IP 地地址                       检查网络是否通畅
编辑器vi的使用：（vi和vim的联系）
编辑器：编辑器就是一款软件，他的主要作用是用来编辑。如编写文件，编写代码等。
windows中的常用编辑器： notepad（笔记本） notepad++,UltraEditor, SlickEditor
linux中常用的编辑器：  自带的最古老的vi。比较好用的是vim，gedit。
注意：vim是vi的升级版，推荐使用vim。
       但使用vim（vi）打开一个文件时，如果文件不存在他会帮你新建一个文件。
  vi的两种工作模式：
  命令模式：  当vi打开时默认为命令模式，要转入输入模式，需要按a或i键。在命令模式               下所有的输入都被vi当作命令来对待。（所以不要乱按）
  输入模式： 输入模式用来向文件输入内容。当输入完成要保存文件时需要按Esc键切换到命令模式。
注意 :  看屏幕左下角，当命令模式时无提示信息或者提示文件名等信息，当输入模式时，提示：--INSERT--

  使用方式：  vi  pathname     打开或创建一个文件

在命令模式下保存文件：
        ：wq      保存并且退出
        ：w         只保存不退出
         ：q         不保存退出  （只是进来看了一下没改时退出用）
         ：q!         不保存强制退出
         ：wq!      保存并强制退出

vi  的高级使用(在命令模式下使用)
*       /xxx      查找 xxx 
*  ：行数   快速切换到指定行数
*  ：set nu  设置显示行号
*   ：set nonu  设置不显示行号
注意：设置永久显示行号，需要修改vi的配置文件。打开vi的配置文件~/.vimrc 在其中输入set nu 即可。
*     dd        删除一整行
*    numdd    删除num行
*     numyy    复制num行
*     p              粘贴
 注意:    复制时要把光标放在多行的第一行，粘贴时实际粘贴到当前光标所在行的下一行。

*     vim水平分屏的使用 :vim -on file1 file2 ...其中:
      o(是小写字母o,不是数字零)n(表示你要分屏的文件个数)
     filen(文件名多个文件用空格分开)
*  vim垂直分屏:vim -On file1 file2 .....
 其中:O(是大写字母O,不是数字零)n(表示你要分屏的文件个数)    
       filen(文件名多个文件用空格分开)
*  撤销命令（命令模式下有效）
u ：小写的 u 键。 
-  常用命令:
  1、sudo raspi-config  初始化配置
  2、startx 启动图形化界面
  3、sudo rpi-update 升级系统
  4、sudo reboot 重启
  5、sudo shutdown -h now 立即关机
  6、sudo apt-get update   更新软件源
  7、sudo apt-get upgrade  更新已经安装的软件
  8、sudo apt-get install XX  安装XX软件
  9、su root 切换到root用户
 10、passwd user  设置user用户的密码
 





