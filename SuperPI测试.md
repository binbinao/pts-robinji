# SuperPI测试安装和使用

SuperPI下载和安装

```创建下载安装目录

$ git clone https://github.com/Fibonacci43/SuperPI.git

或者使用国内的代码仓库

$ git clone https://gitee.com/lg19891024/SuperPI.git

$ cd SuperPI/

$ ls
CMakeLists.txt  fftsg_h.c  install.txt  Makefile  pi_fftcs.c  README.md  readme.txt

$ gcc -O -funroll-loops -fomit-frame-pointer pi_fftcs.c fftsg_h.c -lm -o pi_css5

编译后文件如下，生成了pi_css5

$ ls
CMakeLists.txt  fftsg_h.c  install.txt  Makefile  pi_css5  pi_fftcs.c  README.md  readme.txt

执行测试。将计算圆周率小数点后2的26次方位的数值，即64M（6700万）位。

$ ./pi_css5 $((1<<26))    # 等同于 ./pi_css5 67108864
```

```
watch grep \'cpu MHz\' /proc/cpuinfo
```