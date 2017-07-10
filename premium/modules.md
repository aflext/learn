### Events
- [Events and timing in-depth](http://javascript.info/tutorial/events-and-timing-depth)
- [循环依赖](http://www.ruanyifeng.com/blog/2015/11/circular-dependency.html)
 - CommonJS模块的重要特性是加载时执行，即脚本代码在require的时候，就会全部执行。CommonJS的做法是，一旦出现某个模块被"循环加载"，就只输出已经执行的部分，还未执行的部分不会输出。
 - ES6模块的运行机制与CommonJS不一样，它遇到模块加载命令import时，不会去执行模块，而是只生成一个引用。等到真的需要用到时，再到模块里面去取值。ES6模块不会缓存运行结果，而是动态地去被加载的模块取值，以及变量总是绑定其所在的模块。
 - [https://medium.com/webpack/the-state-of-javascript-modules-4636d1774358](https://medium.com/webpack/the-state-of-javascript-modules-4636d1774358)