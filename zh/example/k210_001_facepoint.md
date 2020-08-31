# K210 实现人脸关键点检测教程


## 概述

## 实例

- 运行方法
- 实例效果
- 实例解析
- 注意事项

# K210 实现人脸关键点检测教程


章节贡献：

    作者：Jungang An

    [博客]:https://blog.csdn.net/yunxinan

    [联系方式]:1090542758@qq.com

## 概述
   本教程主要是针对基于嘉楠科技的K210的RSIC-V指令芯片的Sipeed开发板实现人脸关键点检测（landmark）详细教程

## 实例

- 运行方法
   第一步：Kflash_gui_1.6.5安装驱动烧录工具，该工具可以在window、ubuntu、maco。驱动下载地址： https://cn.dl.sipeed.com/MAIX/tools/kflash_gui   

   第二步：下载更新文件ken_gen.bin后使用kflash_gui工具将驱动升级的更新文件下发给开发板来完成板卡刷新系统，波特率：115200，速度模式：高速模式，开发板选择自己的开发板类型，下载到是你的开发板内存，在本次实验没安装内存卡所以之间下载到flash,更新文件地址:https://dl.sipeed.com/MAIX/MaixHub_Tools 下载key_gen_v1.2bin。（注意：在这个过程中要注意端口COM的检测，如果没法正常连接的时候要使用最新的驱动工具或者换用手机的type-c数据线）

   第三步：通过串口查询机器码使用putty或者使用mobaxterm工具。（注意：如果该过程出现机器码长时间无法显示时候板卡上面有个蓝色的灯的复位键重新复位一下同时重新烧录一下ken_gen.bin文件）
   
   第四步：通过获取的机器码验证链接官方的Hub下载模型文件及其相关配置文件,在下载的文件kfpkg包里面其实一个是配置文件json，其他是驱动文件和模型权重文件。模型下载地址：https://www.maixhub.com/index.php/index/user/download/id/22,接下来使用Kflash工具将模型烧录到板卡上。

   第五步：使用编辑器链接开发板编译代码实现整体功能

- 实例效果

   实验效果后续用图片方式上传说明

- 实例解析

   这是一个完整的人工智能项目小工程，在学习和理解方面非常有帮助，主要体现在以下方面：

   1：开发板测试

   2：开发板驱动

   3：系统安装

   4：模型环境安装

   5：模型推理加载

- 注意事项

    1：数据链接线要采用可以通信的不能使用只是单一供电的数据线。

    2：获取机器码过程中如果停顿就按复位键进行恢复

    3：编译器链接时候如果长时间链接不到com端口就按复位键或者重复换数据线


relatework
https://github.com/sipeed/MaixPy_scripts