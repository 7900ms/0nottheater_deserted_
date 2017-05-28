
系统升级
yum check-update
yum update

源
sudo yum install epel-release

安装软件
yum info git (installed)
yum info wget(available)
sudo yum install wget
sudo yum --enablerepo=base install wget

安装组
yum grouplist
yum grouplist | Tools
yum groupinfo xfce
yum groupinfo "X Window System"
yum groupinfo "Development Tools"
sudo yum --enablerepo=base groupinstall xfce


