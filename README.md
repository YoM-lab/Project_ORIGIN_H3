## Project-ORIGIN_H3
![](6_Docs/Image1.jpg)

## 项目简介
> 小up是一个开发板兴趣爱好者:-)，市面上绝大部分Linuix开发板都是没有小巧屏幕的，而且设计闭源不能随心所欲的更改，只是买回来玩并不能深刻理解，引用费曼所说：“What I cannot create，I do not understand”，结合网上的开源方案，所以就有了想自己制作的想法，一来是想熟悉Allegro软件，二来是巩固Linux驱动开发。现在发布出来供后来人参考，同时也参考一些开源社区和UP主，后面会一一列出。硬件在23年5月份完成，由于up是一个学生，制作过程全部自费，所以采用了四层板，对于初学者走线非常痛苦:-(；软件在23年9月份完成，由于研二阶段太忙了，一直到现在才正式发出来:-)
>
> 项目在硬件上包括了1.14寸显示屏、麦克风、音频、HDMI、WIFI、MIPI摄像头(未驱动成功，非必须)，基本上可以实现一个卡片电脑的功能。

**项目制作流程**：[【自制】开源四核A7卡片电脑，从规划到实物软硬件开发，拥有自己的小电脑](https://www.bilibili.com/video/BV1XW421P7bK/?share_source=copy_web&vd_source=7833e202419e0abc2ac3d27a5c3fbd21)

## 硬件部分

* 硬件设计全部在**1_Hardware**文件夹
* 设计使用的**软件是Allegro，而不是AD！！！**在**1_Hardware**文件夹内给出了原理图
* 焊接使用了**加热台、热风枪、低温焊锡膏、钢网**
* 由于up只进行了一次打板（自费），在后期难免的遇到了一些问题，大部分都是因为板层不够多（四层）导致的，**但不影响第一板的正常运行**。up时间有限，未能作出更改，如果有后来者复刻，可以上六层板，进一步缩小体积，方便布线，项目硬件上可改进之处参考**1_Hardware/README.md**文件
## 软件部分

* **Uboot**
	
	* 在**2_Uboot**文件夹内
	* Uboot适配的是全志官方支线，没有做出太多修改
* **Linux**
	* 在**3_Linux**文件夹内
	* 内核是自己适配4.14.111内核，也可采用第三方内核（国内开发板厂商）
* **Rootfs** 
	* 在**4_Rootfs**文件夹内
	
	* 根文件系统是自己移植的ubuntu16.04， 也可采用第三方根文件系统（国内开发板厂商）
* 编译方法可以参考教程：[Building U-boot and Linux for H5/H3/H2+/zh - FriendlyELEC WiKi](https://wiki.friendlyelec.com/wiki/index.php/Building_U-boot_and_Linux_for_H5/H3/H2+/zh)
* 由于Github不能上传大文件，所以请大家通过百度云下载:-(

## 烧录镜像
* 烧录SD镜像在**5_Images**文件夹内
* Ubuntu16.04为个人制作的镜像，用户名：pi，密码：pi，root密码：oh3
* Debian 8为第三方镜像，参考连接：[NanoPi M1 Plus/zh - FriendlyELEC WiKi](https://wiki.friendlyelec.com/wiki/index.php/NanoPi_M1_Plus/zh#Linux-3.4.E5.92.8CLinux-4.14.E7.B3.BB.E7.BB.9F.E5.9B.BA.E4.BB.B6.E5.B7.AE.E5.BC.82)
## 驱动部分

* Linux简单的驱动移植在7_Drivers文件夹内，在up本人学习时编写的，把ORIGIN_H3当成一个小型的开发板:-)
* MPU6050驱动在21_I2C文件夹内
* 驱动编写参考：[i.MX6ULL Linux阿尔法开发板 — 正点原子资料下载中心 1.0.0 文档 (openedv.com)](http://www.openedv.com/docs/boards/arm-linux/zdyz-i.mx6ull.html)

## 参考链接

* [NanoPi M1 Plus/zh - FriendlyELEC WiKi](https://wiki.friendlyelec.com/wiki/index.php/NanoPi_M1_Plus/zh#Linux-3.4.E5.92.8CLinux-4.14.E7.B3.BB.E7.BB.9F.E5.9B.BA.E4.BB.B6.E5.B7.AE.E5.BC.82)
* [orangepi-xunlong (Orange Pi) (github.com)](https://github.com/orangepi-xunlong)
*  [OSHW\] Yuzuki Chameleon is a Raspberry Pi A Shaped SBC based on Allwinner H616 (github.com)](https://github.com/YuzukiHD/YuzukiChameleon)
* [peng-zhihui/Project-Quantum: 超迷你模块化卡片电脑计划 (github.com)](https://github.com/peng-zhihui/Project-Quantum)
* [小白自制Linux开发板(F1C200s)整理系列，持续更新中 / 全志 SOC / WhyCan Forum(哇酷开发者社区)](https://whycan.com/t_7275.html)
* [i.MX6ULL Linux阿尔法开发板 — 正点原子资料下载中心 1.0.0 文档 (openedv.com)](http://www.openedv.com/docs/boards/arm-linux/zdyz-i.mx6ull.html)

