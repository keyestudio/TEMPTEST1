# Arduino下载以及驱动安装

## 1 Arduino IDE安装

我们先到arduino官方的网站<https://www.arduino.cc/>下载最新版本的arduino开发软件,进入网站之后点击界面上的SOFTWARE,，选择DOWNLOADS进入下载页面，如下图：

![](../media/4636aac9aca9b3aa9d86580caac51b81.png)

Arduino 软件有很多版本，有wodows,mac linux系统的（如下图），而且还有过去老的版本，你只需要下载一个适合系统的版本。这里我们以WINDOWS系统的为例给大家介绍一下下载和安装的步骤。

![](../media/c12c9b34d9c8c91931cf0b6716eeeac5.png)

WINDOWS系统的也有两个版本，一个版本是安装版的，一个是下载版的不用安装，直接下载文件到电脑，解压缩就可以用了。

![](../media/3de06358873b1f90b42e88ae36fb36a2.png)两个版本都可以正常使用，看你自己的喜好了。选择一个版本，然后将Arduino
开发软件下载到我们的电脑。

![](../media/7c58250fe25d90cb4536978d98725bc5.png)

一般情况下，我们点击JUST DOWNLOAD就可以下载了。

## 2 ARDUINO UNO R3开发板

在开始所有的项目之前，我们首先要了解下面这片arduino uno R3开发板，因为这个智能车的核心就是这个开发板。

![](../media/3412008d30fb541910d27b7fd3c67530.jpg)

ARDUINO UNO R3开发板是我们最新推出的一款易用型开源控制器，硬件上与Arduino UNO相比并没有大的变动。外观上我们将蓝色换成了红色，给你们一种新的体验。硬件上，我们用ATmega16U2代替了8U2，这个更新为是USB接口芯片服务的，理论上它让UNO能模拟USB HID，比如MIDI/Joystick/Keyboard。

![](../media/259b91cad3470095d1eb58101f5db165.png)  
它具有14个数字输入/输出引脚（其中6个可用作PWM输出），6个模拟输入，一个16 MHz石英晶体，一个USB连接，一个电源插孔，2个ICSP接头和一个复位按钮。

![](../media/06ee496817391727502329769363c6e6.png)  
它包含支持微控制器所需的一切；只需使用USB电缆将其连接到计算机，或使用AC-DC适配器或电池为其供电即可开始使用。


| Microcontroller             | ATmega328P-PU                                            |
| --------------------------- | -------------------------------------------------------- |
| Operating Voltage           | 5V                                                       |
| Input Voltage (recommended) | DC7-12V                                                  |
| 数字引脚                    | 14 (D0-D13) (其中包含6个PWM输出口)                       |
| PWM引脚                     | 6 个(D3, D5, D6, D9, D10, D11)                           |
| 模拟输入引脚                | 6 个(A0-A5)                                              |
| 每个I / O引脚的直流电流     | 20 mA                                                    |
| 3.3V引脚的直流电流          | 50 mA                                                    |
| Flash Memory                | 32 KB (ATmega328P-PU) of which 0.5 KB used by bootloader |
| SRAM                        | 2 KB (ATmega328P-PU)                                     |
| EEPROM                      | 1 KB (ATmega328P-PU)                                     |
| 时钟频率                    | 16 MHz                                                   |
| LED按键                     | D13                                                      |

## 3 安装开发板驱动文件

接下来，我们将介绍UNO R3开发板的驱动程序安装。在不同的计算机系统中，驱动程序的安装可能略有不同。因此，下面我们继续在WIN 7系统中安装驱动程序。Arduino文件夹包含Arduino程序本身和驱动程序，这些驱动程序允许Arduino通过USB电缆连接到您的计算机。在我们启动Arduino软件之前，您将需要安装USB驱动程序。

![](../media/f8e5811e4e295f13e87d1d8aa441fbd9.jpeg)

将USB先的一端插入Arduino，另一端插入计算机上的USB插座。第一次将UNO板连接到计算机时，右键单击“计算机”图标-\>“属性”-\>单击“设备管理器”，在“其他设备”下，您应看到“未知设备”旁边带有一个黄色警告三角形。 这是您的Arduino。

![](../media/ec400b95c7271bb5fadce12be2f73fed.png)

然后右键单击设备，然后选择顶部菜单选项（更新驱动程序软件...），如下图所示。

![](../media/1598b59a32fbf5e844ef522a22b0bbad.png)

然后将提示您“自动搜索更新的驱动程序软件”或“浏览我的计算机以获取驱动程序软件”。如下图所示。 在此页面中，选择“浏览我的计算机以获取驱动程序软件”。

![](../media/931cabb3633c100c4d9760a26462321d.png)

之后，选择浏览器选项并导航到Arduino安装的“ drivers”文件夹。

![](../media/cca481d16263c158c26ea11e6c83cb5c.png)

单击“下一步”，您可能会收到安全警告，如果这样，则允许安装该软件。
如下图所示。

![](../media/5240132703a319a60cbf7e343d460900.png)

安装软件后，您将收到确认消息。 安装完成后，单击“关闭”。

![](../media/0f9c629828737c99d072f193aacc0ce2.png)

现在驱动程序已经安装好。然后您可以右键单击“计算机”-\>“属性”-\>“设备管理器”，您将看到如下图所示的设备。

![](../media/fc3b3afe1ae5c75ecfb2d2c321c73242.png)

## 4 添加库

1.首先复制链接到百度网盘下载我们提供的资料到电脑上，解压之后，找到文件名为“ke0165库文件”的文件，打开文件：

![image-20250425185345176](../media/image-20250425185345176.png) 

2.点击Arduino IDE菜单栏的文件（File）>首选项（Preference），弹出如下窗口

![img](../media/wps2.jpg) 

3.点击“浏览”，选择“Arduino”文件夹，打开“libraries”文件夹，把文件拖进去。

 ![image-20250425185556336](../media/image-20250425185556336.png)

## 5 Arduino IDE设置和工具栏介绍

装好了开发板的驱动，我们下面要了解Arduino开发软件的使用了，首先我们点击电脑桌面上的![](../media/15ee1732a5c94b90c848898712b66390.png)图标，打开Arduino IDE。

![](../media/1cded8c58d09814b4d0f5840c6b43c02.png)

为了避免在将程序上载到板上时出现任何错误，必须选择正确的Arduino板名称，该名称与连接到计算机的电路板相匹配。转到Tools→Board，然后选择你的板。

![](../media/23556d5d5178d3e9c78deff162329326.png)

然后再选择正确的COM口（安装驱动成功后可看到对应COM口）。

![](../media/fc3b3afe1ae5c75ecfb2d2c321c73242.png)

![](../media/0d7149770640729ad5031f43674832ba.png)

我们的程序上传到板之前，我们必须演示Arduino IDE工具栏中出现的每个符号的功能。

![](../media/4a2d854778c633819c1af28a245e340d.png)

A - 用于检查是否存在任何编译错误。

B - 用于将程序上传到Arduino板。

C - 用于创建新草图的快捷方式。

D - 用于直接打开示例草图之一。

E - 用于保存草图。

F - 用于从板接收串行数据并将串行数据发送到板的串行监视器。

## 6 启动你的第一个程序

上面我们学习了怎么下载软件和安装开发板的驱动，那下面我们就开始正式开始第一个程序，打开文件选择例子，选择第一个文件BASIC里面的BLINK程序

![](../media/a10884363fe0f51d8c7ffcd0cb2846db.png)

![](../media/a3c641837f358c1dd70d3ad1c916b102.png)

按照前面方法设置板和COM口，IDE右下角显示对应板和COM口。

![](../media/9c5b1d88c241ea35bbd10e119dbf36f0.png)

点击![](../media/ddd21c81338ae1f6b7f84de2a3caecf0.png)图标开始编译程序，检查错误，检查无误。

![](../media/177e1c9ae50aa822eec1c943dec3963b.png)

点击点击![](../media/9c9158a5d49baa740ea2f0048f655017.png)图标开始上传程序，上传成功。

![](../media/cdcdfaeba69bde24386b02cf6e75c29e.png)

程序上传成功，板载的LED灯亮一秒钟，灭一秒钟，恭喜你的第一个程序完成了！
