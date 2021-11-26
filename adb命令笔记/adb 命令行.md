## adb 命令行

### push

* 将电脑上的图片传入手机

  * 在cmd命令行

  * ~~~
    adb push 电脑文件目录 手机文件目录
    ~~~
  
  * ~~~
    adb push .\photo /storage/sdcard0/
    ~~~
  
    

### install

* 将电脑上的apk安装到手机上
  *  1、adb devices查看手机是否连接（命令 adb devices）
  * 2、输入安装命令： adb install +apk存放路径

