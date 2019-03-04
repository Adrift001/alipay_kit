# fake_alipay

[![Build Status](https://cloud.drone.io/api/badges/v7lin/fake_alipay/status.svg)](https://cloud.drone.io/v7lin/fake_alipay)
[![GitHub tag](https://img.shields.io/github/tag/v7lin/fake_alipay.svg)](https://github.com/v7lin/fake_alipay/releases)

flutter版支付宝SDK

## fake 系列 libraries

1. [flutter版okhttp3](https://github.com/v7lin/fake_http)
2. [flutter版微信SDK](https://github.com/v7lin/fake_wechat)
3. [flutter版腾讯(QQ)SDK](https://github.com/v7lin/fake_tencent)
4. [flutter版新浪微博SDK](https://github.com/v7lin/fake_weibo)
5. [flutter版支付宝SDK](https://github.com/v7lin/fake_alipay)
6. [flutter版百度移动统计SDK](https://github.com/v7lin/fake_analytics)
7. [flutter版百度移动推送SDK](https://github.com/v7lin/fake_push)

## android

````
# 不需要做任何额外接入工作
# 混淆已打入 Library，随 Library 引用，自动添加到 apk 打包混淆
````

## ios

````
在Xcode中，选择你的工程设置项，选中“TARGETS”一栏，在“info”标签栏的“URL type“添加“URL scheme”为你所注册的应用程序id

URL Types
alipay: identifier=alipay schemes=${your app scheme name}
````

````
iOS 9系统策略更新，限制了http协议的访问，此外应用需要在“Info.plist”中将要使用的URL Schemes列为白名单，才可正常检查其他应用是否安装。

<key>LSApplicationQueriesSchemes</key>
<array>
    <string>alipay</string>
</array>
<key>NSAppTransportSecurity</key>
<dict>
    <key>NSAllowsArbitraryLoads</key>
    <true/>
</dict>
````

## flutter

#### snapshot
````
dependencies:
  fake_alipay:
    git:
      url: https://github.com/v7lin/fake_alipay.git
````

#### release
````
latestVersion = 0.0.1+1
````

````
dependencies:
  fake_alipay: ^${latestVersion}
````

#### example
[示例](./example/lib/main.dart)

## Getting Started

This project is a starting point for a Flutter
[plug-in package](https://flutter.io/developing-packages/),
a specialized package that includes platform-specific implementation code for
Android and/or iOS.

For help getting started with Flutter, view our 
[online documentation](https://flutter.io/docs), which offers tutorials, 
samples, guidance on mobile development, and a full API reference.
