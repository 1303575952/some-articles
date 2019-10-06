## 漫话：如何给女朋友解释什么是HTTP

周末一大早，我正在电脑前面浏览一些技术网站，突然女朋友大喊起来：哇，杭州又下大雪啦，快来看啊。我并没有理她，于是她跑过来拉我。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rJMabxw9YrVsvuydPQ9SNqLVAKrGN16gelZ1hhibkOobRE1cD8dk4Dvw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rF112MUmTXjVzCduDg9lWuFDbDc1z34hnExYYHrLSlBJib7NXZyBnWQQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rWCxicTdfeuMVU0uck8M7upstpW5HuHSchrvu8GBgLUbv3IFTVJumbnQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rrib597K05khTdtwgXVsYpeUbdGf9d9GIeICVDIqUgbubEGEDg9sdCpw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6r9lBDNQd157t35ypf0vx8AjwbC2ia9rXDicLWUkcXSgSEEuQmwDibfvicdg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

￼ 图，雪后杭州



![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rE5gwpY2d7icpib07fgksfhnjiburvUUypzfguhX10GhxFBd7ScG2QIiayg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rMM9j3QCEtNf4ibRcgJlNZMo3cdL5H8MMia8EgichEhFtWQeFVFOTFMiaxg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

上次杭州下雪的时候，[[给女朋友介绍了什么是RPC\]](http://mp.weixin.qq.com/s?__biz=Mzg3MjA4MTExMw==&mid=2247484671&idx=1&sn=008b9fad52cfdd96d0d4c838b8364fea&chksm=cef5f749f9827e5f46bcc0272f5af74b8eeb1fb6860001b6fd53ce6fb25f18014143c1bb2eaf&scene=21#wechat_redirect)，这次下雪将要介绍的HTTP和RPC也有点关系，都是通信方式。

### **什么是HTTP协议**

HTTP是HyperText Transfer Protocol的缩写，中文翻译为**超文本传输协议**。他是一种用于分布式、协作式和超媒体信息系统的应用层协议。HTTP是万维网的数据通信的基础。

说的简单点，**其实HTTP协议主要就是用来进行客户端和服务器之间进行通信的标准协议**。HTTP主要规定了客户端如何与服务器建立链接、客户端如何从服务器请求数据、服务器如何响应请求，以及最后连接如何关闭。

当我们在浏览器中输入一个url，如http://www.taobao.com ，然后按下回车，一直到页面显示淘宝网的首页的过程就是一次HTTP的网络通信。

这次通信过程中，我们查看淘宝使用的电脑就是**客户端**，而搭建淘宝网的那些计算机机器就是**服务器**。

![img](https://mmbiz.qpic.cn/mmbiz_png/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6reNkApC9po4l9h4Y3wDQKagxF72xFNxcHnDLqv75ciciapcC51P942Udg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

￼

这个过程有点像老板通过电话给员工下达命令。当我们在浏览器输入网址并按下回车之后，共发生了以下四件事：

1、建立连接：老板拨通手下员工的电话 

2、进行请求：老板提出自己的要求 

3、响应：员工应答老板的请求 

4、关闭连接：挂断电话

**建立连接**

老板找出自己公司的总机电话号并拨通，员工接听电话的过程就是**建立连接**。

根据用户输入的URL地址，通过DNS、负载均衡等技术找到一台服务器，客户端与服务器的80端口建立一个TCP链接。

**进行请求**

电话被接通之后，老板可能要求某个具体员工来进行接听，并且会对该员工下达一些命令，比如帮他取个快递，帮他预订个酒店，帮他收购一家公司等。这个过程就**进行请求（request）**。

客户端向服务器发送消息，请求URL中指定的页面，要求执行指定的操作。

老板对员工下达的命令中，可以分为很多种，比如有些命令只是简单的事情询问、而有些命令则要求员工执行某些决定，如收购公司等。

同样的，HTTP的请求方法也有很多种，主要的有**GET**、**POST**、**HEAD**等。

**响应**

员工在接收到老板下单的命令后，需要对该命令做出回应。比如直接告知老板他接下来的行程，帮老板预订好酒店后告诉他已经预订成功等。这个过程就是**响应（response）**

服务器向客户端发送响应。响应以状态码开头。常见的状态码有：200、302、404、500等。

HTTP状态码由三个十进制数字组成，第一个十进制数字定义了状态码的类型，后两个数字没有分类的作用。HTTP状态码共分为5种类型：

| 分类 | 分类描述                                       |
| ---- | ---------------------------------------------- |
| 1**  | 信息，服务器收到请求，需要请求者继续执行操作   |
| 2**  | 成功，操作被成功接收并处理                     |
| 3**  | 重定向，需要进一步的操作以完成请求             |
| 4**  | 客户端错误，请求包含语法错误或无法完成请求     |
| 5**  | 服务器错误，服务器在处理请求的过程中发生了错误 |

**关闭连接**

老板在下达完命令，并且员工给予响应之后，双方会挂断电话。这个过程就是**关闭连接**。

客户端或服务端都可以关闭连接。每个请求都是用一个单独的网络连接。

特别的是：**服务器不回记忆前面一次连接或者其结果，这种不记忆过去请求的协议被称为无状态(stateless)协议。**

![-w1647](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6r1hndLkX8Uyp7pSKqmz5ISHXU0s5UCGDG2HDtPsOsLCtkrzibgEpC9QQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

￼

上图就是一次淘宝网的HTTP请求的过程。其中显示了request（请求）和response（响应）的所有信息。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rTngReaQibeXWIlHVA9xvaDJsdL23ATYibMsWsBfXIFWk6o0OOkYn3tKA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rJuTib8eBKtB8qmKD2ibpYSkNevD1xDUZicL8scrteq0CvSDuVpAua2p9Q/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6ry19ske6fm7MY41ePMVKcKzUwWXBJtTyjnOgZT22kQk0S2hul6dxrMg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rQcgDjOXPQ3CnibvBicSwyRJgzbOz70lvRSGF5jhxa1tUapPOq7LDhFQQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### **HTTP协议的迭代**

前面我们把HTTP通信比喻成打电话，严格一点来说，HTTP/2更像是现在的打电话。HTTP协议主要的版本有3个，分别是HTTP/1.0、HTTP/1.1和HTTP/2。

**HTTP/1.0**

1996年5月，HTTP/1.0 版本发布，为了提高系统的效率，**HTTP/1.0规定浏览器与服务器只保持短暂的连接，浏览器的每次请求都需要与服务器建立一个TCP连接，服务器完成请求处理后立即断开TCP连接**，服务器不跟踪每个客户也不记录过去的请求。

这种方式就好像我们打电话的时候，只能说一件事儿一样，说完之后就要挂断，想要说另外一件事儿的时候就要重新拨打电话。

HTTP/1.0中浏览器与服务器只保持短暂的连接，连接无法复用。也就是说每个TCP连接只能发送一个请求。发送数据完毕，连接就关闭，如果还要请求其他资源，就必须再新建一个连接。

我们知道TCP连接的建立需要三次握手，是很耗费时间的一个过程。所以，HTTP/1.0版本的性能比较差。

**HTTP/1.1**

为了解决HTTP/1.0存在的缺陷，HTTP/1.1于1999年诞生。相比较于HTTP/1.0来说，最主要的改进就是引入了持久连接。所谓的持久连接即**TCP连接默认不关闭，可以被多个请求复用**。

由于之前打一次电话只能说一件事儿，效率很低。后来人们提出一种想法，就是电话打完之后，先不直接挂断，而是持续一小段时间，这一小段时间内，如果还有事情沟通可以再次进行沟通。

客户端和服务器发现对方一段时间没有活动，就可以主动关闭连接。或者客户端在最后一个请求时，主动告诉服务端要关闭连接。

HTTP/1.1版还引入了管道机制（pipelining），即在同一个TCP连接里面，客户端可以同时发送多个请求。这样就进一步改进了HTTP协议的效率。

![img](https://mmbiz.qpic.cn/mmbiz_png/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6riceRAJLM534mGI6zM14RJudaib6LhjSHI4R4wCGSPaeMOL3qsn246IPw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

￼

也就是说，现在打电话，一个电话里面可以吩咐多件事儿了。但是对于执行者来说，还是需要按照顺序，先执行完一件事儿以后再执行另外一件事儿。

**有了持久连接和管道，大大的提升了HTTP的效率。但是服务端还是顺序执行的，效率还有提升的空间。**

**HTTP/2**

HTTP/2 是 HTTP 协议自 1999 年 HTTP 1.1 发布后的首个更新，主要基于 SPDY 协议。

HTTP/2 为了解决HTTP/1.1中仍然存在的效率问题，HTTP/2 采用了**多路复用**。即在一个连接里，客户端和浏览器都可以同时发送多个请求或回应，而且不用按照顺序一一对应。能这样做有一个前提，就是HTTP/2进行了**二进制分帧**，即 HTTP/2 会将所有传输的信息分割为更小的消息和帧（frame）,并对它们采用二进制格式的编码。

也就是说，老板可以同时下达多个命令，员工也可以收到了A请求和B请求，于是先回应A请求，结果发现处理过程非常耗时，于是就发送A请求已经处理好的部分， 接着回应B请求，完成后，再发送A请求剩下的部分。A请求的两部分响应在组合到一起发给老板。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rWFc9dzibjbz8DFP9cz32T0KlvcFQ6brFPaIQdYFia8jDFCW5uMaC0GUA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

￼

而这个负责拆分、组装请求和二进制帧的一层就叫做

二进制分帧层

。

除此之外，还有一些其他的优化，比如做Header压缩、服务端推送等。

**Header压缩**就是压缩老板和员工之间的对话。

**服务端推送**就是员工事先把一些老板可能询问的事情提现发送到老板的手机（缓存）上。这样老板想要知道的时候就可以直接读取短信（缓存）了。

目前，主流的HTTP协议还是HTTP/1.1 和 HTTP/2。并且各大网站的HTTP/2的使用率也在逐年增加。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rgOWfCcRpNiaIcksQCs4Q0xGJyzxSVMeIkGPRBU2YbnNqu8KJPnDnaZQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rxAmGsGSUKhI7MrLicUS2aFWENicN7lT5GfMutI5dKd8zj3ggrcYlsogA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rc2uavG6o4EkibtZsdsdx7r35acnoWwnqicia8MtfgFV9t9tLqRlg4G6ibA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6r1VqRP4NUdveI97kf7IQFwcSCvsr2uklZf2GVjJaCh1WQ2W0Y7SrUibg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### **HTTP-over-QUIC**

据国际互联网工程任务组（The Internet Engineering Task Force，简称 IETF ）消息，HTTP-over-QUIC 实验性协议将被重命名为 HTTP/3，并有望成为 HTTP 协议的第三个正式版本。

QUIC （Quick UDP Internet Connections）是 Google 推出的一个项目，旨在降低基于 TCP 通讯的 Web 延迟。QUIC 非常类似 TCP+TLS+SPDY ，**但是基于 UDP 实现的**。

这种通信方式有点像现在我们使用的微信语言，在通话之前，老板和下属之间并没有直接的建立可靠连接，即不需要拨通电话，而是拿起微信，直接通过语音直接下达了命令。

![img](https://mmbiz.qpic.cn/mmbiz_gif/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rFLlkIBCkCNEto6uLh8gibXjXncROsDhkAKnhVCG3JrxcvV8szzEC1fw/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)

￼

HTTP/3使用UDP代替了TCP

，UDP是一个非连接的协议，传输数据之前源端和终端

不建立连接

。 UDP信息包的标题很

短

，对系统资源的要求比TCP要低。并且UDP是使用最大努力交付，即

不保证可靠交付

。

我们经常使用的“ping”命令的原理就是向对方主机发送UDP数据包，然后对方主机确认收到数据包， 如果数据包是否到达的消息及时反馈回来，那么网络就是通的。

至于，这种基于QUIC的HTTP协议究竟未来发展如何，目前只能拭目以待了。

下面是一张大图，通过图解来介绍HTTP/1.0、HTTP/1.1、HTTP/2.0（SDPY）和HTTP over QUIC(HTTP/3)

![img](https://mmbiz.qpic.cn/mmbiz_png/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rJIs18LN7ch3mUdbrhuw7v9bwoNmkKRtbAhXHw44dGQ1G4fhtLm2jlw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

￼

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rxNVmK6bkN6YnWibYjUXqqFbwsK91kqzVepIDa9QTFe4ZWP3otBLYib7A/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rODRFl7xMnyic320pX7ibicR48Ed51VTxz3ppAu1C6oibsMYiaWDD6auYI0w/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rVcAZT9HqulFuFOpBm3I3nYpfWWPgOHa714uZdMPkKu2wWdLLTQkbzQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6r8jtUXlCsYQh6cY3oJIPMNvgOHkqohicqrak0VvfnfPz9oh4X8rz0GhQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### **HTTPS**

HTTPS是Hypertext Transfer Protocol Secure的缩写，翻译为超文本传输安全协议。**HTTPS经由HTTP进行通信，但利用SSL/TLS来加密数据包。**

HTTPS就像是加密电话，通过一些手段来加密通话内容的。他是基于普通电话的，但是又不是普通的电话，更不是普通电话的升级版。

所以，**HTTP和HTTPS是两个不同的协议**。

HTTP的URL是由“http://”起始与默认使用端口80，而HTTPS的URL则是由“https://”起始与默认使用端口443。

HTTP不是安全的，而且攻击者可以通过监听和中间人攻击等手段，获取网站帐户和敏感信息等。HTTPS的设计可以防止前述攻击，在正确配置时是安全的。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rqic6qsk9QJLTQd2opzvPiaUkzMXSl0tpqdd8r8IP2VDI2BcSVVBypiaAA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rDVFjul9mVoIsS6Y6ZZoapsicjY0spYpwV2AOXxnIBQCPcZgXHlNrXzw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

美国民主与技术中心 CDT 首席技术专家 Joseph Hall 表示： "使用 HTTPS，你的互联网服务供应商不会知道你在网站上干了些什么，即使是政府和间谍也不能办到。"

![-w367](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6r628aib0c7a8NickfnGPx05iaAC1KGGxSqbWv89f99nFbGvNjx9YqU27Wg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

所以，目前已经有很多网站都在使用HTTPS协议了，包括全球最大的程序员交友网站：github！我说的是github，不是pornhub哦，虽然他也是https的。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/C1uDMDqjn1ib4kj3n4DrruNCnZm6Cpia6rTs1icQKbkao25Mfc6kSmHFUVMlVUtKjCwHFOpIawjWmEa6libgiac4xVw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)