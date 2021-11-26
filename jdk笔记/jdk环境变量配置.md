### jdk环境变量配置

#### 一、找到自己下好的jdk

* ![image-20211115092622772](C:\Users\zcq\Desktop\image-20211115092622772.png)

#### 二、环境变量配置

* 鼠标右键 “此电脑” 选择属性，之后会出现一个弹窗，点击 “高级系统设置”

![image-20211115092844452](C:\Users\zcq\Desktop\image-20211115092844452.png)

* 点击环境变量

![image-20211115092924475](C:\Users\zcq\Desktop\image-20211115092924475.png)

* 一、在系统变量中新建一个变量
  * 变量名：**JAVA_HOME**
  * 变量值：C:\Program Files\Java\jdk1.8.0_162(JDK的安装路径，这里以你自己的安装路径为准)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200324145127273.png#pic_center)

* 二、在系统变量中新建一个classpath变量
  * **.;%JAVA_HOME%\lib;%JAVA_HOME%\lib\tools.jar**(注意前面是有一个点的)，配置好之后如下图，这里是可以复制粘贴的。

![![在这里插入图片描述](https://img-blog.csdnimg.cn/20200324145920366.png](https://img-blog.csdnimg.cn/20200324151159228.png#pic_center)

* 三、配置 path变量

![在这里插入图片描述](https://img-blog.csdnimg.cn/202003241458326.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NDM2MjE0,size_16,color_FFFFFF,t_70#pic_center)

* 然后新建一个

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200324151748558.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4NDM2MjE0,size_16,color_FFFFFF,t_70#pic_center)

* 四、点击保存保存保存！！！
* 五、打开cmd命令行
  * 输入Java -version 来验证
  * 输入javac来验证

![image-20211115093649585](C:\Users\zcq\Desktop\image-20211115093649585.png)

![image-20211115093847710](C:\Users\zcq\Desktop\image-20211115093847710.png)

* 到这里就结束了

