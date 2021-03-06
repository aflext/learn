### dns轮训
- [DNS解析过程详解](http://blog.csdn.net/crazw/article/details/8986504)
 - 本机是否命中-isp缓存是否命中-13个根域名服务器-顶级域名服务器-权威域名服务器-ip
 - 根域，顶级域（包括通用顶级域和国家顶级域），顶级域权威服务器
- [dnsflow](http://myname.pchome.com.tw/learn/dnsflow.htm)
- [DNS原理及其解析过程精彩剖析](http://369369.blog.51cto.com/319630/812889)
 1. 在浏览器中输入www.qq.com域名，操作系统会先检查自己本地的hosts文件是否有这个网址映射关系，如果有，就先调用这个IP地址映射，完成域名解析。 
 2. 如果hosts里没有这个域名的映射，则查找本地DNS解析器缓存，是否有这个网址映射关系，如果有，直接返回，完成域名解析。 
 3. 如果hosts与本地DNS解析器缓存都没有相应的网址映射关系，首先会找TCP/ip参数中设置的首选DNS服务器，在此我们叫它本地DNS服务器，此服务器收到查询时，如果要查询的域名，包含在本地配置区域资源中，则返回解析结果给客户机，完成域名解析，此解析具有权威性。 
 4. 如果要查询的域名，不由本地DNS服务器区域解析，但该服务器已缓存了此网址映射关系，则调用这个IP地址映射，完成域名解析，此解析不具有权威性。 
 5. 如果本地DNS服务器本地区域文件与缓存解析都失效，则根据本地DNS服务器的设置（是否设置转发器）进行查询，如果未用转发模式，本地DNS就把请求发至13台根DNS，根DNS服务器收到请求后会判断这个域名(.com)是谁来授权管理，并会返回一个负责该顶级域名服务器的一个IP。本地DNS服务器收到IP信息后，将会联系负责.com域的这台服务器。这台负责.com域的服务器收到请求后，如果自己无法解析，它就会找一个管理.com域的下一级DNS服务器地址(qq.com)给本地DNS服务器。当本地DNS服务器收到这个地址后，就会找qq.com域服务器，重复上面的动作，进行查询，直至找到www.qq.com主机。 
 6. 如果用的是转发模式，此DNS服务器就会把请求转发至上一级DNS服务器，由上一级服务器进行解析，上一级服务器如果不能解析，或找根DNS或把转请求转至上上级，以此循环。不管是本地DNS服务器用是是转发，还是根提示，最后都是把结果返回给本地DNS服务器，由此DNS服务器再返回给客户机。
- [DNS 查询的工作原理](https://msdn.microsoft.com/zh-cn/library/cc775637(v=ws.10).aspx)
- [域名解析中A记录、CNAME、MX记录、NS记录的区别和联系](http://blog.csdn.net/crazw/article/details/8986581)
- [https://blog.cloudflare.com/how-we-made-our-dns-stack-3x-faster/](https://blog.cloudflare.com/how-we-made-our-dns-stack-3x-faster/)

### 学习资料
- [WebFundamentals](https://github.com/google/WebFundamentals)
- [前端只是规范](http://jixianqianduan.com/frontend-resource/2016/01/26/front-end-learning-list.html)
- [前端手册](http://www.frontendhandbook.com/index.html)
- [前端手册](https://dwqs.gitbooks.io/frontenddevhandbook/content/index.html)
- [Angular 2 versus React: There Will Be Blood](https://medium.freecodecamp.com/angular-2-versus-react-there-will-be-blood-66595faafd51#.vouqhe5rq)

### 域名劫持
- [https://techblog.toutiao.com/2017/05/09/cdn/](https://techblog.toutiao.com/2017/05/09/cdn/)

### dns 架构
- [https://githubengineering.com/dns-infrastructure-at-github/](https://githubengineering.com/dns-infrastructure-at-github/)
