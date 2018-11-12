# GDB



* 打印内存

```
#查看内存分布
pmap -d pid 

#gdb 挂到进程
gdb -p pid

# 打印内存
# 地址类似于 0X2131 
# endAddrk可以是起始地址加一个偏移量，例如 0X2131+1234
dump binary memory fileName startAddr endAddr

#查看二进制文件
vim -b fileName
xxd fileName
hexdump fileName
```




