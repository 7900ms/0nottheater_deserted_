
安装
```
桌面环境

sudo yum install epel-release
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
```

设置 用户免密码登入

sudo vi /etc/gdm/custom.conf 加入
```
[daemon]
AutomaticLoginEnable=True
AutomaticLogin=sysadmin
```


```
LXDE 支持 Fedora
Xfce 支持 Fedora, CentOS
```
