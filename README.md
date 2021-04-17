### - I never saw a wild thing sorry for itself. A small bird will drop frozen dead from a bough, without ever having felt sorry for itself

  作为一个程序猿，其实一直并没有觉得github有什么特别的作用，但这个观点最近两年开始有了改变。  
  先是会有同事推荐，可以在GitHub上找找某些东西的样例代码，然后自己想找些书看看，就开始翻翻某些repository上的藏书推荐，直到现在第一次开始建自己的repository，想着把以前和以后遇到和研究过的东西都记一下，也可以自己经常复习复习。   

# 读过的书 

* 企业应用架构设计

# 不懂的问题   
* java 8和java 11的区别
* hystrix 熔断，重连算法
* restful 接口定义规范
* 本地通过docker打包调试
* 微服务的test case中怎么做外部服务的接口模拟
* 微服务中依赖的接口响应慢该如何解决
* json配置忽略null值
* rate limit(限流器)
  * [常见限流算法](https://blog.csdn.net/fuqianming/article/details/100532819) 
  * [hystrix原理](https://blog.csdn.net/loushuiyifan/article/details/82702522)
    * [Official guide](https://github.com/Netflix/Hystrix/wiki) 
  * Guava的RateLimiter
    * [基于RateLimiter与AOP实现api限流](https://www.cnblogs.com/chongaizhen/p/11125485.html) 
* [circuit breaker(断路器)](https://www.oschina.net/question/54100_2285459)
* cache 深入理解
* [Http与Https的区别](https://blog.csdn.net/xiaoming100001/article/details/81109617)
  
# java
* hashmap在并发环境下会遇到什么问题  
  [数据结构](https://blog.csdn.net/weixin_44460333/article/details/86770169)  
  [resize节点循环产生模拟](https://blog.csdn.net/paincupid/article/details/51241783)  
* concurrenthashmap是如何解决并发问题的，其内部数据结构是什么  
  [ConcurrentHashmap详解](https://blog.csdn.net/zzu_seu/article/details/106698150)这个问题太难了 
* 同步/异步
* 阻塞/非阻塞
* BIO/NIO/AIO
* [protected关键字详解](https://blog.csdn.net/chepwavege/article/details/7340998)  
* 自定义String类能否加载 -- 双亲委托机制(https://blog.csdn.net/xiongyouqiang/article/details/79151903)
* java自带的运行状况检测工具   
   [jvm性能检测工具](https://blog.csdn.net/qq_25825923/article/details/85074022)  
* 内存泄漏
  * [原因总结](https://blog.csdn.net/weter_drop/article/details/89387564) 
  * [可能原因与避免](https://blog.csdn.net/u012516166/article/details/77014910)
* [反射](https://blog.csdn.net/ye1714505125/article/details/108919425)
  * [类的加载机制](https://blog.csdn.net/justloveyou_/article/details/72217806)
# 多线程
* [线程基础](https://www.jianshu.com/p/d901b25e0d4a)
  * [线程操作](https://www.jianshu.com/p/f65ea68a4a7f) 
* [线程与进程的区别](https://blog.csdn.net/feiBlog/article/details/85397287)
* [java 线程池](https://www.jianshu.com/p/7726c70cdc40)  
  * [executor框架](https://blog.csdn.net/tongdanping/article/details/79604637)
  * [线程池工作原理](https://www.cnblogs.com/yanggb/p/10629387.html)      
* 死锁原因和基本解决思路  
  [参考资料1](https://www.jianshu.com/p/68c0fef7b63e)  
  [参考资料2](https://blog.csdn.net/wb_zjp283121/article/details/89673921)  
* [java内存模型](https://www.jianshu.com/p/d52fea0d6ba5)
* [volatile](https://zhuanlan.zhihu.com/p/138819184)
* [ReentrantLock](https://blog.csdn.net/fuyuwei2015/article/details/83719444)
  * [公平锁机制](https://blog.csdn.net/fuyuwei2015/article/details/83719444)
  * AQS 
* [synchronized](https://blog.csdn.net/hebtu666/article/details/103057476)
* [threadlocal](https://www.jianshu.com/p/3c5d7f09dfbd)
  * [应用场景1](https://blog.csdn.net/Lynn_coder/article/details/102492360)  
  * [应用场景2](https://zhuanlan.zhihu.com/p/82737256)  
* [CAS](https://www.jianshu.com/p/ab2c8fce878b)
  * [compareAndSwapInt()](https://blog.csdn.net/qq_29519041/article/details/100048114)  
* [AQS](https://www.jianshu.com/p/da9d051dcc3d)
* [CopyOnWrite](https://www.jianshu.com/p/afc6e0ae08b0)
* [Unsafe](https://blog.csdn.net/zmx729618/article/details/78528227)   
* [runnable和thread的区别](https://blog.csdn.net/u013755987/article/details/51855098)
* [悲观锁与乐观锁](https://blog.csdn.net/qq_34337272/article/details/81072874)
* [锁在内存中的位置--对象头](https://blog.csdn.net/weixin_39634900/article/details/110724757)
* 锁竞争升级
# mysql 
* 数据库单表的优化问题
参考链接  
[1，理论](https://blog.csdn.net/yjn1995/article/details/98472759)  
[2，例子 1](https://blog.csdn.net/liu1390910/article/details/96300318/)  
[3，例子 2](https://blog.csdn.net/qq_43162613/article/details/103774920)
  * 缩减表本身的大小
    * int类优化
    * 枚举或整型代替字符串
    * [字符串类型空间占用](https://blog.csdn.net/imzoer/article/details/8435540)  
    * timestamp代替datetime [参考链接](https://blog.csdn.net/qq_43792882/article/details/104491761)
    * 为什么要避免使用null   
    [参考链接1](https://www.jianshu.com/p/766ccd8d216e)  
    [在myisam中使用null](https://dev.mysql.com/doc/internals/en/myisam-introduction.html)  
    [在innodb中使用null](https://dev.mysql.com/doc/internals/en/innodb-field-contents.html)  
    [使用null的问题](https://dev.mysql.com/doc/refman/8.0/en/problems-with-null.html)  
    null会使索引变的复杂，增加一个索引字节， 但是null值查询也是可以走索引的
  * 索引优化
  	* 什么是聚簇索引，什么是非聚簇索引  
  	  [二者比较](https://blog.csdn.net/cacacai/article/details/83268678)  
      [数据结构比较](https://blog.csdn.net/ruanhao1203/article/details/98061034)  
      聚簇索引和非聚簇索引在innodb和myisam上的表现并不一样，在innodb里非聚簇索引项包含了主键
  	  * 非聚簇索引：普通索引，唯一索引，全文索引
  	  [唯一索引参考](https://blog.csdn.net/winy_lm/article/details/49718193)  
  	  唯一索引对应的列（或者多列）的值是唯一的
  	* 什么样的查询关键字会触发索引，什么样的不会  
  	  [参考资料1](https://www.jianshu.com/p/3ccca0444432)  
      [参考资料2](https://zhuanlan.zhihu.com/p/222122928)  
  	* 联合索引  
      [定义](https://www.jianshu.com/p/f65be52d5e2b)  
      [数据结构](https://blog.csdn.net/feichitianxia/article/details/107997795)   
    * explain 的用法  
    [1，理论](https://blog.csdn.net/why15732625998/article/details/80388236)  
    [2，key_len](https://blog.csdn.net/wll_1017/article/details/71179577)
  * 引擎优化  
      MyISAM和InnoDB的[区别](https://www.runoob.com/w3cnote/mysql-different-nnodb-myisam.html)
* [分库分表](https://blog.csdn.net/azhuyangjun/article/details/86976514)  
* [事务的实现原理](https://www.cnblogs.com/kismetv/p/10331633.html)
  * ACID -- undo log, redo log, 锁， MVCC 
* [mysql的四种隔离级别](https://www.cnblogs.com/jian-gao/p/10795407.html)
# spring boot 
* [依赖反转原则](https://zh.wikipedia.org/zh-hans/%E4%BE%9D%E8%B5%96%E5%8F%8D%E8%BD%AC%E5%8E%9F%E5%88%99)
  * [button & lamp例子](https://flylib.com/books/en/4.444.1.71/1/) 
* [启动流程解析](https://www.jianshu.com/p/87f101d8ec41)
* [@SpringBootApplication与run()](https://blog.csdn.net/weixin_38405253/article/details/90375003)  
* spring boot如何加载pom中的依赖
  * 寻找依赖中的spring.factories文件，在配置application时加载所需的factory，并在run时初始化对应的类
* spring 注解原理
  * [@Configuration](https://mp.weixin.qq.com/s/ScF8n-SRj8NHmuQdO8M97A) 
  * [元注解](https://blog.csdn.net/pengjunlee/article/details/79683621)
* 依赖冲突问题
# Spring Cloud

## Zuul
* 限流机制
## 缓存
# redis
* [常用场景](https://www.cnblogs.com/liuqingzheng/p/11080539.html)
* [db与缓存不一致问题](https://www.cnblogs.com/rjzheng/p/9041659.html)
* [内存不足时淘汰策略](https://blog.csdn.net/u014590757/article/details/79788076)
* [集群策略](https://blog.csdn.net/miss1181248983/article/details/90056960)
* [单线程内核处理并发请求 -- epoll](https://blog.csdn.net/songchuwang1868/article/details/89877739/)
* [缓存穿透，缓存击穿，缓存雪崩](https://blog.csdn.net/kongtiao5/article/details/82771694)
* [基础数据结构](https://www.runoob.com/redis/redis-data-types.html)
* 内部结构
  * dict
  * sds
  * quicklist
  * ziplist 
  * [skipList](https://www.cnblogs.com/xindoo/p/14020053.html) 
# MQ
* [为什么要使用MQ](https://www.jianshu.com/p/2820561158c4)
  * 解耦，异步，削峰 
* 常用MQ
  * 几种常见模式
  * 怎么解决消息丢失问题
* [RabbitMQ与Kafka对比](https://zhuanlan.zhihu.com/p/161224418)
## RabbitMQ
## ActiveMQ
* MQ的常见问题
  * 消息可靠传递(0丢失)
  * 消息传递幂等性
  * 消息积压问题
* [重复消费的原因和解决方式](https://www.cnblogs.com/zhixie/p/13444213.html)  
# 设计模式
* [设计模式分类](https://blog.csdn.net/FBB360JAVA/article/details/105796205)
* [23种设计模式简介](https://blog.csdn.net/weixin_34014555/article/details/89583679)
* 单例模式
* 观察者模式
* 建造者模式
* 代理模式
  * [java动态代理](https://blog.csdn.net/jiankunking/article/details/52143504)
  * [动态代理和静态代理的区别](https://blog.csdn.net/fangqun663775/article/details/78960545) 
  * 对于没有接口的类，spring使用[cglib代理](https://blog.csdn.net/qq_33661044/article/details/79767596)
* 命令模式
* 装饰模式
  * [java io看装饰模式和适配器模式](https://blog.csdn.net/philsonzhao/article/details/82188639)    
* 抽象工厂模式
* 其他需要掌握的模式
# GC
* [新生代老生代](https://www.cnblogs.com/E-star/p/5556188.html)
* [Minor GC + Major GC = Full GC](https://blog.csdn.net/u012988901/article/details/100630491)
* 各种GC的触发条件
* 如何判断内存是否需要回收
  * 引用计数
  * 可达性分析
    * GC Roots  
* [GC 算法](https://www.cnblogs.com/fangfuhai/p/7203468.html?utm_source=itdadao&utm_medium=referral)
  * 复制算法，标记清除算法，标记整理算法 
* [G1回收器](https://www.jianshu.com/p/aef0f4765098)
# Netty
* [零拷贝](https://mp.weixin.qq.com/s?__biz=Mzg2MjM1ODAyNQ==&mid=2247486558&idx=1&sn=9988d09238db763ac316ea9cdc93fc41&chksm=ce085338f97fda2e972a5b55956911dc184c2ffff8005576c7a1dca0fbe306e56e03be913214&token=940474257&lang=zh_CN#rd)  
# 数据结构
* 红黑树
  * [数据插入](https://zhuanlan.zhihu.com/p/79980618)
# 分布式
* [CAP](https://blog.csdn.net/qq_40180411/article/details/88413611)
  * spring cloud实现了[AP原则](https://blog.csdn.net/eson_15/article/details/85561179) 
