#### 5.3.0.尝试使用git
	user:东
	这是一个移动端页面,有我使用git的一些心得。


#### 5.3.1.初始化一个本地GIT仓储

	// 定位到仓储文件夹目录
	$ cd /dir
	// 初始化本地仓储
	$ git init
		初始化一个本地仓库。


#### 5.3.2.查看本地仓储的变更状态
	$ git status  (如果出出红色  代表文件冲突)
	    解决：编辑一下内容 > git add  > commit

	$ git status -s
	```
		第一次查看是一堆没有被跟踪的文件。



#### 5.3.3.添加本地暂存（托管）文件
```
	添加指定文件名的文件
	$ git add index.html。




#### 5.3.4.添加git忽略清单 哪些文件不用被管理
```
	建立.gitignore文件




#### 5.3.5.提交被托管的文件变化到本地仓储
```
	git commit -m '提交日志' （把本地“全部”文件的变化提交到本地仓库存档）
	git commit -m "xxx" yyy.file   （提交某一个文件）
	

#### 5.3.6.  git diff(提交后，和提交前的代码有什么不同)
```


#### 5.3.7.git log
```
	git log  查看提交版本次数


#### 5.3.8.  回归到指定版本
```
	git reset --hard [path] //输入前6位



#### 5.3.9  不用每次都输入密码 配置 config文件
```
	[core]
		repositoryformatversion = 0
		filemode = false
		bare = false
		logallrefupdates = true
		symlinks = false
		ignorecase = true
	[remote "origin"]
		url = https://[user:name]:[parsword:parsword]@github.com/youzhidong/my-todomvc.git
		fetch = +refs/heads/*:refs/remotes/origin/*
	[branch "master"]
		remote = origin
		merge = refs/heads/master


#### 5.4.0  把文本拉到本地
```
	git pull origin master



#### 5.4.1 如果pull回来报错了
```
		error: Your local changes to the following files would be overwritten by merge:
        protected/config/main.php
		Please, commit your changes or stash them before you can merge.

		如果希望保留生产服务器上所做的改动,仅仅并入新配置项, 处理方法如下:

		git stash
		git pull
		git stash pop
		然后可以使用Git diff -w +文件名 来确认代码自动合并的情况.



		反过来,如果希望用代码库中的文件完全覆盖本地工作版本. 方法如下:

		git reset --hard
		git pull


#### 5.4.2  如何上传文件
```
	echo "# git_home" >> README.md
	git init
	git add README.md
	git commit -m "first commit"
	git remote add origin https://github.com/youzhidong/git_home.git
	git push -u origin master
	```




