
为什么不是 supervisor [1](#systemdsupervisor)

[1](http://www.linuxprobe.com/chapter-00.html)

测试
```
时区同步
sudo yum install ntp
sudo systemctl status ntpd
sudo systemctl start ntpd
sudo systemctl status ntpd
sudo systemctl enable ntpd # 开机自启
```
