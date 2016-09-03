# git-book
一、协作工作：
1. fork `other github`
2. git remote -v 查看当前本地的git
3. git remote add upstream `other github`
4. git remote -v 重新查看当前的git

二、推送文件到远程管理
git init -> git add. -> git commit -a -m ‘’ -> 在github上创建远程仓库 -> git push -> git remote add origin `远程链接`

三、拉去方式
pull —- 更新本地仓库和工作区
fetch，merge — fetch，只会更新本地仓库，不会更新工作区；merge，将本地仓库merge到工作区

四、回退(提交到本地仓库回退)
1. git log —pretty=oneline
2. git reset —hard HEAD^ | git reset —hard HEAD~1 —- 默认回到上一个版本（HEAD只能会退到之前的版本，而不能会退到未来的版本）

五，回退2(紧急修复回退)
git stash 保存暂存区和工作区的数据

git stash pop 将stash区的数据婆婆出来，并删除

六、标签
git tag <tagName> -m ‘first tag’ 添加标签

git tag -l 查看所有标签

git push origin --tags 一次性推送全部尚未推送到远程的本地标签 


七、删除远程分支和tag
1. 分支操作
1.1 新建本地分支和远程分钟
git checkout -b <branchName>
git push origin <branchName>

1.1 删除远程分支
git push origin --delete <branchName>


2. 标签操作
2.1 新建本地标签和远程标签
git tag <tagName>
git push origin --tags
2.2 删除远程tag
git push origin --delete tag <tagName>


八、总结

git reset HEAD file —> 暂存区到工作区

git checkout —- file —> 回退到未add之前的数据（除暂存区以外的数据）


九、附录
1. 查看配置信息
git config —list

2. 修改最后一次提交
git commit --amend

3. 查看远程仓库信息
git remote show [remote-name]

