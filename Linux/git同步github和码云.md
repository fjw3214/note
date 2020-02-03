首先github和码云上的仓库都要建好。然后将其中一个仓库clone到本地
`git clone XXXXX`
修改.git里面的配置文件config
```git
[core]    
	repositoryformatversion = 0    
	filemode = false    
	bare = false    
	logallrefupdates = true    
	symlinks = false    
	ignorecase = true
[remote "github"]    
	url = https://github.com/****/note    
	fetch = +refs/heads/*:refs/remotes/origin/*
	
# 添加码云的url
[remote "gitee"]    
	url = https://gitee.com/****/note    
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]    
	remote = origin    merge = refs/heads/master

```
提交代码时
```git
git add .
git commit -m "update"
#提交到github
git push github master
#提交到码云
git push gitee master
```
拉取更新时
```git
#从github拉取更新
git pull github
#从码云拉取更新
git pull gitee

```
如果很少拉取更新或者嫌上面这个麻烦可以
```git
[core]    
	repositoryformatversion = 0    
	filemode = false    
	bare = false    
	logallrefupdates = true    
	symlinks = false    
	ignorecase = true
[remote "origin"]    
	url = https://github.com/****/note    
	# 在这里添加码云的url
	url = https://gitee.com/****/note    
	fetch = +refs/heads/*:refs/remotes/origin/*
	
[branch "master"]    
	remote = origin    
	merge = refs/heads/master

```
这样提交时只用`git  push origin master`,不用分别提交。

