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

## 2 修改Nacos配置

使用下列命令进入配置编辑界面，变更其中`server.port`配置为65000，并保存。

```
edit nacos/conf/application.properties
```

**注意** 该端口您可以随意修改，但只有修改为65000时可以在实验中访问控制台。


## 3. 启动Nacos服务端

进入解压后的Nacos目录，然后使用下列命令即可启动一个单例模式的Nacos服务端。

```
cd nacos
bin/startup.sh -m standalone
```

## 4. 查看启动成功

```
tail -f logs/start.out
```

观察到日志显示`Nacos started successfully in xxx mode. use xxx storage`则表示启动成功。

使用

```
curl localhost:65000/nacos/v1/ns/health/server
```

也能够获得反馈～

接下来可以进入到<tutorial-web-preview port="65000" path="/nacos/#/login">Nacos控制台</tutorial-web-preview> 进行查看和操作。

## 5. 部署完成

完成上述步骤后，nacos已经部署完成。您可以查看更多官方文档来获取更多部署Nacos的相关信息

- [Nacos部署手册](https://nacos.io/zh-cn/docs/deployment.html)
- [集群部署说明](https://nacos.io/zh-cn/docs/cluster-mode-quick-start.html)
- [Nacos 系统参数介绍](https://nacos.io/zh-cn/docs/system-configurations.html)
