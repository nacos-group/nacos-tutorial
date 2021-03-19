# Nacos 部署文档

![Nacos](https://github.com/alibaba/nacos/blob/develop/doc/Nacos_Logo.png?raw=true)

欢迎来到 Nacos 的世界！

Nacos 致力于帮助您发现、配置和管理微服务。Nacos 提供了一组简单易用的特性集，帮助您快速实现动态服务发现、服务配置、服务元数据及流量管理。

Nacos 帮助您更敏捷和容易地构建、交付和管理微服务平台。 Nacos 是构建以“服务”为中心的现代应用架构 (例如微服务范式、云原生范式) 的服务基础设施

* Github: [https://github.com/alibaba/nacos](https://github.com/alibaba/nacos)
* 官方网站: [https://nacos.io/zh-cn/index.html](https://nacos.io/zh-cn/index.html)

## 0. 依赖说明

使用Nacos前，需要在运行环境中安装Java(x64) 8～11版本。

本实验环境已经安装完成。

## 1. 下载并安装Nacos服务端

详细的部署教程请使用 上一个课程。这里直接执行下列命令进行启动

```
curl -OL https://handson.oss-cn-shanghai.aliyuncs.com/nacos-server-2.0.0-tutorial.tar.gz
tar -zxvf nacos-server-2.0.0-tutorial.tar.gz
sed -i 's/8848/60000/g' nacos/conf/application.properties
nacos/bin/startup.sh -m standalone
```

## 2. TODO
