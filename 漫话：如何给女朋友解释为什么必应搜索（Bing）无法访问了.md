## 漫话：如何给女朋友解释为什么必应搜索（Bing）无法访问了？

2019年1月23日下午，我正在公司疯狂的撸着代码，沉浸在我的代码世界中，正在欣赏着自己刚刚写下的一行lambda表达式，突然微信上传来女朋友的消息。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzSCsibUTlEgYibF70y1oWLTDqo68FZCzZI46X1qEpcBqiatQcPtjecibGIg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzhIibxq8LUWSCtiao3fj2KbQxpTibKt55OKfHySwmiaeQEvfa4xt5Py1xYQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

在浏览器输入cn.bing.com，显示结果如下：

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzFnpuBQMP3ys9weWSX4StbaaZRXSIaXz0ROcTEXdQGQN9zVr9MA0AfA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

￼

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzQ3WEPpKEHm2OicBIy2VcKksYZ5MgqgTUZn3JEw9PzuPmsxORPgFOBYQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzvusS2IeL7nYMmsFDZFVgEqEZnYZFNib4lqfkCyFjKjlClibPVZXHEluQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

于是，我打开我的terminal，准备ping一下，看看到底怎么回事：

```
➜  mhcoding ping cn.bing.com
PING cn.bing.com (127.0.0.1): 56 data bytes
64 bytes from 127.0.0.1: icmp_seq=0 ttl=64 time=0.046 ms
64 bytes from 127.0.0.1: icmp_seq=1 ttl=64 time=0.091 ms
64 bytes from 127.0.0.1: icmp_seq=2 ttl=64 time=0.098 ms
```

于是，我再微信上给女朋友回复：

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzA5rlpD7S6CJSHaFAI9Iiac7mQ9dFcJmU8qibmsNlt7NtVy0INFjaUxjw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

晚上下班回到家，还没等我脱下我的双肩包，女朋友就快速的跑过来找我。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzroQIB6KUeiaNFVH2FCibZnF2Y0lS4B27k94iacAWqibfJGm7hvHiaXy36eg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzvRum0ico8ZC607oI5lneW89icRWeOibn5GrFQmmnbXuZl5DE53UIM3xrg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzpmPBeiciare8KULrk9IMVwZHkB5vyxVibMau8lKK38MvU0kospEWq2Gzg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzVryBFKicPYpADT862z40xBIl3FMlw8xLPFkY0aXnsebiam8p64ulLwkA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### **DNS**

DNS，是Domain Name System的缩写，翻译成域名系统。它作为将域名和IP地址相互映射的一个分布式数据库，能够使人更方便地访问互联网。

**DNS最主要的作用就是将域名翻译成ip地址。**

**IP地址**

IP地址是IP Address的缩写，指互联网协议地址（英语：Internet Protocol Address，又译为网际协议地址）。IP地址是IP协议提供的一种统一的地址格式，它为互联网上的每一个网络和每一台主机分配一个逻辑地址，以此来屏蔽物理地址的差异。

互联网上的每一台计算机，都会分配到一个IP地址。

IP地址被用来给Internet上的电脑一个编号。大家日常见到的情况是每台联网的PC上都需要有IP地址，才能正常通信。

IP地址是一个32位的二进制数，通常被分割为4个“8位二进制数”（也就是4个字节）。IP地址通常用“点分十进制”表示成（a.b.c.d）的形式。如：208.80.152.2

**域名**

域名，这个是很多人都熟悉的概念，我们大多数情况下，在浏览器上访问某个网站的时候，都是通过域名访问的。

域名是由一串用点分隔的字符组成的互联网上某一台计算机或计算机组的名称，用于在数据传输时标识计算机的电子方位。

域名可以说是一个IP地址的代称，目的是为了便于记忆后者。

例如，wikipedia.org是一个域名，和IP地址208.80.152.2相对应。人们可以直接访问wikipedia.org来代替IP地址，然后域名系统（DNS）就会将它转化成便于机器识别的IP地址。

这样，人们只需要记忆wikipedia.org这一串带有特殊含义的字符，而不需要记忆没有含义的数字。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzPurnk6a0jG2CfLbrlLEicdkHmpZXjiaeWy2WQu0fEnria6O5QAkSuvtVQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQz76zUTvo67iaMb3CY7oF1Fv4spxicarY3oibZaM2lBiaHXcb91icHITyu1icw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### **域名、IP和DNS**

在现实生活中，我们可能经常需要通过电话找人，每一台接入网络的电话都有一个自己独一无二的号码。

有的时候，我们想要打某个公司的客服电话，如想要给工商银行的客服打电话，想查询账户余额。但是我们不知道具体号码，我们可以拨打114，告诉他们自己想要拨打工商银行的电话。然后114的客服会帮你查询到工商银行的电话，并帮你自动转接到工商银行的客服电话。

这个过程就和域名、IP地址以及DNS之间的关系比较像了。

```
每一台接入网络的电话 -> 每一台接入网络的计算机
工商银行 -> 域名
电话号码 -> ip地址
114咨询台  -> DNS
```

有了DNS，我们不需要记住每一个网站的多个IP地址，我们只需要之道这个网站的域名就可以了。就像我们不关心工商银行的客服电话，我们只需要知道我们要找工商银行就可以了。

而且，对于一个网站来说，一个域名会对应其无数个IP地址。会通过负载均衡等方式进行调配。就像工商银行的客服中心也有很多分机的道理是一样的。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzTzygRsVwMib4N2KK53hr0pib3ZMfTYWaZ2AcHK7g17E3niczWweOHY87Q/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzBFDRC3qtmZiazLe55NH5xpajdISfiaay2xx7esfdV2sgPP2ZtJDqDWow/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzd1LKHMK67o7LgnKUU7HfoGBepTtKcibu0TvlIJsr3UvUXLB0EngXs3w/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzrKdFadq2VDeBwQiaX5SNP1ruXsYNMHkPpWYcUtqxMcGRk9QvQRvQFRg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

某些网络运营商为了某些目的，可能会限制某些用户访问某一些特定的网站，而限制手段最常用的就是DNS污染和DNS劫持。

正常情况下，当我们访问某个域名的时候，会跳转到失败页面，但是如果爬到墙外，就可以正常访问。比如所谓的qiang。

还有一种典型场景，当我们的宽带欠费的时候，访问某个网站时，被自动跳转到运营商网站，提示充值。

这都是运营商在DNS上做了手脚。其目的是为了让域名无法解析到正常的IP地址。

**而此次必应无法访问期间，通过ping可以发现，cn.bing.com被DNS解析成127.0.0.1。这是无法访问bing的直接原因原因。**

> 127.0.0.1是回送地址，指本地机，一般用来测试使用。

### **DNS污染**

网域服务器缓存污染（DNS cache pollution），又称域名服务器缓存投毒（DNS cache poisoning），是指一些刻意制造或无意中制造出来的域名服务器数据包，把域名指往不正确的IP地址。

其工作方式是：由于通常的DNS查询没有任何认证机制，而且DNS查询通常基于的UDP是无连接不可靠的协议，因此DNS的查询非常容易被篡改，通过对UDP端口53上的DNS查询进行入侵检测，一经发现与关键词相匹配的请求则立即伪装成目标域名的解析服务器（NS，Name Server）给查询者返回虚假结果。

DNS污染指的是用户访问一个地址，国内的服务器(非DNS)监控到用户访问的已经被标记地址时，服务器伪装成DNS服务器向用户发回错误的地址的行为。为了减免网络上的交通，一般的域名都会把外间的域名服务器数据暂存起来，待下次有其他机器要求解析域名时，可以立即提供服务。一旦有关网域的局域域名服务器的缓存受到污染，就会把网域内的电脑导引往错误的服务器或服务器的网址。

![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDIby7MALwE30ReibyvicvMIQzoAiaI3ibz5fGH4FbSzicaIdiaZFVD57ibOqvsASibUsicB2gmI5No3e1QibpNg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

简单点说，DNS污染是指把自己伪装成DNS服务器，在检查到用户访问某些网站后，使域名解析到错误的IP地址。

### **DNS劫持**

DNS劫持又称域名劫持，是指在劫持的网络范围内拦截域名解析的请求，分析请求的域名，把审查范围以外的请求放行，否则返回假的IP地址或者什么都不做使请求失去响应，其效果就是对特定的网络不能访问或访问的是假网址。

![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDIby7MALwE30ReibyvicvMIQztpYoUcibgyicTXEibVX6V0Bgic5RibVxvaOqRCBs6uhVZficicHXZdjSMtA8Q/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

￼

简单点说，DNS劫持指的是通过非法手段，获取DNS服务器的权限，然后把DNS配置进行修改，使域名解析到错误的IP地址。

**DNS污染和DNS劫持的区别**

DNS劫持是劫持了DNS服务器，进而修改其解析结果。

DNS污染是国内的某些服务器对DNS查询进行入侵检测，发现与黑名单上匹配的请求，该服务器就伪装成DNS服务器，给查询者返回虚假结果。它利用了UDP协议是无连接不可靠性。

**一个是劫持了DNS服务器，一个是伪装成DNS服务器。造成的结果都是返回错误的IP地址。**

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzt0ibSjvuXXicq4WkCfDxyeY7JuU8NLLx2FhGza2icnfcZOpiatBIib6hhrA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzs3dpGRiaa5Ds2XVT9suzo6OUvWnqxupB0l0h5Vp8MfsLA12uzicz1icbg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### **如何解决DNS污染和劫持**

对于 DNS劫持，可以通过手动更换DNS服务器为第三方公共DNS解决。

> 公共DNS 是一种面向大众的免费的 DNS 互联网基础服务。更换 DNS 服务器地址为 公共DNS 后，可以在一定程度上加快域名解析速度、防止 DNS劫持、加强上网安全，还可以屏蔽大部分运营商的广告。

下图就是常用的公共DNS：

![-w694](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzMPVt6cztcJ6DiaoqkHSUSctoKmSfkffnHnuYkvCADTmFb09fTwvm6Bg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

￼

 

*（图源：http://www.yunweipai.com/archives/5175.html）*

对于 DNS污染，可以说，个人用户很难单单靠设置解决，通常可以使用 VPN 或者域名远程解析的方法解决。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzDE3PYYLPyWweCtANIaniaYoj93vfHrEJqViaeIcvBXI4Y6UpNutHDq5Q/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzYqUWGcnIthgGOpemko5cYAshbpFgLWrgshoYSShicmMwJ2T6ic5fdP6w/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### **必应挂了如何访问**



![-w837](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQziaiabrsTzNU3zZwRWmAIibP3NHIuhl19BbGk0mZxzVTxqWWrC9AtibohZA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

￼

一、用必应（Bing）临时域名

www2.bing.com 或者 www4.bing.com

**二、强制绑定host**

用户只需要暂时修改下host然后坐等微软服务器恢复后再删除即可。即强制指定cn.bing.com指向的IP地址。

13.107.21.200 cn.bing.com

修改后如果浏览器依然无法正常打开请直接重启系统，重启后再尝试打开必应搜索看看能否恢复正常访问。

**三、修改DNS服务器**

把DNS修改成公共DNS，如8.8.8.8 或者 114.114.114.114。

参考：https://laod.cn/news/cn-bing-com-404.html

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzx0os8fl3ibmRw7we2GTxr5ThdUPFZenciaOn9abn1fKGIiaZTicaiadmHyA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzw14zia5NicQXgoFiahUcXEFB0P3J7zpzXwkVxI51fAl4g0O495gnoZicMw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzcXEgPqAud47xSoAyBtgjAg6o1XE3KMbEkiaXFibdIrBZK6TosY4QVs1g/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDIby7MALwE30ReibyvicvMIQzeuQzjh1txG7paM5PCJEAN01g1sj0rhTpicpf9cce5QLmiaGYtZwSOLBg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### **事件后续**

1月23日下午，有网友发现微软搜索引擎网站必应（Bing）出现无法访问故障。打开之后显示，“无法访问此网站”。

1月24日，微软发言人先后回复记者称，“正在展开调查”以及“我们正在积极应对，以确定下一步相关措施”。

1月25日早上，微软发言人回复记者称，“我们确认必应网站之前在中国无法访问，但是现已恢复正常”。不过，微软并未透露此前不能正常访问的原因。

本文的重点是分析必应无法被正常访问的原因，关于域名、DNS等并未深入和展开介绍，如果读者感兴趣，后面会继续逐一展开介绍。


  