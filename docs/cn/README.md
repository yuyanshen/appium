<<<<<<< HEAD
# Appium
=======
## Appium
>>>>>>> d611d3e17027bbba996837e2c3cb0fa8ef5a53c1

[![NPM version](https://badge.fury.io/js/appium.png)](https://npmjs.org/package/appium)
[![Dependency Status](https://david-dm.org/appium/appium.svg)](https://david-dm.org/appium/appium)
[![devDependency Status](https://david-dm.org/appium/appium/dev-status.svg)](https://david-dm.org/appium/appium#info=devDependencies)

[![Build Status](https://team-appium.ci.cloudbees.com/job/appium-master/badge/icon)](https://team-appium.ci.cloudbees.com/job/appium-master/)

<<<<<<< HEAD
> Appium是一个支持原生,混合和移动web apps的开源的跨平台测试框架工具

**Note:** 我们最近发布了Appium 1.0。如果已有Appium测试脚本，你可以检查这个文件[迁移到 1.0](/docs/en/advanced-concepts/migrating-to-1-0.md)！

## 支持平台
=======
Appium 是一个开源的，跨平台的自动化测试工具。
它支持模拟器（iOS，FirefoxOS，Android）和真机（iOS， Android， FirefoxOS）上的原生应用，混合应用和移动 web 应用。

**Note:** 我们最近发布了Appium 1.0。如果已有 Appium 测试脚本，你可以参考这个文件[迁移到 1.0](advanced-concepts/migrating-to-1-0.cn.md)！

### 支持平台
>>>>>>> d611d3e17027bbba996837e2c3cb0fa8ef5a53c1

* iOS
* Android
* FirefoxOS

<<<<<<< HEAD
## [文档网站](http://appium.io/documentation.html?lang=zh)

## 为什么选择appium ?

1. 你不需要以任何方式重新编译或者修改你的app,就可以在所有的平台上使用标准的自动化APIs
2. 你可以用你喜欢的开发工具使用任何 [WebDriver](https://code.google.com/p/selenium/wiki/JsonWireProtocol) 兼容的语言来编写测试用例.比如
Java, [Objective-C](https://github.com/appium/selenium-objective-c),
   JavaScript with Node.js (in both [callback](https://github.com/admc/wd) and [yield-based](https://github.com/jlipps/yiewd) flavours),
   PHP, Python, [Ruby](https://github.com/appium/ruby_lib), C#, Clojure, 或者 Perl
   可以使用标准的Selenium WebDriver API和特定语言的客户端库.
3. 你可以使用任何测试框架.

依托  [WebDriver](https://code.google.com/p/selenium/wiki/JsonWireProtocol) 意味着你可以押宝在一个已经成为事实上标准的独立,自由和开放的协议，而不会被限制在任何的专利中。


如果在没有使用Appium的情况,你使用了Apple的UIAutomation库就只能通过Javascript,并且只能通过Instruments application插桩应用来运行你的测试.
同样的,在Google的UiAutomator体系下,你只能用Java写你的测试案例.
Appium最终开启了跨平台原生移动自动化的可能.

## 依赖

你的环境需要配置好运行测试相关的特定移动平台,下面列出相关的依赖平台
如果你想通过`npm install`来运行appium, 为Appium研究和贡献力量.你需要[node.js and npm](http://nodejs.org) 0.8 或者更高版本 (`brew install node`).

你可以使用 `appium-doctor` 来验证 Appium 的所有依赖。运行 `appium-doctor`，然后提供 `--ios` 或者 `--android` 参数来验证两个平台的依赖是否配置正确。如果从源代码运行，你可以使用 `bin/appium-doctor.js` 或者 `node bin/appium-doctor.js`

### IOS依赖

* Mac OS X 10.7 or higher, 10.8.4 recommended
* XCode &gt;= 4.6.3
* Apple Developer Tools (iPhone simulator SDK, command line tools)
* [Ensure you read our documentation on setting yourself up for iOS testing!](running-on-osx.cn.md)

### android依赖

* [Android SDK](http://developer.android.com) API &gt;= 17 (Additional features require 18)
* Appium支持OS X上的Android, Linux和Windows上的beta支持.确保你通过如下的指示来配置你需要运行测试的不同系统的环境
  * [linux](running-on-linux.cn.md)
  * [osx](running-on-osx.cn.md)
  * [windows](running-on-windows.cn.md)

### FirefoxOS Requirements

* [Firefox OS Simulator](https://developer.mozilla.org/en/docs/Tools/Firefox_OS_Simulator)

## 快速开始
启动Appium server,并运行用你喜欢的 [WebDriver](https://code.google.com/p/selenium/wiki/JsonWireProtocol) 兼容的语言编写的测试用例.
你可以用node.js或者下面的应用程序来运行Appium

### 使用Node.js

    $ npm install -g appium
    $ appium &

### 使用app

* [下载 Appium app](https://github.com/appium/appium/releases)
* 运行它!

## 为Appium编写测试

我们支持 [Selenium WebDriver JSON Wire Protocol](https://github.com/appium/appium/wiki/JSON-Wire-Protocol:-Supported-Methods) 的一个子集
首先还需要指定特定移动平台相关的 [desired capabilities](caps.cn.md) 来通过appium运行你的测试

你可以通过 [WebDriver](https://code.google.com/p/selenium/wiki/JsonWireProtocol) 的元素定位策略的一个子集来定位元素
更多信息请参考 [finding elements](finding-elements.cn.md)


我们也对 JSON Wire Protocol for [automating mobile gestures](gestures.cn.md) 做了一些扩展以支持像 tap, flick, 和 swipe 这样的动作(松开,按压,滑动等手机手势)

你也可以在混合模式下自动化你的用HTML5构建的Web页面 [hybrid app guide](hybrid.cn.md)
这个代码地址包含了 [很多不同语言的测试例子](/sample-code/examples/node)!


想了解全部的Appium的文档页面,请访问 [这个目录](#).

## 工作原理

Appium通过多种原生自动化框架来提供基于Selenium的 [WebDriver JSON wire protocol](https://code.google.com/p/selenium/wiki/JsonWireProtocol) api

Appium驱动Apple的UIAutomation库提供IOS支持. UIAutomation基于[Dan Cuellar's](http://github.com/penguinho)

Android支持上, 在新版本的Android使用了Uiautomator框架,老版本的android上使用了
[Selendroid](http://github.com/DominikDary/selendroid)

FirefoxOS的支持依赖一个基于Gecko平台并且兼容WebDriver的自动化驱动[Marionette](https://developer.mozilla.org/en-US/docs/Marionette),不过暂不翻译了.因为暂时用不到


## 如何贡献代码
可以看下我们的文档  [contribution documentation](../../CONTRIBUTING.md)
以了解如何从源代码中进行编译,测试和运行
=======
### 详细请参见[文档网站](http://appium.io/documentation.html?lang=zh)

### 为什么选择appium ?

1. 因为 Appium 在所有平台上都使用了标准的自动化接口，
所以你不需要以重新编译或者修改你的 app。
2. 你可以用你喜欢的开发工具，使用任何 [WebDriver](https://code.google.com/p/selenium/wiki/JsonWireProtocol) 兼容的语言来编写测试用例。比如
Java， [Objective-C](https://github.com/appium/selenium-objective-c)，
   JavaScript with Node.js (in both [callback](https://github.com/admc/wd) and [yield-based](https://github.com/jlipps/yiewd) flavours)，
   PHP， Python， [Ruby](https://github.com/appium/ruby_lib)， C#， Clojure， 或者 Perl。
   可以使用标准的Selenium WebDriver API和特定语言的客户端库。
3. 你可以使用任何测试框架。

投资  [WebDriver](https://code.google.com/p/selenium/wiki/JsonWireProtocol) 意味着你可以押宝在一个已经成为标准的独立，自由和开放的协议。你不会被任何专利限制。


如果没有 Appium，你就只能用 Javascript 来写 Apple 的 UIAutomation 脚本，并且只能通过Instruments 应用来运行你的测试。同样的，在 Google 的UiAutomator体系下，你只能用 Java 写你的测试案例。Appium 最终开启了跨平台原生移动自动化的可能。

### 我还是不太明白……

如果你第一次接触 Appium 或者想要一个完整的描述，请通读我们的 [Introduction to Appium Concepts](about-appium/intro.cn.md)。


### 依赖

为了运行测试，针对不同的移动平台，你需要配置下环境，下面列出相关的依赖平台的需求。

如果你想通过 `npm install` 安装的 appium 来运行 Appium 或者研究 Appium 或者为 Appium 贡献力量。你需要安装 [node.js 和 npm](http://nodejs.org) 0.10 或者更高版本 (使用 [n](https://github.com/visionmedia/n)或者`brew install node`来安装 Nodejs，确保安装过程中，你没有使用任何 sudo，否则你会遇到很多问题)。我们推荐最新的稳定版本。

你可以使用 `appium-doctor` 来验证 Appium 的所有依赖。运行 `appium-doctor`，然后提供 `--ios` 或者 `--android` 参数来验证两个平台的依赖是否配置正确。如果从源代码运行，你可以使用 `bin/appium-doctor.js` 或者 `node bin/appium-doctor.js`

#### iOS 需求

* Mac OS X 10.7 或者更高，推荐 10.9.2
* XCode &gt;= 4.6.3，推荐 5.1.1
* Apple Developer Tools (iPhone simulator SDK， command line tools)
* [确保你已经读了我们写的如何配置 iOS 测试环境的文档](appium-setup/running-on-osx.cn.md)


#### Android 需求

* [Android SDK](http://developer.android.com) API &gt;= 17 (额外的特性需要 18/19）
* Appium 支持OS X，Linux，Windows 上的 Android，确保你是按照如下文档的指示来配置不同的测试环境的。
  * [linux](appium-setup/running-on-linux.cn.md)
  * [osx](appium-setup/running-on-osx.cn.md)
  * [windows](appium-setup/running-on-windows.cn.md)

#### FirefoxOS 需求

* [Firefox OS Simulator](https://developer.mozilla.org/en/docs/Tools/Firefox_OS_Simulator)

### 快速开始
启动 Appium server，并运行用你喜欢的 [WebDriver](https://code.google.com/p/selenium/wiki/JsonWireProtocol) 兼容的语言编写的测试用例。
你可以用 node.js 或者下面的应用程序来运行 Appium

#### 使用 Node.js

```center
    $ npm install -g appium
    $ appium &
```

#### 使用 app

* [下载 Appium app](https://github.com/appium/appium/releases)
* 运行它！

### 为Appium编写测试

如何开始写测试用例，运行测试用例，可以看[the running tests](writing-running-appium/running-tests.cn.md)，这个文档描述了iOS，Android 和老版本的 Android 机器的情况。如果你想在实体机上运行测试的话，
你可能会对[真机指南](appium-setup/real-devices.cn.md)感兴趣。

我们支持 [Selenium WebDriver JSON Wire Protocol](https://github.com/appium/appium/wiki/JSON-Wire-Protocol:-Supported-Methods) 的一个子集，而且在此之上扩展了移动平台相关的特性。所以你可以
指定特定移动平台[desired capabilities](writing-running-appium/caps.cn.md) 来运行你的测试。

你可以通过 [WebDriver](https://code.google.com/p/selenium/wiki/JsonWireProtocol) 元素定位策略的子集来定位元素。更多信息请参考 [finding elements](writing-running-appium/finding-elements.cn.md)
为了支持移动手势[automating mobile gestures](writing-running-appium/touch-actions.cn.md)，比如
 tap，flick 和 swipe，我们扩展了JSON Wire Protocolor。

你也可以对混合应用中的webview进行自动化 [hybrid app guide](advanced-concepts/hybrid.cn.md)

该代码库有 [很多不同语言的测试例子](https://github.com/appium/sample-code)！

### 工作原理

Appium 可以驱动多种原生自动化框架，同时也提供基于 Selenium 的 [WebDriver JSON wire protocol](https://code.google.com/p/selenium/wiki/JsonWireProtocol) api。

基于[Dan Cuellar's](http://github.com/penguinho) 在 iOS 自动化上的成果，Appium 通过驱动 Apple 的 UIAutomation 库来提供 iOS 支持。

而在新版本的 Android 上，我们使用 Uiautomator 框架，老版本的 Android，则使用了
[Selendroid](http://github.com/DominikDary/selendroid)

FirefoxOS 的支持依赖一个基于 Gecko 平台并且兼容 WebDriver 的自动化驱动[Marionette](https://developer.mozilla.org/en-US/docs/Marionette)。


### 如何贡献代码
可以看下我们的文档  [contribution documentation](../../CONTRIBUTING.md)
以了解如何从源代码中进行编译，测试和运行
>>>>>>> d611d3e17027bbba996837e2c3cb0fa8ef5a53c1


## 其他项目的授权和灵感来源

<<<<<<< HEAD
[Credits](credits.cn.md)

## 邮件列表

声明和公告经常放到讨论组 [Discussion Group](https://groups.google.com/d/forum/appium-discuss), 需要注册

## 问题定位

我们增加了一个 [问题定位指南](troubleshooting.cn.md).
如果你遇到一些问题,请看下这个问的那个.它包含了一些常见的错误说明,以及在无法解决的情况如何和社区联系


## 使用Robots扩展
可以使用appium的一些robots扩展.或者其他的robots.想了解更多可以看看 [Appium Robots](https://github.com/appium/robots)


## 翻译工作
文档翻译工作由[testerhome](http://testerhome.com/topics/150)在推动, 我们会不断补充更多的文档和测试用例.
欢迎对Appium感兴趣的同学加入我们, 为开源社区贡献中国人的力量.

## 贡献者
来自 testerhome 的：

* seveniruby
* monkey
* lihuazhang
* FredZero
* pinghailinfeng
* niweyzhuce
=======
[Credits](contributing-to-appium/credits.cn.md)

### 邮件列表

声明和公告经常放到讨论组 [Discussion Group](https://groups.google.com/d/forum/appium-discuss)， 需要注册

### 问题定位

我们增加了一个 [问题定位指南](appium-setup/troubleshooting.cn.md)。
如果你遇到一些问题，请看下这个问的那个。它包含了一些常见的错误说明，以及在无法解决的情况如何和社区联系。


### 使用Robots扩展
可以使用 appium 的一些 robots 扩展。或者其他的 robots。想了解更多可以看看 [Appium Robots](https://github.com/appium/robots)


### 翻译工作
文档翻译工作由[testerhome](http://testerhome.com)在推动， 我们会不断补充更多的文档和测试用例.
欢迎对 Appium 感兴趣的同学加入我们， 为开源社区贡献中国人的力量.
>>>>>>> d611d3e17027bbba996837e2c3cb0fa8ef5a53c1
