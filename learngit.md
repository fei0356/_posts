---
title: learngit
date: 2017-01-04 10:31:53
tags:
---

工作区｛
	file
｝

版本库｛

	git add -> 暂存区（stage）

	HEAD 指针
	git commit -> 默认分支（master）
｝

repository : 仓库名；
pwd : 显示路径；


## git常用命令
	
	1. git init 

		把这个目录变成Git可以管理的仓库；

	2. git add filename

		把文件添加到仓库；

	3. git commit -m "log"

		把文件提交到仓库；

	4. git status

		查看文件是否被修改；

	5. git diff

		查看修改具体内容

	6. git log / git log --pretty=oneline / git log --graph

		查看提交日志 ／ 查看简洁信息的提交日志 / 查看分支合并图

	7. git reset --hard HEAD^ ／ git reset --hard HEAD^^ / git reset --hard HEAD~100

		版本回退到上个版本 ／ 回退上上个版本 ／ 回退到前100个版本

	8. git reset --hard 3628164

		回到指定版本

	9. git reflog

		查看命令历史

	10. git checkout -- file

		恢复工作区内容

	11. git reset HEAD file

		撤销暂存区内容	

	12. git rm

		删除一个文件

	13. git remote add origin http"//***

		关联远程库

	14. git push -u origin master ／ git push origin master

		第一次推送master分支的所有内容 ／ 第一次以后推送

	15. git clone

		克隆一个仓库(Git支持多种协议，包括https，但通过ssh支持的原生git协议速度最快。)

	16. git branch

		查看分支

	17. git branch <name>

		创建分支

	18. git checkout <name>

		切换分支

	19. git checkout -b <name>

		创建＋切换分支

	20. git merge <name>

		合并某分支到当前分支

	21. git branch -d <name>

		删除分支 

	22. git merge --no-ff -m "merge with no-ff" dev

		合并分支时，加上--no-ff参数就可以用普通模式合并，合并后的历史有分支，能看出来曾经做过合并，而fast forward合并就看不出来曾经做过合并

	23. git stash 

		暂时封存

	24. git stash pop

		回到工作现场

	25. git stash list

		可以多次stash，用git stash list查看

	26. git branch -D <name>

		强行删除分支

	27. git remote -v

		查看远程库的信息

	28. git tag <name>

		新建一个标签

	29. git tag -a <tagname> -m "blablabla..."

		可以指定标签信息

	30. git tag -s <tagname> -m "blablabla..."

		可以用PGP签名标签

	31. git tag

		可以查看所有标签

	32. git push origin <tagname>

		推送一个本地标签

	33. git push origin --tags

		可以推送全部未推送过的本地标签

	34. git tag -d <tagname>

		可以删除一个本地标签

	35. git push origin :refs/tags/<tagname>

		可以删除一个远程标签

## 多人协作

	1. 首先，可以试图用git push origin branch-name推送自己的修改；

    2. 如果推送失败，则因为远程分支比你的本地更新，需要先用git pull试图合并；

	3. 如果合并有冲突，则解决冲突，并在本地提交；

 	4. 没有冲突或者解决掉冲突后，再用git push origin branch-name推送就能成功！

	5.如果git pull提示“no tracking information”则说明本地分支和远程分支的链接关系没有创建，用命令
	  git branch --set-upstream branch-name origin/branch-name。 




