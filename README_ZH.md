## 介绍

node-webkit是一个基于`Chromium`和`node.js`的应用运行时. 
借助于node-webkit你可以使用HTML和Javascript来编写本地应用. 
同样, 通过它你可以在DOM中直接调用Node.js的模块, 
这样就产生了一种可以使用任意的Web技术来编写本地应用的全新方式.

它诞生自英特尔开源技术中心.


[node-webkit介绍(幻灯片)](https://speakerdeck.com/u/zcbenz/p/node-webkit-app-runtime-based-on-chromium-and-node-dot-js)   
[使用node-webkit创建桌面应用程序](http://strongloop.com/strongblog/creating-desktop-applications-with-node-webkit/)     
[使用node-webkit将Web应用转化为桌面应用(幻灯片)](http://oldgeeksguide.github.io/presentations/html5devconf2013/wtod.html)

## 特性

* 使用HTML5, CSS3, JS 和 WebGL 来编写应用.
* 完全的支持[Node.js APIs](http://nodejs.org/api/) 和它所有的 [第三方库](https://npmjs.org).
* 性能高效: Node 和 WebKit在同一个线程中运行: 函数可以直接调用; 对象在同一个堆中, 并可以直接相互引用;
* 便捷的打包和发布应用.
* 支持Linux, Mac OSX 和 Windows

## 下载
[v0.9.2 发布日志](https://groups.google.com/d/msg/node-webkit/qpBhcWr-hSc/caGjhtl8cEgJ)

预编译二进制文件 (v0.9.2 - 2014/2/20):

* Linux: [32位](https://s3.amazonaws.com/node-webkit/v0.9.2/node-webkit-v0.9.2-linux-ia32.tar.gz) / [64位] (https://s3.amazonaws.com/node-webkit/v0.9.2/node-webkit-v0.9.2-linux-x64.tar.gz)
* Windows: [win32](https://s3.amazonaws.com/node-webkit/v0.9.2/node-webkit-v0.9.2-win-ia32.zip)
* Mac: [32位, 10.7+](https://s3.amazonaws.com/node-webkit/v0.9.2/node-webkit-v0.9.2-osx-ia32.zip)

**如果你的本地Node模块只能在Node v0.10下运行, 你可以选择 node-webkit v0.8.x, 它也是正常维护的一个分支. [更多信息](https://groups.google.com/d/msg/node-webkit/2OJ1cEMPLlA/09BvpTagSA0J)**  
[v0.8.5 发布日志](https://groups.google.com/d/msg/node-webkit/Izwu5icHFOQ/0A-3uEKfldkJ)

预编译二进制文件 (v0.8.5 - 2014/2/26):

* Linux: [32位](https://s3.amazonaws.com/node-webkit/v0.8.5/node-webkit-v0.8.5-linux-ia32.tar.gz) / [64位] (https://s3.amazonaws.com/node-webkit/v0.8.5/node-webkit-v0.8.5-linux-x64.tar.gz)
* Windows: [win32](https://s3.amazonaws.com/node-webkit/v0.8.5/node-webkit-v0.8.5-win-ia32.zip)
* Mac: [32位, 10.7+](https://s3.amazonaws.com/node-webkit/v0.8.5/node-webkit-v0.8.5-osx-ia32.zip)

[历史版本](https://github.com/rogerwang/node-webkit/wiki/Downloads-of-old-versions)

###示例和真实应用
你可能同样对[我们的示例库](https://github.com/zcbenz/nw-sample-apps) and the [List of apps and companies using node-webkit](https://github.com/rogerwang/node-webkit/wiki/List-of-apps-and-companies-using-node-webkit)感兴趣.


## 快速入门

创建 `index.html`:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Hello World!</title>
  </head>
  <body>
    <h1>Hello World!</h1>
    We are using node.js <script>document.write(process.version)</script>.
  </body>
</html>
```

创建 `package.json`:

```json
{
  "name": "nw-demo",
  "main": "index.html"
}
```

将`index.html`和`package.json`打进一个zip包, 命名为`app.nw`:

````bash
$ zip app.nw index.html package.json
````

这样会产生一个这样的结构:

```
app.nw
|-- package.json
`-- index.html
```

下载适合你操作系统的node-webkit版本, 然后使用它打开`app.nw`文件:

````bash
$ ./nw app.nw
````

注意: Windows下, 你可以通过将`app.nw`直接拖拽到`nw.exe`上来打开它.

## 文档

想了解更多关于如何编写/打包/运行应用, 请看:

* [如何运行应用](https://github.com/rogerwang/node-webkit/wiki/How-to-run-apps)
* [如何打包和发布你的应用](https://github.com/rogerwang/node-webkit/wiki/How-to-package-and-distribute-your-apps)
* [在node-webkit中如何使用Node.js的模块(库)](https://github.com/rogerwang/node-webkit/wiki/Using-Node-modules)

然后通过我们的[Wiki](https://github.com/rogerwang/node-webkit/wiki)了解更对.

## 社区

我们使用[node-webkit group](http://groups.google.com/group/node-webkit)作为邮件清单 (只使用英语).
通过[node-webkit+subscribe@googlegroups.com](mailto:node-webkit+subscribe@googlegroups.com)订阅.
问题在GitHub上跟踪.

你可以在IRC上和我们聊天, irc.freenode.net上的##node-webkit 频道

## 许可

`node-webkit`的代码采用了MIT许可, 可以查看我们的`LICENSE`文件. 重新发布二进制的话, 参考[如何打包和发布你的应用](https://github.com/rogerwang/node-webkit/wiki/How-to-package-and-distribute-your-apps)
