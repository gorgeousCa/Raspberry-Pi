# Raspberry Pi 远程连接的三种方法
## THE FRIST 使用Windows自带的远程桌面连接
   - 先安装tightvncserver。
     `sudo apt-get install tightvncserver`
   -  再安装xrdp服务。
       `sudo apt-get install xrdp`
   - 启动xrdp服务
       `sudo /etc/init.d/xrdp restart`
     如出现以下画面，可使用 netstat tnl 查看端口3350 3389 5910 这三个端口处于LISTEN
![在这里插入图片描述](https://img-blog.csdn.net/20181005195303868watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzAzMDg5Nw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
## THE SECOND 使用putty远程连接
- 确认树莓派SSH打开
![在这里插入图片描述](https://img-blog.csdn.net/20181005195942505?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzAzMDg5Nw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
 - 在Windows电脑上下载putty.exe。,并打开（如上图所示）
r![在这里插入图片描述](https://img-blog.csdn.net/20181005200359862?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzAzMDg5Nw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)              
- 输入IP地址，并点击open
![在这里插入图片描述](https://img-blog.csdn.net/20181005200809664?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzAzMDg5Nw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
 - 输入登录名和密码，按回车即可。然后就大功告成啦。
![在这里插入图片描述](https://img-blog.csdn.net/20181005201045773?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzAzMDg5Nw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
 ## THE THIRD 使用VNC远程登陆树莓派
 - 开启Raspbian的VNC Server
   在终端输入命令：
    `sudo raspi-config`
![在这里插入图片描述](https://img-blog.csdn.net/20181005202258915?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzAzMDg5Nw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
- 将光标移至第5项：Interfacing Options，并敲回车。
![在这里插入图片描述](https://img-blog.csdn.net/20181005202529543?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzAzMDg5Nw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
- 选择第3项：VNC，并敲回车。
![在这里插入图片描述](https://img-blog.csdn.net/20181005202818746?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzAzMDg5Nw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
- 选择“是”，并敲回车。
![在这里插入图片描述](https://img-blog.csdn.net/20181005203007315?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzAzMDg5Nw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
- 设置结束，敲回车进行确认。
- 通过以上操作，VNC Server开启完毕。之后树莓派每次开机，VNC Server都会自启动。这就确保了我们可以随时远程登陆树莓派。
 - 在windows计算机上使用VNC Viewer
打开你的windows计算机并安装VNC Viewer。顾名思义，VNC Viewer与VNC Server是配合使用的，而且是单向控制，即你只能使用Viewer端登陆Server端。VNC是免费软件，你可以在VNC官方网站上获取。 
VNC的软件界面示例如下（不同的版本可能会有差别）： 
![在这里插入图片描述](https://img-blog.csdn.net/20181005203409216?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzAzMDg5Nw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
- VNC Server这一栏填写树莓派ip地址。 
- Username和Password指的是你登陆树莓派的用户名和密码，如果你没有对树莓派进行用户配置，用户名为pi，密码为raspberry。 
添加完成后，VNC窗体中就会出现新的连接图标（就像上图示意的那样），双击即可远程登陆你的树莓派。





