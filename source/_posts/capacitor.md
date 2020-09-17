---
title: 使用capacitor+vue+vant开发一个App
date: 2020-09-17 09:18:15
tags:
---

## capacitor 是什么？(机译)

capacitor：Web应用的跨平台本地运行时

Capacitor是一个跨平台的本机运行时，可轻松构建可在iOS，Android和Web上本机运行的Web应用程序。代表混合应用程序的下一个发展，它为希望构建Web优先应用程序的团队提供了一种现代的本机容器方法，这些应用程序在需要时可以完全访问本机SDK

## vant 是什么？（自述）

vant 是一套基于vue的移动端UI组件

## 初始化一个项目

我们使用最新的 vue3预览版进行测试

```bash
vue create app
  Default ([Vue 2] babel, eslint) 
❯ Default (Vue 3 Preview) ([Vue 3] babel, eslint) 
  Manually select features 
```

### 安装 vant

```bash
yarn add vant@next
npm i babel-plugin-import -D

# vim babel.config.js 添加

plugins: [
    ['import', {
        libraryName: 'vant',
        libraryDirectory: 'es',
        style: true
    }, 'vant']
]
```

### 集成 capacitor

```bash
# 安装依赖
npm install @capacitor/core @capacitor/cli

# 初始化
npx cap init

# 修改 capacitor.config.json webDir => "dist"

# 生成静态代码 到 dist 目录（默认的）
yarn build
```

### 自动生成 anroid 端代码

```bash
# 增加安卓端
npx cap add android

# 如果修改了代码可以执行 将编译后的 dist 复制到安卓端
npx cap copy
```