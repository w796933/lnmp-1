# 开发环境

## 开发过程

在 `docker-compose.yml` 修改需要启用的软件。

在 `.env` 修改镜像前缀、PHP 项目路径。

克隆已有的 PHP 项目文件到 `./app/` 目录下，或新建 PHP 项目文件夹（可以使用 `./lnmp-docker.sh new` 交互式的填入项目路径 url）。

在 `./config/nginx/` 参考示例配置，新建 `nginx` 配置文件（可以使用 `./lnmp-docker.sh nginx-conf` 便捷的生成 nginx 配置文件）。

执行 `./lnmp-docker.sh development`。

`PhpStorm` 打开 `./app/你的项目名称` ，开始编写代码。

### 使用 Composer

`./lnmp-docker.sh composer 路径 命令` 进行依赖的安装或升级。

### 命令行执行 PHP 文件

```bash
$ ./lnmp-docker.sh php 路径 命令
```

## 自行构建镜像

在 `./dockerfile/` 下修改各个软件 `dockerfile` 文件，之后运行如下命令：

```bash
$ ./lnmp-docker.sh build

$ curl 127.0.0.1

Welcome use khs1994-docker/lnmp v17.11 x86_64 With Build Docker Image

development

```
