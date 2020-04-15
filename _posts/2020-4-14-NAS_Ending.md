---
layout: post
author: Bob Guo
title: 垃圾佬的家庭网络中心 （3）
subtitle: 其他硬件
date: 2020-4-14
tags: 网络 NAS
published: true
---
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;如果没有太大的变动，这篇文章就应该会是短期内我软路由的最终章了。由于我有计划使用这个平台作为专门的软路由主机和NAS主机，特地挑选了这个具有10个3.5寸硬盘位的机箱，H81M-K稀疏的SATA接口（2x2 2x3）显然无法承担重任，加上我还有一台屏幕损坏了的ThinkPad T430笔记本电脑，它也需要在更换屏幕之前得到妥善的利用。所以，现在的计划如下：
1. ThinkPad T430作为专用NAS主机，安装2个2TB笔记本硬盘并使用256G mSATA固态硬盘启动。安装基于Debian的Open Media Vault，也是我个人最喜欢的NAS OS，它负责通过Resilio Sync和BitTorrenet作为资源节点活跃在网络上。人人为我，我为人人，这是互联网精神（确信）
2. HP Elitebook 2570P作为日用主机，安装600GB S3500固态硬盘、16GB RAM和3630QM，运行Arch Linux操作系统，是我最主要和最核心的电子设备。它承载了我几乎所有的CPU算力需求，而即使出现问题三百元的售价也让抛弃这台设备完全不值得任何心疼。
3. H81M-K作为软路由主机，装载i340网卡、128GB固态硬盘，使用2TB机械盘作为从盘挂载。至于未来换成什么平台，我现在的打算是考虑一个功耗较低的桌面平台，用于对文件进行转码加密和上传到云上保存。由于经济上的问题，我现在没有办法通过磁盘阵列的方式保证数据安全，那就只能依靠加密过的压缩包来保证数据安全。毕竟，当Microsoft或Google停止服务，那个时候我可能也没心情来处理我的数据了。
4. Surface Pro就只要像Surface Pro那样工作就好。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;OMV的安装基本是无难度的。只要按照屏幕上的指示（不要问我哪里来的屏幕，VGA和miniDP都还活得好好的），一步一步确认完所有的东西，就可以很快完成整个安装流程。唯一需要注意的就是跟任何发行版一样在安装的时候确认软件包的repo是在那个mirror。尽量选择物理位置离你比较近的Mirror，例如我就更适合选择163（网易）或者ZJU（浙大）的mirror。当然，实际使用中只要物理位置在中国境内就没那么多问题，用就完事了。Debian有一个很离谱的设计就是你选择的软件源不是全面应用的，也就是说你仍然得从某几个服务器慢吞吞的爬文件。我个人觉得这样的设计是并不合理的，既然用户选择使用某一个mirror就应该完全使用那个mirror，但Debian团队可能有自己的想法。这里我也不过多judge别人。