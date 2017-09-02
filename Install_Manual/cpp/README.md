
安装
`sudo yum install gcc gcc-c++.x86_64`

使用

g++ main.cpp -o a.out


参考1
- 本机
```
> yum list | grep gcc
compat-gcc-44.x86_64                  4.4.7-8.el7             installed         
compat-gcc-44-c++.x86_64              4.4.7-8.el7             installed         
gcc.x86_64                            4.8.5-11.el7            installed         
gcc-c++.x86_64                        4.8.5-11.el7            installed         
gcc-gfortran.x86_64                   4.8.5-11.el7            installed         
libgcc.x86_64                         4.8.5-11.el7            installed         
gcc-gnat.x86_64                       4.8.5-11.el7            client-7.3-updates
gcc-objc.x86_64                       4.8.5-11.el7            client-7.3-updates
gcc-objc++.x86_64                     4.8.5-11.el7            client-7.3-updates
libgcc.i686                           4.8.5-11.el7            client-7.3-updates

```

参考2
```
基础开发环境
GCC 系列

sudo yum install gcc                     # C 编译器
sudo yum install gcc-c++                 # C++ 编译器
sudo yum install gcc-gfortran            # Fortran 编译器
sudo yum install compat-gcc-44           # 兼容 gcc 4.4
sudo yum install compat-gcc-44-c++       # 兼容 gcc-c++ 4.4
sudo yum install compat-gcc-44-gfortran  # 兼容 gcc-fortran 4.4
sudo yum install compat-libf2c-34        # g77 3.4.x 兼容库

软件开发辅助工具

sudo yum install make
sudo yum install gdb     # 代码调试器
sudo yum install cmake   # Cmake
sudo yum install git     # 版本控制
```
http://seisman.info/linux-environment-for-seismology-research.html

-
