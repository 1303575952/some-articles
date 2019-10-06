## 漫话：如何给女朋友解释什么是DDoS攻击

周五下班比较早，我正在家里面玩吃鸡游戏，正在疯狂的跑毒，这时候坐在旁边刷着抖音的女朋友问了我一个奇怪的问题。



![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0dDxKI9PQ9vic0FiaEIdB1WARauGOKEJdzk8sUpFEgHGqBGUbx6C114laQ/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0dCy7HLP9Xr7ibsQGxRbBO1xdCRY7cnOtwPO5dwqTiayVo1dqFSoAauR2A/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0d0VvmZKJkb6Qwd3GAyPMtYJibV1raQU19klUasylI1sXfl5hGlruZ9FA/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0dlmpOubwK2JXhzTKJv6sl99ceULg7oU92YNEqg1EZdwXdUnovHhT2JQ/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**分布式拒绝服务(DDoS：Distributed Denial of Service)攻击，是指攻击者利用大量“肉鸡”对攻击目标发动大量的正常或非正常请求、耗尽目标主机资源或网络资源，从而使被攻击的主机不能为正常用户提供服务。**

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0dWXdLHJiaqMDBnaSJuibeXicNPooqwEagSUuTAWXYYfReUev8zwFYHzFmA/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0dMO2RCNa5Qb9q3XfyiaiaD9MpM7IPZJwvrT0KCibdK7BeCibMReylFQibHQA/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### **DoS**



在介绍DDoS之前，需要先简单介绍一下什么是DoS。

DoS（拒绝服务，Denial of Service）就是利用合理的服务请求来占用过多的服务资源，从而使合法用户无法得到服务的响应。这是早期非常基本的网络攻击方式。

举一个简单的例子，小王开了一家商店，店面不大，加上小王一共有三个服务员。由于他们这里物美价廉，工作人员的态度又比较友善，所以慢慢的生意越来越好。

但是，这家店所在的小镇上有一个恶霸，恶霸看到小王的店很赚钱，想要通过一些下作的手段谋取私利。于是他装扮成普通的顾客，在小王的店里有一搭无一搭的总和店员攀谈，问问这个多少钱，问问那个怎么卖，还时不时的给店员提供一些虚假信息，比如哪里缺货了之类的信息。使店员们都被他搞的团团转。

由于恶霸是装作普通顾客的，小王和店员们又不能彻底不理他，所以就要分出一些精力来服务他，但是由于店内的服务员有限。这样一来，很多其他的顾客就可能受到了冷落。

对于网站来说，其实也是一样的，网站就像是小王的商店一样。对于一个网站来说，他是要搭建在服务器上面的，而由于硬件资源有限，所以服务能力也是有限的。如果有人频繁访问或者长时间占用资源，就会导致其他用户的体验有所下降。

这种，利用合理的服务请求来占用过多的服务资源，从而使合法用户无法得到服务的响应的行为，就是DoS攻击。

在信息安全的三要素——**保密性**、**完整性**和**可用性**中，DoS针对的目标正是**可用性**。该攻击方式利用目标系统网络服务功能缺陷或者直接消耗其系统资源，使得该目标系统无法提供正常的服务。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0dkfHWUjFBd5vBvb01ETQyQoGjGyvCn0cmMrEYnmD9sPvSaepEqq05Uw/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0dw8qmiaZvq44a45adHzjk8xvawDibiciaMRMlTgobEs8ZJtqTGVkc7Jzj7A/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### **DDoS**

如果只是一个恶霸的话，只要能够识别出来，然后阻止他进入店铺就行了。

随着恶霸被发现之后，他也想了一个办法，这次他不再自己一个人跑去店里捣乱了，而是纠集了一群无赖，而这些无赖每天都换，店铺里面的服务员根本识别不出来到底谁是恶霸派来的。

无赖们扮作普通客户一直拥挤在商场，赖着不走，真正的购物者却无法进入；或者总是和营业员有一搭没一搭的东扯西扯，让工作人员不能正常服务客户；也可以为商铺的经营者提供虚假信息，商铺的上上下下忙成一团之后却发现都是一场空，最终跑了真正的大客户，损失惨重。一个无赖去胡闹，就是 DoS攻击，而一群无赖去胡闹，就是 DDoS攻击。

![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0dpqSAVP5Ece9swpVMrjb1fSTVY99tOF1MVxmAia8XnA65miaPEvmyE6gg/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

￼

一般来说，DDoS 攻击可以具体分成两种形式：带宽消耗型以及资源消耗型。它们都是透过大量合法或伪造的请求占用大量网络以及器材资源，以达到瘫痪网络以及系统的目的。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0dJ2fnSehsOZn0RtCk9y93DqbshK1zdnpic5kxoTibIL5De2iaZ6q0JGEMw/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0d9nNZpATBspeg6FnKzYR5533hHS3E14EaanicdHUM77YBRTPMQw5Wolw/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0d184jwu6A13XsDUBRXpV1pnmvx8GicAvQBRU5KapwUXGJgmnqurvVQvw/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0dV3bIvxHek1rql4VAZ8agR1YpxVibD1Y6xEsmpNqqicB9uI0EEY92d7Hw/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### **DDoS的危害**

当服务器被DDos攻击时，一般会出现以下现象：

被攻击主机上有大量等待的TCP连接；

 网络中充斥着大量的无用的数据包； 

受害主机无法正常和外界通讯； 

受害主机无法处理所有正常请求；严重时会造成系统死机。 

对于用户来说，在常见的现象就是网站无法访问。



![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0dXyteXLYdrBeTMy5iakPS3TaSUf4W8v0liar1pjeRnWVicicqvmfw8Tl2WQ/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0dibvKLqOqiaoOOQ34icgQ8a9AAXaG4drK2G3fFvoEfxVK87pjR2DZehtIA/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0dXUZMyNbibZTDZXibdPLUqVQ7PqhS1fK7lON8rFZosgoZDaeTa1vXq2dw/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0dfa2pnWCKYp3P6MEttBWOaeuOgJlmaAS9sAqgfnZVqMcAlziaAluLJPQ/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0dC2c1PkFNW9CjQPJDiahl1tj6KyOmFwV7v4BicXIdm9vicPtzqBNCsDSzA/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### **DDoS的防范**

为了对抗 DDoS攻击，你需要对攻击时发生了什么有一个清楚的理解。简单来讲，DDoS 攻击可以通过利用服务器上的漏洞，或者消耗服务器上的资源(例如 内存、硬盘等等)来达到目的。

一般来说，可以用以下办法防范：

1、如果可以识别出攻击源，如机器IP等，可以在防火墙服务器上放置一份 ACL（访问控制列表) 来阻断这些来自这些 IP 的访问。

2、对于带宽消耗型攻击，最有效的办法那就是增加带宽。

3、提高服务器的服务能力，增加负载均衡，多地部署等。

4、优化资源使用提高 web server 的负载能力。例如，使用 apache 可以安装 apachebooster 插件，该插件与 varnish 和 nginx 集成，可以应对突增的流量和内存占用。

5、使用高可扩展性的 DNS 设备来保护针对 DNS 的 DDOS 攻击。可以考虑购买 Cloudfair 的商业解决方案，它可以提供针对 DNS 或 TCP/IP3 到7层的 DDOS 攻击保护。

6、启用路由器或防火墙的反IP欺骗功能。

7、付费，使用第三方的服务来保护你的网站。

8、监控网络和 web 的流量。时刻观察流量变化

9、保护好 DNS 避免 DNS 放大攻击。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0dffiaWukdkbib7MOGPVr6k3Oxj8u3mMibecLibtFbjNCdSJExmxuXhRHN6w/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0dYI8ic8A6fjjbwBic1Sj0WeaE2vFw4cPRSiaxOQef1lWwx0o7hOrLkozPw/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0dHzYPXe62P4oTT0QAJIwOwGTOnCwTzW61SDMEm1Vj1twfFHSEXzKLdA/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/mQlO20PgUDL8kN66ICm5ZoYrvurf4ib0dLUTrluKJ3nAxPCAlQZRToDaSWz5gdw5GkxzHfYAdgfsiaYIcsdicUGjA/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

对于网络攻击，没有任何办法彻底阻止和避免 ，只能尽最大努力不断提高黑客攻击成本。