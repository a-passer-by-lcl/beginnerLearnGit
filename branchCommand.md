#分支命令

	列出所有本地分支,当前分支前面会标一个*号
	$ git branch
	列出所有远程分支
	$ git branch -r
	列出所有本地分支和远程分支
	$ git branch -a
	

	创建一个新分支,但依然停留在当前分支
	$ git branch <branch-name>
	创建一个新分支，指向指定commit
	$ git branch <branch-name> <commit>
	创建并切换到指定分支（等于上面两步）
	$ git checkout -b <branch-name>
	创建一个新分支，与指定的远程分支建立追踪关系
	$ git branch --track <branch-name> <remote-branch>
	切换到指定分支，并更新工作区
	$ git checkout <branch-name>
	

	合并指定分支到当前分支
	$ git merge --no-ff <branch-name>
	选择一个commit，合并进当前分支
	$ git cherry-pick <commit>
	

	删除分支,但是如果没有合并的时候会导致删除失败
	$ git branch -d <branch-name>
	当没有合并的时候也会删除
	$ git branch -D <branch-name>
	删除远程分支
	$ git push origin --delete <branch-name>
	$ git branch -dr <remote/branch>
	

	查看分支合并图
	$ git log --graph
	建立追踪关系，在现有分支与指定的远程分支之间
	$ git branch --set-upstream <branch-name> <remote-branch>