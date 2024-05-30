<div align="center">

# Insta360_素材管理

[**中文简体**](./README.md) | [**English**](./README_en_US.md)

[![Licence](https://img.shields.io/badge/LICENSE-GPL3.0-green.svg?style=for-the-badge)](https://github.com/Han-Zhong/Insta360_MaterialOrganization/blob/main/LICENSE)

用来管理 "Insta360 Pro 2" 和 "Insta360 Titan"拍摄回来的素材

</div>

## 说明

> [!IMPORTANT]
> 此项目是因为每次insta360 pro2和titan拍摄回来以后每张卡素材需要合并、整理、检查等等
>
> 偶然发现MKlink软链接可以使用Insta360 Stitcher缝合，并且输出的目录是0kb，不占用空间！
>
> 故做此软件方便素材的合并、整理和检查！

支持的功能:

[✓] 统计Pro2和Titan 图像素材和视频素材 数目

[✓] 检查Pro2和Titan 卡目录数量和结构

[✓] 列出Pro2和Titan 所有素材 文件列表

[✓] 区分检查每个视频素材条目内文件名称和数量（Pro2为14个，Titan为18个）

[✓] 在GUI界面红色标出错误信息

[✓] 在GUI界面"文件列表"高亮红色错误 素材条目

[✓] 完全本地化运行，大小为1M左右 [![下载地址](https://img.shields.io/badge/软件下载-release-green)](https://github.com/Han-Zhong/Insta360_MaterialOrganization/blob/main/LICENSE)

> [!CAUTION]
> 声明：此项目只发布于 Github，基于 GPL3.0 协议，免费且作为开源学习使用。并且不会有任何形式的卖号、付费服务、讨论群、讨论组等行为。谨防受骗。


## 使用方法

### 预处理

- 使用 "Insta360 Pro 2" 和 "Insta360 Titan" 拍摄素材

- 预处理素材文件夹

``2024-03-24`` 为顶级目录，可以任意命名，我们拍摄多天的话为了方便所以命名为日期

``Pro2-A-0``...``Pro2-A-6`` 为Pro2 7张卡的文件夹，中间``A-Z``的意思是第几套卡，比如我们有3套卡（或者1套卡格式化了3次），那么命名为``Pro-A、Pro-B、Pro-C``，末尾``0-6``的意思是分别的7张卡（Pro2是1张SD卡 + 6张TF卡）

``Titan-A-0``...``Titan-A-8`` 为Titan 9张卡的文件夹，中间``A-Z``的意思是第几套卡，比如我们有3套卡（或者1套卡格式化了3次），那么命名为``Titan-A、Titan-B、Titan-C``，末尾``0-8``的意思是分别的9张卡（Titan是9张SD卡）

<details>
  <summary>
    预处理文件夹如下展开的树状图结构所示
  </summary>
  
```shell
2024-03-24
├─ Pro2-A-0
│    ├─ .LOST.DIR
│    ├─ .pro_suc
│    └─ VID_20240324_090228
│           ├─ origin_1_lrv.mp4
│           ├─ origin_2_lrv.mp4
│           ├─ origin_3_lrv.mp4
│           ├─ origin_4_lrv.mp4
│           ├─ origin_5_lrv.mp4
│           ├─ origin_6_lrv.mp4
│           ├─ preview.mp4
│           └─ pro.prj
├─ Pro2-A-1
│    ├─ .pro_suc
│    ├─ DCIM
│    ├─ EVENT
│    └─ VID_20240324_090228
│           └─ origin_1.mp4
├─ Pro2-A-2
│    ├─ .pro_suc
│    ├─ DCIM
│    ├─ EVENT
│    └─ VID_20240324_090228
│           └─ origin_2.mp4
├─ Pro2-A-3
│    ├─ .pro_suc
│    ├─ DCIM
│    ├─ EVENT
│    └─ VID_20240324_090228
│           └─ origin_3.mp4
├─ Pro2-A-4
│    ├─ .pro_suc
│    ├─ DCIM
│    ├─ EVENT
│    └─ VID_20240324_090228
│           └─ origin_4.mp4
├─ Pro2-A-5
│    ├─ .pro_suc
│    ├─ DCIM
│    ├─ EVENT
│    └─ VID_20240324_090228
│           └─ origin_5.mp4
├─ Pro2-A-6
│    ├─ .pro_suc
│    ├─ DCIM
│    ├─ EVENT
│    └─ VID_20240324_090228
│           └─ origin_6.mp4
├─ Titan-A-0
│    ├─ .LOST.DIR
│    ├─ .pro_suc
│    ├─ AMBA
│    ├─ EVENT
│    ├─ PIC_20240324_183332
│    │    ├─ gyro.mp4
│    │    ├─ origin_1_1.jpg
│    │    ├─ origin_1_2.jpg
│    │    ├─ origin_1_3.jpg
│    │    ├─ origin_1_4.jpg
│    │    ├─ origin_1_5.jpg
│    │    ├─ origin_1_6.jpg
│    │    ├─ origin_1_7.jpg
│    │    ├─ origin_1_8.jpg
│    │    ├─ origin_2_1.jpg
│    │    ├─ origin_2_2.jpg
│    │    ├─ origin_2_3.jpg
│    │    ├─ origin_2_4.jpg
│    │    ├─ origin_2_5.jpg
│    │    ├─ origin_2_6.jpg
│    │    ├─ origin_2_7.jpg
│    │    ├─ origin_2_8.jpg
│    │    ├─ origin_3_1.jpg
│    │    ├─ origin_3_2.jpg
│    │    ├─ origin_3_3.jpg
│    │    ├─ origin_3_4.jpg
│    │    ├─ origin_3_5.jpg
│    │    ├─ origin_3_6.jpg
│    │    ├─ origin_3_7.jpg
│    │    ├─ origin_3_8.jpg
│    │    ├─ pro.prj
│    │    └─ thumbnail.jpg
│    └─ VID_20240324_095334
│           ├─ origin_1_lrv.mp4
│           ├─ origin_2_lrv.mp4
│           ├─ origin_3_lrv.mp4
│           ├─ origin_4_lrv.mp4
│           ├─ origin_5_lrv.mp4
│           ├─ origin_6_lrv.mp4
│           ├─ origin_7_lrv.mp4
│           ├─ origin_8_lrv.mp4
│           ├─ preview.mp4
│           └─ pro.prj
├─ Titan-A-1
│    ├─ .pro_suc
│    ├─ AMBA
│    ├─ EVENT
│    ├─ PIC_20240324_183332
│    │    ├─ origin_1_1.dng
│    │    ├─ origin_2_1.dng
│    │    └─ origin_3_1.dng
│    └─ VID_20240324_095334
│           └─ origin_1.mp4
├─ Titan-A-2
│    ├─ .pro_suc
│    ├─ AMBA
│    ├─ EVENT
│    ├─ PIC_20240324_183332
│    │    ├─ origin_1_2.dng
│    │    ├─ origin_2_2.dng
│    │    └─ origin_3_2.dng
│    └─ VID_20240324_095334
│           └─ origin_2.mp4
├─ Titan-A-3
│    ├─ .pro_suc
│    ├─ AMBA
│    ├─ EVENT
│    ├─ PIC_20240324_183332
│    │    ├─ origin_1_3.dng
│    │    ├─ origin_2_3.dng
│    │    └─ origin_3_3.dng
│    └─ VID_20240324_095334
│           └─ origin_3.mp4
├─ Titan-A-4
│    ├─ .pro_suc
│    ├─ AMBA
│    ├─ EVENT
│    ├─ PIC_20240324_183332
│    │    ├─ origin_1_4.dng
│    │    ├─ origin_2_4.dng
│    │    └─ origin_3_4.dng
│    └─ VID_20240324_095334
│           └─ origin_4.mp4
├─ Titan-A-5
│    ├─ .LOST.DIR
│    ├─ .pro_suc
│    ├─ AMBA
│    ├─ EVENT
│    ├─ PIC_20240324_183332
│    │    ├─ origin_1_5.dng
│    │    ├─ origin_2_5.dng
│    │    └─ origin_3_5.dng
│    └─ VID_20240324_095334
│           └─ origin_5.mp4
├─ Titan-A-6
│    ├─ .pro_suc
│    ├─ AMBA
│    ├─ EVENT
│    ├─ PIC_20240324_183332
│    │    ├─ origin_1_6.dng
│    │    ├─ origin_2_6.dng
│    │    └─ origin_3_6.dng
│    └─ VID_20240324_095334
│           └─ origin_6.mp4
├─ Titan-A-7
│    ├─ .pro_suc
│    ├─ AMBA
│    ├─ EVENT
│    ├─ PIC_20240324_183332
│    │    ├─ origin_1_7.dng
│    │    ├─ origin_2_7.dng
│    │    └─ origin_3_7.dng
│    └─ VID_20240324_095334
│           └─ origin_7.mp4
└─ Titan-A-8
       ├─ .pro_suc
       ├─ AMBA
       ├─ EVENT
       ├─ PIC_20240324_183332
       │    ├─ origin_1_8.dng
       │    ├─ origin_2_8.dng
       │    └─ origin_3_8.dng
       └─ VID_20240324_095334
              └─ origin_8.mp4
```
</details>


### 界面

#### GUI

界面_软链接

![GUI](https://raw.githubusercontent.com/Han-Zhong/Insta360_MaterialOrganization/main/docs/gui_mklink.png)

界面_主界面:测试版界面

![GUI](https://raw.githubusercontent.com/Han-Zhong/Insta360_MaterialOrganization/main/docs/gui_main.png)

在 软链接界面中

1.选择你已经预处理的文件夹 我的是``Dailies\2024-03-24``

2.选择你的目标文件夹 我的是``D:\Test``

3.点击生成".bat"文件（会生成在本软件同目录下）

4.运行 .bat
