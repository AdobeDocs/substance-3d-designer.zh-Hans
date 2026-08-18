---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration/retrieving-the-installation-path.html"
breadcrumb-title: ''
description: 了解如何检索Substance 3D Designer安装路径以用于脚本编写和自动化目的。
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Retrieving the installation path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 检索安装路径
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 8%

---


# 检索安装路径

此页面根据版本和平台，对检索[Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)的安装路径的方法进行了重新分组。

## Windows

### Creative Cloud 桌面版

1. 打开<b>Windows注册表编辑器</b> (regedit)
1. 导航到注册表项： <b>HKEY\_LOCAL\_MACHINE\Software\Microsoft\Windows\CurrentVersion\App Paths\&lt;/b>
1. 打开名为<b>Adobe Substance 3D Designer.exe</b>的子密钥
1. 密钥的值包含安装该密钥的应用程序可执行文件的路径

>[!NOTE]
>
> 此注册表项仅从版本11.2开始可用。\
> 对于旧版本，可从HKEY\_CURRENT\_USER\Software\Microsoft\Windows\CurrentVersion\ Explorer\FileExts中的文件关联检索安装路径

### Substance版（独立）

1. 打开<b>Windows注册表编辑器</b> (regedit)
1. 导航到注册表项： <b>HKEY\_LOCAL\_MACHINE\ SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall</b>
1. 查找与应用程序版本的<b>AppID</b>匹配的子项（请参阅下表）
1. 密钥的值包含应用程序安装位置的路径

| 版本 | AppId |
| --- | --- |
| **版本5.x** | {25E7D16D-1FBA-49EA-BF36-E2D6B20A9206} |
| **版本6.x** | {09a302b1-8da8-4f62-b0cb-a208faa210f9} |
| **版本7.x (2017.x)到11.1** | {e9e3d6d9-3023-41c7-b223-11d8fdd691b9} |
| **版本11.2（或更高版本）** | {662bb79f-5616-44e6-a84d-b3d6abebe002} |

### Steam 版

应用程序安装在Steam安装文件夹的steamapps/common/子文件夹中。

## macOS

在Mac上，该应用程序安装在以下软件中：

| 版本 | 路径 |
| --- | --- |
| **11.2或更高版本** | **/Applications/Adobe Substance 3D Designer.app** |
| **旧版** | **/Applications/Substance Designer.app** |

## Linux

在Linux上， rpm软件包安装在以下路径中：

| 版本 | 路径 |
| --- | --- |
| **11.2或更高版本** | **/opt/Adobe/Adobe\_Substance\_3D\_Designer** |
| **旧版** | **/opt/Allegorithmic/Substance\_Designer** |
