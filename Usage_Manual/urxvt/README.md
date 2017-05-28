终端显示中文：用正确的[字体](https://github.com/7900ms/0nottheater_deserted_/tree/master/Usage_Manual/fonts)
```
查看区:
/usr/bin/urxvt
/usr/lib64/urxvt/perl (/usr/lib/urxvt/perl)
~/.Xresources

urxvt --help 2>&1 | grep options:  #=>不支持unicode3 (urxvt -v)
urxvt --help 2>&1| sed -n '/:  /s/^ */! URxvt*/gp'   #=> 全部可配置项 

doc
http://www.askapache.com/linux/rxvt-xresources/
https://linux.die.net/man/1/urxvt

配置区：

1.
安装
sudo yum install rxvt-unicode

which urxvt
#=> /usr/bin/urxvt

vi ~/.xinitrc 空文件加入
`
export LANG=en_GB.UTF-8
[[ -f ~/.Xresources ]] && xrdb -merge ~/.Xresources
`
source ~/.xinitrc

2.
测试

urxvt

复制粘贴：
ctrl+alt+c
ctrl+alt+v

3.
命令行测试
urxvt -fn "xft:monospace:size=14:antialias=true"
(Unicode的支持很差)

4.
配置测试

vi ~/.Xresources
`
URxvt.font: xft:Monospace:style=Regular:size=14:antialias=true
URxvt.scrollBar:True
URxvt.scrollBar_right:True
URxvt.scrollBar_floating:False
URxvt.scrollstyle:next
`

生效
xrdb ~/.Xresources

成功


5.
图标
https://wiki.gentoo.org/wiki/Rxvt-unicode



参考区:
urxvt会按照 X 的配置来运行。X 的配置 见 fvwm

参考区:
urxvt Unicode
https://github.com/powerline/powerline/issues/684#issuecomment-120308226


```
