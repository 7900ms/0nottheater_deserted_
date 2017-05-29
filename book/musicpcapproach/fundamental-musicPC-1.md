aka CentOS-fundamental-安装.md

```
检测区

结果区

CentOS7 xfce

查看区

配置区：

1.
安装系统

下载 CentOS-7-x86_64-Minimal-1611.iso  (0.7G)

设置：语言、时区、组件(mininal)、打开网络(Installation Summary)

2.
设置用户

3.
第一次
进入系统, 通过使用协议
重启

yum check-update
sudo yum install epel-release
sudo yum install yum-axelget
sudo yum update

4.
locale (跳过)


5.
【建立快照】

6.
桌面环境

yum groupinfo -v "X Window system"
sudo yum groupinstall "X Window system"
sudo yum --enablerepo=epel groupinstall xfce
yum groupinfo -v xfce

测试
systemctl isolate graphical.target
sudo reboot
正式配置从GUI启动
systemctl get-default
sudo systemctl set-default graphical.target
systemctl get-default
sudo reboot

重启 自动进入GUI

7.
资源管理器

资源管理器

设置 Xcfe - Thunar 资源管理器 侧面板树形

压缩解压

sudo yum install p7zip zip unzip git nano

文件查找

sudo yum install mlocate

sudo updatedb

locate curl

8.
【建立快照】

(安完后共2.8G, 压缩后 1.1G)


9.
虚拟机增强

设置 用户免密码登入

sudo vi /etc/gdm/custom.conf 加入

[daemon]
AutomaticLoginEnable=True
AutomaticLogin=sysadmin




10.
安装虚拟机增强
mkdir /media/cdrom
mount -o exec /dev/cdrom /media/cdrom
cd /media/cdrom
./install

https://wpguru.co.uk/2015/07/how-to-install-parallels-tools-via-the-command-line-in-centos/
http://www.cnblogs.com/ghj1976/p/4114759.html

```
