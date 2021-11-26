## API

### let命令

* ES6新增了 let 命令，用来声明变量。它的用法类似于 var ，但是所声明的变量，只在 let 命令所在的代码块内有效。
  * **let 声明的变量只在它所在的代码块有效。**

## setAlarm

### Alarm 类型：

* RTC_WAKEUP：在指定的时间唤醒设备，并激活 Pending Intent。
* RTC：在指定的时间点激活 Pending Intent，但是不会唤醒设备。
* ELAPSED_REALTIME：根据设备启动之后经过的时间激活 Pending Intent，但是不会唤醒设备。经过的时间包含设备休眠的所有时间。
* ELAPSED_REALTIME_WAKEUP：在设备启动并经过指定的时间之后唤醒设备和激活 Pending Intent。
