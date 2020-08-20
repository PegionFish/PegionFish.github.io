---
layout: post
author: Bob Guo
title: 如何定义产品力
subtitle: 笔记本评测之我见
date: 2020-8-15
tags: 业界分析
published: true #write true to publish this article.
---
## 什么是产品力？  
对于消费电子产品爱好者来说，这个名词犹如“萌え”对于御宅族一样-所有人都知道它指代什么，但所有人都无法为此给出完全精确的定义。由于市场细分的不断进步，现如今“产品力”三个字所指代的内容已然是一系列难以定义的评判维度。由于不同产品指向的用户群体与用户需求截然不同，其在设计中的思路与限制也大相径庭；而上游供应链的技术限制也使得OEM与ODM不得不对设计进行二次修改与妥协。而这些妥协的结果，就是整个业界无法给出一个通用且有说服力的针对“产品力”一词的标准。笔者作为消费电子产业的爱好者，希望借此拙作对消费电子业界中的”产品力“这一概念进行简单的分析。  
## 以戴尔Latitude E7470为例
这台笔记本电脑是戴尔经典商务本，搭载Skylake架构处理器、双通道DDR4内存、NVMe固态硬盘；屏幕最高可选2560x1440p的触摸屏，而接口方面也十分扎实。虽然由于各种原因它并不支持USB Type-C或PD供电，但三个USB、miniDP、HDMI、千兆网卡、SD卡、耳机口和E-port也能保证正常使用不会出现接口瓶颈。  
我们现在来分析一下这台笔记本的特征：
* IO齐全，虽然不支持更先进的USB Type C技术但仍然无法评价为”不够“。尤其是E-Port的存在允许更新新设备的企业可以继续使用以前的拓展坞以节省成本。个人来讲，我更偏向戴尔的设计而非联想那种外形根据机型固定的设计：这种设计可以有效降低IT维护的成本，且作为终端用户在几年后购买二手也可以更加方便。也可以更加方便也可以更加方便
* 商务取向。黑银配色的外观简洁干练，给人的第一印象就是默默干活的专业工具而非那些张扬的玩具、指点杆、指纹识别和NFC功能也都可以选配。对于重视信息资产的企业来说，这种功能也是必要选项。虽然最高可选2K触摸屏但也仍然有传统的768p 45NTSC TN可选。
* 性能够用。商务本不像游戏本一样追求无限高的性能。对于商务本的用户来说，真正重要的是get the job done而不是how fast your pc run。六代酷睿低压U、双通道DDR4和固态硬盘的搭配十分灵活，在保证可以干活的前提下可以继续削减配置，这也是IT部门十分看重的。

所以其实我们可以看出，这台电脑完完全全是为了商务而设计的机型，其所有的设计思路与取舍都建立在商务产品的需求上。这些客户需要高度安全、设计简洁的机器，但性能不需要太强，够用就行。这台电脑由于身处戴尔14寸商务本的巅峰，自然完全以商务需求为重设计，完全不考虑商务用户以外的需求。而这样的需求造就的结果就是如图所示的
![alt text](/img/e7470/power_comsumption_while_coding.png)
在单纯进行商务用户会涉及的操作比如写稿子这些的时候它的功耗会很低，风扇也几乎不转，加上14nm工艺和Skylake架构的高性能保证了即使在这种情况下也能流畅运作并得到足够的续航。针对一台商务本来说这样的设计完全没有任何问题，甚至可以说是精妙。  
但是，如果在执行高负载任务（比如编译Linux内核）时，如果不接入AC电源，功耗会被锁死在15w，此时频率仅为2.8Ghz。不能说不够用，但是对于我这样一个性能取向型用户来说明显不够。
![alt text](/img/e7470/power_comsumption_while_compiling.png)
如果插上AC电源，再次进行编译，测试结果也是只有15w的TDP。
![alt text](/img/e7470/power_comsumption_while_compiling_w_ac.png)
如果按照评判一般轻薄本的标准，这种性能释放水平显然仅仅是勉强合格。在它刚发售的2016年如此，在现在2020年更甚。我们看到小新Pro 13把35w的TDP普及到5000以下价位，如果你是一个普通的用户，这种性能释放相交于传统笔记本可谓降维打击。  
但是，toB不一样。他们的使用场景不仅仅是宿舍，而是从飞机到高铁，从星巴克到会议室。35w的性能释放确实强劲，但对于他们来说纯粹是方向错了。他们需要的是安静、长续航，这个时候仅仅15w的性能释放就能做到这一点。  
## 为什么？
我为什么要用一台商务本来引入这个话题呢？我个人认为，现在笔记本社群里存在一个极其不好的风气-只要CPU性能不强的本子就是电子垃圾。这种思潮显然是不合适的。诚然，包括我在内的许多用户需要的就是rawr performance，而且我也不介意公开表达这一点。但是，“性能”并非笔记本电脑的唯一维度。笔记本电脑是一个妥协的产物，即使一切都为性能服务也需要将“移动性”纳入考量。典型的例子就是曾经的一代机皇-蓝天P570WM，X79芯片组。这台机器的性能即使是在今天也堪称梦幻，但由于笔记本的尺寸限制，它像某些寨板一样无法使用2011平台的顶级处理器-供电吃不消。更平民一点的P7xx/8xx系列也饱受同样的困扰-即使采用了支持超频的Z系列芯片组，想要像普通台式机一样超频也是一个不大可能的任务；而最近的NH55更是直接将CPU功耗限制在65w-即使是有TSMC 7nm工艺加持，AMD Ryzen 3000处理器的高性能带来的高功耗也是笔记本电脑难以招架的。而且，笔记本电脑的用户囊括五湖四海，不是每个人都追求性能。对于有的用户来说，优质的屏幕远强于35w的CPU（虽然现在完全可以我全都要）；对于有的用户来说，20小时的续航比什么都重要。而且，这些并不是完全的矛盾体。我的习惯是同时拥有多部机器，不仅可以互相备用，也可以通过高低搭配的方式满足不同的需要。  
## 所以，当我们提到产品力的时候，我们到底在说什么？
我个人认为，对产品力的评价需要综合多个因素才能完成，这其中就包括产品的定位和受众，而且我个人认为这两者应该占据上风。由于我在前文中提到笔记本电脑的设计核心思路就是妥协，而“定位和受众”就代表了妥协的最终成果，所以任何对其的评价都应该基于这两者来考虑。续航、性能、接口、尺寸、屏幕等参数是否优良的标准应当浮动决定，例如，对于Surface Pro这种设备，能把一颗低压U压到默认的TDP就已经足够献上掌声和鲜花;而一台自诩高性能的笔记本做到这种成绩就只能得到无数的嘘声。7470的性能释放不如自家灵越15 7559游戏本，但这并不代表这台机器就不如那台同样称得上优秀的游戏本。不同的用户有不同的需求，而性能的倍增在越过某个阈值后其实对很多人来说是真的感知不强了：我现在还在用E3V2和V3,但我同样也能正常地听课看片打游戏甚至写写代码剪点视频都没有任何问题。如果对于我都是如此，那么对于那些需求真的只是上上网看看片的用户来说，15w和35w之间，又能有什么区别呢？