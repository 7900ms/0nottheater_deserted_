yum 系统组件

= = = 碎碎念 = = =

系统组件/包管理

查看软件信息

安装软件

卸载软件

更新软件

查看list

源：为了尽 可能保证系统的稳定性，此处大型第三方源只添加 EPEL 源、Nux Dextop 和 ELRepo 源[-](http://seisman.info/linux-environment-for-seismology-research.html)

大型软件：商业软件或第三方软件都安装到 /opt 目录下 [-](http://seisman.info/linux-environment-for-seismology-research.html)

源码编译：(一般来说，这类软件的默认安装目录都是 /usr/local ，最终文件会被分别放在 /usr/local 的 bin、lib、share、man 目录下。)不分散走各个目录，指定目录 ./configure --prefix=/opt/xxxx [-](http://seisman.info/how-to-install-softwares-under-centos-7.html)

```

系统升级 (所有组件更新,linux内核4.8.6到4.10.8,firefox48到52,vlc2版本到3不稳定版本)
yum check-update
yum update

源
yum repolist all
sudo yum install epel-release

安装软件
yum info git (installed)
yum info wget(available)
sudo yum install wget
sudo yum --disablerepo=* --enablerepo=base install wget

安装组
yum grouplist
yum grouplist | Tools
yum groupinfo xfce
yum groupinfo "X Window System"
yum groupinfo "Development Tools"
sudo yum --enablerepo=base groupinstall xfce
sudo yum groupinstall "Development Tools"

更新软件
sudo yum update xxx
sudo yum groupupdate xxx

查看list
yum list installed | grep wget
yum list installed | grep kernel
yum group list
yum group list installed


/supplementary/傲游
https://github.com/7900ms/0nottheater_deserted/blob/master/supplementary/鲁大师-系统管理-系统组件.txt

```
