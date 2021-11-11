### react-native 生命周期

* constructor
  * 组件化被实例化的时候发出一般用做对组件做初始工作，如设置state等
* render
  *  组件开始渲染时触发
  * 组件被更新时触发 state和props发生改变时触发
* componentDidMount
  * 组件挂载完毕，可以发送异步请求获取数据
* componentWillUnmount
  * 组件被卸载时触发

