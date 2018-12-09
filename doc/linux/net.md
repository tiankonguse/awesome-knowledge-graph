# 网络相关


## TIME_WAIT

快速回收 TIME_WAIT

```
sysctl net.ipv4.tcp_syncookies=1
sysctl net.ipv4.tcp_tw_reuse=1
sysctl net.ipv4.tcp_tw_recycle=1
sysctl net.ipv4.tcp_fin_timeout=30 
sysctl -p
```
## RST

RST 含义是复位，用来关闭异常的链接。  
发送 RST 那一端，发送 RST 的时候，会清空缓冲区。
接收 RST 那一端，不会对 RST 回 ACK 包。

1. 服务端口未打开

客户端向服务端发起三次握手时，服务端的端口未打开时，向客户端回 RST 。  

2. 服务端超时

客户端向服务端发起三次握手时，服务端回 ACK 了，但是回来的时间超过了客户端设置的连接时间。
此时客户端向服务端回 RST 。

3. 接收端关闭连接

TCP 通信是双通道的。  
如果某一端关闭了一个通道，而另一端对这个通道操作，就会收到 RST 。  
这个相当于接收到一个不识别的包。

4. 连接已关闭  

如果对已关闭的连接进行发包，也会收到 RST 。

注：RST不能主动发出来。比如程序 shutdown、 close、异常退出、正常退出时，都是发送 FIN 包。   




