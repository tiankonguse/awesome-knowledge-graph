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



