yum 系统组件

```

系统升级 (所有组件更新,linux内核4.8.6到4.10.8,firefox48到52,vlc2版本到3不稳定版本)
yum check-update
yum update

源
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
