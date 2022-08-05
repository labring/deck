# sealos 是什么

sealos 是以 kubernetes 为内核的云操作系统发行版，让云原生简单普及。

![image](https://user-images.githubusercontent.com/8912557/172759650-1c2529a2-f5f1-4b1a-ab4c-e9873ab74b60.png)

sealos 是用来管理数据中心所有机器的云操作系统，kubernetes 就是这个操作系统的内核，sealos上 面会跑各种各样的分布式应用。

* 早期单机操作系统也是分层架构，后面才演化成今天的宏内核微内核架构，云操作系统也一定会有类似发展趋势
* 以前都是单机应用，而现代应用几乎都是分布式应用，kubernetes 已经成为事实上的“云操作系统内核”，能让内核普及的发型版呼之欲出
* sealos 抛弃了 IaaS, 基于云内核的高内聚设计，决定了 sealos 可以让云更简单，更便宜，从而像 linux 发行版一样普及

> 产品概览 （简单 干净 极致）

![dashboard](https://user-images.githubusercontent.com/8912557/181175228-ce599b53-340a-4eb2-9a66-0563267a8d2c.png)

![terminal](https://user-images.githubusercontent.com/8912557/181174718-12aa119e-880e-41d0-b4ba-b60d0c7283b8.png)

# 行业背景

- 基于开源技术的云服务在侵蚀厂商绑定且封闭的公有云的服务
- 云原生侵蚀传统 IaaS 服务，基于 kubernetes 的云原生技术每年几十倍增长，大量企业切换至云原生架构
- kubernetes 在与 mesos swarm 等技术的竞争中胜出，成为云原生领域事实标准，基于 kuberentes 的发行版呼之欲出
- 云原生的落地门槛较高，无法进入大众市场，sealos 能降低云原生落地门槛

# 解决的问题

<img width="1075" alt="image" src="https://user-images.githubusercontent.com/8912557/173273292-8209d5cd-837d-46a5-8a64-380a350767df.png">

**现有云厂商价格昂贵体系封闭，企业上云强绑定，私有云以及各云厂商之间无法自由切换**

<img width="1281" alt="image" src="https://user-images.githubusercontent.com/8912557/172760276-5652a6d2-5d5d-4633-b017-d892460a6dfc.png">

<img width="689" alt="image" src="https://user-images.githubusercontent.com/8912557/171235734-589d1769-2fc2-4c35-8d44-4c98f3e3f006.png">

> 目前公有云昂贵的根本原因

* 软件成本高，还是基于传统分层架构去设计，导致每一层成本都很高，如分布式存储 IaaS，而内核架构可以绕开这些甚至达到更好的效果
* 机房备货必须要有预留资源，这部分成本会加到用户身上
* 如果是传统架构，目前的公有云自然会更便宜，因为类似 openstack 这类软件成本高。 而 sealos 是一个变量，让软件成本降下来，裸机 + sealos 成本自然低了很多

# 解决方案

<img width="1134" alt="image" src="https://user-images.githubusercontent.com/8912557/173273555-25d581fc-6777-4f39-940c-6cbc1ce30a03.png">

> 提供一个开源开放的云操作系统，利用云原生的能力做一个目前云厂商的可替代品

- 开源 sealos，提供出一个抽象的云操作系统，一切皆应用的设计理念。
- sealos cloud - 环界自己运行的 sealos 公有云版本，服务能力对标 aws 阿里云等公有云
- 用户自由下载社区版或商业版本 sealos，在任意地方启动一个属于自己的 sealos cloud

> 分布式应用生态构建

- 广度，常用分布式软件如 mysql 集群，redis 集群，消息队列等逐步覆盖，不断扩展常用分布式应用数量
- 深度，基本安装->高可用->可监控->自运维->高性能/安全性->GUI管控，六个阶段衡量一个分布式应用成熟度

应用包含三个来源：环界自研应用如函数计算，开源二次封装应用，第三方应用如与讯飞合作的 AI 能力应用与 sealos 结合

# 现状

> sealos Star History

[![Star History Chart](https://api.star-history.com/svg?repos=labring/sealos&type=Date)](https://star-history.com/#labring/sealos&Date)

> laf star history

[![Star History Chart](https://api.star-history.com/svg?repos=labring/laf&type=Date)](https://star-history.com/#labring/laf&Date)

社区现状：
- sealos 是目前全球最受欢迎的 kubernetes 发行版之一，社区用户包含 阿里/华为/讯飞/海康 等头部企业
- sealos 内置函数计算应用拥有, 保持月 100% 的高速增长

市场现状：
- sealos 函数计算 laf 当前 1100 注册用户 900 在线应用，sealos 累计付费订阅用户 4k
- sealos 推动商业化 1 个多月时间已经落地一家企业客户，合同额 45w
- sealos 公有云用户保持每个月 50% 以上速度增长

# 市场&路径

> 市场

<img width="2732" alt="image" src="https://user-images.githubusercontent.com/8912557/181909271-f9f4101a-a743-456b-97dd-3dfc5f57e7e0.png">

> 云计算 1.0 2.0 3.0

* 试想 web1 web2 web3 的区别是什么? 关联到云计算上其实一样，现在是计算厂商生产服务开发者来使用，模型处于 1.0 时代。生产关系 1 <-> n。
* 云计算 2.0 开发者上产服务和软件，软件消费者消费，生产关系变成 n <-> n 的网状关系。
* 云计算 3.0 所有计算资源连接在一起，构建成了一台超级计算机，所有的算力属于全网的参与者。

> 转化漏斗

- 开源：两年时间把 sealos 与 laf 打造成国际顶尖开源项目，创造一个大的转化漏斗开口
- 公有云：但凡要使用 sealos 的用户一定会去找应用，就一定会到我们的仓库中去找，拿到应用一定是想启动应用，在 sealos cloud 上启动就是一个按键，这是最快捷最便宜产品体验最佳的方式，是个极其顺其自然的转化过程。
- 订阅：用户拿到应用另外一种启动方式就是在自己的服务器上启动，此时付费订阅下载即可
- 在这些客户中沉淀一批 大B 客户，买 sealos 的产品与服务。

# 目标客户

- sealos 开源社区用户，4k(用户量) * 2598￥（3台4C8G）= 10,392,000 营收/月 毛利 30% = 3,117,600 ￥/月，以现有 sealos 的付费订阅用户体量计算，平均每个用户起一个最小高可用集群，可以达到千万级别月营收，月毛利在 300w左右
- 使用 sealos 的 B 端客户，习惯 sealos 的简单易用，这类客户大部分是社区用户把 sealos 带到企业中，集群体量会比开发者大很多，一个大 B 就可以一年带来 40w 以上的毛利
- 想在自己机房构建私有云的 B 端客户，客单价在 40w ~ 100w 之间，他们要在自己的机房中拥有公有云的能力。

特别强调：在 sealos 的设计理念中，公有云与私有云没有本质区别，完全是一个东西，大部分企业私有云的能力都是多租户包含计量计费等能力，而 sealos 的特殊地方就在于高度抽象，公有云与私有云只是 sealos 的配置和上面安装的应用不同而已，没有其它任何区别。所以不用担心小团队既做公有云又做私有云不聚焦的问题，我们非常聚焦只做一个东西就是 sealos.

# 团队介绍

<img width="1362" alt="image" src="https://user-images.githubusercontent.com/8912557/172760851-3f9bb574-9076-41b8-9bca-d35ec4337bd9.png">

- 方海涛(阿里云) sealos 作者，CNCF sealer 项目发起人，集群镜像概念提出者。
- 王福根 laf 作者，基于 kubernetes minio 等基础服务自主研发函数计算平台，实现 SaaS 开发完全在线化。
- 栾绍童(前阿里云) - 星际争霸AI算法大赛世界第二，华为软件精英赛亚军，因编程出色本科保送科大，天池调度算法大赛冠军等。
- 曾镇(前字节跳动) - 半次元技术合伙人，半次元后被头条收购，从字节离职后创业做阅读器月流水几十万，后被整改关停。
- ***(兼职，腾讯) - 负责全国三大区市场，担任市场负责人。
- 杨**(兼职，前IBM) - 某知名云原生公众号博主，运营负责人，曾帮助某开源项目完成1k到10k star 的增长。

# roadmap

- 2022.9 
  - 完成 sealos cloud 公有云上线，可在线启动 sealos，100 客户端 30 个启动集群
  - 社区海外布局，主要包含英文文档，海外社区运营，海外开发者吸引
- 2023.3
  - 2k 注册用户，500 在线启动集群
  - 40 款常用分布式软件实现高可用，可监控，自运维和安全加固
  - sealos 公有云服务面向海外开放
- 2023.12
  - B轮融资，自建公有云，降低资源成本
  - 构建海外本土化市场/销售与服务团队

# 增长指标

目标设定 12 个月：公共云高速增长

业务增长：
-  为 2w 开发者提供在线服务
-  每月公有云用户 50% 增长
-  公有云月毛利达到 300w, 月营收达到 1000w ￥

社区增长：
-  sealos 达到 16k star 2.5k fork, 100 名贡献者 10 名社区活跃 maintainer
-  laf 达到 10k star 1k fork，50 名贡献者，5 名社区活跃 maintainer

团队扩张：11~20名精英，包括市场/运营，垂直领域专家，各种编程比赛成绩优异同学或有自己亮眼作品的人才

业务规划： 

sealos cloud，打法简单，做好开源，做好云服务，投入运营资源（预计亏损 200w 到 500w）

* 最基础的内核镜像完全向开发者免费。在线化启动 sealos，让用户以最方便的方式启动在线集群，而且可以比公有云成本降低 10%~20% (代理商返利一部分给用户)
*  sealos 中的高可用存储/数据库/消息队列等应用付费提供
*  制作企业级发型版服务订阅费用 6900~69000 之间，根据企业组装的组件不同价格不同
*  公有云导流企业级服务，针对大B,客单价 40万 到 100w 之间，渠道商推广以及其他推广方式

# 竞争对手

- [bitnami](https://bitnami.com/)  被 vmware 收购，做应用市场，与 sealos 部分重叠
- [helm](https://developer.aliyun.com/article/156936?spm=5176.24320532.content1.5.78ea1cb92aB4sW) 也是做应用管理的，有一点重合但是差异也明显，见 [sealos 与 helm 区别](https://github.com/labring/sealos/discussions/1078)
- AWS 终极但不可怕的竞争对手是这些很重且封闭的公有云厂商，sealos 尝试建立一个基于开源的开放/简单的云操作系统替代今天公有云厂商提供的能力。
- Vercel 基于静态托管为入口，逐渐切入 serverless，对于 laf 来说是强大可怕的竞争对手。
- rancher kubesphere 等，这类产品并非 sealos 竞争对手，定位不同，他们把 k8s 当成目的，而 sealos 中 k8s 是手段，利用云内核的能力给客户真正想要的服务和能力才是 sealos 要做的事， sealos 定位的是大众市场。
- 头部公有云公司，他们最核心的 KPI 是公有云 vCPU 的增长，这意味着不可能在用户方便迁云上做多少投入，他们更反对和妖魔化更便宜的私有云，很重的体系也没有办法在别的地方运行，成本极高。

# 其它链接
[blog - 以 kuberentes 为内核的云操作系统发行版](https://www.sealos.io/blog/kubernetes%20with%20sealos)
