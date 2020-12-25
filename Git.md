# Git

#### 查看git安装版本

`git --version`

#### 清屏

`clear`

#### 设置签名

`git config --global user.name "Chauncy"`

`git config --global user.email "liu5831835@163.com"`

#### 本地仓库初始化（进入需要初始化文件夹）

`git init`

#### 添加文件到暂存区

`git add demo.txt`

#### 将文件从暂存区提交到本地库

`git commit -m "demo.txt first commit" demo.txt`

#### 查看状态

`git status`

#### 查看日志

b 上一页      空格 下一页 

方式一`git log`

方式二 `git log --pretty=oneline`

方式三 `git log --oneline`

**方式四 `git reflog`  多了指针信息**

#### 返回上一版本

`git reset --hard 索引号` 本地库、暂存区、工作区都回退

`git reset --mixed 索引号` 本地库、暂存区回退

`git rest --soft 索引号` 只有本地库回退

#### 删除文件

删除工作区文件

`rm demo2.txt`

将操作同步到暂存区

`git add demo2.txt`

同步到本地库

`git commit -m "delete demo2.txt" demo2.txt`

恢复文件

`git reset --hard 索引号`

#### 比对差异

`git diff demo3.txt` 比对工作区与暂存区的文件差异

`git diff HEAD demo3.txt` 比对暂存区与本地库文件的差异

#### 分支

查看分支 `git branch -v`

创建分支 `git branch 分支名字`

切换分支 `git checkout 分支名字`

合并分支 `git merge 分支名字` 将所描述分支内容合并到当前分支上

若出现冲突需要手动解决，解决完毕后再次add，commit，注意commit的时候不需要带文件名。

#### 远程库

由于远程库地址很长，可以给远程库地址取别名

查看远程库别名 `git remote -v`

给远程库地址起别名 `git remote add 别名 远程库地址`

推送 `git push 别名 master`

拉取  `git pull别名 master`

pull 相当于 fetch+merge

生成ssh免密推送

`ssh--keygen -t rsa -C 邮箱`生成ssh，去用户目录下把ssh.pub内的内容在GitHub上记录下来，就可以了。

别忘了对ssh改别名

#### 参考文献及学习网站

[马士兵教育女老师手撕GIT]: https://www.bilibili.com/video/BV1zp4y167Cw?p=16
[Learning GIT Branching 项目]: https://learngitbranching.js.org/?locale=zh_CN

