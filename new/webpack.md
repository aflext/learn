### handbook
- [requirejs-to-webpack - Part 1 (the why)](http://j-query.blogspot.com/2015/06/from-requirejs-to-webpack-part-1-reasons.html)
- [From Require.js to Webpack - Part 2 (the how)](https://gist.github.com/xjamundx/b1c800e9282e16a6a18e)
- [ditching-requirejs-webpack-reasons-lessons-learned](http://blog.player.me/ditching-requirejs-webpack-reasons-lessons-learned/)
- [用 ES6 编写 Webpack 的配置文件](https://segmentfault.com/a/1190000003932889)
 - babel-node可以代替node来先把webpack配置文件编译
 - webpack.config.babel.js  webpack.config.[loader].js这种黑科技
 - nodejs4对es6支持不完整
- [webpack-tutorial](https://www.zfanw.com/blog/webpack-tutorial.html)
- [beginner-s-guide-to-webpack](https://medium.com/@dabit3/beginner-s-guide-to-webpack-b1f1a3638460#.88assdv7l)
- [advanced-webpack-part-1-the-commonschunk-plugin](http://jonathancreamer.com/advanced-webpack-part-1-the-commonschunk-plugin/)
- [how-to-split-your-apps-by-routes-with-webpack](https://medium.com/@somebody32/how-to-split-your-apps-by-routes-with-webpack-36b7a8a6231#.adbm776bg) 太长了没看
- [Setting up CSS Modules with React and Webpack](http://javascriptplayground.com/blog/2016/07/css-modules-webpack-react/)

### treeshaking 
> babel-preset-es2015-native-modules:  A preset without transform-es2015-modules-commonjs would help with tree-shaking when using Babel 6 and webpack 2  
This preset is no longer necessary as the function that it performed can now be achieved natively.

Instead of es2015-native-modules please use es2015 with { "modules": false } option:

presets: [
  ["es2015", { "modules": false }]
]

- [https://webpack.js.org/guides/tree-shaking/](https://webpack.js.org/guides/tree-shaking/)
- [https://medium.com/modus-create-front-end-development/webpack-2-tree-shaking-configuration-9f1de90f3233](https://medium.com/modus-create-front-end-development/webpack-2-tree-shaking-configuration-9f1de90f3233)
- [https://www.npmjs.com/package/babel-preset-es2015-native-modules](https://www.npmjs.com/package/babel-preset-es2015-native-modules)
- [http://2ality.com/2015/12/webpack-tree-shaking.html](http://2ality.com/2015/12/webpack-tree-shaking.html)
- [https://www.zhihu.com/question/41922432](https://www.zhihu.com/question/41922432)
- [http://imweb.io/topic/58666d57b3ce6d8e3f9f99b0](http://imweb.io/topic/58666d57b3ce6d8e3f9f99b0)