### 需求分析

- front-end 前端
- back-end 后端

### Node.js 是什么

- Node.js不是库 不是框架
- 简单来讲就是Node.js可以解析和执行javaScript代码 
- 以前只有浏览器能够解析执行JavaScript代码
- 现在的JavaScript可以完全脱离浏览器来运行,一切归功于Node.js 

### Node.js中的JavaScript

- 没有 **Bom、Dom**
- EcmaScript
- 在Node这个JavaScript执行环境中为JavaScript位提供了一些服务器级别操作API
  + 例如文件读写
  + 网络服务的构建
  + 网络通信
  + http服务器
  + 等...
- 构建与Chrome的V8引擎之上
  + 代码只是具有特定格式的字符串而已
  + 引擎可以认识它，引擎可以帮你取解析和执行
  + Google Chrome 的V8引擎是目前公认的解析执行JavaScript代码最快的
  + Node.js的作者吧中的V8引擎移植出来开发了一个独立的JavaScript运行环境

### Node.js 能做什么

- Web服务器后台
- 命令行工具
  + npm （node）
  + git（c语言）
  + hexo（node）

### 总结

- Node 中的JavaScript
  + EcmScript
    * 变量
    * 方法
    * 数据类型
    * 内置对象
    * Array
    * Object
    * Date
    * Math
  + 模块系统
    * 在Node中没有全局作用域的概念
    * 在Node中，只能通过require方法来加载执行多个JavaScript脚本文件
    * require加载只能是执行其中的代码，文件与文件之间由于是模块作用域，所以不会有污染的问题
      - 模块完全是封闭的
      - 外部无法访问内部
      - 内部也无法访问外部
    * 模块作用域固然带来了一些好处，可以加载执行多个文件，可以完全避免变量命名冲突污染的问题
    * 但是某些情况下，模块与模块是需要进行通信的
    * 在每个模块中，都提供了一个对象： `exports`
    * 该对象默认是一个空对象
    * 你要做的就是吧需要被外部访问使用的成员手动挂载到`exports`接口对象中
    * 然后谁来`exports`这个模块，谁就可以得到模块内部的`exports`接口对象
  + 核心模块
    * 核心模块是有Node提供的一个个的具名的模块，他们都有自己特殊的名称标识，例如
      - fs 文件操作模块
      - http 网络服务构建模块
      - os 操作系统信息模块
      - path 路径处理模块
- http
  + require
  + 端口号
    * ip 地址定位计算机
    * 端口号定位具体的应用程序
  + Content-Type
    * 服务器最好把每次响应的数据是什么内容类型都告诉客户端，而且要正确的告诉
    * 不同的资源对于的Content-Type是不一样的
    * 对于文本类型的数据，最好都加上编码，目的是为了防止中文解析乱码的问题
    * 发送的并不是文件，本质上来讲发送的是文件的内容
    * 当浏览器收到服务器响应的内容之后，就会根据你的Content-Type进行对应的解析处理
    * 



