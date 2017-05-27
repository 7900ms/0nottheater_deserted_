
```
echo "alias la='ls -la'" >> /home/$(logname)/.bashrc
```

用 .bashrc 而不是 .bash_profile 的原因：后者只在登入时自动source 前者在每次打开新tab时自己source

http://seisman.info/linux-environment-for-seismology-research.html

