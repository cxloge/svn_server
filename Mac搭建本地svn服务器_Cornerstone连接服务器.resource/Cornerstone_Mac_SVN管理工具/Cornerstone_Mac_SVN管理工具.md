Cornerstone_Mac_SVN管理工具

cornerstone303.zip
百度网盘下载链接：
https://pan.baidu.com/s/1DBt_q4aimhnEa6V_ZKf1ww

Cornerstone是Mac上最佳的SVN管理工具，CornerStone V2.7.10 破解版是Mac OS X系统下非常好用的一款svn工具，至XCode5之后，我的使用环境是Mac OS X 10.9, dmg文件来的，不用进行破解操作，直接拉到application的文件夹那里就行了。

本人觉得XCode5的Svn实在让人不得要领，而CornerStone配置虽不难，但也有几个需要注意的地方！客户端应用程序是专门为Mac用户设计的Subversion的控制，无论您是那个版本，或者一个Subversion的测试版，Cornerstone将有助于简化工作流程，使版本控制更加透明。

功能介绍

*结合了颠覆力量的Mac优雅。

*完美伴侣到Xcode，BBEdit，TextMate，Coda等

*使用Subversion，无需安装在10.4 Tiger了。

*所有功能于一身的UI模式优化，在笔记本电脑和其他小型显示器使用。

*多窗口界面模式在桌面系统使用大（甚至多重优化）显示器。

*还有更多更多。

添加repository
点击左侧栏中REPOSITORY那一栏的+选择添加repository

如果你公司的给你的repository地址为svn://开头，则选择SVN Server，如果为 Http://或https://开头 ，则选择HTTP Server

1.SVN配置

假设你公司svn地址为： svn://192.168.1.111/svn/ios ， 用户名：svnserver，密码：123456

1：填写主机地址

2：如果你的主机地址中有端口号，如为192.168.1.111:8080，则2中填写8080

3：填写主机后面的路径

4：自动生成，如果你填写完之后不是这种 svn://用户名@主机地址:端口号/路径的格式，则说明填写有误

5：也会自动生成，将会在侧边栏显示为5中的名称，可以自定义名称

6：用户名

7：密码

以上信息填写无误之后选择添加即可，如遇添加失败，信息填写无误，则联系管理员，查看地址，用户名，密码是否正确

2.HTTP配置

与svn一样，只有一个地方需要注意，如果地址是https://，则需修改下图所示位置的选项为HTTPS，否则也会添加失败

Mac 安装Cornerstone.app 已损坏，打不开。您应该将它移到废纸篓
软件安装过程比较简单，

问题：

安装后打开出现“Cornerstone.app 已损坏，打不开。您应该将它移到废纸篓。”

解决：

在安全性与隐私中打开任何来源就解决了。但是，在安全性与隐私中并没有打开任何来源这一选项。原来是10.12 后需要手动开启任何来源。开启方式如下：

打开终端

sudo spctl –master-disable

会出现 Password: 这个提示, 你这个时候要输入你的账户的密码, 如果没有密码需要到系统偏好设置 - 账户 - 设置密码. 不可以是空的密码.

然后你输入密码的的时候会发现光标不动 , 这是正常的, 实际上已经输入进入了, 输入完成后回车即可生效. 然后你重启电脑就会出现任何来源的选项了. (也不用重启电脑，重启设置即可)

如果不显示”任何来源”选项（macOS 10.12默认为不显示）在控制台中执行：

sudo spctl --master-enable

更新内容：
搁置 - 允许用户暂时“搁置”（预留）进程内更改并恢复到工作树 - 例如，快速修复生产中的错误。完成后，用户可以简单地检索他们搁置的更改并继续他们离开的地方。

检查点 - 允许用户在特定时间点创建其存储库的“快照”或副本。如果用户遇到了严重问题，他们可以将项目恢复到之前创建的任何检查点。它本质上是一个重大问题的撤销按钮。

Subversion 1.10 - Cornerstone现在支持所有版本的Subversion 1.7以上

使用SSH隧道设置环境变量 - 新的SendEnv字段允许用户使用form variable = value设置任何环境变量

与Assembla SVN + SSH集成 - Cornerstone现在通过SSH连接与Assembla SVN存储库兼容。

性能改进 - 众多代码优化可加快整体应用程序性能，尤其是在将代码从中央存储库更新到Cornerstone时。

收起详细介绍
下载地址
特别说明

已经破解，可以直接使用。
dmg文件无密码，也不需要注册机。直接使用即可

mac10.12需要开启允许任何来源
操作步骤： 
1打开终端，输入以下命令： sudo spctl --master-disable 
2 输入电脑的密码,再重新打开安全隐私 
3 就可以发现选中“任何来源” 不然会报数据包损坏