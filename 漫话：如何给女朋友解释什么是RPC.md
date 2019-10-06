## 漫话：如何给女朋友解释什么是RPC

周末一大早，我正在电脑前面看新闻，突然女朋友大喊起来：哇，杭州下大雪啦，快来看啊。我并没有理她，于是她跑过来拉我。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQG2pjiahPicpuXLq9PicDAZKfHmKroIwAsyFrCTSSNC3E15LY0BNAJyND7A/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGicDKL8e27FpGoagEhLsGqDwvicp4lPt23afC1S44wAiaFDwwmWDgQiaSkg/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGkJ3lJmbzLjHaVr8W3uCRDd7DaOLgp8hric4a6yQ0icy7Rd2Y64icVCpicg/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGQa5wZbJ33sWmj2RoN9icVicibDBvys7Qrjj1ULIWVzOMOUuzs7GGrlZWw/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGiaVIPEiauApb4uVWSXARmiaGXIBVVboFmmMlqoudETLK4aHuNBIZucuicg/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGpSSMwnxPSRNgVxbotNWicT5lRCmXHHY8NfQceowpx41yp9z8Wlv5QOw/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGPRxtWQMxkZLfarDsm1aLpUA113oicrfz8xEdHlFehFtZBh24ic0t6EaQ/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

雪后杭州

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGrKzw1TlNfcuM9kTUbU3SH8k85WvEmHeUu0bK4jhppqeibW83lmhdLpg/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGFulcmiatkCyraDiahbRWhkLHcqPZqSp89aHzTXjJ0Y7ck0MfwHwzrZFA/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**RPC 是Remote Procedure Call的缩写，译为远程过程调用。是一个计算机通信协议。**

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGajdhzMapUX4NfYB5aSH8Zj3FBbI2erSz7EhhnYNHY9oP7nHccSzyKw/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGjUyTMH31xCfzkEicNQ6bxUib831EMFFib9HMJvfx9uTTfeT9m3UuGtPng/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### **为什么需要远程调用**

在[如何给女朋友解释什么是分布式](http://mp.weixin.qq.com/s?__biz=MzU3OTYxOTU4NA==&mid=2247483700&idx=1&sn=7ba76648097d419431c9f8a4df047d2d&chksm=fd621f5bca15964d4a792fe8eeb423d4024381050f6c1cd697e05b251adcd9227c6883346100&scene=21#wechat_redirect)这一篇文章中介绍过，为了提升饭店的服务能力，饭店从一开始只有一个负责所有事情的厨师发展成有厨师、切菜师、备菜师等多个角色。

在饭店只有一个厨师的时候，厨师想要做出一道美味的番茄炒蛋的时候，他需要自己洗番茄、切番茄、打鸡蛋、炒菜。整个过程不需要其他人参与自己就完全可以完成了。这就是古老的集中式应用中，一台单体计算机就可以搞定所有事情了。

```
制作番茄炒蛋{
    厨师->洗菜->切菜->炒菜
}
```

随着饭店发展，需要明确分工，让专业的人负责专业的事儿。所以，整个做菜过程中不再只有厨师参与了。需要有多个角色，备菜师傅负责准备番茄和鸡蛋、切菜师傅负责切菜、厨师只要负责炒菜就行了。

但是，随着分工明确，制作番茄炒蛋的过程不再是只有一个人参与的过程了。这个过程中需要多方协作。厨师准备炒菜之前，需要先通知备菜师傅和切菜师傅，前序工作准备好之后才能进行炒菜。

```
制作番茄炒蛋{
    备菜师->洗菜
    切菜师->切菜
    厨师->炒菜
}
```

这种情况下，厨师就要依赖很多外人来参与这个炒菜工作。而他在通知备菜师帮他洗菜，通知切菜师傅帮他切菜的时候，这个过程就是远程过程调用。

大多数情况下，一般是服务员直接到厨房下单，然后后厨有一个人员分别把菜单分发给备菜师、切菜师和厨师。

这个过程就和计算机系统很像了。如今的大型网站都是分布式部署的。拿一个下单流程来说，可能涉及到物流、支付、库存、红包等多个系统后，而多个系统又是分别部署在不同的机器上的，分别由不同的团队负责。而要想实现下单流程，就需要用到远程调用。

```
下单{
    库存->减少库存
    支付->扣款
    红包->红包抵用
    物流->生成物流信息
}
```

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGZdmedsUhpwqn0Rzo0EUsREJIMuP04wMtKmeQ8u2zicnzeq3vGE6zm7w/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGz9HvNq4ysVgWwR65ZAZfASkaXttoSrQWIcHyRiaSVJxztI7CLKBibKsg/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### **到底什么是远程过程调用** 

RPC 是指计算机 A 上的进程，调用另外一台计算机 B 上的进程，其中 A 上的调用进程被挂起，而 B 上的被调用进程开始执行，当值返回给 A 时，A 进程继续执行。调用方可以通过使用参数将信息传送给被调用方，而后可以通过传回的结果得到信息。而这一过程，对于开发人员来说是透明的。

就像后厨的例子一样，服务员把菜单传给后厨，厨师告诉备菜师和洗菜师开始工作，然后他等待他们完成工作。备菜师和洗菜师工作完之后，厨师开始炒菜。这个过程对于服务员来说其实是透明的，他不需要关心到底后厨是怎么做菜的。

![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGFbVIibmy3bJnTJMztISQ37trxwn5rL12Vg25I0OH4Ttmc1QMOPDEGkA/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

￼

由于各服务部署在不同机器上，要想在服务间进行远程调用免不了网络通信过程，服务消费方每调用一个服务都要写一坨网络通信相关的代码，不仅复杂而且极易出错。

如果有一种方式能让我们像调用本地服务一样调用远程服务，而让调用者对网络通信这些细节透明，那么将大大提高生产力，比如服务消费方在执行`orderService.buy("HHKB键盘")`时，实质上调用的是远端的服务。这种方式其实就是RPC。而提供了这种功能的工具我们称之为RPC框架。

在RPC框架中主要有三个角色：Provider、Consumer和Registry。如下图所示：

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGblYfauY1dfPjdnIYEF1ibTiaqicrQOg4xqIsagbbIo1cAeicPCx4oRZvGQ/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

￼

Server: 暴露服务的服务提供方。 Client: 调用远程服务的服务消费方。 Registry: 服务注册与发现的注册中心。

服务提供方和服务消费方都比较好理解，就是后厨的洗菜师和厨师啦。厨师就是服务消费方，洗菜师就是服务提供方。厨师依赖洗菜师提供的服务。

服务注册中心又是个什么东西呢？

其实这个也比较好理解。对于那种很大的饭店来说，厨师可能有很多（集群部署），洗菜师也有很多（集群部署）。而厨师想要洗菜师帮忙洗菜的时候，他不会直接找某个洗菜师，而是通知一个中间人，这个人可能是洗菜师团队的领导，也可能就是一个专门协调后厨的人员。他知道整个厨房有多少洗菜师，也知道哪个洗菜师今天来上班了（需要先进行服务注册）。而且，他还可以根据各个洗菜师的忙碌情况动态分配任务（负载均衡）。

这个中间人就是服务注册中心。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGFPcIFHOYs7ue5I4fJsbAUiaOgc4hLebkLamN318VANc1YWOhMcjIL1w/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

￼

服务提供者启动后主动向注册中心注册机器ip、port以及提供的服务列表； 服务消费者启动时向注册中心获取服务提供方地址列表，可实现软负载均衡和Failover；

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGQAMafmV0LfYzHiaic2RfiaQBUeMj7vfV6fIdBjuvTriaaQHukGok3Pg3aA/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGIW410VNRGylgJAvL1GibpyjFxgVdc5ETu8QMFglR208torn7SL03gDA/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGYUA6hhzibgnf0V1nN5NCCMNyRT8OcIjF5icRUJNKYqibxic2BqmyD8YgicQ/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGYAT9popgw18HjV7vvCRylkarZLsxlqa4AzHbbgxb2G4xs61YLfS9Tg/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### **实现RPC需要用到的技术**

一个成熟的RPC框架需要考虑的问题有很多，这里只介绍实现一个远程调用需要用到的基本技术，感兴趣的朋友可以找一些开源的RPC框架代码来看下。

**动态代理**

生成 client stub和server stub需要用到Java 动态代理技术，我们可以使用JDK原生的动态代理机制，可以使用一些开源字节码工具框架 如：CgLib、Javassist等。

**序列化** 

为了能在网络上传输和接收 Java对象，我们需要对它进行序列化和反序列化操作。

可以使用Java原生的序列化机制，但是效率非常低，推荐使用一些开源的、成熟的序列化技术，例如：protobuf、Thrift、hessian、Kryo、Msgpack

**NIO**

当前很多RPC框架都直接基于netty这一IO通信框架，比如阿里巴巴的HSF、dubbo，Hadoop Avro，推荐使用Netty 作为底层通信框架。

**服务注册中心** 

可选技术： Redis、Zookeeper、Consul、Etcd

参考资料 ：https://www.jianshu.com/p/dbfac2b876b1

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGicQLT4ekkQlSJpvxhEUibK2N8ich4MoCB9qywQVKOUibPh2q97BYWMDJpQ/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQG3WVMDwV1pIa6QGVlMXMpSQvd1AUxhePZO43mLyx7foRou0o0EkEdHQ/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### **开源RPC框架**

**Dubbo**

Dubbo 是阿里巴巴公司开源的一个Java高性能优秀的服务框架，使得应用可通过高性能的 RPC 实现服务的输出和输入功能，可以和 Spring框架无缝集成。目前已经进入Apache孵化器。

**Motan**

Motan是新浪微博开源的一个Java RPC框架。2016年5月开源。Motan 在微博平台中已经广泛应用，每天为数百个服务完成近千亿次的调用。

**gRPC**

gRPC是Google开发的高性能、通用的开源RPC框架，其由Google主要面向移动应用开发并基于HTTP/2协议标准而设计，基于ProtoBuf(Protocol Buffers)序列化协议开发，且支持众多开发语言。本身它不是分布式的，所以要实现上面的框架的功能需要进一步的开发。

**thrift**

thrift是Apache的一个跨语言的高性能的服务框架，也得到了广泛的应用。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGibGxrJCgejicLWzYbPVcXa9ThURotfCs3amJibQPut9NsvpxqZq5XicneA/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGbwXDiciakGmVQgKgARnvYQod8oOlxpDd4fknFjGtTGoulibzX9z3Zq6Eg/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGRiaItZp7YqyeSbjELwjEftnK3DQFcotMWkkLhNicjUKficRJ35k2Aqtfg/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDI4AfgCOmJHtbBdwyibD6tQGF4SXPk55yWtlbE4AWibe0WN9NXmZxgudpXJNPJGicuxughbKyFX8Y59g/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)