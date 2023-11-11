#查询Git版本
git -v

#配置用户名
git config --global user.name "Forrest Zeng"

#配置用户邮箱
git config --global user.email Forrest36@163.com

#保存用户配置信息
git config --global credential.helper store

#查看用户配置信息
git config --global --list

#创建⼀个新的本地仓库（省略project-name则在当前⽬录创建。
git init <project-name>

git clone <url>
#克隆⼀个远程仓库。
git clone https://github.com/geekhall-laoyang/remote-repo.git
#报错
error: RPC failed; curl 28 OpenSSL SSL_read: Connection was reset, errno 10054
#设置全局禁用Git SSL验证，针对所有远程服务器全局执行。这样我们就可以直接跳过验证直接下载了，再次执行命令就不会再出现上述错误了。
git config --global http.sslVerify "false"

warning: in the working copy of ‘...‘, LF will be replaced by CRLF the next time Git touche
#执行git add .的时候出现的警告(没有处理这个告警，之后再说)
git config --global core.autocrlf true
#提交时转换为LF，检出时转换为CRLF：

git commit -m "message"
#提交所有暂存区的⽂件到本地仓库。

git add . #文件夹下所有文件
git add *.txt #所有txt文件
#提交至暂存区的通配符命令

git status
#查看仓库状态，列出还未提交的新的或修改的⽂件。

git log --oneline
#查看提交历史，--oneline表示简介模式。

git reset --soft <commit-id>
git reset --hard <commit-id>
git reset --mixed <commit-id>
#<commit-id>
HEAD^
#回退到上一个版本

git diff
#查看未暂存的⽂件更新了哪些部分。

git diff HEAD
#比较工作区与版本库之间的差异

git diff --cached
#比较暂存区与版本库之间的差异

git diff HEAD~2 HEAD
#比较前两个版本与当前版本之间的差异

rm file;git add file 
#先从工作区删除文件，然后再暂存删除文件

git rm <file>
#把文件从工作区和暂存区同时删除

git rm --cached <file>
#把文件从暂存区删除，但保留在当前工作区中

git rm -r*
#递归删除某个目录下的所有子目录和文件
#删除后不要忘记提交

git remote add <远程仓库别名><远程仓库地址>
#添加远程仓库
git remote add origin git@github.com:Forrest36/Forrest.git

git branch -M main
#命令用于将本地分支重命名为 main

git push -u <远程仓库别名><分支名>
git push -u origin main

git remote -v
#查看远程仓库

git pull <远程仓库别名><远程分支名>:<本地分支名>
#                      相同可省略冒号后面部分
#拉取远程仓库内容

gitee.com #码云
gitlab.com #Gitlab

git branch
#查看分支列表

git branch branch-name
#创建分支

git switch branch-name
#切换分支

git merge branch-name
#合并分支

git branch -d branch-name #已合并
git branch -D branch-name #未合并
#删除分支

