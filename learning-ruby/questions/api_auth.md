## 简介
web端直接使用默认的devise登录就可以了，而ios，android这种api模式的需要其它的认证方法，网络上看到最多的就是基于token的


## 参考资料
1. [devise 3.1移除Token Authenticatable](http://blog.plataformatec.com.br/2013/08/devise-3-1-now-with-more-secure-defaults/), 注意只是devise把之前的实现TokenAuthenticatable移除了，但并不是对基于token的认证方式的不认可