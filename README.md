# configTest522
> 测试文件：关联本地git仓库与远程git仓库

## 步骤：
-------
#### 新建与连接

1、新建远程git仓库（repository）；<br>
2、新建本地git仓库，右键点击 “git Bash here”<br>
3、在客户端中初始化，命令：git init   //此时生成本地.git文件<br>


#### 下载“远程git仓库文件”到“本地文件”(注：如果远程git库有文件，则必须有这一步，空的仓库则不需这一步)

命令：git pull origin master

#### 推送同步“本地文件”到“远程git仓库”（注：同步前必须先add、commit）

1.方法一：先添加待同步的文件，可加上“commit”，方便提示每次更新了哪部分内容，然后再push到远程库当中<br>
命令：<br>
$git add filename
$git commit -m "备注内容"
$git remote add origin git@github.com:Liquan-gdut/repo-name.git   //本地git客户端进行远程连接
$git push origin master“（注：首次push则需加上要“-u”，以后则不用）


## git常见错误集锦

1、如果输入$ git push origin master

提示出错信息：error:failed to push som refs to...

解决办法如下：

（1）、先输入$ git pull origin master //先把远程服务器github上面的文件拉下来

（2）、再输入$ git push origin master

（3）、如果出现报错 fatal: Couldn't find remote ref master或者fatal:'origin' does not appear to be a git repository以及fatal:Could not read from remote repository.

（4）、则需要重新输入$ git remote add origingit@github.com:djqiang/gitdemo.git


2、如果输入$ git push origin master

error: failed to push some refs to 'git@git.oschina.net:summving/XXXXXXXXX.git' 
hint: Updates were rejected because the remote contains work that you do 
hint: not have locally. This is usually caused by another repository pushing 
hint: to the same ref. You may want to first merge the remote changes (e.g., 
hint: 'git pull') before pushing again. 
hint: See the 'Note about fast-forwards' in 'git push --help' for details. 

解释的已经很清楚了。因为远程仓库比本地库更新，所以得先 pull 下，再 push 就 ok 了。

没有设定远程跟踪分支的话 要使用这个命令 git pull origin master 

3、如果输入$ git remote add origin git@github.com:djqiang（github帐号名）/gitdemo（项目名）.git 

提示出错信息：fatal: remote origin already exists.

解决办法如下：

（1）、先输入$ git remote rm origin，解除当前已有连接

（2）、再输入$ git remote add origin git@github.com:djqiang/gitdemo.git 就不会报错了！<br>
 
4、如果输入$ git push origin master 出现：error:src refspec master does not match any<br>
    表示在push过程中，没发现缓存中有准备上传的文件，就是你没有“add”啦<br>
    解决：add、commit
    
 
