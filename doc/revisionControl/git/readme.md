# GIT 知识图谱


## 简介


Git 是一个免费的开源的分布式版本控制系统，不管是小项目还是超级大项目，都可以快速、高效的使用这个系统。  

官网地址： https://git-scm.com/  
官当文档：https://git-scm.com/book/en/v2  

## 命令


* 创建本地仓库 `git init`  


* 指定文件加入到暂存区 `git add file`  
* 提交空目录（确实为空） - git默认不会提交空目录，可以在目录中创建 `.gitkeep`文件。  
* 提交空目录（不希望里面的文件提交） - 在对应的目录中创建 `.gitignore` 文件。  

```
# 忽略所有文件
*
# 除了这个文件
!.gitignore
```


* 暂存区文件提交到本地仓库 `git commit -m "修改说明"`  


* 设置远程仓库地址 `git remote add origin https://github.com/tiankonguse/awesome-knowledge-graph.git`  


* 推动到远程仓库 `git push -u origin master`  



