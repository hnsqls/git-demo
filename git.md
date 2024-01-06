# 1.版本控制

![image-20231230094903920](images/git.assets/image-20231230094903920.png)

## 1.本地版本控制

## 2.集中式版本控制

![image-20231230095410586](images\git.assets\image-20231230095410586.png)



## 3.分布式版本控制

![image-20231230095610821](images\git.assets\image-20231230095610821.png)







![image-20231230095729830](images\git.assets\image-20231230095729830.png)



# 2.GIT安装

1.删除

* 查看环境变量，删除
* 打开控制面板卸载git



2.安装 下一步

# 3.GIT配置

```shell
git config -l    #git 所有的配置
```

![image-20231230103457761](images\git.assets\image-20231230103457761.png)



```shell
git config --system --list #系统配置
```

![image-20231230103723553](images\git.assets\image-20231230103723553.png)

```shell
git config --global --list  #用户配置
```

![image-20231230103904010](images\git.assets\image-20231230103904010.png)



**GIT相关配置文件**

1) GIT\etc\gitconfig          --system

![image-20240102182832719](images\git.assets\image-20240102182832719.png)

1)C:user\Administrato\\. gitconfig         当前用户的

![image-20240102182733744](images\git.assets\image-20240102182733744.png)

![image-20240102182746862](images\git.assets\image-20240102182746862.png)



> 设置用户名与邮箱

```shell
git config --global user.name "hnsqls"
git config --global user.emial "2661108038@qq.com"
```





# 4. GIT理论

> 工作区域

GIT有四个工作区域，工作区（Working Directory），缓存区（Stage/index），本地仓库（GIt Directory），远程仓库（Remote Directory）

![image-20240102184122233](images\git.assets\image-20240102184122233.png)

![image-20240102184850614](images\git.assets\image-20240102184850614.png)



> 工作流程

![image-20240102185256766](images\git.assets\image-20240102185256766.png)



# 5.GIT项目搭建

> 创建工作目录与常用指令

![image-20240102185455111](images\git.assets\image-20240102185455111.png)





> 本地搭建仓库

选择合适位置进入git bsah，执行初始化指令，会在该位置生成 .git文件

```shell
git init    #创建全新的仓库
```



> 克隆远程仓库

* 就是将远程的仓库复制到本地

```shell
git clone [url]
```



# 6.GIT 文件状态

![image-20240102191742161](images\git.assets\image-20240102191742161.png)

![image-20240102193306323](images\git.assets\image-20240102193306323.png)

![image-20240102194258664](images\git.assets\image-20240102194258664.png)





# 7.GIT使用

密钥 : 在 c：/administar/.ssh 打开git bash

```bash
ssh-keygen -t rsa
```



![image-20240102200345345](images\git.assets\image-20240102200345345.png)







# 8. IDEA集成、GIT





# 9 使用过程中的问题

1.  退回commit 版本
   1. git reflog 查看版本号
      1. ![image-20240105145151284](images/git.assets/image-20240105145151284.png)

2. git reset --hard <commitid>
   1. ![image-20240105145420882](images/git.assets/image-20240105145420882.png)

![image-20240105145613789](images/git.assets/image-20240105145613789.png)

本地项目出现了问题，好多东西都没了

![image-20240105152246405](images/git.assets/image-20240105152246405.png)

![image-20240105152352269](images/git.assets/image-20240105152352269.png)

我想退回到最新，但是出现了下面的情况

![image-20240105152612467](images/git.assets/image-20240105152612467.png)







--------------------------------------------------------------------------git学习-------------------------------------------------------------

# 10 GIT是什么

* git 就是版本控制的软件

**版本控制**

1. 本地版本控制![image-20240105155340676](images/git.assets/image-20240105155340676.png)
   * 虽然在本地更简便的管理本地不同版本的文件，但是不能协同开发
2. 集中式版本控制![image-20240105155618229](images/git.assets/image-20240105155618229.png)
   * SVN最具代表性，但是中央服务器宕机了，会影响开发
3. 分布式版本控制![image-20240105160027783](images/git.assets/image-20240105160027783.png)

# 11. GIT工作机制

![image-20240105164400881](images/git.assets/image-20240105164400881.png)

**还有个远程库**

* 只要commit，代码就不可能删除



# 12 GIT常用命令

```shell
git init
```

```shell
git status
```

![](images/git.assets/image-20240105170852882.png)

文件在工作区没有被追踪-->暂存区

```shell
git add .
```

![image-20240105170940722](images/git.assets/image-20240105170940722.png)

![image-20240105171008679](images/git.assets/image-20240105171008679.png)

追踪到了文件

不想要这个暂存区的文件怎么办，如下 还在工作区 

![image-20240105171457761](images/git.assets/image-20240105171457761.png)

![image-20240105172010252](images/git.assets/image-20240105172010252.png)



```shell
git reflog
git log
```

![image-20240105172259290](images/git.assets/image-20240105172259290.png)

![image-20240105173031423](images/git.assets/image-20240105173031423.png)

不同版本的信息，单文件夹就有一个，相当于就是本地的版本控制器

![image-20240105173141294](images/git.assets/image-20240105173141294.png)

觉得还是之前的版本写的好，就回到之前的版本

```shell
git reflog   #查看版本信息
git reset --hard <commitID>
```



![image-20240105174502455](images/git.assets/image-20240105174502455.png)



# 13 GIT 分支

![image-20240105175032453](images/git.assets/image-20240105175032453.png)

![image-20240105175329638](images/git.assets/image-20240105175329638.png)

* 分支的好处，能够同时进行多个功能开发，提高开发效率
* 各个分支开发过程中，一个分支失败了不会对其他分支有影响，删除该失败分支即可

> 分支的命令

```shell
git branch  <分支名>    #创建分支
git branch -v   #查看分支
git checkout <分支名> #切换分支
git merge <分支名> # 合并分支
```

查看分支 git branch -v

```shell
git branch -v
```

![image-20240105175911567](images/git.assets/image-20240105175911567.png)

创建分支 git branch <分支名>

```shell
git branch hot-fix
```

![image-20240105180038525](images/git.assets/image-20240105180038525.png)

**切换分支 git checkout <分支名>**

```shell
git chekout hot-fix
```

![image-20240105180851385](images/git.assets/image-20240105180851385.png)

* 绿色和* 是指向当前分支 



在hot-fix分支下修改hello.txt 文件

![image-20240105181352757](images/git.assets/image-20240105181352757.png)



切换到主分支,查看hello.txt

```shell
git checkout master
cat hello.txt
```

![image-20240105181637955](images/git.assets/image-20240105181637955.png)

发现没有作者信息，这只是指针指向了master分支，master指向的版本并没有添加hot-fix，hot-fix已经修改好了，可以添加到master分支上，也就是分支合并

切换到主分支合并hot-fix分支 **git merge <分支名>**

```shell
git merge hot-fix
```

![image-20240105182259935](images/git.assets/image-20240105182259935.png)

* hot-fix分支是在master分支的基础上该的，在编写hot-fix分支时，我们没有修改master分支，所以合并的时候没有冲突



> 产生冲突

​     合并分支时，两个分支都修改了相同的文件夹，git就不能自动合并了，会报合并冲突

eg：master分支上的hello.txt 添加 I love china,

​        hot-fix 分支上的hello.txt添加I love Henan, 修改后合并



![image-20240105201640955](images/git.assets/image-20240105201640955.png)

​      

![image-20240105201906780](images/git.assets/image-20240105201906780.png)



切换到master分支，合并

![image-20240105202253989](images/git.assets/image-20240105202253989.png)

怎么解决？

手动解决->在合并状态下查看文件

```shell
vim hello.txt
```

![image-20240105203505190](images/git.assets/image-20240105203505190.png)

修改成这个样子

![image-20240105203622074](images/git.assets/image-20240105203622074.png)



之后将文件添加到缓存去，然后commit到本地库

```shell
git add .
git commit -m "解决合并冲突问题"
```

![image-20240105203919095](images/git.assets/image-20240105203919095.png)



合并成功解决了不能自动合并的冲突，查看一下hello.txt文件

![image-20240105204013285](images/git.assets/image-20240105204013285.png)

是符合我们的需求的

* 需要注意的是，master分支是符号要求了，但是hot-fix分支并没有修改内容

![image-20240105204126375](images/git.assets/image-20240105204126375.png)

# 14. GIT团队合作

* 团队内合作

![image-20240105205348335](images/git.assets/image-20240105205348335.png)

* 跨队外合作

![image-20240105205322357](images/git.assets/image-20240105205322357.png)

# 16 Github操作

* 创建远程仓库

![image-20240105210359990](images/git.assets/image-20240105210359990.png)

远程仓库连接：有https连接还有ssh连接

![image-20240105210718806](images/git.assets/image-20240105210718806.png)

用https连接 复制https  用ssh连接就复制ssh连接

>远程仓库操作

```shell
git remote -v     #查看当前所有远程地址的别名
git remote add 别名 远程地址   # 给远程地址连接起别名
git push 别名 分支        #推送本地分支上的内容到远程仓库
git clone             #将远程仓库内容克隆到本地
git pull 远程仓库别名  远程分支名  #将远程仓库对于分支最新内容拉下来后与当前本地分支直接合并 
```





## push 本地库到远程库

创建上述仓库别名  git remote add 别名 远程地址

```shell
git remote add git-demo 
```

![image-20240105211833761](images/git.assets/image-20240105211833761.png)



将本地库的代码推送到远程库 git pull 别名 分支

```shell
git pull git-demo master
```

![image-20240105212249868](images/git.assets/image-20240105212249868.png)

发现报错

切换到master分支后推送

![image-20240105212700849](images/git.assets/image-20240105212700849.png)

发现还是错，第一次是说网络原因，后几次就不能指向master分支？？？

不明白怎么不行，网络我开了vpngithub也能正常访问

换ssh 

给ssh连接起别名

```shell
git remote add git-demo ssh连接
```

![image-20240105213347009](images/git.assets/image-20240105213347009.png)

**显示已经存在？怎么删除别名（坑）**

![image-20240105213603120](images/git.assets/image-20240105213603120.png)

还是报错

..............................

发现是我的命令的问题是 push 而不是pull

![image-20240105214307657](images/git.assets/image-20240105214307657.png)

查看远程仓库

![image-20240105214355686](images/git.assets/image-20240105214355686.png)



## 拉取远程库到本地库

可以在github上直接修改远程仓库点开文件修改

![image-20240105214750253](images/git.assets/image-20240105214750253.png)

![image-20240105214825054](images/git.assets/image-20240105214825054.png)

远程仓库修改，本地仓库和远程仓库不一致，本地拉去远程仓库保持一致

```shell
pull git-demo master
```

![image-20240105215323197](images/git.assets/image-20240105215323197.png)

报错！！！！！！！！！！



换了ssh才成功，不懂

![image-20240105230922307](images/git.assets/image-20240105230922307.png)

拉去远程仓库到本地仓库成功，查看一下文件是否和远程仓库一样

![image-20240105231049358](images/git.assets/image-20240105231049358.png)

符合

添加本地库笔记push到远程库

![image-20240105232021354](images/git.assets/image-20240105232021354.png)

```shell
git add .
git commit -m "添加笔记"
git push git-demo master
```

![image-20240105232113737](images/git.assets/image-20240105232113737.png)

![image-20240105232130312](images/git.assets/image-20240105232130312.png)

在远程仓库中查看

![image-20240105232201828](images/git.assets/image-20240105232201828.png)



发现笔记中图片不i可看，发现是路径错误，将绝对路径改成相对路径

参考我的博客：[Typora如何管理图片地址-CSDN博客](https://blog.csdn.net/hnsqls/article/details/134694253?spm=1001.2014.3001.5501)

修改后重新push

![image-20240105232728928](images/git.assets/image-20240105232728928.png)

ssh更稳定一些

![image-20240105232928637](images/git.assets/image-20240105232928637.png)



修改为相对路径后github上的笔记图片也不可以看

![image-20240105234021379](images/git.assets/image-20240105234021379.png)

我直接在github上的编辑markdown笔记发现路径是相对路径

![image-20240105234125920](images/git.assets/image-20240105234125920.png)

![image-20240105234203712](images/git.assets/image-20240105234203712.png)

不明白为什么显示不出来（坑）





## CLone远程仓库到本地库

* 需要注意的是Clone、是完完全全将远程库的信息完全copy到本地库上
* pull 是拉去不同的代码进行整合

> 命令

```shell
git clone <项目地址>
```



实验 ： 在新的目录中拉去该项目

![image-20240105234554925](images/git.assets/image-20240105234554925.png)

![image-20240105234627510](images/git.assets/image-20240105234627510.png)



![image-20240106000715186](images/git.assets/image-20240106000715186.png)

查看本地库

![image-20240106000805724](images/git.assets/image-20240106000805724.png)

![image-20240106000821759](images/git.assets/image-20240106000821759.png)

很顺利

* CLone所作的事情1.拉去代码2.初始化本地仓库，3.创建别名

![image-20240106001628470](images/git.assets/image-20240106001628470.png)



## 团队内协作邀请成员到项目中

![image-20240106002346866](images/git.assets/image-20240106002346866.png)

![image-20240106002445358](images/git.assets/image-20240106002445358.png)

![image-20240106002502428](images/git.assets/image-20240106002502428.png)

![image-20240106002602909](images/git.assets/image-20240106002602909.png)

![image-20240106002636480](images/git.assets/image-20240106002636480.png)

复制发给邀请的人，别人点击pending invite邀请连接同意就可以加入到项目中了

## 跨团队协作

fork -pullrequest

# 17 IDEA——GIT

## 配置git.ignore 文件

![image-20240106004533712](images/git.assets/image-20240106004533712.png)



在C:user/实际用户下，创建git.ignore文件

我的电脑是![image-20240106004843004](images/git.assets/image-20240106004843004.png)

新建

![image-20240106005027949](images/git.assets/image-20240106005027949.png)

记事本打开编写一下内容

![image-20240106005428553](images/git.assets/image-20240106005428553.png)

```shell
## .gitignore for Grails 1.2 and 1.3

# .gitignore for maven 
target/
*.releaseBackup

# web application files
#/web-app/WEB-INF

# IDE support files
/.classpath
/.launch
/.project
/.settings
/*.launch
/*.tmproj
/ivy*
/eclipse

# default HSQL database files for production mode
/prodDb.*

# general HSQL database files
*Db.properties
*Db.script

# logs
/stacktrace.log
/test/reports
/logs
*.log
*.log.*

# project release file
/*.war

# plugin release file
/*.zip
/*.zip.sha1
 
# older plugin install locations
/plugins
/web-app/plugins
/web-app/WEB-INF/classes
 
# "temporary" build files
target/
out/
build/
 
# other
*.iws
 
#.gitignore for java
*.class
 
# Package Files #
*.jar
*.war
*.ear
 
## .gitignore for eclipse
 
*.pydevproject
.project
.metadata
bin/**
tmp/**
tmp/**/*
*.tmp
*.bak
*.swp
*~.nib
local.properties
.classpath
.settings/
.loadpath
 
# External tool builders
.externalToolBuilders/
 
# Locally stored "Eclipse launch configurations"
*.launch
 
# CDT-specific
.cproject
 
# PDT-specific
.buildpath
 
## .gitignore for intellij
 
*.iml
*.ipr
*.iws
.idea/
 
## .gitignore for linux
.*
!.gitignore
!.gitattributes
!.editorconfig
!.eslintrc
!.travis.yml
*~
 
## .gitignore for windows
 
# Windows image file caches
Thumbs.db
ehthumbs.db
 
# Folder config file
Desktop.ini
 
# Recycle Bin used on file shares
$RECYCLE.BIN/
 
## .gitignore for mac os x
 
.DS_Store
.AppleDouble
.LSOverride
Icon
 
 
# Thumbnails
._*
 
# Files that might appear on external disk
.Spotlight-V100
.Trashes

## hack for graddle wrapper
!wrapper/*.jar
!**/wrapper/*.jar
```

完事之后在.gitconfig文件（忽略文件同级目录下）引用忽略配置文件

格式为

```shell
[core]
    xecludesfile =  C:/Users/xxx/git.ignore    
```

* 需要注意的是，在引用全局配置中引用git.ignore文件 路径的斜杠（/）

![image-20240106005919852](images/git.assets/image-20240106005919852.png)

## Idea

创建maven项目测试

![image-20240106124227815](images/git.assets/image-20240106124227815.png)

![image-20240106124408745](images/git.assets/image-20240106124408745.png)

![image-20240106124438800](images/git.assets/image-20240106124438800.png)

新版的idea会自动识别电脑上的git，不能自动识别的话手动添加一个到git.exe文件下，点击test会提示git版本信息



初始化本地仓库，也就是让该项目由git管理

此时查看文件没有.git文件，可以看出项目并没有被git所管理，当然可以在该位置git bash ```git init``不在赘述

![image-20240106124901977](images/git.assets/image-20240106124901977.png)

在idea中点击VSC---->

![image-20240106125133371](images/git.assets/image-20240106125133371.png)

![image-20240106125154652](images/git.assets/image-20240106125154652.png)

默认就在该项目下创建本地库

![image-20240106125238789](images/git.assets/image-20240106125238789.png)

![image-20240106125255908](images/git.assets/image-20240106125255908.png)

说明该项目已经被git管理

添加到缓存区 git add.

![image-20240106125453801](images/git.assets/image-20240106125453801.png)

文件颜色变绿色 说明加入到了暂存区

![image-20240106125535635](images/git.assets/image-20240106125535635.png)



添加到本地库

写点东西提交报本地库

![image-20240106125942414](images/git.assets/image-20240106125942414.png)

![image-20240106130102790](images/git.assets/image-20240106130102790.png)

先git add. 在git commit

![image-20240106130242377](images/git.assets/image-20240106130242377.png) 

![image-20240106130620470](images/git.assets/image-20240106130620470.png)

![image-20240106130707679](images/git.assets/image-20240106130707679.png)

颜色变成看正常的颜色



> 切换版本

多提交几次先

![image-20240106130830438](images/git.assets/image-20240106130830438.png)

![image-20240106131400608](images/git.assets/image-20240106131400608.png)

当由多个文件改变的时候，可以从整个项目中添加到暂存区

![image-20240106130920183](images/git.assets/image-20240106130920183.png)

![image-20240106131640323](images/git.assets/image-20240106131640323.png)

查看版本信息点击VersionContral ----->log

![image-20240106132013810](images/git.assets/image-20240106132013810.png)

![image-20240106132342607](images/git.assets/image-20240106132342607.png)

切换版本 

在想要选择的版本单机右键选择checkout revision ”xxxx“

![image-20240106132456712](images/git.assets/image-20240106132456712.png)

![image-20240106132600312](images/git.assets/image-20240106132600312.png)

切换成功，代码也回到之前的代码了

切换回去 同上

![image-20240106132724529](images/git.assets/image-20240106132724529.png)



> 分支

![image-20240106135817575](images/git.assets/image-20240106135817575.png)

![image-20240106135903239](images/git.assets/image-20240106135903239.png)

![image-20240106135921357](images/git.assets/image-20240106135921357.png)

创建分支会复制master分支内容

> 合并分支

* 没有冲突的情况下，也就是master内容不改变，只修改分支内容没然后合并

修改分支内容

![image-20240106140417960](images/git.assets/image-20240106140417960.png)

不要忘记提交

合并需要先切换到主分支上 

```shell
git checkout master 
git merge hot-fix
```

idea 操作

![image-20240106141020819](images/git.assets/image-20240106141020819.png)

合并成功

![image-20240106141107366](images/git.assets/image-20240106141107366.png)



**合并冲突**

分支在master基础上修改的同时， master也修改

![image-20240106141625432](images/git.assets/image-20240106141625432.png)

commit master

![image-20240106141841109](images/git.assets/image-20240106141841109.png)

commit hot-fix

合并

![image-20240106142058663](images/git.assets/image-20240106142058663.png)

？？？ 怎么没冲突



![image-20240106142639614](images/git.assets/image-20240106142639614.png)

需要手动合并

显示出都修改的地方

![image-20240106142813880](images/git.assets/image-20240106142813880.png)

![image-20240106142946008](images/git.assets/image-20240106142946008.png)

> idea中绑定github账号

![image-20240106143804460](images/git.assets/image-20240106143804460.png)

有浏览器github授权还有token授权选择其一

![image-20240106143849290](images/git.assets/image-20240106143849290.png)



> 使用idea分享代码到github

正常情况是在github上创建新项目，在本地初始化git项目，写项目，push 到github上

使用idea如何操作呢

VSC->github->share