环境的准备
======

开发Web网站，使用合适的工具和环境会极大的提升开发的效率。本章将讲述如何准备用于AngularJS项目开发的环境。

本书将会使用如下工具和库：
* [WebStorm](https://www.jetbrains.com/webstorm/) - 前端开发
* [Chrome](https://www.google.com/chrome/browser/desktop/index.html?standalone=1) - Google Chrome浏览器
* [AngularJS](https://angularjs.org/) - 前端JS框架
* [Angular Material](https://material.angularjs.org/latest/) - 前端界面框架
* [bower](http://bower.io/) - 获取包括AngularJS在内的各种开发库

为了使用bower，您可能还需要安装如下工具：
* [cnpm](http://npm.taobao.org/) - 国内用户推荐，淘宝的npm加速服务
* [npm](https://www.npmjs.com/) - Node.js的包管理软件
* [Node.js](https://nodejs.org/en/) - 基于Chrome V8引擎的本地/服务端JS运行环境

```
以上内容除去WebStorm外，都可以免费获得。WebStorm可以获取免费试用30天的版本。
因此，您在学习本书的过程中，并不需要花费购买任何软件。
```

## WebStorm
在过去的开发中，WebStorm一直是我对编辑器的首选。WebStorm是商业化的产品，如果长期使用，需要花钱购买（目前已经支持支付宝购买）。价格的话，如果你是一名专职的前端工作人员，可以自行购买或者要求公司购买，个人购买的费用是第一年$59美金，我个人认为还是非常超值的（对比工作效率的提升而言）。另外，出于个人习惯，我使用的是英文版的WebStorm，目前网络上也存在有汉化包，如果希望使用汉化界面的朋友可以自行搜索尝试。

在学习本书的过程中，您可以使用WebStorm的30天尝试版本（直接下载安装即可）。30天的时间对于学习AngularJS和进行一些初级的开发尝试完全足够了。

本书写作时使用的WebStorm版本是11.0.3。


>WebStorm自8.x版本起就可以正确的开发AngularJS网站（再往前的版本没有评估）。
>使用最新的11.0.3版本是在准备本书内容过程中，评估了Angular 2。
>而WebStorm是从11版本才开始部分支持Angular 2的TypeScript开发。

```
另：使用哪种编辑器更多的是个人的偏好。如果您有其他喜欢的编辑器，可以自行选择。
```

## Chrome
Chrome浏览器的开发者工具可以极大的方便开发时的调试工作，目前国内大量浏览器也是基于Chrome的开源内核开发，在通用性上也有保证。另外，Chrome上有支持WebStorm的插件“JetBrains IDE Support”。

由于国内网络原因，Chrome浏览器必须要连接至国外路由才能下载。另外推荐您点击以下链接进行下载，这样可以直接下载完整的安装包（直接在Google搜索Chrome的官网页面下载的是一个小型下载器，在国内无法正确安装）。

 [Chrome完整版本下载链接](https://www.google.com/chrome/browser/desktop/index.html?standalone=1)

```
https://www.google.com/chrome/browser/desktop/index.html?standalone=1
```
本书写作时使用的Chrome版本是47.0.2526.106 m。


>Chrome的版本对于应用AngularJS并不关键，本书特意安装目前的最新版本，是因为要同时评估Angular 2，
>而Angular 2必须要在非常新的浏览器上才能正确运行（v 46+）。


## Node.js
Node.js在本书中主要的使用用途是运行bower工具，用以安装AngularJS极其相关的库文件。通过官网可以直接下载Node.js的安装包（Windows/OS X都有对应的安装包）。

本书使用的Node.js版本是5.4.1（目前最新的Stable稳定版本）。推荐安装较新的稳定版本。

## 其他工具
在安装好Node.js后，可以通过Node.js的npm命令安装最新版本的npm/cnpm/bower(如果已经存在，自动安装最新版本)。

使用命令如下：

Windows上打开cmd，OS X上打开Terminal。

```bash
//Windows
> npm install -g npm --registry=https://registry.npm.taobao.org
> npm install -g cnpm --registry=https://registry.npm.taobao.org
> npm install -g bower --registry=https://registry.npm.taobao.org

//可选，将npm默认设置从淘宝服务器上获取数据
> npm config set registry "https://registry.npm.taobao.org"



//OS X （会需要您输入本机的密码）
$ sudo npm install -g npm --registry=https://registry.npm.taobao.org
$ sudo npm install -g cnpm --registry=https://registry.npm.taobao.org
$ sudo npm install -g bower --registry=https://registry.npm.taobao.org

//可选，将npm默认设置从淘宝服务器上获取数据
$ npm config set registry "https://registry.npm.taobao.org"
```

所有命令后面都跟上了一个*--registry=https://registry.npm.taobao.org*标志，这是使用了淘宝提供的npm镜像服务来安装所需的软件，这样访问的速度会加快非常多。如果您优先运行了后面的可选的命令，那么之前三个命令的此标志项都可以去除。

OS X的命令和Windows类似，但是前面都加了一个sudo，用于提权后把这些工具安装到Node.js的公共库中。

安装完成后，请手动命令确认这几个工具的版本。（如果您安装时不成功，请先确认Node.js工具的版本是否是最新的）

安装好后，您的几个工具的版本应该如下（或者更高）：
```bash
$ npm -v
3.5.3

$ cnpm -v
3.4.0

$ bower -v
1.7.2
```

## 其他工具
其他的工具和库，我们将不再需要从网站上下载安装，直接通过bower在项目内进行下载使用。
