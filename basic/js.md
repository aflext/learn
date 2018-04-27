### js细节
- [10-small-things-you-may-not-know-about-javascript](http://samuli.hakoniemi.net/10-small-things-you-may-not-know-about-javascript/) 一些细节需要注意
### 数学
- 浮点数
    + 最大安全整数：2^53-1，最大数Number.MAX_VALUE（不安全），小数要转换成二进制是通过不断乘以2，拿到余数的，所以小数会永远是10循环，所以有精度问题
    + [https://medium.com/dailyjs/javascripts-number-type-8d59199db1b6](https://medium.com/dailyjs/javascripts-number-type-8d59199db1b6)
    + [https://blog.angularindepth.com/the-mechanics-behind-exponent-bias-in-floating-point-9b3185083528](https://blog.angularindepth.com/the-mechanics-behind-exponent-bias-in-floating-point-9b3185083528)
    + [https://github.com/camsong/blog/issues/9](https://github.com/camsong/blog/issues/9)
    + [https://www.zhihu.com/question/29010688](https://www.zhihu.com/question/29010688)