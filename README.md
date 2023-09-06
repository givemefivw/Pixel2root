# Pixel2刷机root

## 一、购买

咸鱼购买，200-400价位之间

买之前注意挑选工作室，比个人用户靠谱，同时记得询问是否已解锁，是否漏液，解锁之后才可以进行刷机

## 二、准备工具

### 1、刷机包

Google地址：[https://developers.google.com/android/images](https://developers.google.com/android/images)，右侧选择手机型号，pixel2专用，选择OPM1.171019.011版本，点击Link下载链接进行下载

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062033551.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062033551.png)

解压之后共有6个文件

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062034356.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062034356.png)

### 2、TWRP

TWRP是国外android爱好者开发的一款工具 ，全名是：Tearwin Recovery Project。TWRP的主要作用包括刷机（cm7、cm9、miui等），备份，恢复等。修复的时候TWRP是必不可少的工具。是一款知名第三方recovery刷机工具 ，功能强大，支持触屏操作。

TWRP地址：[https://twrp.me/Devices/](https://twrp.me/Devices/)，搜索框输入pixel，点击pixel 2 walleye

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062041869.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062041869.png)

选择Primary (Americas)

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062042127.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062042127.png)

点击img，进入下载界面

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062043775.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062043775.png)

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062044015.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062044015.png)

### 3、Magisk

Magisk下载地址：https://github.com/topjohnwu/Magisk/releases，下载Magisk.apk文件

### 4、Lsposed

Lsposed下载地址：https://github.com/LSPosed/LSPosed/releases，下载LSPosed-v1.9.1-6990-zygisk-release.zip文件

### 5、Lsposed Manager

似乎没有releases，自行搜索，也可直接访问[LSPosed manager](https://github.com/dioos886/LSPosed)，下载第一个apk文件，安全性自查！

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062058818.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062058818.png)

### 6、ADB_ROOT

下载地址：https://github.com/evdenis/adb_root/releases，下载adb_root.zip

## 三、刷入安卓8

使用数据线连接PC电脑和Pixel2手机，在手机关机状态下先按住音量下键，再按住开机键进入fastboot模式

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062102047.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062102047.png)

电脑上双击flash-all.bat，自动开始刷机，注意过程中不要拔掉数据线

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062109817.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062109817.png)

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062109627.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062109627.png)

如果运行脚本后提示<waiting for any device>，[https://www.ytechb.com/install-google-usb-driver-windows/](https://www.ytechb.com/install-google-usb-driver-windows/)下载google usb drive

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062116988.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062116988.png)

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062117035.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062117035.png)

然后打开设备管理器，找到手机，右键点击更新驱动程序，弹出的框选择浏览我的电脑查找程序，找到解压的位置，选择到usb_dricer目录即可，自动勾选了包含子文件夹，最后下一步安装驱动，提示你的设备最佳驱动程序已安装即可。

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062120428.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062120428.png)

然后再重复刷机的操作，重新运行刷机脚本就可以了。

如果遇到其他问题，参看[刷机时使用fastboot 出现 ＜ waiting for any device ＞ 的问题的解决](https://blog.csdn.net/weixin_44183483/article/details/119330911)

等待刷机完成，重启设备，即可进入系统，查看系统版本，安卓8版本

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062110789.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062110789.png)

再查看WIFI和蓝牙功能是否正常即可

## 四、ROOT

将Magisk.zip push到/sdcard目录

这里注意，Magisk新版本releses直接打包成了apk，下载本地之后，直接修改后缀apk为zip即可，不需要压缩成zip，否则无法刷入

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062112009.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062112009.png)

接着同样进入fastboot模式，数据线连接手机电脑，运行fastboot boot twrp-3.3.0-0-walleye.img，脚本执行完毕后立即拔掉数据线，手机自动进入重启

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062114009.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062114009.png)

首次刷入提示输入密码，这个密码是上面刷机完成后，手机初始化时设置的密码（如果没有设置密码应该就不会提示了）

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062122150.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062122150.png)

接着下一步，直接滑动下方滑块即可

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062124043.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062124043.png)

接着选择install，从sdcard目录安装Magisk

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062125082.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062125082.png)

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062126519.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062126519.png)

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062130204.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062130204.png)

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062131103.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062131103.png)

如果前面直接打包成了zip，那么这步会提示错误

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062132342.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062132342.png)

失败后点击重启系统，重新关机进入fastboot，重新刷入即可。

成功刷入Magisk之后，重启进入系统，打开开发者模式，配置adb调试，adb shell之后，输入su，成功进入root，刷机root成功

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062133614.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062133614.png)

## 五、adb root

这个时候虽然su可以提升到root，但是外部的adb无法执行adb root，会提示adbd cannot run as root in production builds

将上面下载的adb_root.zip push到sdcard中，打开Magisk，模块界面选择从本地安装，选择sdcard目录，选择adb_root.zip，进行安装

![https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062157825.png](https://zebpic-1301715962.cos.ap-nanjing.myqcloud.com//blog/202309062157825.png)

安装完成重启手机，确保处于开发者模式并打开adb调试，执行adb root，此时可以成功root运行，进入Shell也直接是root权限。此时如果开发者设置里面充电设置无法切换到传输或MIT模式，重启手机1-2次，再次切换连接模式即可。

Lsposed安装方式一致，推送LSPosed-v1.9.1-6990-zygisk-release.zip到目录，Magisk本地安装。Lsposed Manager如果adb install直接安装可能会提示no package无法安装，可以先推送进sdcard，通过手机文件浏览器进入目录，手动点击安装即可。

至此，刷机结束。之后的各种模块安装方式基本遵循此例。

## 六、参考文章

[https://mp.weixin.qq.com/s?__biz=Mzg5MDY1NTg3OQ==&mid=2247484451&idx=1&sn=b3a96357e177cb5cc29c92f19b2f96b5&chksm=cfd801cbf8af88dde48fe616d466ad9893191249fcb4701ffc1871f26b618347bb5fab78a853&mpshare=1&scene=1&srcid=0826Yluv8ALwisncdvGNI9Y3&sharer_sharetime=1693046124469&sharer_shareid=075ab9d93676b59da2db56b4bd4b691c#rd](https://mp.weixin.qq.com/s?__biz=Mzg5MDY1NTg3OQ==&mid=2247484451&idx=1&sn=b3a96357e177cb5cc29c92f19b2f96b5&chksm=cfd801cbf8af88dde48fe616d466ad9893191249fcb4701ffc1871f26b618347bb5fab78a853&mpshare=1&scene=1&srcid=0826Yluv8ALwisncdvGNI9Y3&sharer_sharetime=1693046124469&sharer_shareid=075ab9d93676b59da2db56b4bd4b691c#rd)

[https://blog.csdn.net/weixin_44183483/article/details/119330911](https://blog.csdn.net/weixin_44183483/article/details/119330911)

[https://blog.csdn.net/T_I_A_N_/article/details/125239850](https://blog.csdn.net/T_I_A_N_/article/details/125239850)

[http://www.siwei.me/blog/posts/android-adb-root-adbd-cannot-run-as-root-in-production-builds](http://www.siwei.me/blog/posts/android-adb-root-adbd-cannot-run-as-root-in-production-builds)