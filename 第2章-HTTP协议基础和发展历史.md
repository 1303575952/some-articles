# 第2章-HTTP协议基础和发展历史

## 网络协议分层

![经典五层模型](pic/经典五层模型.PNG)

**低三层**

* 物理层主要是定义物理设备如何传输数据
* 数据链路层在通信的实体间建立数据链路连接
* 网络层为数据在节点之间创建逻辑链路

**传输层**

* 向用户提供可靠的端到端（End-to-End）服务
* 传输层向高层屏蔽了下层数据通信的细节

**应用层**

* 为应用程序提供了很多服务
* 构建于TCP协议之上
* 屏蔽网络传输相关细节

## HTTP三次握手

在客户端和服务器进行HTTP请求的发送和返回过程中，需要创建一个TCP connection，HTTP不存在连接的概念，只有请求和响应（请求和响应均为数据包）。数据包的传输需要通道，此通道即由TCP创建，一个TCP连接是可以发送多个HTTP请求的（HTTP1.1之后）。

![HTTP三次握手](pic/HTTP三次握手.PNG)

## URI、URL和URN

**URI**

* Uniform Resource Identifier/统一资源标识符

* 用来唯一标识互联网上的信息资源

* 包括URL和URN

**URL**

* Uniform Resource Locator/统一资源定位器
* http://user:pass@host.com:80/path?query=string#hash
* 此类格式的都叫URL，比如ftp协议

**URN**

* 永久统一资源定位符
* 在资源移动之后还能找到
* 目前还没有非常成熟的使用方案

## HTTP报文格式

![HTTP报文格式](pic/HTTP报文格式.PNG)

**HTTP方法**

* 用来定义对资源的操作
* 常用的有GET、POST等
* 从定义上讲有各自的语义

**HTTP CODE**

* 定义服务器对请求的处理结果

* 各个区间的CODE有各自的语义
* 好的HTTP服务可以通过CODE判断结果

**一个简单的server**

```js
const http = require('http')

http.createServer(function (request, response) {
    console.log('request come', request.url)

    response.end('123')
}).listen(8888)

console.log('server listening on 8888')
```

