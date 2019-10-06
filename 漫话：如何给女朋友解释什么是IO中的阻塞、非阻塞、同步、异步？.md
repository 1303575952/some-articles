## 漫话：如何给女朋友解释什么是IO中的阻塞、非阻塞、同步、异步？

周末在家加班，正在疯狂的撸代码，女朋友很开心的跑过来，手里拿着他刚刚画好的一副漫画。

我刚刚画了一个很好看的漫画，能不能帮我做个网站把它上传到网上啊？



![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3jrwrt2Sia50KUib1Nicta9THqKSbibvKZC15d2ibHgujZpHO7UmFmgiaNdkQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)





做网站可难不倒我。漫画上传，你希望是同步的还是异步的啊？

![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3YdzC8cNDZh8p32YEIgpks99ic5r6c9LVsaL9kOe7p9zhHFto3fjYEPQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



啥同步异步的我不懂，同步吧。



![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3ApZhvZapxchW07NILBljuMAdtowzE914I12ulIdTdrxzQgJP7Z90KQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)





哦，那是阻塞的还是非阻塞的呢？

![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3YdzC8cNDZh8p32YEIgpks99ic5r6c9LVsaL9kOe7p9zhHFto3fjYEPQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



额、阻塞吧。



![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3Q6M53R5OLeWBjV9r3mhBvAGHfwKegEsDAPC1xVaHuhL9PicyjN51QtQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)





恭喜你，选择了一种最慢的方式。

![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3YdzC8cNDZh8p32YEIgpks99ic5r6c9LVsaL9kOe7p9zhHFto3fjYEPQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)





什么鬼嘛，你给我绕懵了，给我讲讲这都是啥意思。



![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3S3z5ncfL0M1JfSgM5oc6VJTibGicVlRvMnjrHFib81S97hDBCLrAVsbnQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



**同步、异步、阻塞、非阻塞都是和IO（输入输出）有关的概念。最简单的文件读取就是IO操作。而在文件读取这件事儿上，可以有多种方式。**

又拽概念了，你先给我说说啥叫同步、啥叫异步。



![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3vCB6zeSKFrxoBrhEDMiafLyG4vvDFAA0aDb45UCHicT4FhlibJWk6Ohibg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)





好吧，你去给我烧点水，泡杯咖啡我慢慢给你讲。

![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3YdzC8cNDZh8p32YEIgpks99ic5r6c9LVsaL9kOe7p9zhHFto3fjYEPQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



### **什么是同步和异步** 

说到烧水，我们都是通过热水壶来烧水的。在很久之前，科技还没有这么发达的时候，如果我们要烧水，需要把水壶放到火炉上，我们通过观察水壶内的水的沸腾程度来判断水有没有烧开。

随着科技的发展，现在市面上的水壶都有了提醒功能，当我们把水壶插电之后，水壶水烧开之后会通过声音提醒我们水开了。

对于烧水这件事儿来说，传统水壶的烧水就是同步的，高科技水壶的烧水就是异步的。

**同步请求**，A调用B，B的处理是同步的，在处理完之前他不会通知A，只有处理完之后才会明确的通知A。

**异步请求**，A调用B，B的处理是异步的，B在接到请求后先告诉A我已经接到请求了，然后异步去处理，处理完之后通过回调等方式再通知A。

所以说，同步和异步最大的区别就是被调用方的执行方式和返回时机。同步指的是被调用方做完事情之后再返回，异步指的是被调用方先返回，然后再做事情，做完之后再想办法通知调用方。

原来是这样啊，那阻塞和非阻塞呢？



![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3JWwQ1HUBkpImAk7MwuKib3Fc6CmYBxB60S8hwZLG8nxiaIySoTIusicibw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)





别急，听我慢慢和你说。

![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3YdzC8cNDZh8p32YEIgpks99ic5r6c9LVsaL9kOe7p9zhHFto3fjYEPQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



### **什么是阻塞和非阻塞** 

还是那个烧水的例子，当你把水放到水壶里面，按下开关后，你可以坐在水壶前面，别的事情什么都不做，一直等着水烧好。你还可以先去客厅看电视，等着水开就好了。

对于你来说，坐在水壶前面等就是阻塞的，去客厅看电视等着水开就是非阻塞的。

**阻塞请求**，A调用B，A一直等着B的返回，别的事情什么也不干。

**非阻塞请求**，A调用B，A不用一直等着B的返回，先去忙别的事情了。

所以说，同步和异步最大的区别就是在被调用方返回结果之前的这段时间内，调用方是否一直等待。阻塞指的是调用方一直等待别的事情什么都不做。非阻塞指的是调用方先去忙别的事情。

那阻塞和同步难道不是同一回事儿吗？



![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3JWwQ1HUBkpImAk7MwuKib3Fc6CmYBxB60S8hwZLG8nxiaIySoTIusicibw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)





当然不是啦。

![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3YdzC8cNDZh8p32YEIgpks99ic5r6c9LVsaL9kOe7p9zhHFto3fjYEPQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



### **阻塞、非阻塞和同步、异步的区别** 

首先，前面已经提到过，阻塞、非阻塞和同步、异步其实针对的对象是不一样的。阻塞、非阻塞说的是调用者，同步、异步说的是被调用者。

有人认为阻塞和同步是一回事儿，非阻塞和异步是一回事。但是这是不对的。

**先来看同步场景中是如何包含阻塞和非阻塞情况的。**

我们是用传统的水壶烧水。在水烧开之前我们一直做在水壶前面，等着水开。这就是阻塞的。

我们是用传统的水壶烧水。在水烧开之前我们先去客厅看电视了，但是水壶不会主动通知我们，需要我们时不时的去厨房看一下水有没有烧开。这就是非阻塞的。

**再来看异步场景中是如何包含阻塞和非阻塞情况的。**

我们是用带有提醒功能的水壶烧水。在水烧发出提醒之前我们一直做在水壶前面，等着水开。这就是阻塞的。

我们是用带有提醒功能的水壶烧水。在水烧发出提醒之前我们先去客厅看电视了，等水壶发出声音提醒我们。这就是非阻塞的。

奥，我明白了。阻塞非阻塞说的是我，同步异步说的是水壶。



![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3ApZhvZapxchW07NILBljuMAdtowzE914I12ulIdTdrxzQgJP7Z90KQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)





你可以简单的这么理解。

![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3YdzC8cNDZh8p32YEIgpks99ic5r6c9LVsaL9kOe7p9zhHFto3fjYEPQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



那我的网站我想选择异步非阻塞的形式。



![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3YdzC8cNDZh8p32YEIgpks99ic5r6c9LVsaL9kOe7p9zhHFto3fjYEPQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)





其实阻塞、非阻塞和同步、异步之间的组合并不是全都有的。

![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3YdzC8cNDZh8p32YEIgpks99ic5r6c9LVsaL9kOe7p9zhHFto3fjYEPQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



那都有那些呢？



![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3cL06LnT9UBBzwC676OnYs9xbTCe2FcJnjHUW4Tzjxt9kBaWDoIJBoA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



### **Java中的三种IO模型** 

在Java语言中，一共提供了三种IO模型，分别是阻塞IO（BIO）、非阻塞IO（NIO）、异步IO（AIO）。

这里面的BIO和NIO都是同步的IO模型，即同步阻塞IO和同步非阻塞IO，异步IO指的是异步非阻塞IO。

**BIO （Blocking I/O）**：同步阻塞I/O模式，数据的读取写入必须阻塞在一个线程内等待其完成。

**NIO （New I/O）**：同时支持阻塞与非阻塞模式，但主要是使用同步非阻塞IO。

**AIO （Asynchronous I/O）**：异步非阻塞I/O模型。

额、刚刚好像明白了，现在又不懂了。



![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3ApZhvZapxchW07NILBljuMAdtowzE914I12ulIdTdrxzQgJP7Z90KQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)





那我再拿烧水的例子给你解释一遍。

![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3YdzC8cNDZh8p32YEIgpks99ic5r6c9LVsaL9kOe7p9zhHFto3fjYEPQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



**BIO （Blocking I/O）**：有一排水壶在烧开水，BIO的工作模式就是，叫一个线程停留在一个水壶那，直到这个水壶烧开，才去处理下一个水壶。但是实际上线程在等待水壶烧开的时间段什么都没有做。

**NIO （New I/O）**：NIO的做法是叫一个线程不断的轮询每个水壶的状态，看看是否有水壶的状态发生了改变，从而进行下一步的操作。

**AIO （ Asynchronous I/O**）：为每个水壶上面装了一个开关，水烧开之后，水壶会自动通知我水烧开了。

奥，你就说烧水我就明白了。



![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3YdzC8cNDZh8p32YEIgpks99ic5r6c9LVsaL9kOe7p9zhHFto3fjYEPQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)





嗯，这就是Java中的三种IO模型。

![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3YdzC8cNDZh8p32YEIgpks99ic5r6c9LVsaL9kOe7p9zhHFto3fjYEPQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



Java好厉害啊，自己都能实现这些IO组合。



![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3wD5hQyKHhlpcADQz6ZVURb7ce3MpbTxGIiaBbia0Qic1uPVojX4wH6eIw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)





也不是啦，Java中的IO还是借助操作系统的IO模型的，只不过是对操作系统IO模型的封装而已啦。

![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3YdzC8cNDZh8p32YEIgpks99ic5r6c9LVsaL9kOe7p9zhHFto3fjYEPQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



那你再给我讲讲操作系统的IO模型吧。



![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3ApZhvZapxchW07NILBljuMAdtowzE914I12ulIdTdrxzQgJP7Z90KQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



滴滴滴滴，这时候水壶响了，打断了女朋友的发问。女朋友去拿来烧好的热水，给我泡了一杯咖啡。

诺，给你咖啡，我选好了，你就用AIO给我实现个漫画上传的网站吧。我晚上就要用。



![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3wD5hQyKHhlpcADQz6ZVURb7ce3MpbTxGIiaBbia0Qic1uPVojX4wH6eIw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)





额…

![img](https://mmbiz.qpic.cn/mmbiz_png/mQlO20PgUDLkwae79LDHHhLVfOadSbN3aeEhz2nkkClOmpPc8I88OBKJTjsYJMhzClILq3oOQj4jEEicbceDnyg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)