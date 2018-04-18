### 基本概念
- 图形学
- 硬件加速 [http://happyseeker.github.io/graphic/2016/01/29/about-opengl-and-hardware-accelerate.html](http://happyseeker.github.io/graphic/2016/01/29/about-opengl-and-hardware-accelerate.html)
    + 计算机中把计算量大的工作分配给专门的硬件比如显卡来减轻cpu的压力
    + 大量重复的平行计算如傅里叶变换或者绘制图形
- DMA（Direct Memory Access，直接内存访问）
    + 不需要cpu处理，直接读写内存
    + 很多硬件的系统会使用DMA，包含硬盘控制器、绘图显卡、网卡和声卡。
- 内存拷贝
- 显存
- framebuffer
- 标准库
    + direct 3d（微软搞的一套）
    + webgl（开源公共的）
        * 一种c语言编写的跨平台的类库，专注于渲染，由一个委员会定期review规范更新
        * 基于opengl 有很多语言绑定如使用js的webgl（基于OpenGL ES 2.0在Web浏览器中的进行3D渲染的API）
        * 目前最主流的OpenGL实现应该只有两种，一种就是Mesa，Meas是目前应用最广泛的一种标准的开源的OpenGL实现，目前类Unix环境中，基本都支持Mesa，目前Intel和AMD的OpenGL实现都基于Mesa，并在持续对Mesa贡献代码；仅NVIDIA自己实现了一套单独的、跟NVIDIA硬件相关的、闭源的OpenGL，与Mesa无关，选择的是截然不同的另一条道路。
