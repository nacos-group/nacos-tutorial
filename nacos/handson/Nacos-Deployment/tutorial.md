# Nacos 部署文档

![Nacos](https://github.com/alibaba/nacos/blob/develop/doc/Nacos_Logo.png)

欢迎来到 Nacos 的世界！

Nacos 致力于帮助您发现、配置和管理微服务。Nacos 提供了一组简单易用的特性集，帮助您快速实现动态服务发现、服务配置、服务元数据及流量管理。

Nacos 帮助您更敏捷和容易地构建、交付和管理微服务平台。 Nacos 是构建以“服务”为中心的现代应用架构 (例如微服务范式、云原生范式) 的服务基础设施

* Github: [https://github.com/alibaba/nacos](https://github.com/alibaba/nacos)
* 官方网站: [https://nacos.io/zh-cn/index.html](https://nacos.io/zh-cn/index.html)

## 0. 依赖说明

使用Nacos前，需要在运行环境中安装Java(x64) 8～11版本。

## 1. 下载并安装Nacos服务端

官方的Nacos服务端需要在Github上进行下载

[Nacos下载页](https://github.com/alibaba/nacos/releases)

在本实验中，您可以使用以下命令直接下载

```
curl -OL https://handson.oss-cn-shanghai.aliyuncs.com/nacos-server-2.0.0-tutorial.tar.gz
```

下载完成后，仅需要解压即可安装完成。

```
tar -zxvf nacos-server-2.0.0-tutorial.tar.gz
```

## 2. 启动Nacos服务端

进入解压后的Nacos目录，然后使用下列命令即可启动一个单例模式的Nacos服务端。

```
cd nacos
bin/startup.sh -m standalone
```

## 3. 查看启动成功

```
tail -f logs/start.out
```

观察到日志显示`Nacos started successfully in xxx mode. use xxx storage`则表示启动成功。

使用

```
curl localhost:8848/nacos/v1/ns/health/server
```

也能够获得反馈～
