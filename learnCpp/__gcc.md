
# c语言编译

```
    .c   -E预处理--> 展开头文件等  .i
    .i   -S编译-->成汇编代码        .s
    .s   -c汇编 ->object(二进制代码)  .o
    .o   链接 -->可执行文件.         

```
```
gcc -I -L -l srcs -o outfile

    -I  headers' path
        search in  -I > /usr/include >/usr/local/include

    -L  libs' path

    -l  lib 
        search in -L > LD_LIBRARY_PATH > path defined in /etc/ld.so{.conf,  .conf.d}
        修改  export LD_LIBRARY_PATH  或者  编辑  /etc/ld.so.conf || /etc/ld.so.conf.d
    
    -o xxx
    
    -g  调试
    
c++11
    gcc -std=c11 ...
    g++ -std=c++11
    

```

```
args:
      .cpp :   -fPIC    ==> .o
      .o  :   -shared  ===>.so
      .cpp : -fPIC -shared ==>.so
    
```

-static   ==>编译得到静态的. (动态链接库 也编译进了程序?maybe待验证)



