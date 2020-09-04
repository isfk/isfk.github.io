---
title: flutter无线（WIFI）调试真机
date: 2020-09-04 16:21:56
tags:
---

## mac 安装 adb

```bash
brew cask install android-platform-tools
```

## 连接真机，设置无线

```bash
# 查看连接
$ adb devices
List of devices attached
MQS0219912008017	device

# 设置端口号 adb tcpip 8888
adb -s MQS0219912008017 tcpip 8888

# 连接（进入手机查看wifi连接）
adb connect 192.168.0.140:8888
```

## run

```
flutter run
```