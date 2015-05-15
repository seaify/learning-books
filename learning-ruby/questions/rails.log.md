# 现象
rails 对于每一次请求，记录了下列信息:
* url，method，访问ip，访问时间，以及携带的参数
* 其给出了处理该请求的controller#function, 使得新人查bug时，能直接定位，不用查找代码去找到底是在哪儿被处理的。
* 对于涉及到sql语句的，会给出其生成的raw的sql语句，方便定位我们使用model方法是否正确, sql语句是否存在性能问题，如索引用的方法有误
* 给出了状态返回码，总耗费时间, view 和 activerecord分别花费了多少时间，方便性能调优

![如图](../images/http.log.png)

## 问题

rails是如何来实现它的呢？我们自己写的controller里并没有一行代码和它有关。

## 代码篇
1. 默认情况下，我们通过rails generate controller hello index这种模式生成的controller类，都继承了ApplicationController， ApplicationController又继承了ActionController::Base，所以直接看它的源码。
```ruby
```

## 相应参考资料
[lograge](https://github.com/roidrage/lograge), 方便的允许你去修改rails默认的logging输出, 如改成单行，方便grep，方便zabbix等收集信息  
[how-to-log-specific-request-details-to-rails-server-logs](http://stackoverflow.com/questions/11267540/how-to-log-specific-request-details-to-rails-server-logs), stackoverflow上，关于怎样输出更多信息，如useragent等的信息到日志中的问题  
[on-notifications-logsubscribers-and-bringing-sanity-to-rails-logging](http://www.paperplanes.de/2012/3/14/on-notifications-logsubscribers-and-bringing-sanity-to-rails-logging.html), 介绍了rails的logger机制  