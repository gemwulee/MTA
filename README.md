# MTA
MTA 官方CocoaPods Spec镜像

## 使用方法
### 基础统计功能
Podfile 中添加
```
pod 'QQ_MTA'
```
__注意: 为了提高统计的精确性, IDFA 模块已经与 MTA 模块合并, 为避免 IDFA 模块影响 APP上架, 请参考 [idfa 配置文档](http://docs.developer.qq.com/mta/fast_access/ios.html#idfa%E9%87%87%E9%9B%86%E6%8C%87%E5%8D%97)进行相关配置__

### 可视化埋点功能
Podfile 中添加
```
pod 'QQ_MTA/AutoTrack'
```

### 应用崩溃报告
Podfile 中添加
```
pod 'QQ_MTA/CrashReporter'
```

### H5 App 混合统计功能
Podfile 中添加
```
pod 'QQ_MTA/Hybrid'
```

### Idfa 统计
idfa 模块已经与 MTA 统计基础功能合并。不需要单独添加。

### 安装来源分析
安装来源分析已经升级成广告效果监测

### 广告效果监测
Podfile 中添加
```
pod 'QQ_MTA/AdTracker'
```

### 数据洞察
Podfile 中添加
```
pod 'QQ_MTA/DataInsight'
```

### 异常行为监测
Podfile 中添加
```
pod 'QQ_MTA/Fbi'
```


## 更新日志
VERSION 2.5.4
-------------------------------------------
1. 解决getSysInfoByName导致的Crash问题

VERSION 2.5.3
-------------------------------------------
1.解决因为访问UIPasteboard导致的Crash问题

VERSION 2.5.2
-------------------------------------------
1.修复toJsonString的偶现crash
2.修改NSMutableArray的分类，防止命名冲突

VERSION 2.5.1
-------------------------------------------
1.修改多帐号模块加载的时机<br>
2.广告监测增加自定义UserAgent接口<br>
3.使用Xcode10编译<br>
4.增加mid字段

VERSION 2.5.0
-------------------------------------------
1. 修复偶现的crash

VERSION 2.4.3
-------------------------------------------
1.调整多账号注销逻辑

VERSION 2.4.2
-------------------------------------------
1.提高SDK稳定性

VERSION 2.4.1
-------------------------------------------
1.增加Qzone定制版接口

VERSION 2.4.0
-------------------------------------------
1.增加多账号统计功能

VERSION 2.2.1
-------------------------------------------
1.修复模拟器下编译不过的问题

VERSION 2.2.0
-------------------------------------------
1.广告效果监测正式发布
2.为了数据准确，正式集成IDFA采集(请参考idfa集成文档)
3.优化getOpenUdid逻辑

VERSION 2.1.2
-------------------------------------------
* 禁用模拟器下MTA所有功能
* 精简上报接口

VERSION 2.1.0
-------------------------------------------
* 增加自动页面统计功能
* 增加可视化埋点二维码扫描功能
* 优化可视化埋点网页刷新延迟的问题
* 优化启动速度

VERSION 2.0.8
-------------------------------------------
* 增加H5 APP混合统计功能

VERSION 2.0.7
-------------------------------------------
* 解决插件"安装来源追踪"和webview冲突的问题

VERSION 2.0.6
-------------------------------------------
* 增加安装来源追踪

VERSION 2.0.5
-------------------------------------------
* 增加用户分群接口

VERSION 2.0.4
-------------------------------------------
* 提升网速监控的准确性

VERSION 2.0.3
-------------------------------------------
* 可视化埋点增加关联元素
* 修正可视化埋点页面中元素位置不对的问题
* 提升时长相关统计的准确性

VERSION 2.0.2
-------------------------------------------
* 增加无埋点统计功能

VERSION 2.0.1
-------------------------------------------
* 修复符号冲突的问题

VERSION 2.0.0
-------------------------------------------
* 开启新版奔溃报告

VERSION 1.6.9
-------------------------------------------
* 修复MTAEvent doesNotRecognizeSelector的问题

VERSION 1.6.8
-------------------------------------------
* 修复数据库中脏数据引发的问题
* 解决数据库读取死锁的问题

VERSION 1.6.7
-------------------------------------------
* 对服务器返回的异常包做容错处理

VERSION 1.6.6
-------------------------------------------
* 修复一个因为储存问题引发的crash

VERSION 1.6.5
-------------------------------------------
* 增加SDK在iOS10系统下的稳定性

VERSION 1.6.4
-------------------------------------------
* 提高启动次数统计的准确率
* 改进崩溃报告

VERSION 1.6.3
-------------------------------------------
* 增加MID，增加客户端识别准确率

VERSION 1.6.2
-------------------------------------------
* 解决跟部分sdk符号冲突的问题

VERSION 1.6.1
-------------------------------------------
* 迁移数据库

VERSION 1.6.0
-------------------------------------------
* 传输协议切换为tcp

VERSION 1.5.9
-------------------------------------------
* 提报上报准确率

VERSION 1.5.8.1
-------------------------------------------
* 提高 SDK 稳定性

VERSION 1.5.8
-------------------------------------------
* 提高 SDK 稳定性
* 用 Xcode 7 重新编译

VERSION 1.5.7
-------------------------------------------
* 用 Xcode 8 Beta 2 重新编译

VERSION 1.5.6
-------------------------------------------
* 提高 SDK 稳定性

VERSION 1.5.5
-------------------------------------------
* 移除速度测试功能

VERSION 1.5.4
-------------------------------------------
* 修复特定情况下事件不上报的问题

VERSION 1.5.3
-------------------------------------------
* 修复极端情况crash的问题

VERSION 1.5.2
-------------------------------------------
* 修复特定接口crash的问题

VERSION 1.5.1
-------------------------------------------
* 增加ipv6支持

VERSION 1.5.0
-------------------------------------------
* 增加上报准确性
* 提升sdk稳定性

VERSION 1.4.12
-------------------------------------------
* 确保MTAEnv devicename不返回nil
* MTAEvent toJsonString中的encode增加try...catch
* sqlite回调函数中增加nil保护机制

VERSION 1.4.10
-------------------------------------------
* 增加忽略特定自定义事件功能

VERSION 1.4.9
-------------------------------------------
* 提高网络测速稳定性
* debug模式下,写入本地log

VERSION 1.4.8
-------------------------------------------
* 增加用户反馈接口

VERSION 1.4.8.1
-------------------------------------------
* 提高稳定性

VERSION 1.4.7
-------------------------------------------
* 增加特定事件即时上报功能

VERSION 1.4.6
-------------------------------------------
* 解决idx重复的问题

VERSION 1.4.5
-------------------------------------------
* 优化了一些内存管理逻辑

VERSION 1.4.4
-------------------------------------------
* 修复由于bundle id命名导致启动时crash的bug
* 文档优化了一些描述

VERSION 1.4.3
-------------------------------------------
* 支持crash日志半符号化，显示更多函数信息

VERSION 1.4.2
-------------------------------------------
* 支持crash日志删除前回调
* 解决极端情况下出现重复上报的问题
* 升级判断回包成功条件

VERSION 1.4.1
-------------------------------------------
*  补齐1.4.0缺失的两个错误统计的字段(剩余内存，剩余空间)

VERSION 1.4.0
-------------------------------------------
*  支持arm64架构编译
*  解决极端情况下出现重复上报的问题

VERSION 1.3.1
-------------------------------------------
*  增加自定义ifa
*  增加字段，设置苹果的deviceToken

VERSION 1.3.0
-------------------------------------------
*  增加错误上报的详情信息。(进程名，剩余内存，剩余空间)

VERSION 1.2.9
-------------------------------------------
*  支持部分接口指定appkey上报。
*  支持部分接口实时上报。
*  支持服务器端下发配置来禁用MTA
*  增加reportAccount接口(reportQQ增强版)

VERSION 1.2.8
-------------------------------------------
*  修复1.2.6引入的bug，该bug导致指标"活跃用户数"不准确。

VERSION 1.2.7
-------------------------------------------
*  由于苹果的审核关系，删除IDFA部分代码，以防审核不通过

VERSION 1.2.6
-------------------------------------------
*  优化加密解密算法
*  增加设备唯一标识对ios7的支持

VERSION 1.2.5
-------------------------------------------
*  新增用户文档, MTA高级游戏模型开发指南

VERSION 1.2.4
-------------------------------------------
*  优化启动时的上报逻辑

VERSION 1.2.3
-------------------------------------------
*  优化json库，防止和第三方json库冲突

VERSION 1.2.2
-------------------------------------------
*  增加网速监控功能，上报字段 sp cn op
*  SDK下发的配置，字段名_MTA_TEST_SPEED_

VERSION 1.2.1
-------------------------------------------
*  增加自定义app设置cui字段(自定义ui)
*  增加自定义app设置cav字段(自定义app版本)
*  上报数据中增加序号
*  上报数据增加必要字段app版本号，用户类型，渠道

VERSION 1.2.0
-------------------------------------------
*  修改上报策略的名称（增加MTA_前缀），防止编译时名字冲突。升级SDK需要注意同时修改上报策略设置部分的代码。
*  缓存MTA未初始化调用上报接口的数据

VERSION 1.1.2
-------------------------------------------
*  API调用增加初始化判断限制，防止SDK未经初始化的API调用情况
*  只调用SDK初始化方法未嵌入任何统计代码，会上报一次启动数据

VERSION 1.1.1
-------------------------------------------
*  解决批量上报场景下的内存泄漏问题

VERSION 1.1.0
-------------------------------------------
*  强制上报advertisingIdentifier， 需要开发者在Xcode中导入“AdSupport.framework”
*  修改应用版本号上报优先为CFBundleShortVersionString取值
*  Bug fix

VERSION 1.0.0
-------------------------------------------
*  增加游戏用户统计
*  增加自定义事件上报长度限制
*  Bug fix

VERSION 0.9.0
-------------------------------------------
*  Bug fix

VERSION 0.7.0
-------------------------------------------
*  增加Crash自动上报机制

VERSION 0.6.1
-------------------------------------------
*  增加一种发送策略ONLY_WIFI_NO_CACHE：仅在WIFI环境下发送，不缓存任何数据
*  增加启动检查函数+(BOOL) startWithAppkey:(NSString* ) appkey checkedSdkVersion:(NSString* )ver
*  删除JSONKit依赖

VERSION 0.6.0
-------------------------------------------
*  增加监控类统计接口
*  增加maxSessionStatReportCount设置，默认关闭
*  解决缓存内容与单引号冲突问题

VERSION 0.4.4
-------------------------------------------
*  页面统计增加来源字段
*  增加自定义上报地址设置

VERSION 0.4.1
-------------------------------------------
*  跨天逻辑修改

VERSION 0.4.0
-------------------------------------------
*  Bug fix
*  支持SDK休眠配置更新

VERSION 0.3.0
-------------------------------------------
*  IOS6 用IFA字段填充ui字段
*  优化

VERSION 0.2.0
-------------------------------------------
*  增加携带Key-Value参数的自定义事件

VERSION 0.1.2
-------------------------------------------
*  修改XCode编译参数，减小SDK尺寸
*  增加智能上报设置，默认打开（当网络切换到WIFI情况下，自动改成实时上报）

VERSION 0.1.1
-------------------------------------------
*  上传统计数据支持加密
*  增加Demo，文档


VERSION 0.1.0
-------------------------------------------
*  初始版本

