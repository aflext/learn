### 学习资料
- [https://github.com/dexteryy/spellbook-of-modern-webdev](https://github.com/dexteryy/spellbook-of-modern-webdev) 相当完全的前端的一切

### 基本概念
- [像素,浅谈移动Web开发（上）：深入概念](http://www.infoq.com/cn/articles/development-of-the-mobile-web-deep-concept)
- [Understanding JavaScript’s ‘undefined’](https://javascriptweblog.wordpress.com/2010/08/16/understanding-undefined-and-preventing-referenceerrors/)
    A variable Reference will never be unresolvable since the var keyword ensures a VariableObject is always assigned to the base value.
    A variable is not a variable until its declared.
    It’s true, identifiers which were never declared with the var keyword will get created as global variables – but only if they are the object of an assignment.
### 布局

### 网络

- [JavaScript之web通信](http://www.cnblogs.com/hustskyking/p/web-communication.html)
- [HTTP请求的TCP瓶颈分析](https://bhsc881114.github.io/2015/06/23/HTTP%E8%AF%B7%E6%B1%82%E7%9A%84TCP%E7%93%B6%E9%A2%88%E5%88%86%E6%9E%90/)
- [maximum-concurrent-connection-to-same](http://sgdev-blog.blogspot.jp/2014/01/maximum-concurrent-connection-to-same.html)
- [optimizing-http-keep-alive-and-pipelining](https://www.igvita.com/2011/10/04/optimizing-http-keep-alive-and-pipelining/)
- [https://hpbn.co/](https://hpbn.co/) 性能优化

### WebSocket.全双工通信，和http协议不同，握手链接采用http
- [WebSocket 是什么原理？为什么可以实现持久连接？](https://www.zhihu.com/question/20215561)
- [http://www.ruanyifeng.com/blog/2017/05/server-sent_events.html](http://www.ruanyifeng.com/blog/2017/05/server-sent_events.html)
- [http://caibaojian.com/http-connection-and-websocket.html](http://caibaojian.com/http-connection-and-websocket.html)
- [http://blog.zhangruipeng.me/2015/10/22/Web-Connectivity/](http://blog.zhangruipeng.me/2015/10/22/Web-Connectivity/)
- [http://www.ruanyifeng.com/blog/2017/05/websocket.html](http://www.ruanyifeng.com/blog/2017/05/websocket.html)
- [https://www.sitepoint.com/real-time-apps-websockets-server-sent-events/](https://www.sitepoint.com/real-time-apps-websockets-server-sent-events/)

### SPDY && HTTP2.优点一大堆
> HTTP/2 引入了二进制分帧层，将 HTTP/1.1 中的请求和响应拆成颗粒度更细的帧（frame），从而实现了优先级、流量控制和 Server Push 等功能；HTTP/2 在单条 TCP 连接上可以打开多个流，从而实现了多路复用；HTTP/2 使用静态字典、动态字典以及哈夫曼编码，对请求 / 响应头部进行压缩。总之，HTTP/2 从协议层面解决了 HTTP/1.1 的诸多问题。

- [Making The Web Faster With SPDY](http://blog.teamtreehouse.com/making-the-web-faster-with-spdy)
- [SPDY 是什么？如何部署 SPDY？](http://www.geekpark.net/topics/158198)
- [What is SPDY?](https://lincolnloop.com/blog/what-is-spdy/)
- [SPDY介绍 - wikipedia.org](http://javaarm.com/faces/display.xhtml;jsessionid=QYRt0P452bblKILPsbNo26LX?tid=3656&page=1&print=true)
- [SPDY-简介](https://chenhm.com/2014/10/spdy/)
- [SPDY协议 - v3](http://www.fireflysource.com/spdy/spdy-v3-cn.html)
- [https://www.smashingmagazine.com/2017/04/guide-http2-server-push/](https://www.smashingmagazine.com/2017/04/guide-http2-server-push/)
- [https://nickcraver.com/blog/2017/05/22/https-on-stack-overflow/](https://nickcraver.com/blog/2017/05/22/https-on-stack-overflow/)
- [http://www.alloyteam.com/2016/07/httphttp2-0spdyhttps-reading-this-is-enough/](http://www.alloyteam.com/2016/07/httphttp2-0spdyhttps-reading-this-is-enough/)
- [https://www.jianshu.com/p/933f8cf52f15](https://www.jianshu.com/p/933f8cf52f15)
- [https://imququ.com/post/header-compression-in-http2.html](https://imququ.com/post/header-compression-in-http2.html)
- [https://www.zhihu.com/question/34074946](https://www.zhihu.com/question/34074946)
- [https://www.mnot.net/talks/h2fe/](https://www.mnot.net/talks/h2fe/)
- [HTTP/2.0 相比1.0有哪些重大改进？ - victor yu的回答 - 知乎
https://www.zhihu.com/question/34074946/answer/108588042](https://www.zhihu.com/question/34074946/answer/108588042)
- [http://www.cnblogs.com/yingsmirk/p/5248506.html](http://www.cnblogs.com/yingsmirk/p/5248506.html)
- [https://http2.github.io/faq/](https://http2.github.io/faq/)

### server push
- [https://jakearchibald.com/2017/h2-push-tougher-than-i-thought/](https://jakearchibald.com/2017/h2-push-tougher-than-i-thought/)

### XMLHttpRequest2
- [XMLHttpRequest Level 2 使用指南](http://www.ruanyifeng.com/blog/2012/09/xmlhttprequest_level_2.html)
- [你真的会使用XMLHttpRequest吗？](https://segmentfault.com/a/1190000004322487)

### TCP
- [http://www.cnblogs.com/33debug/p/7060752.html](http://www.cnblogs.com/33debug/p/7060752.html)

### SGML
- [relation-and-differences-between-sgml-xml-html-and-xhtml](http://programmers.stackexchange.com/questions/93296/relation-and-differences-between-sgml-xml-html-and-xhtml)
- [any-reason-not-to-start-using-the-html-5-doctypes](http://stackoverflow.com/questions/5629/any-reason-not-to-start-using-the-html-5-doctype)
- [html5-is-html-and-xml](https://www.w3.org/blog/2008/01/html5-is-html-and-xml/)
- [前端开发面试题](https://github.com/markyun/My-blog/tree/master/Front-end-Developer-Questions/Questions-and-Answers) HTML5 为什么只需要写 <!DOCTYPE HTML>？HTML5 不基于 SGML，因此不需要对DTD进行引用，但是需要doctype来规范浏览器的行为（让浏览器按照它们应该的方式来运行）； 而HTML4.01基于SGML,所以需要对DTD进行引用，才能告知浏览器文档所使用的文档类型。

### SVG
- [svg-coordinate-systems](https://sarasoueidan.com/blog/svg-coordinate-systems/)
- [svg-transformations](https://sarasoueidan.com/blog/svg-transformations/)\

### debug
- [https://css-tricks.com/debugging-tips-tricks/](https://css-tricks.com/debugging-tips-tricks/)
