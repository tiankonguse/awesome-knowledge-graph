# GIT 知识图谱


## 简介


Git 是一个免费的开源的分布式版本控制系统。  
不管是小项目还是超级大项目，都可以快速、高效的使用这个系统。  

目前使用的大型开源项目有linux kernel、Android、chromium、mono、dotnet、...  


官网地址： https://git-scm.com/  
官当文档：https://git-scm.com/book/en/v2  
动画版教程： https://learngitbranching.js.org/?demo  

## 相关文章  

* [GIT的基本命令](https://mp.weixin.qq.com/s/-5AfxcJw7xuyEFuOYciryg) 
* [GIT 分支管理](https://mp.weixin.qq.com/s/07z8UOjqFb7HjntYIr7mFw)   
* [GIT：工作流程](https://mp.weixin.qq.com/s/rFL91DJrKMbKEx0lIfc0dg)  
* [Git 实践：SVN 迁移 Git](https://mp.weixin.qq.com/s/10TjsdYTCbyQ_IpTV5uwMg)  


## 基本概念

* origin：默认远程版本库名   
* master：默认分支名  
* origin/master：远程默认分支名  
* HEAD：当前分支顶端Commit的别名  
* commit（提交）：每个commit都是全部文件的完整快照，并用一个 commitID 来唯一标志。  
* detached HEAD：HEAD没有指向任何分支的状态。  
* Working Directory：当前工作区。  
* Stage(Index)：即暂存区，为等待Commit的文件列表。  
* Local Repository：本地版本库。  
* Remote Repository：远程版本库。  


从某个角度上来说，Git维护的就是一个commitID有向无环图。  


## 命令


* 配置全局用户名  `git config --global user.name "tiankonguse" `  
* 配置全局邮箱 `git config --global user.email "i@tiankonguse.com"`  
* 配置默认编辑器 `git config --global core.editor vim`  
* 显示配置列表 `git config --list`  



* 当前目录创建为git仓库 `git init`  
* 创建name目录，目录内创建git仓库 `git init name`  
* 拉去远程仓库 `git clone url`  

* 提交空目录（确实为空） - git默认不会提交空目录，可以在目录中创建 `.gitkeep`文件。  
* 提交空目录（不希望里面的文件提交） - 在对应的目录中创建 `.gitignore` 文件。  

```
# 忽略所有文件
*
# 除了这个文件
!.gitignore
```



* 指定文件加入到暂存区 `git add file`  
* 移动文件 `git mv`  
* 删除文件 `git rm`  

* 撤销修改 `git checkout file`  
* 撤销本地提交 `git reset file`  



* 暂存区文件提交到本地仓库 `git commit -m "修改说明"`  


* 添加远程仓库地址 `git remote add origin https://github.com/tiankonguse/awesome-knowledge-graph.git`  
* 查看远程仓库地址 `git remote -v`  
* 删除远程仓库地址 `git remote remove shotname`
* 修改远程仓库地址 `git remte set-url origin URL`


* 推动到远程仓库 `git push -u origin master`  
* 拉去远程仓库（未合并到本地）  `git fetch [remoteName] [branchName]`   
* 拉去远程仓库（合并到本地）：`git pull [remoteName] [branchName]`  


* 创建分支 `git checkout -b/-B`  
* 查看本地分支 `git branch`   
* 查看远程分支 `git branch -r` 
* 查看全部分支 `git branch -a`  
* 切换分支 `git checkout`  
* 查看tag列表 `git tag`  
* 简单合并分支 `git merge`  
* 高级合并分支 `git rebase`  

* 查看当前的状态 `git status` 
* 以简洁形式查看状态 `git status -s`  
* 查看提交记录 `git log`  
* 查看提交记录（附修改的文件） `git log --stat` 
* 查看指定文件的提交记录 `git log filename`   
* 查看指定文件的提交记录 `git log --follow filename`   
* 搜索提交记录 `git log --grep "word" `  
* 查看指定人的提交 `git log --author=name`  
* 查看最近三天的提交记录 `git log --since=3.days`  
* 查看某个具体时间之前的提交记录 `git log --since="1 weeks 2 days 3 hours 4 minutes 5 seconds ago" `  
* 查看某个时间段的提交记录 `git log --after="2018-10-8" --before="2018-10-10" `  
* 查看最近5条记录 `git log -5`  
* 简洁模式查看提交记录 `git log --pretty`  
* 一行模式查看提交记录 `git log --oneline`  
* 以图形方式显示提交记录 `git log --graph`  
* 查看指定分支的提交记录 `git log name`  
* 查看提交记录的文件状态 `git log --name-status `  
* 查看提交记录的统计数据 `git log --stat `  
* 查看提交记录的简单统计数据 `git log  --shortstat `  
* 查看操作记录 `git reflog`  
* 查看差异 `git diff`  

* 查看标签 `git tag`  


