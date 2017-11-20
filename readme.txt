old﻿1新分支不小心将git远程地址配错了，再次配置提示以下错误：

fatal: 远程 origin 已经存在。

此时只需要将远程配置删除，重新添加即可；

git remote rm origin

git remote add origin https://github.com/***/WebCrawlers.git

再次提交文件即可正常使用

粗心造成的小错误，顺便说一下，如果git没有commit就执行push操作会出现以下错误

fatal: unable to access 'https://github.com/***/WebCrawlers.git/': Empty reply from server

解决：只需要先commit 在 push即可
第一次提交内用：
git push -u origin master第一次推送master分支的所有内容；

创建好之后提交只需执行命令

git push origin master
前提是你已添加并提交git
git add . (添加说有)
git add --文件名
git commit -m 备注

GitHub允许你添加多个Key。假定你有若干电脑，你一会儿在公司提交，一会儿在家里提交，只要把每台电脑的Key都添加到GitHub，就可以在每台电脑上往GitHub推送了
添加key参考链接：https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/001374385852170d9c7adf13c30429b9660d0eb689dd43a000


以上是本地提交远程

下面说说从远程拉取：
git clone git@github.com:wangdenglin/gitskills.git
或者
git clone https://github.com/wangdenglin/gitskills.git

同步
$ git remote -v


执行git remote -v后看到自己的remote端名字为origin:

$ git remote -v
origin  https://code.google.com/p/micolog2 (fetch)
origin  https://code.google.com/p/micolog2 (push)

执行git branch后看到自己当下用的分支是master:

$ git branch

master
因此在本地commit后，再执行

git push origin master

即可。

删除文件：git rm test.txt
删除错误撤销：git checkout -- test.txt
查看改变 git status
查看记录 git log
版本回退：$ git reset --hard HEAD^（^表示上一个版本^^表示上二个版本）
回退指定版本： git reset --hard 3628164（3628164表示版本）
删除远程库的分支：git push origin --delete <branchName>
删除与远程不匹配的本地分支：	git fetch -p

