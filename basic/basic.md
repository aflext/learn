### 基本概念
- [像素,浅谈移动Web开发（上）：深入概念](http://www.infoq.com/cn/articles/development-of-the-mobile-web-deep-concept)

### 布局
- [回流和重绘](http://www.blogjava.net/BearRui/archive/2010/05/10/320502.html)

### 网络

- [JavaScript之web通信](http://www.cnblogs.com/hustskyking/p/web-communication.html)
- [HTTP请求的TCP瓶颈分析](https://bhsc881114.github.io/2015/06/23/HTTP%E8%AF%B7%E6%B1%82%E7%9A%84TCP%E7%93%B6%E9%A2%88%E5%88%86%E6%9E%90/)

### WebSocket.全双工通信，和http协议不同，握手链接采用http
- [WebSocket 是什么原理？为什么可以实现持久连接？](https://www.zhihu.com/question/20215561)

### SPDY && HTTP2.优点一大堆
- [Making The Web Faster With SPDY](http://blog.teamtreehouse.com/making-the-web-faster-with-spdy)
- [SPDY 是什么？如何部署 SPDY？](http://www.geekpark.net/topics/158198)
- [What is SPDY?](https://lincolnloop.com/blog/what-is-spdy/)
- [SPDY介绍 - wikipedia.org](http://javaarm.com/faces/display.xhtml;jsessionid=QYRt0P452bblKILPsbNo26LX?tid=3656&page=1&print=true)
- [SPDY-简介](https://chenhm.com/2014/10/spdy/)
- [SPDY协议 - v3](http://www.fireflysource.com/spdy/spdy-v3-cn.html)

### keep-alive && pipelining。keep-alive减少慢启动的消耗，而pipelining则优化了请求-响应的模式为并行请求-并行响应(遵循先进先出-SPDY解决了这个原则)
- [keep-alive-header-clarification](http://stackoverflow.com/questions/20592698/keep-alive-header-clarification)
- [http-keep-alive-header](https://www.byvoid.com/blog/http-keep-alive-header)
- [optimizing-http-keep-alive-and-pipelining](https://www.igvita.com/2011/10/04/optimizing-http-keep-alive-and-pipelining/)

### bigPipe.页面分子模块加载和优化
- [Facebook创新之BigPipe：优化页面加载时间](http://www.infoq.com/cn/news/2010/08/bigpipe-facebook-optimize)
- [BigPipe: Pipelining web pages for high performance](https://www.facebook.com/notes/facebook-engineering/bigpipe-pipelining-web-pages-for-high-performance/389414033919/)
- [BigPipe学习研究](http://www.searchtb.com/2011/04/an-introduction-to-bigpipe.html)