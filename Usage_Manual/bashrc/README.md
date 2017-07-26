
```
echo "alias la='ls -la'" >> /home/$(logname)/.bashrc
echo "alias la='ls -la'" >> ~/.bashrc
```

用 .bashrc 而不是 .bash_profile 的原因：后者只在登入时自动source 前者在每次打开新tab时自己source

http://seisman.info/linux-environment-for-seismology-research.html

http://123.56.1.216/02.3.html

在 Linux 系统下一般通过文件 $HOME/.bashrc 配置自定义环境变量(根据不同的发行版也可能是文件 $HOME/.profile)

