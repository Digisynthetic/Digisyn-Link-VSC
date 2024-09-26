# Digisyn Link AES67 Virtual Soundcard
![Digisyn Link Logo](https://static.jyshare.com/images/runoob-logo.png)

### Digisyn Link VSC is an AES67 virtual soundcard for Windows that turns your audio into AES67 streams. Which needs the [Digisyn Link](https://www.runoob.com)  controller to manage routings. The Digisyn Link VSC has been tested in the current network audio environment. Includes:
+ __Dante__
+ __Ravenna__
+ __Q-Lan__
+ __Telos__ 
+ __Crestron__

### Features include:
+ Auto discovery of streams via Session Announcement Protocol and manually adding streams by pasting SDP data. 

## 1. 兼容系统版本
本软件需要Win10以上系统，并且系统版本22H2及以上。
最好的版本为Win10 22H2版本，Win11较新的系统版本较不稳定，可能会兼容性不好



## 2. 软件安装
双击软件安装包安装，可以选择安装语言，支持简体中文/English：

选择安装路径、是否需要快捷方式等，一直“下一步”，等待安装完成即可。

## 3. 语言切换
在软件左上角，点击对应的按钮切换语言，支持简体中文/English：


## 4. 激活
点击软件右上角的激活按钮，弹出激活窗口，激活方式有两种：
+ 离线激活：对于不能访问网络的设备，可以复制机器ID，给厂家生成对应的证书导入激活。
+ 在线激活：对于可以访问网络的设备，使用激活码激活。


## 5. 功能设置

启动软件后，选择对应的有线网卡 <u>（只支持有线网卡，无线网卡不能满足超低延迟网络音频传输的要求）</u>


设置对应的采样率，支持48000KHz和96000Khz。


设置通道数量，在对应的范围内，可以自定义通道数量。
点击开启，等待一段时间，软件启动即可。

## 6. 其它设置

点击左上角“设置”按钮，可以打开自定义功能页面。


## 7. 播放、录制通道设置

启动虚拟声卡后，电脑系统的声音播放、录制列表会多出虚拟声卡的通道，

如stereo-01-02表示立体声1,2通道，对应与路由控制GUI中的1,2通道。


电脑播放、录制声音，选择对应的通道即可。


## 8. 问题排查

### 8.1  软件窗口显示过大
系统缩放比率过大导致，可以缩小系统分辨率显示缩放比例。

### 8.2 软件启动提示xxx.dll库缺失
提示dll库缺失，是电脑系统缺少微软运行库，下载“微软VC++运行库合集”安装可解决。

### 8.3 软件启动失败，提示检查驱动
查看电脑是否正确安装了驱动，驱动是软件安装时自动安装的，如果驱动安装失败会导致启动失败。


查看方法：鼠标移动到左下角<kbd>Win</kbd>图标，右键，点击 <kbd>设备管理器</kbd>

如下图则表示驱动正常，如果显示黄色感叹号，则驱动异常，尝试重启机器或者重新安装软件。

### 8.4 电脑声音没有找到虚拟声卡的选项

如果电脑声音播放、录制设备找不到虚拟声卡的选择，打开声音管理页面：


查看播放和录制页面是否有虚拟声卡设备：


如果上面存在但是处于禁用状态，鼠标右键启用即可。

如果开启了防火墙，需要将以下程序设置为允许联网：

+ ___DigisynLinkVSC_V3.0.exe___
+ ___DigisynRoute.exe___









