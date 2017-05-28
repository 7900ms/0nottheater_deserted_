
zsh + urxvt
```
检查区

/usr/bin/zsh
/usr/share/zsh

配置区

chsh -l
which zsh

sudo yum install zsh
(rpm -ql zsh)
chsh -l
su -c "echo $(which zsh) >> /etc/shells"
chsh -l
chsh -s $(which zsh) $(whoami)
// 改回默认bash：sudo chsh -s $(which bash) $(whoami)


```
