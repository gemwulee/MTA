# Rest API 概述（V3）

## v3版本和v2版本的区别

- 完全基于 HTTPs，不再提供HTTP访问

- 支持POST方式访问，不再提供GET方式访问

- 使用 HTTP Basic Authentication 的方式做访问授权。 API 请求可以使用常见的 HTTP 工具来完成，比如：curl，postman等

- API接口按照业务功能分类，类别为：Push API、Tag API、Device API、Tool API。每种类别的API接口采用相同的URL，提高接口易用性

- 功能方面的改进：增加送达统计的查询功能，该接口属于工具类API，目前内测中

  ​

## API概述

信鸽推送提供遵从 REST 规范的 HTTP API，以供开发者远程调用信鸽提供的服务

接口主要分为四大类：

| API类型      | 描述              | 状态   |
| ---------- | --------------- | ---- |
| Push API   | 包含多种消息推送的接口     | 正常   |
| Tag API    | 主要完成标签的新增、删除、查询 | 正常   |
| Device API | 主要完成账号的查询、删除    | 实现中  |
| Tool API   | 用来定位问题和其他数据查询   | 实现中  |



## 请求方式

- 仅支持 HTTPs
- 仅支持 POST




## 权鉴方式

- 采用基础鉴权的方式，HTTP Header（头）里加一个字段（ Key/Value 对）：

  ```
  Authorization: Basic base64_auth_string
  ```

- 其中 base64_auth_string 的生成算法为：`base64(APPID:SECRETKEY)`

  即对 `APPID` 加上冒号，加上 `SECRETKEY` 拼装起来的字符串，再做 `base64` 转换

- `APPID` 和 `SECRET KEY` 可在[信鸽官网](http://xg.qq.com/)【我的应用】【应用配置】中获取

  ​

## 协议描述

**请求URL**：`https://openapi.xg.qq.com/v3/<class_path>/<method>`

| 字段名               | 用途      | 备注            |
| ----------------- | ------- | ------------- |
| openapi.xg.qq.com | 接口域名    | 无             |
| v3                | 版本号     | 无             |
| class_path        | 提供的接口类别 | 不同的接口有不同的路径名  |
| method            | 功能接口名称  | 不同的功能接口有不同的名称 |



## API限制

- Push API中全量推送、标签推送接口有调用频率的限制外，默认为每个ACCESS_ID每小时30次
- 推送的消息体大小限制为 4K，此限制适用于 Push API 中的 `message` 字段