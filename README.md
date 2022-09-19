# Subconverter-Railway
> 将以下大佬项目部署到railway

GitHub [stilleshan/dockerfiles](https://github.com/stilleshan/dockerfiles)  
Docker [stilleshan/subconverter](https://hub.docker.com/r/stilleshan/subconverter)
> *docker image support for X86 and ARM*

## 简介
基于 [tindy2013/subconverter](https://github.com/tindy2013/subconverter) 项目的 docker 镜像.仅修改 **分组配置文件** 以解决以下问题.

- **增加**`Netflix，DisneyPlus`等分组.
- **去除**`自动选择 url-test`以解决连接数爆涨问题.
- **修改时区** 镜像默认时区为 Asia/Shanghai

## 示例
[https://sub.ops.ci](https://sub.ops.ci)  
*`前后端示例,可以直接使用.`*

## 更新
- **2022-07-16** 新增 [stilleshan/sub](https://github.com/stilleshan/dockerfiles/tree/main/sub) subweb + subconverter 合并进阶版.
- **2022-07-04** 新增 [stilleshan/subweb](https://github.com/stilleshan/subweb) 前端项目.
- **2022-04-03** 更新`v0.7.2`版 docker 镜像
- **2021-12-20** 更新优化规则和分组
- **2021-12-01** 添加`Disney+`规则分组
- **2021-09-30** 更新`v0.7.1`版 docker 镜像
- **2021-09-21** 更新`v0.7.0`版 docker 镜像
- **2021-06-09** 更新`v0.6.4`版 docker 镜像,新增同时支持 X86 和 ARM 架构.

## 部署

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/new/template/L5KcmH?referralCode=LKqerK)

- 点击上方图片跳转 Railway
- 登陆你的 Github 账号
- 填写你要创建的库名  
- 点击部署
- 配置自定义域名以通过此域名访问

🎉🎉🎉 完成！你就有了个始终免费在线的订阅转换API🎉🎉🎉

### 绑定域名
> 简述，具体配置请参考[官方文档](https://docs.railway.app/deploy/exposing-your-app#lets-encrypt-ssl-certificates)。

- 在 Cloudflare 中添加 `Cname` 解析指向 `yourapp.yourrailwayproject.com` 
    - 可能长这样 `https://xxxx-xxxxx.xx.railway.app/`
- 并配置 `SSL/TLS` 的 **加密模式** 为 **完全** 或 **完全（严格）**
- 在 `Railway` 的 `Settings - Domains` 中接入该域名


### docker
```shell
docker run  -d --name=subconverter --restart=always -p 25500:25500 stilleshan/subconverter
```

### docker compose
下载 [docker-compose.yml](https://raw.githubusercontent.com/stilleshan/dockerfiles/main/subconverter/docker-compose.yml) 执行以下命令启动:
```shell
docker-compose up -d
```

### subweb + subconverter 合并进阶版
详情查看 [stilleshan/sub](https://github.com/stilleshan/dockerfiles/tree/main/sub)

## 链接
- [stilleshan/sub](https://github.com/stilleshan/dockerfiles/tree/main/sub)
- [stilleshan/subweb](https://github.com/stilleshan/subweb)
- [stilleshan/subconverter](https://github.com/stilleshan/subconverter)
- [tindy2013/subconverter](https://github.com/tindy2013/subconverter)
