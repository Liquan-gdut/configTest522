# configTest522
>测试文件：关联本地git仓库与远程git仓库

步骤：
-------
##新建与连接
1、新建远程git仓库（repository）；
2、新建本地git仓库，右键点击“git Bash here”，在客户端中初始化，命令：git init，此时生成本地.git文件
3、本地git客户端进行远程连接，命令：git remote add origin git@github.com:Liquan-gdut/repo-name.git
(连接完毕！)

##下载“远程git仓库文件”到“本地文件”
命令：git pull git@github.com:Liquan-gdut/respon-name.git(或者filename)

##推送同步“本地文件”到“远程git仓库”
1.方法一：先添加待同步的文件，可加上“commit”，方便提示每次更新了哪部分内容，然后再push到远程库当中
命令：
```$git add filename
$git commit -m "备注内容"

$git push git@github.com:Liquan-gdut/respon-name.git```

2.方法二：直接推送+关联，后续直接更新即可
命令：
```$git push -u origin master   //意思：推送本地的文件到远程git仓库，并关联(-u)
$git push origin master     //后续有更新，直接采用该命令即可。```
