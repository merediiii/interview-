# 阿里、腾讯、百度、华为、京东、搜狗和滴滴最新面试题汇集

# 前言：

前一段时间和大牛们交流了一下，据反馈现在Android岗位也没有以前那么多了，没这么好找了，面临2016年寒冬季节，大量公司模仿O2O模式导致死掉企业的很多，在加之培训机构大量的培训人，导致供大于求，当然这不意味着饱和，只是市场更趋于合理一些（只要技术好不用怕的）。最近结合一些面试的同学和大牛们（张旭童）反馈，前几天听童哥去阿里面试顺便整理了下一些面试题目。希望对大家有所帮助，后期会不断更新添加新的面试题。可以帮大家查漏不缺。以下是（2016、2017 、阿里、腾讯、百度、华为、京东、搜狗和滴滴面试题汇集）
就算写出答案也没必要（我写了部分面试答案），因为开发与实际答案会有所不同，再者怕误导大家，所以这些面试题答案还是自己去理解吧！切记：不要背答案，多理解。

# 最新整理

1、简述synchronized?Object；Monitor机制；

2、简述happen-before规则；

3、JUC和Object；Monitor机制区别是什么；简述AQS原理；

4、简述DCL失效原因，解决方法；

5、简述nio原理；

6、jvm运行时数据区域有哪几部分组成，各自作用；

7、gc算法有哪些；gc收集器有哪些；

8、简述class加载各阶段过程；class；loader有哪些模型；

9、简述常用的JDK命令行工具；

10、简述字节码文件组成；

11、讲讲你平常是如何针对具体的SQL做优化；

12、mysql的存储引擎有哪些，区别；

13、gc:内存模型；

14、gc:垃圾回收；

15、多线程：如何实现一个定时调度和循环调度的工具类。但提交任务处理不过来的时候，拒绝机制应该如何处理；线程池默认有哪几种拒绝机制；

16、多线程：如何实现一个ThreadLocal；

17、说说你了解的一个线程安全队列；

18、Atomic包的实现原理是什么；

19、CAS又是怎么保证原子性的；

20、string分析1000次循环subString用了多少内存；

# Android基础

1、什么是ANR 如何避免它？

答：在Android 上，如果你的应用程序有一段时间响应不够灵敏，系统会向用户显示一个对话框，这个对话框称作应
用程序无响应（ANR：Application Not Responding）对话框。用户可以选择让程序继续运行，但是，他们在使用你的应用程序时，并不希望每次都要处理这个对话框。因此，在程序里对响应性能的设计很重要，这样，系统不会显示ANR 给用户。
不同的组件发生ANR 的时间不一样，主线程（Activity、Service）是5 秒，BroadCastReceiver 是10 秒。
解决方案：
将所有耗时操作，比如访问网络，Socket 通信，查询大量SQL 语句，复杂逻辑计算等都放在子线程中去，然后
通过handler.sendMessage、runonUITread、AsyncTask 等方式更新UI。无论如何都要确保用户界面操作的流畅度。
如果耗时操作需要让用户等待，那么可以在界面上显示进度条。

2、View的绘制流程；自定义View如何考虑机型适配；自定义View的事件分发机制；View和ViewGroup分别有哪些事件分发相关的回调方法；自定义View如何提供获取View属性的接口；

3、Art和Dalvik对比；虚拟机原理，如何自己设计一个虚拟机(内存管理，类加载，双亲委派)；JVM内存模型及类加载机制；内存对象的循环引用及避免；
ddms 和 traceView的区别；

4、内存回收机制与GC算法(各种算法的优缺点以及应用场景)；GC原理时机以及GC对象；内存泄露场景及解决方法；

5、四大组件及生命周期；ContentProvider的权限管理(读写分离，权限控制-精确到表级，URL控制)；Activity的四种启动模式对比；Activity状态保存于恢复；

6、什么是AIDL 以及如何使用；

7、请解释下在单线程模型中Message、Handler、Message Queue、Looper之间的关系；

8、Fragment生命周期；Fragment状态保存；

9、startActivityForResult是哪个类的方法，在什么情况下使用，如果在Adapter中使用应该如何解耦；

10、AsyncTask原理及不足；ntentService原理；

11、Activity 怎么和Service 绑定，怎么在Activity 中启动自己对应的Service；

12、请描述一下Service 的生命周期；

13、AstncTask+HttpClient与AsyncHttpClient有什么区别；

14、如何保证一个后台服务不被杀死；比较省电的方式是什么；

15、如何通过广播拦截和abort一条短信；广播是否可以请求网络；广播引起anr的时间限制；

16、进程间通信，AIDL；

17、事件分发中的onTouch 和onTouchEvent 有什么区别，又该如何使用？

18、说说ContentProvider、ContentResolver、ContentObserver 之间的关系；

19、请介绍下ContentProvider 是如何实现数据共享的；

20、Handler机制及底层实现；

21、Binder机制及底层实现；

22、ListView 中图片错位的问题是如何产生的；

23、在manifest 和代码中如何注册和使用BroadcastReceiver；

24、说说Activity、Intent、Service 是什么关系；

25、ApplicationContext和ActivityContext的区别；

26、一张Bitmap所占内存以及内存占用的计算；

27、Serializable 和Parcelable 的区别；

28、请描述一下BroadcastReceiver；

29、请描述一下Android 的事件分发机制；

30、请介绍一下NDK；

31、什么是NDK库，如何在jni中注册native函数，有几种注册方式；

32、AsyncTask 如何使用；

33、对于应用更新这块是如何做的？(灰度，强制更新，分区域更新)；

34、混合开发，RN，weex，H5，小程序(做Android的了解一些前端js等还是很有好处的)；

35、什么情况下会导致内存泄露；

36、如何对Android 应用进行性能分析以及优化；

37、说一款你认为当前比较火的应用并设计(直播APP)；

38、OOM的避免异常及解决方法；

39、屏幕适配的处理技巧都有哪些；

40、两个Activity 之间跳转时必然会执行的是哪几个方法？

答：一般情况下比如说有两个activity,分别叫A,B,当在A 里面激活B 组件的时候, A 会调用onPause()方法,然后B 调用onCreate() ,onStart(), onResume()。
这个时候B 覆盖了窗体, A 会调用onStop()方法. 如果B 是个透明的,或者是对话框的样式, 就不会调用A 的
onStop()方法。

# Java基础

1、集合类以及集合框架；HashMap与HashTable实现原理，线程安全性，hash冲突及处理算法；ConcurrentHashMap；

2、进程和线程的区别；

3、Java的并发、多线程、线程模型；

4、什么是线程池，如何使用? 

答：线程池就是事先将多个线程对象放到一个容器中，当使用的时候就不用new 线程而是直接去池中拿线程即可，节
省了开辟子线程的时间，提高的代码执行效率。

5、数据一致性如何保证；Synchronized关键字，类锁，方法锁，重入锁；

6、Java中实现多态的机制是什么；

7、如何将一个Java对象序列化到文件里；

8、说说你对Java反射的理解； 

答：Java 中的反射首先是能够获取到Java 中要反射类的字节码， 获取字节码有三种方法，
1.Class.forName(className) 2.类名.class 3.this.getClass()。然后将字节码中的方法，变量，构造函数等映射成相应的Method、Filed、Constructor 等类，这些类提供了丰富的方法可以被我们所使用。

9、同步的方法；多进程开发以及多进程应用场景；

10、在Java中wait和seelp方法的不同；

答：最大的不同是在等待时wait 会释放锁，而sleep 一直持有锁。wait 通常被用于线程间交互，sleep 通常被用于暂停执行。

11、synchronized 和volatile 关键字的作用；

答：
1）保证了不同线程对这个变量进行操作时的可见性，即一个线程修改了某个变量的值，这新值对其他线程来说是立即可见的。
2）禁止进行指令重排序。
volatile 本质是在告诉jvm 当前变量在寄存器（工作内存）中的值是不确定的，需要从主存中读取；
synchronized 则是锁定当前变量，只有当前线程可以访问该变量，其他线程被阻塞住。
1.volatile 仅能使用在变量级别；synchronized 则可以使用在变量、方法、和类级别的
2.volatile 仅能实现变量的修改可见性，并不能保证原子性；synchronized 则可以保证变量的修改可见性和原子性
3.volatile 不会造成线程的阻塞；synchronized 可能会造成线程的阻塞。
4.volatile 标记的变量不会被编译器优化；synchronized 标记的变量可以被编译器优化

13、服务器只提供数据接收接口，在多线程或多进程条件下，如何保证数据的有序到达；

14、ThreadLocal原理，实现及如何保证Local属性；

15、String StringBuilder StringBuffer对比；

16、你所知道的设计模式有哪些； 

答：Java 中一般认为有23 种设计模式，我们不需要所有的都会，但是其中常用的几种设计模式应该去掌握。下面列出了所有的设计模式。需要掌握的设计模式我单独列出来了，当然能掌握的越多越好。
总体来说设计模式分为三大类：
创建型模式，共五种：工厂方法模式、抽象工厂模式、单例模式、建造者模式、原型模式。
结构型模式，共七种：适配器模式、装饰器模式、代理模式、外观模式、桥接模式、组合模式、享元模式。
行为型模式，共十一种：策略模式、模板方法模式、观察者模式、迭代子模式、责任链模式、命令模式、备忘录模式、状态模式、访问者模式、中介者模式、解释器模式。

17、Java如何调用c、c++语言；

18、接口与回调；回调的原理；写一个回调demo；

19、泛型原理，举例说明；解析与分派；

20、抽象类与接口的区别；应用场景；抽象类是否可以没有方法和属性；

21、静态属性和静态方法是否可以被继承？是否可以被重写？以及原因？

22、修改对象A的equals方法的签名，那么使用HashMap存放这个对象实例的时候，会调用哪个equals方法；

23、说说你对泛型的了解；

24、Java的异常体系；

25、如何控制某个方法允许并发访问线程的个数；

26、动态代理的区别，什么场景使用；

# 数据结构与算法

1、堆和栈在内存中的区别是什么(数据结构方面以及实际实现方面)；

2、最快的排序算法是哪个？给阿里2万多名员工按年龄排序应该选择哪个算法？堆和树的区别；写出快排代码；链表逆序代码；

3、求1000以内的水仙花数以及40亿以内的水仙花数；

4、子串包含问题(KMP 算法)写代码实现；

5、万亿级别的两个URL文件A和B，如何求出A和B的差集C,(Bit映射->hash分组->多文件读写效率->磁盘寻址以及应用层面对寻址的优化)

6、蚁群算法与蒙特卡洛算法；

7、写出你所知道的排序算法及时空复杂度，稳定性；

8、百度POI中如何试下查找最近的商家功能(坐标镜像+R树)。

# 其他

1、死锁的四个必要条件；

2、常见编码方式；utf-8编码中的中文占几个字节；int型几个字节；

3、实现一个Json解析器(可以通过正则提高速度)；

4、MVC MVP MVVM; 常见的设计模式；写出观察者模式的代码；

5、TCP的3次握手和四次挥手；TCP与UDP的区别；

6、HTTP协议；HTTP1.0与2.0的区别；HTTP报文结构；

7、HTTP与HTTPS的区别以及如何实现安全性；

8、都使用过哪些框架、平台；

9、都使用过哪些自定义控件；

10、介绍你做过的哪些项目；

# 非技术问题汇总

1、研究比较深入的领域有哪些；

2、对业内信息的关注渠道有哪些；

3、最近都读哪些书；

4、自己最擅长的技术点，最感兴趣的技术领域和技术点；

5、项目中用了哪些开源库，如何避免因为引入开源库而导致的安全性和稳定性问题；

6、实习过程中做了什么，有什么产出；

7、5枚硬币，2正3反如何划分为两堆然后通过翻转让两堆中正面向上的硬币和反面向上的硬币个数相同；

8、时针走一圈，时针分针重合几次；

9、N * N的方格纸,里面有多少个正方形；

10、现在下载速度很慢,试从网络协议的角度分析原因,并优化(网络的5层都可以涉及)。

# HR问题汇总

1、您在前一家公司的离职原因是什么？

2、讲一件你印象最深的一件事情；

3、介绍一个你影响最深的项目；

4、介绍你最热爱最擅长的专业领域；

5、公司实习最大的收获是什么；

6、与上级意见不一致时，你将怎么办；

7、自己的优点和缺点是什么？并举例说明？

8、你的学习方法是什么样的？实习过程中如何学习？实习项目中遇到的最大困难是什么以及如何解决的；

9、说一件最能证明你能力的事情；

10、针对你你申请的这个职位，你认为你还欠缺什么；

11、如果通过这次面试我们单位录用了你，但工作一段时间却发现你根本不适合这个职位，你怎么办；

12、项目中遇到最大的困难是什么？如何解决的；

13、你的职业规划以及个人目标；未来发展路线及求职定位；

14、如果你在这次面试中没有被录用，你怎么打算；

15、评价下自己，评价下自己的技术水平，个人代码量如何；

16、通过哪些渠道了解的招聘信息，其他同学都投了哪些公司；

17、业余都有哪些爱好；

18、你做过的哪件事最令自己感到骄傲；

19、假如你晚上要去送一个出国的同学去机场，可单位临时有事非你办不可，你怎么办；

20、就你申请的这个职位，你认为你还欠缺什么；

21、当前的offer状况；如果BATH都给了offer该如何选；

22、你对一份工作更看重哪些方面？平台，技术，氛围，城市，money；

23、理想薪资范围；杭州岗和北京岗选哪个；

24、理想中的工作环境是什么；

25、谈谈你对跳槽的看法；

26、说说你对行业、技术发展趋势的看法；

27、实习过程中周围同事/同学有哪些值得学习的地方；

28、家人对你的工作期望及自己的工作期望；

29、如果你的工作出现失误，给本公司造成经济损失，你认为该怎么办；

30、若上司在公开会议上误会你了，该如何解决；

31、是否可以实习，可以实习多久；

32、在五年的时间内，你的职业规划；

33、你看中公司的什么？或者公司的那些方面最吸引你。
