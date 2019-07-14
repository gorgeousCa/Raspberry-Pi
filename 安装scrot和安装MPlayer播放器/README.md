
 ***1. 在树莓派上安装scrot***
      首先在终端中用下面的命令安装名叫“scrot”的截屏工具。首先在终端中用下面的命令安装名叫“scrot”的截屏工具。

	
         sudo apt-get install scrot
      
![在这里插入图片描述](https://img-blog.csdn.net/20181006190259937?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzAzMDg5Nw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)      

  截取全屏幕执行：
	
    sudo scrot

   用鼠标选区屏幕区域截取执行：
	
    sudo scrot -s
![在这里插入图片描述](https://img-blog.csdn.net/20181006190010647?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzAzMDg5Nw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)  
 10秒后截取，参数可以自定义：
	
    sudo scrot -d10


执行下面的指令可以查看更多用法：  
	
    sudo scrot -h
    
   指定截取图片的名字：
   
    scrot example.png 
   指定文件位置：
   
    scrot /home/pi/Desktop/example.png
   打开截图，导航到图片目录：  
   
     shotwell “example.png 


  其他命令：     
-h 显示更多帮助 
-v 获取当前版本 
-d x 添加X秒的延迟拍摄 
-c 添加一个倒计时延迟拍摄 
-s 允许用户用鼠标捕捉特定区域 
-u 捕捉当前活动窗口 
-q X 指定图像质量百分率X（默认75） 
-t X 创建一个百分比大小为X的缩略图 
-e 在截图后指定一个命令来运行 



   ***2. 在树莓派上安装MPlayer播放器***
   
   升级安装程序
   
    sudo apt-get update
    sudo apt-get upgrade
   安装VLC
   
    sudo apt-get install vlc
  安装MPlayer

    sudo apt-get install mplayer mplayer-gui alsa-base alsa-utils pulseaudio mpg123
    reboot  
  播放视频
 
     mplayer ***.mp4
   
