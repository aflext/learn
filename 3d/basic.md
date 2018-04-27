### 基本概念
- 图形学：计算机表示合理用几何图形
- 硬件加速 [http://happyseeker.github.io/graphic/2016/01/29/about-opengl-and-hardware-accelerate.html](http://happyseeker.github.io/graphic/2016/01/29/about-opengl-and-hardware-accelerate.html)
    + 计算机中把计算量大的工作分配给专门的硬件比如显卡来减轻cpu的压力(cpu要处理指令和任务)
    + 大量重复的平行计算如傅里叶变换或者绘制图形
- DMA（Direct Memory Access，直接内存访问）
    + 不需要cpu处理，直接读写内存
    + 很多硬件的系统会使用DMA，包含硬盘控制器、绘图显卡、网卡和声卡。
- 内存拷贝：c和c++中从源地址拷贝内存数据到目的地址
- 显存：全称显示存储器，亦称帧缓存，它是用来存储显示芯片处理过或者即将读取的渲染数据。
- GPU（图形处理器）：运行绘图运算工作的微处理器，不同于cpu的通用计算，gpu专用于特殊计算，大量内核可以并行海量运算，在3D渲染、深度学习、机器学习算法中很有用。
- 显卡（显存+GPU）：显示信息转换驱动显示器，并向显示器提供扫描信号
- framebuffer（帧缓冲器）：is a portion of RAM containing a bitmap that drives a video display
- 帧缓冲对象（FBO Frame Buffer Object）：在OpenGL中，渲染管线中的顶点、纹理等经过一系列处理后，最终显示在2D屏幕设备上，渲染管线的最终目的地就是帧缓冲区。帧缓冲包括OpenGL使用的颜色缓冲区(color buffer)、深度缓冲区(depth buffer)、模板缓冲区(stencil buffer)等缓冲区
- 标准库
    + direct 3d（微软搞的一套）：是微软公司在Microsoft Windows操作系统上所开发的一套3D绘图编程接口，是DirectX的一部分，目前广为各家显卡所支持
    + OpenGL：是用于渲染2D、3D矢量图形的跨语言、跨平台的应用程序编程接口（API），350个不同的函数调用，语言独立，因此有各种编程语言的绑定衍生，如WebGL
        * 目前最主流的OpenGL实现应该只有两种，一种就是Mesa，Meas是目前应用最广泛的一种标准的开源的OpenGL实现，目前类Unix环境中，基本都支持Mesa，目前Intel和AMD的OpenGL实现都基于Mesa，并在持续对Mesa贡献代码；仅NVIDIA自己实现了一套单独的、跟NVIDIA硬件相关的、闭源的OpenGL，与Mesa无关，选择的是截然不同的另一条道路。
    + OpenGL规范：1992年成立的OpenGL架构评审委员会（ARB）维护
    + webgl（开源公共的）：一种OpenGL的关于JavaScript的语言绑定变种。是一种JavaScriptAPI，用于在不使用插件的情况下在任何兼容的网页浏览器中呈现交互式2D和3D图形
        * 一种c语言编写的跨平台的类库，专注于渲染，由一个委员会定期review规范更新
        * 基于opengl 有很多语言绑定如使用js的webgl（基于OpenGL ES 2.0在Web浏览器中的进行3D渲染的API，WebGL 2.0基于OpenGL ES 3.0）
        * js句柄+GLSL（OpenGL Shading Language）着色器，运行于GPU上
        * 维护：Mozilla基金会-->非营利性组织Khronos Group维护
    + GLSL：OpenGL Shading Language
        * 着色器代码分成2个部分：Vertex Shader（顶点着色器）和Fragment（片断着色器），有时还会有Geometry Shader（几何着色器）。负责运行顶点着色的是顶点着色器。它可以得到当前OpenGL 中的状态，GLSL内置变量进行传递

### 其他概念
- CSS Shaders
- canvas
    + The canvas element is part of HTML5 and allows for dynamic, scriptable rendering of 2D shapes and bitmap images.
- svg（Scalable Vector Graphics，SVG）
    + 一种基于可扩展标记语言（XML），用于描述二维矢量图形的图形格式。W3C制定
- 矢量图
    + 计算机图形学中用点、直线或者多边形等基于数学方程的几何图元表示图像。现代计算机显示器都要将矢量图形转换成栅格图像的格式，包含屏幕上每个像素数值的栅格图像保存在内存中。
- 矢量图和非矢量图
    + 矢量图则是由一些形状元素构成。放大位图可以看到点，而放大矢量图看到的仍然是形状。SVG属于矢量图，因此能够无级缩放，而不会导致马赛克。
- [http://www.zhangxinxu.com/wordpress/2011/10/html5-canvas-webgl-css-shaders-glsl%E7%9A%84%E6%9A%A7%E6%98%A7%E5%85%B3%E7%B3%BB/](http://www.zhangxinxu.com/wordpress/2011/10/html5-canvas-webgl-css-shaders-glsl%E7%9A%84%E6%9A%A7%E6%98%A7%E5%85%B3%E7%B3%BB/)
- 并行计算
    + CUDA
        * CUDA处理流例子
            1.将主存的处理数据复制入显存中
            2. CPU指令驱动GPU
            3. GPU每一核心并行处理
            4. GPU将显存结果传回主存
- 坐标系
    + 直角坐标系：（笛卡坐标系）
    + 浏览器坐标：有两个坐标轴，x轴（水平轴）和y轴（垂直轴）。两轴的交汇点（左上角）为坐标原点(0,0)。原点沿x轴向右是正值，原点沿y轴向下是正值
    + Canvas坐标系统：
        * 2d：在Canvas中2D环境中其坐标系统和Web的坐标系统是一致的。坐标原点(0,0)在<canvas>画布的的左上角。同样的分为x和y两个轴。x轴向右为正值，y轴向下为正值。
        * 3d：x轴从左向右在水平方向延展，y轴纵向延展，z轴的正值从屏幕中穿出。
    + 坐标系：
        * 右手坐标系：在三维坐标系中，Z轴的正轴方向是根据右手定则确定的。右手定则也决定三维空间中任一坐标轴的正旋转方向。要标注X、Y和Z轴的正轴方向，就将右手背对着屏幕放置，拇指即指向X轴的正方向。伸出食指和中指，如右图所示，食指指向Y轴的正方向，中指所指示的方向即是Z轴的正方向
        * 左手坐标系：伸出左手，让拇指和食指成“L”形，大拇指向右，食指向上。其余的手指指向前方。这样就建立了一个左手坐标系。拇指、食指和其余手指分别代表x，y，z轴的正方向。判断方法：在空间直角坐标系中，让左手拇指指向x轴的正方向，食指指向y轴的正方向，如果中指能指向z轴的正方向，则称这个坐标系为左手直角坐标系．反之则是右手直角坐标系。

### 图形引擎
### 游戏引擎
### webgl vs canvas

### OpenGL ES
- 概念：OpenGL ES（OpenGL for Embedded Systems）是OpenGL三维图形API的子集，针对手机、PDA和游戏主机等嵌入式设备而设计。
### OpenGL。OpenGL ES是从OpenGL裁剪定制而来的，去除了glBegin/glEnd，四边形（GL_QUADS）、多边形（GL_POLYGONS）等复杂图元等许多非绝对必要的特性。

### Unity（底层基于OpenGL或者Direct 3D的游戏引擎）（https://unity3d.com/cn）
- Unity 是一套跨平台的游戏引擎，可用于开发 Windows、MacOS、Linux 平台的单机游戏，或是 iOS、Android 移动设备的游戏。Unity 也可开发支持 WebGL 技术的网页游戏，或PlayStation、XBox、Wii主机上的游戏。
- 类似于Director，Blender，Virtools或Torque Game Builder等利用交互的图型化开发环境为首要方式的软件其编辑器运行在Windows和Mac OS X下，可发布游戏至Windows、Wii、OSX或iOS平台。也可以利用Unity web player插件发布网页游戏，支持Mac和Windows的网页浏览。它的网页播放器也被Mac widgets所支持。
- OpenGL ES是Unity在现在的Android、ios等类似设备上用来渲染的底层库，是OpenGL的一个子集。OpenGL ES在渲染能力、功耗设计中都考虑了移动设备的特殊性，所以现在的移动设备都是基于OpenGL ES 1.1或者2.0来渲染。
- Unity3D：是一个用于创建诸如三维电子游戏、建筑可视化、实时三维动画等类型互动内容的综合型创作工具。
- Cocos2dx、OGRE都是游戏引擎

### OpenGL
- 基础
    + 
- 进阶
- best practice
- 参考链接：
    + [https://learnopengl.com/Getting-started/OpenGL](https://learnopengl.com/Getting-started/OpenGL)，中文：[https://learnopengl-cn.github.io/01%20Getting%20started/01%20OpenGL/](https://learnopengl-cn.github.io/01%20Getting%20started/01%20OpenGL/)

### WebGL
- 基础
    + 使用了canvas
    + 使用了dom
- 进阶
- best practice