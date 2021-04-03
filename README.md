### - I never saw a wild thing sorry for itself. A small bird will drop frozen dead from a bough, without ever having felt sorry for itself
谨记：不论到了哪里，都不能忘了学习和进步

  作为一个程序猿，其实一直并没有觉得github有什么特别的作用，但这个观点最近两年开始有了改变。  
  先是会有同事推荐，可以在GitHub上找找某些东西的样例代码，然后自己想找些书看看，就开始翻翻某些repository上的藏书推荐，直到现在第一次开始建自己的repository，想着把以前和以后遇到和研究过的东西都记一下，也可以自己经常复习复习。  
  不知道能坚持多久，但愿可以一直做下去  

# 读过的书 

* 企业应用架构设计

# 不懂的问题  
* java自带的运行状况检测工具
   [jvm性能检测工具](https://blog.csdn.net/qq_25825923/article/details/85074022)  
* 自定义String类能否加载 -- 双亲委托机制(https://blog.csdn.net/xiongyouqiang/article/details/79151903)
* java 8和java 11的区别
* [mysql的四种隔离级别](https://www.cnblogs.com/jian-gao/p/10795407.html)
  
# java
* hashmap在并发环境下会遇到什么问题  
  [数据结构](https://blog.csdn.net/weixin_44460333/article/details/86770169)  
  [resize节点循环产生模拟](https://blog.csdn.net/paincupid/article/details/51241783)  
* concurrenthashmap是如何解决并发问题的，其内部数据结构是什么  
  [ConcurrentHashmap详解](https://blog.csdn.net/zzu_seu/article/details/106698150)这个问题太难了 
* 同步/异步
* 阻塞/非阻塞
* BIO/NIO/AIO
# 多线程
* [线程基础](https://www.jianshu.com/p/d901b25e0d4a)
  * [线程操作](https://www.jianshu.com/p/f65ea68a4a7f) 
* [线程与进程的区别](https://blog.csdn.net/feiBlog/article/details/85397287)
* [java 线程池](https://www.jianshu.com/p/7726c70cdc40)  
  * [executor框架](https://blog.csdn.net/tongdanping/article/details/79604637)   
* 死锁原因和基本解决思路  
  [参考资料1](https://www.jianshu.com/p/68c0fef7b63e)  
  [参考资料2](https://blog.csdn.net/wb_zjp283121/article/details/89673921)  
* [java内存模型](https://www.jianshu.com/p/d52fea0d6ba5)
* [volatile](https://zhuanlan.zhihu.com/p/138819184)
* ReentrantLock
* [synchronized](https://blog.csdn.net/hebtu666/article/details/103057476)
* [threadlocal](https://www.jianshu.com/p/3c5d7f09dfbd)
  * [应用场景1](https://blog.csdn.net/Lynn_coder/article/details/102492360)  
  * [应用场景2](https://zhuanlan.zhihu.com/p/82737256)  
* [CAS](https://www.jianshu.com/p/ab2c8fce878b)
  * [compareAndSwapInt()](https://blog.csdn.net/qq_29519041/article/details/100048114)  
* [Unsafe](https://blog.csdn.net/zmx729618/article/details/78528227)   
* [runnable和thread的区别](https://blog.csdn.net/u013755987/article/details/51855098)
* [悲观锁与乐观锁](https://blog.csdn.net/qq_34337272/article/details/81072874)
* [锁在内存中的位置--对象头](https://blog.csdn.net/weixin_39634900/article/details/110724757)
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
## 缓存
# redis
# MQ
## RabbitMQ
## ActiveMQ
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
* 抽象工厂模式
* 其他需要掌握的模式
# GC
