### keep-alive && pipelining。keep-alive减少慢启动的消耗，而pipelining则优化了请求-响应的模式为并行请求-并行响应(遵循先进先出-SPDY解决了这个原则)
- [keep-alive-header-clarification](http://stackoverflow.com/questions/20592698/keep-alive-header-clarification)
- [http-keep-alive-header](https://www.byvoid.com/blog/http-keep-alive-header)
- [optimizing-http-keep-alive-and-pipelining](https://www.igvita.com/2011/10/04/optimizing-http-keep-alive-and-pipelining/)
- [Increasing Application Performance with HTTP Cache Headers](https://devcenter.heroku.com/articles/increasing-application-performance-with-http-cache-headers)


### 浏览器缓存

#### Etag 主要为了解决 Last-Modified 无法解决的一些问题：
- 一些文件也许会周期性的更改，但是他的内容并不改变(仅仅改变的修改时间)，这个时候我们并不希望客户端认为这个文件被修改了，而重新GET；
- 某些文件修改非常频繁，比如在秒以下的时间内进行修改，(比方说1s内修改了N次)，If-Modified-Since能检查到的粒度是s级的，这种修改无法判断(或者说UNIX记录MTIME只能精确到秒)；
- 某些服务器不能精确的得到文件的最后修改时间。
    Last-Modified与ETag是可以一起使用的，服务器会优先验证ETag，一致的情况下，才会继续比对Last-Modified，最后才决定是否返回304。Cache-Control/Expires则不同，如果检测到本地的缓存还是有效的时间范围内，浏览器直接使用本地副本，不会发送任何请求。两者一起使用时，Cache-Control/Expires的优先级要高于Last-Modified/ETag。即当本地副本根据Cache-Control/Expires发现还在有效期内时，则不会再次发送请求去服务器询问修改时间（Last-Modified）或实体标识（Etag）了。一个是强验证，一个是弱验证。
- 如果是负载均衡apache的场景中，应该配置apache关掉etag，因为etag和文件的inode相关，而不同的服务器inode不一定相同。或者配置apache不使用inode去计算etag

#### 相关链接
- [浏览器缓存策略](http://imweb.io/topic/55c6f9bac222e3af6ce235b9)
     如果设了max-age，max-age就会覆盖expires
     Last-Modified与If-Modified-Since是一对报文头，属于http 1.0。
     ETag与If-None-Match是一对报文，属于http 1.1。

- [浏览器三种刷新的区别](https://cnodejs.org/topic/4f43614e6ade5ec0780003c3)
- [在浏览器地址栏按回车、F5、Ctrl+F5刷新网页的区别](http://blog.csdn.net/yui/article/details/6584401)
- [浏览器缓存机制](http://www.cnblogs.com/skynet/archive/2012/11/28/2792503.html)
- [【Web缓存机制系列】2 – Web浏览器的缓存机制](http://www.alloyteam.com/2012/03/web-cache-2-browser-cache/)
- [A Beginner's Guide to HTTP Cache Headers](http://www.mobify.com/blog/beginners-guide-to-http-cache-headers/)
- [ETag vs Header Expires](http://stackoverflow.com/questions/499966/etag-vs-header-expires)
- [Increasing Application Performance with HTTP Cache Headers](https://devcenter.heroku.com/articles/increasing-application-performance-with-http-cache-headers)
