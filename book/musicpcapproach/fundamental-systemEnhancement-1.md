“[民用系统](https://github.com/7900ms/00nottheater_deserted/tree/master/small)”

aka CentOS-fundamental-安装.md + 成型阶段划分

毛坯系统 -> 基本系统(systemEnhancement) -> 家用系统之外的其他系统(musicPC)

注意：重心放在 用linux的通用的部分, 而不是 发行版特性 那无关紧要

<hr>

### 毛坯系统

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

设置 SELinux (不动)
> sestatus (CentOS7 默认开启)
> nano /etc/selinux/config

设置 防火墙 (跳过)
> sudo systemctl status firewalld
参考 https://www.digitalocean.com/community/tutorials/additional-recommended-steps-for-new-centos-7-servers

3.
第一次
进入系统, 通过使用协议
重启

yum check-update
sudo yum install epel-release
yum info yum-axelget
sudo yum install yum-axelget
sudo yum update

4.
locale (跳过)

4.
时区
sudo timedatectl list-timezones | grep Asia
sudo timedatectl set-timezone Asia/Taipei
sudo timedatectl set-timezone Australia/Adelaide

时区同步
sudo yum install ntp
sudo systemctl status ntpd
sudo systemctl start ntpd
sudo systemctl status ntpd
sudo systemctl enable ntpd # 开机自启

Swap
参考 https://www.digitalocean.com/community/tutorials/additional-recommended-steps-for-new-centos-7-servers

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

sudo yum install p7zip zip unzip git nano wget mlocate htop trash-cli

文件查找

sudo yum install mlocate

sudo updatedb

locate curl

8.
【建立快照】

(安完后共2.8G, 压缩后 1.1G)


9.
虚拟机增强

安装虚拟机增强
mkdir /media/cdrom
mount -o exec /dev/cdrom /media/cdrom
cd /media/cdrom
./install

https://wpguru.co.uk/2015/07/how-to-install-parallels-tools-via-the-command-line-in-centos/
http://www.cnblogs.com/ghj1976/p/4114759.html

```
<hr>

### 基本系统

```
(必须知道电脑上都安了什么软件。写一个放一个) ~/Library/Application Support/XMenu/Custom/Programs 安完大约18G
```

#### 鼠标

触摸板
锁屏时间
屏幕保护
任务栏/菜单栏位置和样式

#### 资源管理器

资源管理器树形结构
xfce thunar

#### 输入法

#### 开机登入

设置 用户免密码登入

sudo vi /etc/gdm/custom.conf 加入
```
[daemon]
AutomaticLoginEnable=True
AutomaticLogin=sysadmin # 当前用户名
```

#### locale
```
sudo nano /etc/profile 加入

export LC_ALL=en_US.UTF-8  
export LANG=en_US.UTF-8
```

#### 浏览器

[flash]

#### links文件夹
```
mkdir /home/$(logname)/Desktop/links
cd links
```

