# VIM

## 配置

* 显示空白和table

```
highlight RedundantSpaces ctermbg=red guibg=red
match RedundantSpaces /\s\+$\| \+\ze\t\|\t/
```

* 显示换行符

```
:set list
:set nolist
```


## 常见命令


* 左右分割 `:vsp [fileName]`
* 上下分割 `:sp [fileName]`
* 窗口切换 `<C-w> hjkl`  
* TAB页卡 `te [fileName]`
* 上一个TAB `tp`
* 下一个TAB `tn`



## 性能

插件配置较多或者配置有误时，打开会比较慢。

0. 查看文档

```
:help --startuptime
:help slow-start
```

1. 测试不加载插件的速度 `vim -u NONE`  
2. 使用参数 `--startuptime output.log` 来输出时间消耗在哪里了。





