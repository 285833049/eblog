#### 项目说明：

本博客是学习过程中搭建的项目，为了融合更多知识点，让博客看起来更加高大上，使用了多个框架组合，有些也是企业级项目中常用的解决方式。不够说实话，还有挺多内容缺少的，比如xss攻击预防等安全方面的。

0304

#### 项目结构：
```
eblog
│
├─src
│  ├─main
│  │  ├─java
│  │  │  └─com
│  │  │      └─markerhub
│  │  │          │  CodeGenerator.java #代码生成
│  │  │          │
│  │  │          ├─common
│  │  │          │  ├─exception #全局异常处理
│  │  │          │  ├─lang
│  │  │          │  └─templates #自定义Freemarker标签封装
│  │  │          │
│  │  │          ├─config #整合配置
│  │  │          ├─controller
│  │  │          ├─entity
│  │  │          │
│  │  │          ├─im #即时群聊
│  │  │          │  ├─handler
│  │  │          │  ├─message
│  │  │          │  ├─server
│  │  │          │  └─vo
│  │  │          │
│  │  │          ├─mapper
│  │  │          ├─schedules #定时任务
│  │  │          │
│  │  │          ├─search #内容搜索引擎与同步
│  │  │          │  ├─model
│  │  │          │  ├─mq
│  │  │          │  └─repository
│  │  │          │
│  │  │          ├─service
│  │  │          │  └─impl
│  │  │          │
│  │  │          ├─shiro #shiro整合
│  │  │          ├─template #定义标签
│  │  │          ├─util
│  │  │          └─vo
│  │  │
│  │  └─resources
│  │      │  application.yml
│  │      ├─mapper
│  │      ├─static
│  │      │  └─res
│  │      │
│  │      └─templates #页面模板

```

#### 技术选型：

* 核心框架：Springboot 2.1.2
* 安全框架：Apache Shiro 1.4
* 持久层框架：Mybatis + mybatis plus 3.2.0
* 页面模板：Freemarker
* 缓存框架：Redis
* 数据库：mysql
* 消息队列：RabbitMq
* 分布式搜索：Elasticsearch 6.4.3
* 双工通讯协议：websocket
* 网络通讯框架：t-io 3.2.5
* 工具集合：hutool 4.1.17

#### 知识要点：
* 基于mybatis plus快速代码生成
* 封装与自定义Freemarker标签
* 使用shiro+redis完成了会话共享
* redis的zset结构完成本周热议排行榜
* t-io+websocket完成即时消息通知和群聊
* 基于rabbitmq+elasticsearch的内容同步与搜索引擎

#### 项目部署：

项目中我们用到了几个中间件，mysql、rabbitmq、elasticsearch。

#### 如何交流、反馈？

* 详细开发文档：
* Git仓库：[https://github.com/MarkerHub/eblog](https://github.com/MarkerHub/eblog)
* 官方微信：**java-mindman3**
* 技术讨论、问题和建议，请移步到公众号【MarkerHub】菜单栏留言区，我会在第一时间进行解答和回复！
* 如需关注项目最新动态，请Watch、Star项目，同时也是对项目最好的支持
* 官方公众号：**MarkerHub**

![公众号](https://image-1300566513.cos.ap-guangzhou.myqcloud.com/mine/MarkerHub.jpg)

#### 项目视频：

#### 项目演示：

演示地址：[https://eblog.markerhub.com](https://eblog.markerhub.com)

账号密码：自行注册~

#### 项目截图：

![注册](https://oscimg.oschina.net/oscnet/up-5c6b2b3f4c7b415cfbafea06b6aaf365ab9.png "注册")

![首页](https://oscimg.oschina.net/oscnet/up-22214fea0fc4bc67d29232d3c8004609e4f.png "首页")

![群聊](https://oscimg.oschina.net/oscnet/up-e1e6084e96a61dc22c95e820fa6e40a7940.png "群聊")

![搜索引擎](https://oscimg.oschina.net/oscnet/up-1b61685d1b4f7f2b62b6d917e57da7828f8.png "搜索引擎")

![设置](https://oscimg.oschina.net/oscnet/up-083ca0a70f566c208ce3a7aae00ab502622.png "设置")
