
Eclipse [4.5.2](http://www.eclipse.org/downloads/packages/release/Mars/2)

```
~/local/opt
~/.local 未使用

查看区：

/users/0/axxxxxxx/local/opt/eclipse
/users/0/axxxxxxx/local/workspace/workspace_eclipse/test1

Eclipse Run: shift + f11 (no need of makefile)
Makefile Run: make student

低频查看区：

/users/0/a1734530/local/opt/eclipse/plugins
/users/0/a1734530/local/opt/eclipse/features

快捷方式
ln -s '/users/0/a1734530/local/opt/eclipse/eclipse' /users/0/a1734530/Desktop/

清除插件
> rm -r workspace/.metadata

eclipse.ini
/users/0/a1734530/local/opt/eclipse/eclipse.ini

版本
Eclipse 4.5.2


配置区：

1.
下载

版本，支持语言，型号(一般版，开源开发版 with Incubating components)
http://www.eclipse.org/downloads/
http://www.eclipse.org/downloads/eclipse-packages/
http://www.eclipse.org/downloads/packages/eclipse-ide-cc-developers/oxygenr
http://www.eclipse.org/downloads/packages/eclipse-ide-cc-linux-developers-includes-incubating-components/heliossr2 # 早期版本 启动快 不卡
https://en.wikipedia.org/wiki/Eclipse_(software)
http://andrei.gmxhome.de/filesync/links.html#4.4Luna
https://netbeans.org/downloads/index.html


Most Popular c++ IDE linux

eclipse version

java -version
javac -version
java -d64
which java
which javac


最终决定下载
http://www.eclipse.org/downloads/packages/release/Mars/2 (Eclipse 4.5.2)
(7s on startup)


2.
安装准备

避免冲突
/opt/eclipse/4.5.2  mars

避免项目 workspace 冲突
cd ~/local/workspace/workspace_eclipse
rm -r .metadata

3.
安装
cd ~/local/opt
鼠标右键 - Extract Here
（tar -xvzf /path/to/eclipse-cpp-galileo-SR1-linux-gtk-x86_64.tar.gz
tar -xvzf /users/0/a1734530/Downloads/eclipse-cpp-oxygen-R-linux-gtk-x86_64.tar.gz ）

快捷方式
ln -s '/users/0/a1734530/local/opt/eclipse/eclipse' /users/0/a1734530/Desktop/

4.
初次软件设置

第一次启动软件
设置 workspace
/users/0/a1734530/eclipse-workspace (默认)
mkdir -p ~/local/workspace/workspace_eclipse (设为)

- disable spelling check
Window, Preferences, General, Editors, Text Editors, Spelling - to disable spell checking.

- 项目窗口
eclipse welcome 取消勾选 Always show , 再次进入 关掉 welcome，第三次进入正常 

- 询问 workspace 位置
Preferences->General->Startup and Shutdown->Workspaces and activate the checkbox
"prompt for workspace on startup" and restart your eclipse.

- 导入项目
File - Import - General - Existing Projects into Workspace

- 自动刷新
auto refresh
~~~ Project - Properties->Build->Refresh Policy~~~
Preferences - General - Workspace - Refresh using native hooks or polling
Preferences - General - Workspace - Refresh on access
Preferences - General - Workspace - Save automatically before build
Preferences - General - Startup and Shutdown - Refresh workspace on a startup
Project - Build Automatically

- 关掉自动更新
Automatic Updates x


-


4.
reset设置

4.1 重新设置 workspace (避免冲突)
> rm -r workspace/.metadata


4.2 reset project
1) Project->Clean...,
2) close and open Eclipse again,
3) Run As...
https://stackoverflow.com/questions/253357/eclipse-problems-view-not-showing-errors-anymore


4.3 reset Perspective
Window - Perspective - reset perspective

4.4 清除插件
> rm -r workspace/.metadata




4.3 查看
表示符
Navigate - Open Element ...


5.
启动设置

5.1  eclipse no splash screen 
nano eclipse.ini
```+
-showsplash 改为 
-nosplash
```


5.4 优化启动速度
nano eclipse.ini 添加
-Xverify:none
update-alternatives --config java (不要动)
https://stackoverflow.com/questions/316265/how-can-you-speed-up-eclipse



6.
软件设置和插件

6.0 startexplorer （无法安装）
Help
Install New Software
Add...
Name: StartExplorer
Location: https://fabioz.github.com/startexplorer/update/
Tick the StartExplorer Feature checkbox (Window->Show view->Other.)
手动下载 https://github.com/anb0s/EasyShell/releases (a zip contains content.jar and artifacts.jar)
手动下载 http://blog.samsonis.me/2009/02/open-explorer-plugin-for-eclipse/

安装办法
(install-eclipse-plugins-offline)
https://stackoverflow.com/questions/5482554/how-to-install-plugin-for-eclipse-from-zip
解压 之后 
cd $ECLIPSE_HOME/plugins
cd /users/0/a1734530/opt/eclipse/plugins
cd /users/0/a1734530/opt/eclipse/features 对应做 (主要是 plugins)
重启软件之后， Preference 里看到插件设置 即插件安装成功

6.1 EasyShell （已安装）

6.1.1
下载
https://github.com/anb0s/EasyShell/releases
6.1.2
安装
解压 之后 
cd $ECLIPSE_HOME/plugins
cd /users/0/a1734530/opt/eclipse/plugins
cd /users/0/a1734530/opt/eclipse/features 对应做 (主要是 plugins)
重启软件之后，Window - Preference 里看到插件设置 即插件安装成功
6.1.3
配置 “Show in System Explorer”
Preferences - EasyShell
Menu - Add - New ...
填入 command: xdg-open ${easyshell:container_loc}
确定，Menu: Pattern: 选择 User defined
填入 Name: Show in System Explorer

``` 探索过程
搜索 container_loc 相关 command
testing:
gnome-commander --start-left-dir ~/opt
gnome-terminal --working-directory="~/opt"
xdg-open "~/opt"
xdg-open ${easyshell:container_loc}
```




7.
更多设置：

设置软件的 perspective

https://developer.atlassian.com/docs/getting-started/set-up-the-atlassian-plugin-sdk-and-build-a-project/set-up-the-eclipse-ide-for-linux
http://www.math.ucla.edu/~anderson/UsingEclipseCPP/OpeningCPPperspective/index.html
https://www.tutorialspoint.com/eclipse/eclipse_perspectives.htm

新建项目：新建项目，添加文件，编译，看结果，debug 
http://www.math.ucla.edu/~anderson/UsingEclipseCPP/ *****
http://www.math.ucla.edu/~anderson/UsingEclipseCPP/CreatingAProject/index.html
http://www.math.ucla.edu/~anderson/UsingEclipseCPP/AddingFiles/index.html
http://www.math.ucla.edu/~anderson/UsingEclipseCPP/RunningProject/index.html # Run

界面：终端，编辑器，提示器1（class, variable, function），提示器2（main, function）



8.
其他
makefile

G eclipse cpp

https://www3.ntu.edu.sg/home/ehchua/programming/howto/EclipseCpp_HowTo.html



9.
其他

设置 eclipse.ini 并 确认
http://eclipsebook.in/introduction/installing-eclipse/



Tricks to speed up Eclipse
https://stackoverflow.com/questions/1359704/eclipse-refreshing-workspace-takes-forever
https://stackoverflow.com/questions/316265/how-can-you-speed-up-eclipse
FileSync (4.4)



```
