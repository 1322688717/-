### react-native基础知识 

此笔记内容来自

b站  ：【一款强大的程序员学习笔记软件史前巨作-哔哩哔哩】https://b23.tv/RhQU78

react-native中文网 https://www.react-native.cn/

## 目录结构

* 环境搭建
* react native 介绍
* 文件目录结构
* jsx
* rn样式
* 基本标签
* 插值表达式
* 调试
* 事件
* 生命周期
* mobx

## 环境搭建

* 操作系统 win10专业版
* 安卓真机 或 模拟器
* 必须安装的依赖有：Node、JDK 和 Android Studio

### node安装

* 去node官网下载 https://nodejs.org/zh-cn/
* 推荐使用 12.16.3版本
* 安装教程 关注微信公众号 “阿宅的小裙子”

### yarn的安装

* [Yarn](http://yarnpkg.com/)是 Facebook 提供的替代 npm 的工具，可以加速 node 模块的下载。

```
npm install -g yarn
```

* 检查是否安装成功

```
yarn -v
```



* 安装完 yarn 之后就可以用 yarn 代替 npm 了，例如用`yarn`代替`npm install`命令，用`yarn add 某第三方库名`代替`npm install 某第三方库名`

### jdk的安装与配置

* 安装教程 关注微信公众号 “阿宅的小裙子”
* 或者csdn搜索jdk环境搭建

### Android sdk的下载与安装

* Android开发所需的Android SDK、开发中用到的工具https://www.androiddevtools.cn/

![image-20211110194605636](C:\Users\zcq\AppData\Roaming\Typora\typora-user-images\image-20211110194605636.png)

* 下载好后以管理员的身份去运行，傻瓜式安装 下一步 下一步  下一步 懂？

* 这一步选择箭头这项

  ![image-20211110201248923](C:\Users\zcq\AppData\Roaming\Typora\typora-user-images\image-20211110201248923.png)

* 具体配置请转https://www.react-native.cn/docs/environment-setup

## react native 介绍

React Native 是一个使用[React](https://zh-hans.reactjs.org/)和应用平台的原生功能来构建 Android 和 iOS 应用的开源框架。通过 React Native，您可以使用 JavaScript 来访问移动平台的 API，以及使用 React 组件来描述 UI 的外观和行为：一系列可重用、可嵌套的代码

### 文件目录结构



![img](https://img-blog.csdn.net/20180826031703169?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L25pdWJhMTIzNDU2/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

android目录				  Android项目目录，包含了使用AndroidStudio开发项目的环境配置文件；
ios目录	     				  iOS项目目录，包含了XCode的环境
node_modules  				基于node文件依赖系统产生的相关依赖和第三方lib
index.js	          			  ios或android的入口，已经使用index.js代替index.ios.js/index.android.js，android中配置application 文件的getJSMainModuleName()配置入口
app.json	          			 app的json文件
package.json	  		 	 项目基本信息以及依赖信息
package-lock.json			npm install生成的文件，记录当前npm package的信息
App.js			      			相当于Android的MainActivity，可以根据自己的需要进行修改或者删除（同时要修改		index.js的注册的组件入口js文件名）
.babelrc							Babel配置文件，在.babelrc配置文件中，主要是对预设（presets）和插件（plugins）进行配置，因此不同的转译器作用不同的配置项
.buckconfig						Buck的配置文件，buck是Facebook开源的高效构建系统
.flowconfig						Flow的配置文件，flowconfig是是Flow的配置文件
.gitattributes					git配置文件，指定非文本文件的对比合并方式
.gitignore							git配置文件，用于忽略你不想提交到Git上的文件
.watchmanconfig				watchman的配置文件，watchman用于监控文件变化，辅助实现工程修改信息

### vs code安装插件

![image-20211110165020479](C:\Users\zcq\AppData\Roaming\Typora\typora-user-images\image-20211110165020479.png)

代码格式化插件

![image-20211110165056385](C:\Users\zcq\AppData\Roaming\Typora\typora-user-images\image-20211110165056385.png)

代码快捷方式

## JSX 

* React 使用 JSX 来替代常规的 JavaScript。
* JSX 是一个看起来很像 XML 的 JavaScript 语法扩展：
* 我们不需要一定使用 JSX，但它有以下优点：
* 全称为 Java script xml
  * JSX 执行更快，因为它在编译为 JavaScript 代码后进行了优化。
  * 它是类型安全的，在编译过程中就能发现错误。
  * 使用 JSX 编写模板更加简单快速。

![image-20211110210631373](C:\Users\zcq\AppData\Roaming\Typora\typora-user-images\image-20211110210631373.png)

## RN样式

* flex布局
* 样式继承
* 单位
* 屏幕宽度和高度
* 变换

### flex布局

* 所有容器默认都是flexbox
* 并且是纵向排列 也就是 flex-dirextion:column

### 样式继承

* 背景颜色、字体颜色、字体大小等没有继承

### 单位

* 不能加px单位
* 不能加vw vh等单位
* 可以加百分比单位

### 屏幕宽的和高度



* 需要去引包

![image-20211110212646662](C:\Users\zcq\AppData\Roaming\Typora\typora-user-images\image-20211110212646662.png)

 

## 标签

### view

* 不支持设置字体大小颜色等
* 不能直接放文本内容
* 不支持直接绑定点击事件（一般使用TouchableOpacity来代替）

### Text

* 文本标签可以设置 字体大小 颜色等
* 支持绑定点击事件

### TouchableOpacity

* 相当于块级的容器
* 支持绑定时间  onPress
* 可以设置点击时的透明度
* 用法网址 https://www.react-native.cn/docs/touchableopacity 

### Image

* 用于显示多种不同类型图片的 React 组件，包括网络图片、静态资源、临时的本地图片、以及本地磁盘上的图片（如相册）等。
* 用法网址 https://www.react-native.cn/docs/image

### TextInput

* TextInput 是一个允许用户在应用中通过键盘输入文本的基本组件。本组件的属性提供了多种特性的配置，譬如自动完成、自动大小写、占位文字，以及多种不同的键盘类型（如纯数字键盘）等等。
* 用法网址 https://www.react-native.cn/docs/textinput

### 其他

#### Button

#### FlatList

#### ScrollView

#### StatusBar

#### TextInput



## 语法

### 插值表达式

* 花括号中间写js代码 {}

### 组件

#### 状态state

* 定义：如果把 props 理解为定制组件渲染的参数， 那么**state**就像是组件的私人数据记录。状态用于记录那些随时间或者用户交互而变化的数据。状态使组件拥有了记忆！

* 函数组件
  * 没有staste（通过hooks可以有）
  * 没有生命周期（通过hooks可以有）
  * 适合简单的场景
* 类组件
  * 适合复杂的场景
  * 有state
  * 有生命周期

#### 属性props

* 定义:   **Props** 是“properties”（属性）的简写。Props 使得我们可以定制组件
* 用法网址 https://www.react-native.cn/docs/intro-react#props-%E5%B1%9E%E6%80%A7

### 调试

### 事件

### react-native 生命周期

* constructor
  * 组件化被实例化的时候发出一般用做对组件做初始工作，如设置state等
* render
  *  组件开始渲染时触发
  *  组件被更新时触发 state和props发生改变时触发
* componentDidMount
  * 组件挂载完毕，可以发送异步请求获取数据
* componentWillUnmount
  * 组件被卸载时触发

