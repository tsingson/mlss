# mlss
music lesson scheduling system 音乐课编排系统

## 0. 背景/起因

这个 repo 创建的原因, 见[这里](https://zhuanlan.zhihu.com/p/161988813) 

## 1. 开发涉及的技术选择
1. 前台 web 浏览器, 采用 react JS  + HTML 
2. 后台当然是 web 服务
3. 后台 web 服务主要由 web proxy 做为网关实现, 同时提供静态 HTML/JS 服务
4. 在 web proxy 后面, 分别是 websocket 服务提供 IM 与提醒功能 ,  REST 应用服务提供主要的音乐学员管理/课程管理/教室管理/教师管理/学员授课跟踪等主业务,  图像服务器提供图像上传/存储/显示,  postgres 12 数据库做为 REST 应用提供主要存储
5. 在时间允许情况下, 计划开发 android APK ( java 或  kotlin ) 客户端, 以及开发微信小程序..........etc


## 2. repo 结构

```
├── cmd
├── db
├── docs
└── web
```

```
├── cmd  ---------- 后台服务的可执行程序
├── db   ---------- postgres 12 数据库的 sql 文档, 包括数据表与存储过程
├── docs ---------- 开发文档/部署文档等
└── web  ---------- web 前端 HTML + JS 源码等
```