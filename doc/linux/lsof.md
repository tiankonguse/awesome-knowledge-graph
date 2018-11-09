# lsof

lsof 功能很简单，用于查打开的文件列表。  
可是你知道吗？在 Linux 的世界里，所有事物都是文件，所有操作几乎都是文件操作。  


## 字段介绍


`lsof`默认显示字段有`COMMAND PID USER FD TYPE DEVICE SIZE/OFF NODE NAME`.  

含义如下:  

* `COMMAND` 程序命令,默认以9个字符长度显示的命令名称。可使用+c参数指定显示的宽度，若+c后跟的参数为零，则显示命令的全名  
* `PID` 进程id  
* `PPID` 父进程的IP号，默认不显示，当使用-R参数可打开。  
* `PGID` 进程组的ID编号，默认也不会显示，当使用-g参数时可打开。  
* `USER` 命令的执行UID或系统中登陆的用户名称。默认显示为用户名，当使用-l参数时，可显示UID。  
* `FD` 文件描述符  
* `TYPE` IPv4的包,IPv6包，DIR 目录，LINK 链接文件等  
* `DEVICE` 使用`character special`、`block special`表示的设备号  
* `SIZE/OFF` 文件的大小，如果不能用大小表示的，会留空。使用`-s`参数控制。  
* `NODE` 本地文件的node码，或者协议，如TCP等  
* `NAME` 挂载点和文件的全路径（链接会被解析为实际路径），或者连接双方的地址和端口、状态等  



## 使用  

* 查看端口 `lsof -i :80`  
* 查看进程名 `lsof -c chrome | more`   
* 查看进程号 `lsof -p 2127`  
* 查看进程组 `lsof -g 2127`  
* 查看目录 `lsof +D /home/`  
* 万能搜索 `lsof -nP | grep 2017`  




