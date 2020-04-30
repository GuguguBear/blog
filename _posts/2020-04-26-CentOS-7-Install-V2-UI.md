---
layout: default
title: "CentOS 7 Install V2-UI"
tags: Linux
---

![QQ图片20200420131137.jpg](JekyII_Blog/Wannk%E6%89%91%E5%85%8B%E7%B3%BB%E5%88%97/QQ%E5%9B%BE%E7%89%8720200420131137.jpg)

[V2Ray](https://www.v2ray.com/)算是基于SS&SSR之上进行再次升级的一款翻墙软件，它默认已经提供了非常安全的配置选项给大家。

一些加密的选择也让大家在敏感时期稳如泰山的可以上纲上线继续翻墙愉快玩耍。

但是由于V2Ray本身的稳定性，安全性，连接性各方面的优越，它的缺点则是难配置。

并且官方原生的V2Ray仅支持单用户进行设置，无法给予多用户，以及单端口多用户玩法，这让许多希望自己开设伺服器给朋友翻墙的小伙伴望而却步。

实际上不需要这么诙谐，已经有成熟并且开源干净的面板给予我们使用了。

今天就来姑且讲解一下在CentOS上搭建V2Ray-UI面板的一些记录笔记，防止日后重新部署时候踩坑。

SSH连接至CentOS之后首先执行系统更行命令：

```
yum update -y
```

更新完毕以后开始部署v2Ray-UI面板：

```
bash <(curl -Ls https://blog.sprov.xyz/v2-ui.sh)
```

如果一切顺利，到了这一步，你应该已经可以输入v2-ui来打开设置列表了。

如果不顺利，别着急，我们接下来看看，手动安装的步骤。

倒霉的孩子，继续折腾一下吧。

[V2Ray-UI GitHub](https://github.com/sprov065/v2-ui/releases/tag/5.1.2)

首先进入上面地址，下载好最新的版本到你的VPS里的root目录下。

使用以下命令进行本地安装v2ray，如果你将v2ray-linux-64.zip文件上传至了其它目录，那么需要将命令中的/root/v2ray-linux-64.zip替换为你实际的文件路径。

```
bash <(curl -L -s https://install.direct/go.sh) --local /root/v2ray-linux-64.zip
```

至此你的V2Ray本体应该安装完毕了，可以去Happy了！

如果之后还有一些其它可能出现的错误，我这边会再更新一下文章。
