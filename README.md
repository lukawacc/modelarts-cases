目录
=================

* [整体原则](#整体原则)
* [云上数据存储](#云上数据存储)
  * [OBS对象存储](#OBS对象存储)
* [Tests](#tests)
* [Dependency](#dependency)
    
# ModelArts自定义训练实战案例——操作指导

## 整体原则

- [ModelArts一站式AI开发平台](https://www.huaweicloud.com/product/ai-modelarts.html)是Cloud & AI的旗舰产品，是华为公司AI战略的重要组成部分，也是EI产品部每一个从AI算法开发的同学，必定会接触甚至深度使用的一款云服务。

- 本案例通过一个end-to-end的自定义训练作业的实践，示例了如何使用华为公司ModelArts平台进行云上训练，并最终将训练出来的模型发布成Cloud API。

- 本案例仅示例ModelArts平台的部分功能以及所以依赖的相关云服务，包含OBS对象存储服务、开发环境-Notebook、训练作业、模型管理-导入模型、部署上线-在线服务。

- ModelArts平台基本操作请参考ModelArts平台各类指导文档，请各位用户详细阅读，指导文档链接：https://support.huaweicloud.com/modelarts/index.html

- 本示例仅做简单流程示例，具体详细操作，请参考平台提供的各在线操作指导文档

## 云上数据存储

- 在云上进行算法开发，首先要了解的是数据在云上存储的事情。

- 通常我们都熟悉的是计算机系统中的硬盘/磁盘，eg, 300GB，500GB，1TB等多种规格，可以供我们存储数据。

- 华为云也提供了类似的云服务——[云硬盘EVS](https://www.huaweicloud.com/product/evs.html)，价格低至￥0.30/GB/月起（按申请磁盘的容量大小计费），可主动在线扩容，单盘容量最多支持32TB。

- 然而我们有更好的选择——[对象存储服务OBS](https://www.huaweicloud.com/product/obs.html)，低至￥0.099/GB/月起（按实际数据存储容量计费），容量无上限，99.99%以上的稳定与可靠。代价是数据访问方式与我们熟悉的略有不同，需要一点点的学习成本。

- 开发者可以将训练数据、代码等上传到自己的对象存储服务OBS中，通过授权，ModelArts的计算资源可以访问到这些数据。开发者创建训练作业后，产生的中间数据、最终模型也都可以再存储到对象存储服务OBS中。

- 大多数算法开发者或数据科学家，在他们第一次接触OBS时，都会很迷茫，但熟悉之后，就会感觉这东西其实很棒。业内的其他云服务供应商[Amazon Web Service](https://aws.amazon.com/cn/s3/)、[Microsoft Azure](https://azure.microsoft.com/en-us/services/storage/blobs/)、[Google Cloud](https://cloud.google.com/storage/)也都是使用了对象存储的方案。

### OBS对象存储

- 打开华为云主页：https://www.huaweicloud.com/
- 如下图所示，转到 产品>基础服务>存储>对象存储服务 OBS> 管理控制台
![Aaron Swartz](https://img.buzzfeed.com/buzzfeed-static/static/2018-01/23/15/asset/buzzfeed-prod-fastlane-01/anigif_sub-buzz-27474-1516737829-1.gif)

#### 创建OBS Bucket





## 添加访问密钥

- 

- 在移动互联网时代，每个用户都会熟悉账号+密码，或者诸如手机号+验证码的用户登录/鉴权方式。

- 然而在开发侧，或云服务侧，需要更安全灵活的鉴权方案，业内大多使用了公钥和私钥的方案来做鉴权认证





### 2. *谁*创造了它？
它由[**Aaron Swartz**](http://www.aaronsw.com/)和**John Gruber**共同设计，**Aaron Swartz**就是那位于去年（*2013年1月11日*）自杀,有着**开挂**一般人生经历的程序员。维基百科对他的[介绍](http://zh.wikipedia.org/wiki/%E4%BA%9A%E4%BC%A6%C2%B7%E6%96%AF%E6%B2%83%E8%8C%A8)是：**软件工程师、作家、政治组织者、互联网活动家、维基百科人**。    

他有着足以让你跪拜的人生经历：    
+ **14岁**参与RSS 1.0规格标准的制订。     
+ **2004**年入读**斯坦福**，之后退学。   
+ **2005**年创建[Infogami](http://infogami.org/)，之后与[Reddit](http://www.reddit.com/)合并成为其合伙人。   
+ **2010**年创立求进会（Demand Progress），积极参与禁止网络盗版法案（SOPA）活动，最终该提案被撤回。   
+ **2011**年7月19日，因被控从MIT和JSTOR下载480万篇学术论文并以免费形式上传于网络被捕。     
+ **2013**年1月自杀身亡。    

![Aaron Swartz](https://modelarts-cnnorth1-modelhub-meta.obs.cn-north-1.myhuaweicloud.com/picture/05d4ae2d-739f-441d-a34f-72c60606c61f.gif)

天才都有早逝的归途。

