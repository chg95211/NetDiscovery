![](images/logo.png)
# NetDiscovery

[![@Tony沈哲 on weibo](https://img.shields.io/badge/weibo-%40Tony%E6%B2%88%E5%93%B2-blue.svg)](http://www.weibo.com/fengzhizi715)
[![License](https://img.shields.io/badge/license-Apache%202-lightgrey.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/703e0ba9760b4affaf39188dbbdd2811)](https://app.codacy.com/app/fengzhizi715/NetDiscovery?utm_source=github.com&utm_medium=referral&utm_content=fengzhizi715/NetDiscovery&utm_campaign=Badge_Grade_Dashboard)


# 功能特点：

* 轻量级爬虫
* 模块化设计，便于扩展：支持多种消息队列、多种网络框架，也支持自己实现。
* 支持分布式
* 多线程、异步化：底层使用 RxJava 2 的多线程机制
* 支持 Request 添加到正在运行爬虫的 Queue 中
* 支持 Kotlin 协程
* 支持 JS 渲染
* Request 支持自定义 header 信息
* Request 支持 debug 功能：在调试时可以使用 RxCache，从而避免多次请求同一个网页。
* 支持失败重试的机制
* 多纬度控制爬取速度（Pipeline、Request、Download、Domain）等等
* 支持代理池、User Agent 池、Cookies 池
* 支持爬虫的深度抓取：能够在 Pipeline 中发起深度抓取
* 支持 URL 去重：使用布隆过滤器
* Spider 的监控、SpiderEngine 的监控 (基于Etcd、Zookeeper)
* agent 模块能够对当前服务器的 CPU 和内存进行实时监控
* SpiderEngine 整合 Quartz


# 最新版本

模块名|最新版本|
---|:-------------:
netdiscovery-core-core|[ ![Download](https://api.bintray.com/packages/fengzhizi715/maven/netdiscovery-core-core/images/download.svg) ](https://bintray.com/fengzhizi715/maven/netdiscovery-core-core/_latestVersion)
netdiscovery-core-engine|[ ![Download](https://api.bintray.com/packages/fengzhizi715/maven/netdiscovery-core-engine/images/download.svg) ](https://bintray.com/fengzhizi715/maven/netdiscovery-core-engine/_latestVersion)
netdiscovery-core-engine-monitor|[ ![Download](https://api.bintray.com/packages/fengzhizi715/maven/netdiscovery-core-engine-monitor/images/download.svg) ](https://bintray.com/fengzhizi715/maven/netdiscovery-core-engine-monitor/_latestVersion)
netdiscovery-downloader-htmlunit|[ ![Download](https://api.bintray.com/packages/fengzhizi715/maven/netdiscovery-downloader-htmlunit/images/download.svg) ](https://bintray.com/fengzhizi715/maven/netdiscovery-downloader-htmlunit/_latestVersion)
netdiscovery-downloader-httpclient|[ ![Download](https://api.bintray.com/packages/fengzhizi715/maven/netdiscovery-downloader-httpclient/images/download.svg) ](https://bintray.com/fengzhizi715/maven/netdiscovery-downloader-httpclient/_latestVersion)
netdiscovery-downloader-okhttp|[ ![Download](https://api.bintray.com/packages/fengzhizi715/maven/netdiscovery-downloader-okhttp/images/download.svg) ](https://bintray.com/fengzhizi715/maven/netdiscovery-downloader-okhttp/_latestVersion)
netdiscovery-downloader-selenium|[ ![Download](https://api.bintray.com/packages/fengzhizi715/maven/netdiscovery-downloader-selenium/images/download.svg) ](https://bintray.com/fengzhizi715/maven/netdiscovery-downloader-selenium/_latestVersion)
netdiscovery-pipeline-couchbase|[ ![Download](https://api.bintray.com/packages/fengzhizi715/maven/netdiscovery-pipeline-couchbase/images/download.svg) ](https://bintray.com/fengzhizi715/maven/netdiscovery-pipeline-couchbase/_latestVersion)
netdiscovery-pipeline-elasticsearch|[ ![Download](https://api.bintray.com/packages/fengzhizi715/maven/netdiscovery-pipeline-elasticsearch/images/download.svg) ](https://bintray.com/fengzhizi715/maven/netdiscovery-pipeline-elasticsearch/_latestVersion)
netdiscovery-pipeline-mongo|[ ![Download](https://api.bintray.com/packages/fengzhizi715/maven/netdiscovery-pipeline-mongo/images/download.svg) ](https://bintray.com/fengzhizi715/maven/netdiscovery-pipeline-mongo/_latestVersion)
netdiscovery-pipeline-redis|[ ![Download](https://api.bintray.com/packages/fengzhizi715/maven/netdiscovery-pipeline-redis/images/download.svg) ](https://bintray.com/fengzhizi715/maven/netdiscovery-pipeline-redis/_latestVersion)
netdiscovery-queue-kafka|[ ![Download](https://api.bintray.com/packages/fengzhizi715/maven/netdiscovery-queue-kafka/images/download.svg) ](https://bintray.com/fengzhizi715/maven/netdiscovery-queue-kafka/_latestVersion)
netdiscovery-queue-rabbitmq|[ ![Download](https://api.bintray.com/packages/fengzhizi715/maven/netdiscovery-queue-rabbitmq/images/download.svg) ](https://bintray.com/fengzhizi715/maven/netdiscovery-queue-rabbitmq/_latestVersion)
netdiscovery-queue-redis|[ ![Download](https://api.bintray.com/packages/fengzhizi715/maven/netdiscovery-queue-redis/images/download.svg) ](https://bintray.com/fengzhizi715/maven/netdiscovery-queue-redis/_latestVersion)
netdiscovery-kotlin-coroutines|[ ![Download](https://api.bintray.com/packages/fengzhizi715/maven/netdiscovery-kotlin-coroutines/images/download.svg) ](https://bintray.com/fengzhizi715/maven/netdiscovery-kotlin-coroutines/_latestVersion)
netdiscovery-kotlin-dsl|[ ![Download](https://api.bintray.com/packages/fengzhizi715/maven/netdiscovery-kotlin-coroutines/images/download.svg) ](https://bintray.com/fengzhizi715/maven/netdiscovery-kotlin-coroutines/_latestVersion)

NetDiscovery 是基于 Vert.x、RxJava 2 等框架实现的爬虫框架。目前正在不断地完善中，未来会做成一个更为通用的爬虫框架。

对于 Java 工程，如果使用 gradle 构建，由于默认没有使用 jcenter()，需要在相应 module 的 build.gradle 中配置

```groovy
repositories {
    mavenCentral()
    jcenter()
}
```

在 NetDiscovery 中，Spider 可以单独运行，Spider 也可以交给 SpiderEngine 来控制。

SpiderEngine 可以在运行之前注册到 Etcd/Zookeeper，然后由 monitor 对 SpiderEngine 进行监控。

![](https://github.com/fengzhizi715/NetDiscovery/blob/master/images/SpiderEngine_Cluster.png)

# 详细功能查看[wiki](https://github.com/fengzhizi715/NetDiscovery/wiki)

# [下载](https://github.com/fengzhizi715/NetDiscovery/blob/master/Download.md)

# 案例:

* [user-agent-list](https://github.com/fengzhizi715/user-agent-list):抓取常用浏览器的user agent
* [FXHParser](https://github.com/fengzhizi715/FXHParser):抓取非小号数字货币

# 基于本人的开源项目

* [RxCache](https://github.com/fengzhizi715/RxCache)
* [ProxyPool](https://github.com/fengzhizi715/ProxyPool)

# TODO List:

1. 整合[cv4j](https://github.com/imageprocessor/cv4j)以及 Tesseract，实现 OCR 识别的功能
2. 整合 RocketMQ
3. SpiderEngine 提供http/rpc接口，用于构建爬虫的任务
4. 完善协程的模块
5. 完善 wiki，增加各个模式的使用说明
6. 各个模块能够从配置文件中获取爬虫相应的配置
7. 增强 HtmlUnit 模块
8. 增加 chromium 的支持


# Contributors:

* [bdqfork](https://github.com/bdqfork)
* [homchou](https://github.com/homchou)
* [sinkinka](https://github.com/sinkinka)


# Contributing:

[Pull requests](https://help.github.com/categories/collaborating-with-issues-and-pull-requests/) are welcome



# 联系方式:

Wechat：fengzhizi715

> Java与Android技术栈：每周更新推送原创技术文章，欢迎扫描下方的公众号二维码并关注，期待与您的共同成长和进步。

![](https://user-gold-cdn.xitu.io/2018/7/24/164cc729c7c69ac1?w=344&h=344&f=jpeg&s=9082)


License
-------

    Copyright (C) 2017 - present, Tony Shen.

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.


