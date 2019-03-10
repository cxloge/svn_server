# Mac搭建本地svn服务器，并用Cornerstone连接服务器

> https://www.cnblogs.com/czq1989/p/4913692.html



Mac默认已经安装了svn，我们只需要进行配置并开启就可以了

首先我们可以验证一下是否安装了svn，打开终端，输入命令

svnserve --version

![img](https://images2015.cnblogs.com/blog/800567/201510/800567-20151027102426435-835359663.png)

这里可以看到目前svn的版本号，说明已经安装好了svn

下面正式开始配置svn

## 1.创建代码库

我们来创建一个代码库用于保存代码

在终端输入命令

sudo mkdir -p /Users/apple(根据自己的用户名修改)/svn/mycode    //创建了一个文件夹，这个文件夹路径可以自己随意设定

sudo svnadmin create /Users/apple(根据自己的用户名修改)/svn/mycode   //将之前创建的文件夹设置为svn的代码库

我们在Finder中打开上面的路径，我们可以开到其中生成了一些文件，我们需要配置conf文件夹下的文件

![img](https://images2015.cnblogs.com/blog/800567/201510/800567-20151027103337982-1000508898.png)

## 2.配置svn用户权限

### 1）配置svnserve.conf文件

![img](https://images2015.cnblogs.com/blog/800567/201510/800567-20151027103823763-622300343.png)

用编辑器打开文件

![img](https://images2015.cnblogs.com/blog/800567/201510/800567-20151027104052247-724978499.png)

修改以上位置，其中anon-access = read代表匿名访问的时候是只读的，若改为anon-access = none代表禁止匿名访问，需要帐号密码才能访问

### 2）配置passwd文件

![img](https://images2015.cnblogs.com/blog/800567/201510/800567-20151027104414247-11392025.png)

在文件中添加以上内容，需要将内容添加在[users]下面，以上内容标示创建了两个用户，用户aaa密码是111，用户bbb密码是222

### 3）配置authz文件

![img](https://images2015.cnblogs.com/blog/800567/201510/800567-20151027105239872-1928623086.png)

在[groups]下添加uesrs = aaa,bbb标示创建了一个用户组，此用户组包含有aaa和bbb两个用户

[/]

@users = rw 这两句标示给users用户组相应的权限

[/]表示授权的目录路径，这里是根目录，假如根目录下有一个目录叫做test,那么我们如果要编辑此目录的权限那么就要写成[test:/]

@uesr表示给用户组授权，如果要给某一个用户授权则不用写前面的@

r表示可读，w表示可写

## 3.启动svn服务器

在终端输入

svnserve -d -r /Users/apple/svn

注意不要输入svnserve -d -r /Users/apple/svn/mycode

没有错误返回就说明svn服务器开启成功了

我们也可以在活动监视器里进行检验

![img](https://images2015.cnblogs.com/blog/800567/201510/800567-20151027110652357-1167123809.png)

## 下面来配置Cornerstone

给个下载的链接http://down.xiazai2.net/?/121625/cr173/SVN%B9%DC%C0%ED%B9%A4%BE%DF.exe

SVN管理工具(Cornerstone Mac版) V2.7.10 破解版 已经破解 dmg文件无密码，也不需要注册机 直接使用即可

打开Cornerstone

点击+添加代码库

![img](https://images2015.cnblogs.com/blog/800567/201510/800567-20151027111459247-473842849.png)

 

选择svn server并填写红框中那些内容 

server :如果服务器在本地就写localhost 在局域网的其他电脑上就写他的ip地址

repository path:这里的地址用的是上面配置svn时的代码库路径，如果上面的路径跟我不同自己改一下

最下面两个是用户名和密码，最后save就好了,如果连接成功会显示success

![img](https://images2015.cnblogs.com/blog/800567/201510/800567-20151027111651310-2072232528.png)

![img](https://images2015.cnblogs.com/blog/800567/201510/800567-20151027112209419-1241353763.png)

至此，用mac配置本地svn服务器，并用Cornerstone连接svn服务器就做完了

 

参考:http://blog.sqstudio.com/otherskill/1048.html

　　http://m.blog.csdn.net/blog/kekey1210/16463289



分类: [版本控制](https://www.cnblogs.com/czq1989/category/748601.html)

标签: [svn](https://www.cnblogs.com/czq1989/tag/svn/), [Cornerstone](https://www.cnblogs.com/czq1989/tag/Cornerstone/)