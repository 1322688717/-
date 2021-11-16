## node.js环境搭建

* 这里的环境配置以及创建空白文件夹，主要配置的是npm安装的全局模块所在的路径，以及缓存cache的路径，因为以后在执行类似：npm install express [-g] 的安装语句时，会将安装的模块安装到【C:\Users\用户名\AppData\Roaming\npm】路径中，占C盘空间，所以才进行的配置，如果C盘容量足够，可省略这一步，不影响node使用。
* 在安装目录下新建两个文件夹【node_global】和【node_cache】

![img](https://img-blog.csdnimg.cn/20200322160914610.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjg4MTc2OA==,size_16,color_FFFFFF,t_70)

* 再次打开cmd命令窗口，输入npm config set prefix “你的路径\node_global”（`“你的路径”默认安装的情况下为 C:\Program Files\nodejs`）
*  npm config set cache “你的路径\node_cache” 可直接复制刚刚新建的空文件夹目录

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322161819222.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjg4MTc2OA==,size_16,color_FFFFFF,t_70)

* 在【我的电脑】右键→【属性】→【高级系统![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322154051964.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjg4MTc2OA==,size_16,color_FFFFFF,t_70)设置】

* 点击环境变量![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322154157333.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjg4MTc2OA==,size_16,color_FFFFFF,t_70)

* 打开系统属性-高级-环境变量，在`系统变量`中新建 变量名：NODE_PATH,变量值： C:\Program Files\nodejs\node_global\node_modules

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322162440631.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjg4MTc2OA==,size_16,color_FFFFFF,t_70)

* 编辑`用户变量（环境变量）`的 path，将默认的 C 盘下 APPData\Roaming\npm 修改为 C:\Program Files\nodejs\node_global，点击确定

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322162235754.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mjg4MTc2OA==,size_16,color_FFFFFF,t_70)

* 测试，配置完成后，安装个module测试下，我们就安装最常用的express模块，打开cmd窗口，输入如下命令进行模块的全局安装：

  * npm install express -g   *// -g是全局安装的意思*

* rn项目记得一定要 

  * **yarn add react-native-cli**

    

