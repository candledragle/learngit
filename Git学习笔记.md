##Git学习笔记
>问题： git冲突Please move or remove them before you can merge

 ```
git clean -d -fx ""
其中
x -----删除忽略文件已经对git来说不识别的文件
d -----删除未被添加到git的路径中的文件
f -----强制运行
 ```
>Git远程仓库管理

```
	git remote -v # 查看远程服务器地址和仓库名称
	git remote show origin # 查看远程服务器仓库状态
	git remote add origin git@ github:robbin/robbin_site.git # 添加远程仓库地址
	git remote set-url origin git@ github.com:robbin/robbin_site.git # 设置远程仓库地址(用于修改远程仓库地址) git remote rm <repository> # 删除远程仓库
```
>Git 一键推送多个远程仓库

```
	修改本地repo的.git/config文件，添加如下内容
	[remote "all"]
		url = 远程仓库地址一
		url = 远程仓库地址二
```
>Git 查看commit 历史

```
	git log 将看到一个详细的提交日志
	git log fd0a1b2 查看某一分支的详细提交日志
```
>Git 推送内容到指定的远程仓库的指定分支

	git push -u 远程仓库名称 分支名称