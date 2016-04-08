### 渲染机制
- [S 一定要放在 Body 的最底部么？聊聊浏览器的渲染机制](https://mp.weixin.qq.com/s?__biz=MjM5NTEwMTAwNg==&mid=401857646&idx=1&sn=0b92213c90d442637793bb9e5154336b&scene=1&srcid=0120k4k2Wadk7V2iFwfR1jo3&key=710a5d99946419d9c2f8b73f80c52b8a5a6136f9c4b469c509fb35fe158a91a83862600c1861fb5e3314a0bb89c7f6ef&ascene=0&uin=MjgyNzQwMzY4MQ%3D%3D&devicetype=iMac+MacBookPro11%2C1+OSX+OSX+10.10+build(14A389)&version=11020201&pass_ticket=p%2FHgRlr%2Fr5y6oHHe1u%2BWwDfQZHu2K%2FwbsNmGZij8OfZjENKEA9WRG2O3Ndqp2IWh).
     js 的下载和执行会阻塞 Dom 树的构建（严谨地说是中断了 Dom 树的更新），所以 script 标签放在首屏范围内的HTML代码段里会截断首屏的内容。
     script 标签放在 body 底部，做与不做 async 或者 defer 处理，都不会影响首屏时间，但影响 DomContentLoad 和 load 的时间，进而影响依赖他们的代码的执行的开始时间
- [google WebFundamentals](https://github.com/google/WebFundamentals)
- [How browsers work](http://taligarsiel.com/Projects/howbrowserswork1.htm). 内容比较多
- [回流和重绘](http://www.blogjava.net/BearRui/archive/2010/05/10/320502.html)
- [What Every Frontend Developer Should Know About Webpage Rendering](http://frontendbabel.info/articles/webpage-rendering-101/)
     浏览器会对回流和重绘进行优化，尽量减少回流。但是如果访问标签属性，则会有一个强制的回流
- [Optimizing the Critical Rendering Path](http://www.sitepoint.com/optimizing-critical-rendering-path/) 介绍了渲染的关键路径.
- [what-happens-when-you-type-in-a-url-in-browser](http://stackoverflow.com/questions/2092527/what-happens-when-you-type-in-a-url-in-browser)
- [What is the complete process from entering a url to the browser's address bar to get the rendered page in browser?](http://stackoverflow.com/questions/5165310/what-is-the-complete-process-from-entering-a-url-to-the-browsers-address-bar-to)
- [describe-the-page-rendering-process-in-a-browser](http://stackoverflow.com/questions/7515227/describe-the-page-rendering-process-in-a-browser)
- [async-vs-defer-attributes](http://www.growingwiththeweb.com/2014/02/async-vs-defer-attributes.html) 没有这两个属性，则在解析html时下载然后执行js然后继续解析html,有async时，则在解析html时同时下载js，js下载后html解析暂停，同时执行js。有defer时，则在解析html时下载js，html解析完成后执行js。async不保证执行顺序，而defer则会保证。
- [script的defer和async](http://ued.ctrip.com/blog/script-defer-and-async.html)
- [Comparison_of_layout_engines_(Cascading_Style_Sheets)](https://en.wikipedia.org/wiki/Comparison_of_layout_engines_(Cascading_Style_Sheets))
- [script-injected-async-scripts-considered-harmful](https://www.igvita.com/2014/05/20/script-injected-async-scripts-considered-harmful/)
- [deciphering-the-critical-rendering-path](http://calendar.perfplanet.com/2012/deciphering-the-critical-rendering-path/)
- [css-paint-times](http://www.html5rocks.com/en/tutorials/speed/css-paint-times/)
- [understanding-the-critical-rendering-path-rendering-pages-in-1-second](https://medium.com/@luisvieira_gmr/understanding-the-critical-rendering-path-rendering-pages-in-1-second-735c6e45b47a#.5l6hbpfkt)