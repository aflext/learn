### 综述
> Appcache是有问题的，全量更新
- 即使在线，文件总是从 AppCache 中来
- 只有 Manifest 变化时文件才会更新，一旦变化总会更新所有文件
- 不支持 conditional download，破坏响应式设计
- 失败的 fallback 页面，无法区分网络错误和状态码
- 重定向被处理为访问失败

> 权限问题、生命周期（浏览器支持？）、https only ？
- 关掉浏览器、关掉页面的情况
  - [https://stackoverflow.com/a/39208140/1468517](https://stackoverflow.com/a/39208140/1468517)
  - [https://stackoverflow.com/a/20105455/1468517](https://stackoverflow.com/a/20105455/1468517)
- 缓存大小限制
- 浏览器支持
- 生产环节

> 与WebWorker、浏览器线程的关系，底层细节的实现？
> PWA相关

### 基本链接
- [https://developer.mozilla.org/zh-CN/docs/Web/API/Service_Worker_API](https://developer.mozilla.org/zh-CN/docs/Web/API/Service_Worker_API)
- [http://imweb.io/topic/56592b8a823633e31839fc01](http://imweb.io/topic/56592b8a823633e31839fc01)
- [http://www.alloyteam.com/2016/01/9274/](http://www.alloyteam.com/2016/01/9274/)
- [https://developers.google.cn/web/fundamentals/getting-started/primers/service-workers?hl=zh-cn](https://developers.google.cn/web/fundamentals/getting-started/primers/service-workers?hl=zh-cn)
- [http://harttle.com/2017/04/09/service-worker-now.html](http://harttle.com/2017/04/09/service-worker-now.html)
- [https://x5.tencent.com/tbs/guide/serviceworker.html](https://x5.tencent.com/tbs/guide/serviceworker.html)
- [http://zhenhua-lee.github.io/http/service-worker.html](http://zhenhua-lee.github.io/http/service-worker.html)