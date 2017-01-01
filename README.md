#### 5.3.0.尝试使用git
	user:东
	这是一个移动端页面,有我使用git的一些心得。


#### 5.3.1.初始化一个本地GIT仓储
```
	// 定位到仓储文件夹目录
	$ cd /dir
	// 初始化本地仓储
	$ git init
		初始化一个本地仓库

#### 5.3.3.查看本地仓储的变更状态
	$ git status
	$ git status -s
	```
	第一次查看是一堆没有被跟踪的文件



#### 5.3.4.添加本地暂存（托管）文件
```
// 添加指定文件名的文件
$ git add index.html



####添加git忽略清单 哪些文件不用被管理
	建立.gitignore文件




#### 5.3.5.提交被托管的文件变化到本地仓储
	git commit -m '提交日志 这个说明你写了什么东东啊，很有用，要写的。'   把本地文件的变化提交到本地仓库存档
	

#### 5.3.6  git diff(提交后，和提交前的代码有什么不同)


#### 5.3.8
	git log  查看提交版本次数




#### 5.3.9  回归到指定版本
	git reset --hard [path] //输入前6位


#### 5.3.9  把文本拉到本地
	git pull origin master



#### 5.3.9  如何上传文件
	echo "# git_home" >> README.md
	git init
	git add README.md
	git commit -m "first commit"
	git remote add origin https://github.com/youzhidong/git_home.git
	git push -u origin master
	```

