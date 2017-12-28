# BlueUtils
经典蓝牙搜索，连接，数据传输小DEMO

通过经典模式 搜索 蓝牙应用。蓝牙有蓝牙1.0、蓝牙2.0、蓝牙3.0、蓝牙4.0之类的以数字结尾的蓝牙版本号，而实际上，在最新的标准中，
已经不再使用数字版本号作为蓝牙版本的区分了，取而代之的是经典蓝牙与低功耗蓝牙（BLE）这两种区别。
BLE 蓝牙不做过多讲解。具体的信息大家可以参考。
 http://www.loverobots.cn/the-analysis-is-simple-compared-with-the-classic-bluetooth-and-bluetooth-low-energy-in-android.html

# 流程
  发现设备->配对/绑定设备->建立连接->数据通信
  经典蓝牙和低功耗蓝牙除了配对/绑定这个环节是一样的之外，其它三个环节都是不同的。
  
# 详解
  公司最近在要做一个蓝牙与串口通讯的项目，然后就涉及到手机端与蓝牙的连接及数据交互。大致需求就是通过手机搜索硬件蓝牙设备，然后
  连接上蓝牙，通过手机端的指令消息来获取串口信息，在通过蓝牙返回数据到手机端。在这之前看了一些开源的项目 包括BluetoothKit，FastBle，BluetoothHelper等
  其中BluetoothKit和FastBle只支持BLE 模式蓝牙，因为硬件的模式是经典模式，后来自己在两个项目的基础上做了一些修改，然后可以搜索到经典蓝牙。但是怎么也是
  链接不上我们的硬件设备。（应该是底层不是经典蓝牙连接导致。）后来发现了BluetoothHelper等项目。在这个项目的基础上做了一些修改及优化 ，能够满足项目需求，
  现在将这个项目做了分包及优化。然后在这分享自己的一些踩坑心得。

