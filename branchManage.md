#分支管理

###一、主分支master
    1、代码库有且仅有一个主分支，即master分支

    2、主分支是用来发布某软件或程序正式版本的，即提供给用户版本(1.0, 2.0...)

    3、git主分支的名字，默认叫做master，而且是自动建立的，版本库初始化以后，默认就是在主分支在进行开发

###二、开发分支develop
    1、日常开发在develop分支上进行，即开发用的分支，叫做develop

    2、如果要对外发布，要在master分支对其develop分支进行合并(merge)

    3、develop分支要比主分支master(待更新)

    4、开发分支develop命令
		(1)、创建dev分支
		$ git branch dev master
		(2)、切换到dev合并
		$ git checkout dev
		或者创建并切换
		$git checkout -b <branchName>

		(3)、查看分支
		$ git branch

		(4)、在dev分支进行开发，即
		$ git add <filename>
		$ git status
		$ git commit <filename> -m <message>

		(5)、切换到master分支
		$ git checkout master

		(6)、将dev分支合并到master分支
		$ git merge --no-ff dev

		(7)、删除dev分支
		$ git branch -d dev

		(8)、查看合并图
		$ git log --graph
　　
###三、临时性分支
    1、版本库主要有两条主要分支，即：主分支master与开发分支develop

    2、除两条主要分支外还有用于某些特定目的的版本开发，即临时分支

    3、临时分支主要有三种，即：功能分支-feature、预发布分支-release、修补bug分支-fixbug

###四、功能分支-feature
    1、即用于开发某些特定功能，从开发分支develop分出来支分支，开发完成后再并入开发分支develop

    2、功能分支feature命名形式：feature-*

    3、创建一个功能分支
		(1)创建并切换到功能分支
		$ git checkout -b feature-x develop

		(2)开发完成后，将功能分支合并到develop分支
		$ git checkout develop
		$ git merge --no-ff feature-x

		(3)删除feature分支
		$ git branch -d feature-x

###五、预发布分支-release
    1、即指发布正式版本之前（即合并到master分支之前），预发布的版本进行测试

    2、预发布分支从开发分支develop上分出来支分支，预发布结束以后，必须合并到开发分支develop和主分支master上

    3、预发布分支release命名形式：release-*

	4、创建一个预发布分支
		(1)创建并切换到预发布分支
		$ git checkout -b release-1.0 develop

		(2)无误后，合并到master分支
		$ git checkout master
		$ git merge --no-ff release-1.0

		(3)对合并生成的新节点，做一个标签
		$ git tag -a 1.0

		(4)再合并到develop分支
		$ git checkout develop
		$ git merge --no-ff release-1.0

		(5)删除预发布分支
		$ git branch -d release-1.0

###六、修补bug分支-fixbug
    1、即对于正式版本中遇到的bug，进行bug修补的分支

    2、修补bug分支是从主分支master上分出来的。修补结束以后，再合并进master和develop分支。它的命名，可以采用fixbug-*的形式。


    3、修补bug分支fixbug命名形式：fixbug-*

    4、创建一个修补bug分支
	    (1)创建并切换到修补bug分支
		$ git checkout -b fixbug-0.1 master

	    (2)修补bug完成后，合并到主分支master上
		$ git checkout master
		$ git merge --no-ff fixbug-0.1
		$ git tag -a 0.1.1

	    (3)再合并到开发分支develop上
		$ git checkout develop
		$ git merge --no-ff fixbug-0.1

		(4)删除修补bug分支
		$ git branch -d fixbug-0.1

    5、当遇到bug需要修改，且现在工作还没有完成时，先把现在的分支隐藏起来，拉下分支，修改bug后，再找到隐藏的分支继续完成

		(1)把当前工作现场“储藏”起来,等以后恢复现场后继续工作
		$ git stash

		(2)切换到mester分支
		$ git checkout master

		(3)拉下bug分支
		$ git checkout -b fixbug-0.1 master

		(4)提交bug分支，并删除
		$ git checkout master
		$ git merge --no-ff fixbug-0.1
		$ git branch -d fixbug-0.1

		(5)查看工作区
		$ git status

		(6)查看隐藏起的工作现场
		$ git stash list

		(7)恢复隐藏起的工作现场
		$ git stash apply----恢复后，stash内容并不删除，还需要用git stash drop来删除(不推荐使用)
		$ git stash pop-----恢复的同时把stash内容也删除了

		(8)多次stash,恢复的时候
		$ git stash list

		(9)恢复指定的stash
		$ git stash apply stash@{0}