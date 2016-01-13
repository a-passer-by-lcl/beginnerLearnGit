#Git入门

###1、Git简介
* Git是目前世界上最先进的分布式版本控制系统。
* Git是一个分布式的版本控制系统，最初由Linus Torvalds编写，用作Linux内核代码的管理。
* GitHub 使用 git 分布式版本控制系统，而 git 最初是 Linus Torvalds 为帮助Linux开发而创造的，它针对的是 Linux 平台，与Windows有些矛盾，后来GitHub 发布了GitHub for Windows，为 Windows 平台开发者提供了一个易于使用的 Git 图形客户端。

###2、创建Git仓库
1. 注册账户以及创建仓库
	* 登陆[Github](https://github.com/)注册Github账号--[注册](http://wiki.jikexueyuan.com/project/github-basics/sign-up.html)
	* [创建仓库](http://wiki.jikexueyuan.com/project/github-basics/creat-new-repo.html)（免费用户只能建公共仓库）

2. 安装客户端msysGit
	* Windows用户推荐[msysGit](https://git-for-windows.github.io/)
	Github是服务端，要想在自己电脑上使用Git还需要一个git客户端
	* Windows用户推荐[msysGit](https://git-for-windows.github.io/)
	* [msysGit安装教程](http://jingyan.baidu.com/article/e52e36154233ef40c70c5153.html)
	* 装完msysgit后，右键鼠标，在本地仓库里右键选择Git Init Here，会多出来一个.git文件夹，这就表示本地git创建成功。

3. 配置Git
	* 要在本地运行msysGit，以及远程到Github仓库，需要对其做出一系列配置
	* 在本地仓库中右键Git Bash进入git命令行，进行全局配置你的用户名与邮箱
		* $ git config --global user.name "your name"
		* $ git config --global user.email "\your-email@youremail.com"

	* 由于本地Git仓库和GitHub仓库之间的传输是通过SSH加密的，创建SSH Key
	* 在用户主目录下，看看有没有.ssh目录，如果有，看看这个目录下有没有id_rsa和id_rsa.pub这两个文件，如果已经有了，可直接跳到下一步
	* 如果没有运行下面命令行，输入yes,一路回车
		* $ ssh-keygen -t rsa -C "\your-email@youremail.com"

	* id_rsa和id_rsa.pub文件SSH Key的秘钥对，id_rsa是私钥，不可泄露，id_rsa.pub是公钥，可告诉任何人

	* 登录Github，[设置SSH Key](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/001374385852170d9c7adf13c30429b9660d0eb689dd43a000)
	* 验证是否成功，输入命令行 $ ssh -T \git@github.com

4. 添加远程仓库，当你的Github上的仓库没有README.md文件时，即当创建仓库时你不选择Initialize this repository with a README
	* $ git remote add origin \git@github.com:yourName/yourRepo.git
		* yourName-----------你的Github用户名
		* yourRepo-----------你的Github上的仓库

5.提交、上传
* $ git add <files>-----------------------添加文件，上传到暂存区
* $ git status------------------------------查看有哪些修改
* $ git commit -m "<message>"-------------上传到分支
* $ git push origin master----------------将本地仓库推送到远程仓库


