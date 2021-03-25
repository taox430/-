### - I never saw a wild thing sorry for itself. A small bird will drop frozen dead from a bough, without ever having felt sorry for itself
谨记：不论到了哪里，都不能忘了学习和进步

  作为一个程序猿，其实一直并没有觉得github有什么特别的作用，但这个观点最近两年开始有了改变。  
  先是会有同事推荐，可以在GitHub上找找某些东西的样例代码，然后自己想找些书看看，就开始翻翻某些repository上的藏书推荐，直到现在第一次开始建自己的repository，想着把以前和以后遇到和研究过的东西都记一下，也可以自己经常复习复习。  
  不知道能坚持多久，但愿可以一直做下去  

# 读过的书 

* 企业应用架构设计

# 不懂的问题 

* hashmap在并发环境下会遇到什么问题
* concurrenthashmap是如何解决并发问题的，其内部数据结构是什么
* spring boot是如何加载额外的依赖的
* 查询性能问题如何优化
* 自定义String类能否加载 -- 双亲委托机制
* 数据库单表的优化问题
参考链接  
[1，理论](https://blog.csdn.net/yjn1995/article/details/98472759)  
[2，例子 1](https://blog.csdn.net/liu1390910/article/details/96300318/)  
[3，例子 2](https://blog.csdn.net/qq_43162613/article/details/103774920)
  * 缩减表本身的大小
    * int类优化
    * 枚举或整型代替字符串
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
  	  [参考资料](https://www.jianshu.com/p/3ccca0444432)  
  	* 联合索引  
      [定义](https://www.jianshu.com/p/f65be52d5e2b)  
      [数据结构](https://blog.csdn.net/feichitianxia/article/details/107997795)   
* explain 的用法  
[1，理论](https://blog.csdn.net/why15732625998/article/details/80388236)  
* java 8和java 11的区别
  
* mysql的四种隔离级别
* MyISAM和InnoDB的区别
# java

# mysql 

# spring boot 

# MQ
## RabbitMQ
## ActiveMQ
