
### 热更新、ES6/7、LESS、Router4、redux、webpack2、async／await、前端node服务器，按需加载...
<hr />

[![Build Status](https://travis-ci.org/hyy1115/react-redux-webpack2.svg?branch=master)](https://travis-ci.org/hyy1115/react-redux-webpack2)  [![codebeat badge](https://codebeat.co/badges/8be7b4c1-85f3-4da9-ab23-d470624b40ad)](https://codebeat.co/projects/github-com-hyy1115-react-redux-webpack2-master)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md#pull-requests)  

适用人群：该框架集成了react开发常用技术栈，适用于想要学习单向数据流框架搭建的新手、以及想要一个比较干净、简洁的框架从事实践项目的开发者。（doc文件夹附有教程文档）

不适用人群：想要学习完整项目，比如饿了么，社区论坛这种应用型项目，请搜索其他开源项目。

欢迎 watch、star、fork，因为我自己也是基于这套框架做开发，所以我会长期维护该项目，跟随相关插件的升级而升级优化。  

针对最近有人反映在windows热更新之后，浏览器不自动刷新的情况，我专门买了台i7 7700k台式机（说笑的，另有用处）。

2017.6.7 更新

1、新增了global（action）来控制路由切换时调用的动画，我实现了左移动、右移动2种特效，你可以点击下面的demo查看效果。

2017.6.6 更新

1、热更新改成react-hot-loader3；

2、前端改成webpack-dev-server启动；

3、mock移到easy-mock。

4、如果你不喜欢这种启动和热更新方式，请切换tag版本（不会切换tag吗？）。

5、更新了webpack插件和其他几个插件，你打包之后会发现js体积变小了。

6、新版本推送的比较仓促，有bug可以给我反馈。

==========================================

体验动画路由切换：https://hyy1115.github.io/huangyongyue/   

=========================

![image](https://github.com/hyy1115/react-redux-webpack2/blob/master/public/store.gif)

==========================

#### Installation 教程

fork到你的账号，简单省事，或者 download 项目到本地

1、 安装依赖包，已经解决了一些依赖包安装最新版可能出现的bug，如果还有问题，可以看相关社区的issue。
```
npm install 或者cnpm install
```

2、运行demo。
   ```
    mac
    npm run start-mac

    windows
    npm run start-win
   ```

3、将会开启3011端口.
```
http://localhost:3011

```

4、打包发布: 假设你用的是阿里云服务器，你可以把静态资源和图片都放到CDN，index.html放到你的域名服务器下面，请注意路径问题。  

```
mac
npm run build-mac

windows
npm run build-win
```

===========================================

压缩效果图  
![image](https://github.com/hyy1115/react-redux-webpack2/blob/master/public/fenxi.png)

===================================================

#### 关于服务端渲染的建议（内容来自react-router官方文档）  

查看原文：https://reacttraining.cn/web/guides/code-splitting

Code-splitting + server rendering

代码分割 + 服务端渲染

We’ve tried and failed a couple of times. What we learned:

我们尝试了很多次都失败了，我们总结了下面几点：

1、You need synchronous module resolution on the server so you can get those bundles in the initial render.

你需要在服务端同步模块解析使得你可以在初始化渲染的时候得到那些文件。

2、You need to load all the bundles in the client that were involved in the server render before rendering so that the client render is the same as the server render. (The trickiest part, I think its possible but this is where I gave up.)
为了保证服务端渲染和客户端渲染的同步，你需要在客户端渲染前加载和服务端渲染一致的所有文件。（这也是我认为最难搞的地方，所以我放弃了）

3、You need asynchronous resolution for the rest of the client app’s life.
在客户端运行过程中，你需要异步解析其他没有在初始化渲染的部分。

We determined that google was indexing our sites well enough for our needs without server rendering, so we dropped it in favor of code-splitting + service worker caching. Godspeed those who attempt the server-rendered, code-split apps.
我们确定谷歌大神对我们网站的索引做得足够好，并不需要服务端渲染来解决SEO的问题，所以我们放弃了这种模式，而是采用更有利的代码分割 + service worker 缓存5的方式。愿上帝保佑那些想要尝试服务端渲染+代码分割的小白鼠:

==================================================

####Finally, JavaScript is the world's best language, if demand, you can directly send me an email  
