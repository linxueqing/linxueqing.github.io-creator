---
title: "Url"
date: 2020-03-03T21:53:05+08:00
draft: false
---

# 浅析 URL

## URL 包含哪几部分，每部分分别有什么作用

1. 协议：是指规则的约定，例如 Web 使用一种名为 HTTP 的协议作为规范
2. 域名或者 IP：服务器地址
3. 端口号：服务器提供服务的一个号码
4. 路径：带层次指向一个服务器的不同页面
5. 查询字符串：指向一个页面的不同内容
6. 锚点：指向同一个内容的不同位置的片段标识符，不会传给服务器

## DNS 的作用是什么，nslookup 命令怎么用

DNS (Domain Name System) 域名系统，将方便用户记忆的域名地址 domain names 转换为 IP 数字串 IP addresses，从而在因特网 Internet 或者私有网络上找到特定的机器。
简单来说就是域名对应 IP 的一个服务。

nslookup 是一种网络管理命令行工具，可用于查询 DNS 域名和 IP 地址。

nslookup 询问服务器 IP 命令使用方法

```
    nslookup qq.com
```

## IP 的作用是什么，ping 命令怎么用

IP (Internet protocol) 互联网协议，约定了两件事：

1. 如何定位一台设备，可以是电脑、手机、路由器。。。
2. 如何封装数据报文，与其他设备交流

ping 命令使用方法

```
   ping qq.com
```

## 域名是什么，分别哪几类域名

域名是服务器 IP 地址对应的名字，方便使用

- .com 顶级域名
- xxxx.com 二级域名
- www.xxxx.com 三级域名
