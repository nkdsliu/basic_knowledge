# 代码下载&提交
* git clone -b 分支名 ssh链接 -> 拉取指定分支代码
* cd 代码对应目录 -> 切换到对应代码目录
* git checkout 分支名 -> 切换分支
* git status -> 查看文件状态
* git pull -> 拉取最新代码（相当于git fetch 仓库名 分支名 -> 拉取远程代码 + git merge与本地代码合并）
* git add . -> 暂存文件
* git commit -m "更新描述" -> 添加提交信息
* git push origin 分支名 -> 提交代码
# 只修改单个文件
* git commit 文件名 -m "modify dir"
* git push
# git上传空文件夹
* git默认不上传空文件夹
* [上传空文件夹方法](https://blog.csdn.net/itnerd/article/details/114285391)
# git tag用法
* git log -> 查看提交历史，按q退出
* git log --pretty=oneline -> 查看简略log信息，只显示commit id和对应的注释
* git log --graph -> 以图表形式查看分支
* git tag -> 查看所有标签
* git tag -a v1.0 -m "my version 1.0" commit_id -> 给commit_id版本的代码创建v1.0版本并有描述信息的tag，版本号和描述信息可修改（若无commit_id则表示当前版本）
* git show v1.0 -> 显示v1.0版本tag信息
* git push origin v1.0 -> 将v1.0的tag提交到origin远程仓库
# git版本回退
* git reset --hard commit_id -> 将代码回退到commit_id版本（可通过查看tag的commit_id回退到指定tag）
* git push -f origin master -> 推送到远程origin仓库的master分支，不存在冲突时可省略-f参数，不存在多个仓库和多个分支时，origin master可省略
* git reflog -> 可以重返未来，git log命令只能查看以当前状态为终点的历史日志，而git reflog能够查看全部时间下的历史日志，不受当前状态影响
# git多分支开发
* git branch -> 查看所有分支
* git branch 分支名 -> 以当前分支的当前版本为基础创建一个新分支
* git branch --set-upstream master origin/next -> 设置本地master分支与远程next分支追踪关系
* git branch -d 分支名 -> 删除分支
* git checkout 分支名 -> 切换分支
* git checkout -b 分支名 -> 创建并切换分支
* [git分支原理](https://git-scm.com/book/zh/v2/Git-%E5%88%86%E6%94%AF-%E5%88%86%E6%94%AF%E7%AE%80%E4%BB%8B#ch03-git-branching)
* [git push/pull指定仓库和分支](https://www.cnblogs.com/stephen-init/p/3833054.html)
* git pull <远程主机名> <远程分支名>:<本地分支名>, git push <远程主机名> <本地分支名>:<远程分支名>（若远程分支不存在会创建）
* git merge 分支B -> 当前在A分支工作，将B分支合并到A分支，合并结果存储在A分支，对B没有影响
* [git冲突](https://juejin.cn/post/7004643157279244325)，手动解决冲突后需重新add和commit
# 其他常用命令
* 用HEAD表示当前版本，上一个版本是HEAD^，上上一个版本是HEAD^^，往上100个版本写成HEAD~100
* git worktree多分支开发
* git push --set-upstream origin ocr -> 设置本地当前分支与远程ocr分支追踪关系
# git教程
* [廖雪峰](https://www.liaoxuefeng.com/wiki/896043488029600/900004111093344)
* [菜鸟](https://www.runoob.com/git/git-branch.html)
# git分支管理
* [Git flow](https://blog.csdn.net/renxingzhadan/article/details/125602045)
