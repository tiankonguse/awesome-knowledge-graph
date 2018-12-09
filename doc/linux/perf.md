# perf

## 查看实时数据

```
perf top -p 16279
```

## 查看统计数据

```
perf stat -p 5520
```

## 记录性能数据


```
perf record -g -p 4221 
perf report -g
```

