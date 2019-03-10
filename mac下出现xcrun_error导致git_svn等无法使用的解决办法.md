# mac下出现xcrun: error导致git、svn等无法使用的解决办法

> 2018年10月24日 10:39:06 [筱光](https://me.csdn.net/womeng2009) 阅读数：334
>
>  版权声明：本文为博主原创文章，未经博主允许不得转载。 
>
> https://blog.csdn.net/womeng2009/article/details/83339962

今天升级了MacOS Mojave，漏洞应该还是蛮多的，网上反映也不好，界面过黑，UI感觉有些突兀，但是还能接受。正常进入idea开始工作，然后……然后……svn不能用了，终端查看svn，报错。

```
xxxdeMacBook-Pro:~ xxx$ svn --version

xcrun: error: invalid active developer path (/Library/Developer/CommandLineTools), missing xcrun at: /Library/Developer/CommandLineTools/usr/bin/xcrun
```

idea:

![img](https://images2018.cnblogs.com/blog/830693/201711/830693-20171127111121284-2064639033.png)

## 解决办法：

在终端输入‘xcode-select --install’，会安装xcrun

```
xxxdeMacBook-Pro:~ xxx$ xcode-select --install

xcode-select: note: install requested for command line developer tools
```

![img](https://img-blog.csdn.net/20181024103636965?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dvbWVuZzIwMDk=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

## 然后svn就正常了：

在终端输入‘svn --version’，查看SVN安装版本信息

```
xxxMacBook-Pro:~ xxx$ svn --version

svn, version 1.10.0 (r1827917)

   compiled Aug 14 2018, 02:37:13 on x86_64-apple-darwin17.0.0

Copyright (C) 2018 The Apache Software Foundation.

This software consists of contributions made by many people;

see the NOTICE file for more information.

Subversion is open source software, see http://subversion.apache.org/

The following repository access (RA) modules are available:

* ra_svn : Module for accessing a repository using the svn network protocol.

  - with Cyrus SASL authentication

  - handles 'svn' scheme

* ra_local : Module for accessing a repository on local disk.

  - handles 'file' scheme

* ra_serf : Module for accessing a repository via WebDAV protocol using serf.

  - using serf 1.3.9 (compiled with 1.3.9)

  - handles 'http' scheme

  - handles 'https' scheme

The following authentication credential caches are available:

* Plaintext cache in /Users/chenjunliang/.subversion

* GPG-Agent

* Mac OS X Keychain
```

