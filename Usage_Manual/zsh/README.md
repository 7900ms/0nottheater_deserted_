
zsh + urxvt

配色问题：
zsh文字颜色 + urxvt背景色
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
重启，打开终端 选择零
echo $0

(注意：默认的 zsh 不会 source ~/.bashrc 。对 zsh 修改 ~/.zshrc 等于 对 bash 修改 ~/.bashrc (而非 bash_profiel))

sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
nano ~/.zshrc & 打开新tab (打开新tab时会自动source ~/.zshrc)

```
```
ZSH_THEME="ys"
DISABLE_AUTO_UPDATE="true"
plugins=(git bundler osx rake ruby)
plugins=(git bower sublime brew history node npm sudo web-search fedora)

## 1st
DEFAULT_USER=`whoami`
TZ='Asia/Hong_Kong'; export TZ

```
```


```
