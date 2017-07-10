---
title: dns学习笔记
date: 2017-07-10 13:36:00
tags: 协议,protocol
---

dns
================
关于域名的常识
www.baidu.com	是一个主机名，FQDN（Full Qualified Domain Name）
www.baidu.com.	才是一个域名【注意那个点，表示根域】

TLP(Top Level Domain)

递归查询，响应请求下一级查询的地址，DNS本身之间不提问
迭代查询，
yum install bind 
yum install bind-chroot	#用于改变目录/var/named->/var/named/chroot/var/named,提高安全性
cd /var/named
cp -a data/
cp -a dynamic/
cp -a slaves/
cp -a named.ca named.empty named.localhost named.loopback /var/named/chroot/var/named/

关于权限
named下所有文件及目录用户组是named，文件所有者root,目录所有者named

/var/named/chroot/var/named/下放正向解析的zone文件














PTR PoinTeR,指向的缩写，反解到主机名


1. 点击开始, 点击运行, 键入REGEDIT, 然后按确定。
2. 点选至以下的子键:
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip\Linkage
3. 双击Route项,查看键值，找到排第一位的内容，然后点取消
4. 双击Bind项，找到第3步找到的排第一的内容，将其剪切粘贴到第一位，然后点击确定
5. 完成后按确定退出注册表编辑器.

