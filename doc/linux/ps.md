# PS

用于查看当前进程的信息。

# 参数说明

* `-A` 显示所有进程  
* `-e` 显示所有进程  
* `-C cmdlist` 使用命令名字筛选  
* `-G grplist` 使用 group ID 或者 group name 进行筛选  
* `-u userlist` 使用 user ID 或者 user name 进行筛选  
* `-p pidlist` 使用进程 ID 进程筛选
* `f` 输出完整的默认格式
* `-o format` 指定格式，如 `-o pid,lstart,comm,args`

# 常见字段名

## AIX 格式

使用样例： `ps -eo "%p %y %x %c"`  

       CODE   NORMAL   HEADER
       %C     pcpu     %CPU
       %G     group    GROUP
       %P     ppid     PPID
       %U     user     USER
       %a     args     COMMAND
       %c     comm     COMMAND
       %g     rgroup   RGROUP
       %n     nice     NI
       %p     pid      PID
       %r     pgid     PGID
       %t     etime    ELAPSED
       %u     ruser    RUSER
       %x     time     TIME
       %y     tty      TTY
       %z     vsz      VSZ

## 普通格式  

使用样例：`ps -eo pid,user,args --sort user`  

CODE       HEADER   DESCRIPTION  
%cpu       %CPU     CPU  
pcpu       %CPU     CPU  
c          C        CPU使用率  
cp         CP       cpu使用率  
%mem       %MEM     内存使用率  
pmem       %MEM     内存使用率  
args       COMMAND  命令的完整参数  
cmd        CMD      同args  
command    COMMAND  同 args  
comm       COMMAND  命令名  
fname      COMMAND  进程名的前8字符  
bsdstart   START    命令启动时间。格式是 ` HH:MM` 或者 `mmm dd`  
lstart     STARTED  命令启动时间  
start_time START    启动时间
bsdtime    TIME     累计的CPU时间  
cputime    TIME     累计的CPU时间  
euser      EUSER    有效的用户名  








