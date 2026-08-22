---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/getting-started/system-requirements.html"
breadcrumb-title: ''
description: 查看Substance 3D Designer的系统要求，确保您的计算机满足必要的规格。
helpx_creative_field: ""
helpx_description: Designer > Getting started > System requirements
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 系统要求
user-guide-description: ''
user-guide-title: ''
source-git-commit: ec787363bab8318804a71d6cf7c5484fc67a987e
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---


# 支持的系统

以下是应用程序支持的硬件和系统的列表：

## Windows

|  | 最小 | 推荐 | 最佳 |
| --- | --- | --- | --- |
| <b>操作系统</b> | Windows 11（64位）23H2版 | Windows 11（64位）24H1版 | Windows 11（64位）24H2版 |
| <b>CPU</b> | Intel Core i5 AMD Ryzen 5 | Intel Core i7 AMD Ryzen 7 | Intel Core i9 AMD Ryzen 9 |
| <b>GPU</b> | NVIDIA GeForce RTX 2060 Super NVIDIA Quadro RTX 4000 AMD Radeon RX 5700 XT AMD Radeon Pro W5700 | NVIDIA GeForce RTX 3080 NVIDIA Quadro RTX A4000 AMD Radeon RX 6800 XT AMD Radeon Pro W7700 | NVIDIA GeForce RTX 4090 NVIDIA Quadro RTX 5000 Ada代AMD Radeon RX 7900 XTX AMD Radeon Pro W7800 |
| <b>VRAM</b> | 8 GB | 16 GB | 24 GB |
| <b>RAM</b> | 16 GB | 32 GB | 64 GB |
| <b>存储空间</b> | 具有30 GB可用空间的固态硬盘 | 具有50 GB可用空间的固态硬盘 | 具有70 GB可用空间的固态硬盘 |

### macos

|  | 最小 | 推荐 | 最佳 |
| --- | --- | --- | --- |
| <b>操作系统</b> | macOS14 Sonoma | macOS26 Tahoe | macOS26 Tahoe |
| <b>CPU</b> | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| <b>GPU</b> | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| <b>RAM</b> | 16 GB | 32 GB | 64 GB |
| <b>存储空间</b> | 具有30 GB可用空间的固态硬盘 | 具有50 GB可用空间的固态硬盘 | 具有70 GB可用空间的固态硬盘 |

### Linux

| 企业 | 蒸汽 |
| --- | --- |
| RHEL 8 </br>RHEL 9 | Ubuntu 22.04 |

## 一般建议

* 为了在舒适的条件下工作，我们建议使用分辨率大于1 Mega像素且宽于1280像素的显示器。
* 许多Substance应用程序依靠OpenSSL 1.1.1来与RHEL8/9兼容。 对于具有较新OpenSSL版本的系统，您需要手动提供它。
* 为了在<b>MacOS 10.15</b> (Catalina)上运行，仅对&#x200B;*版本<b>2019.x</b>及更高版本进行了公证。*
* 如果OpenGL 3.3上下文可用，则可以<b>远程桌面</b>连接。 它将在<b>Nvidia Quadro</b>上工作，但在Nvidia GeForce上工作&#x200B;*而不是*，因为它仅提供OpenGL 1.4上下文。 如果这是一个问题，我们建议使用替代解决方案，例如<b>VNC</b>/<b>Teamviewer</b>。
* <b>Steam</b>版本用户应&#x200B;*禁用* Designer的<b>Steam叠加</b>，因为它可能会在活动时导致性能问题。

## 支持的GPU

以下是与该应用程序兼容的GPU列表：

* NVIDIA GeForce GTX 1060及更高版本
* NVIDIA Quadro P2200及更高版本
* AMD Radeon RX 580及更高版本
* AMD Radeon Pro 5300 M

>[!TIP]
>
> **TDR（仅限Windows）**
> 
> 为了在GPU上执行大量计算时获得最佳总体稳定性 — 例如，渲染复杂图形、3D视图渲染、从3D视图中导出场景等 — 强烈建议确保<b>超时检测和恢复(TDR)</b>值匹配我们文档的[此页面](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash)中的建议。

## 不支持的配置

<b>Windows</b>

* 不支持虚拟机。
* 不支持Windows Server。

<b>macOS</b>

* 不支持基于Intel的macOS系统。
* 仅支持官方Apple配置。
* eGPU当前不受支持，可能存在稳定性问题。

<b>Linux</b>

* 不支持Linux上的Mesa驱动程序。

<b>任何平台</b>

* x86-64 (Intel、AMD) CPU不支持集成GPU。
* 不支持将Designer与拦截Designer对图形驱动程序的调用的第三方软件结合使用。 此类软件包括：
  * 后期处理喷射器，例如应用颜色分级的整形器、相机效果等……
  * 屏幕叠加，例如自定义十字线、GPU性能度量、视频流的外观……

## 最低GPU驱动程序版本

下表列出了运行无问题的应用程序所需的最低GPU驱动程序版本。 此列表可能会随新版本发布而发生更改。

要下载新驱动程序，请参阅： [GPU具有过时的驱动程序](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-has-outdated-drivers)。

| 操作系统 | NVIDIA | AMD | Intel |
| --- | --- | --- | --- |
| <b>Windows</b> | GeForce 451.48 Quadro 451.48 | Radeon 19.7.1 Radeon Pro / FirePro 18.Q4 | 15.33 |
| <b>Linux</b> | 535.129.03 | Radeon 23.20 Pro 23.Q3 | 不支持 |

>[!NOTE]
>
> 在&#x200B;**Mac OS**&#x200B;上，GPU驱动程序由操作系统本身提供。 更新到最新版本的操作系统以访问最新驱动程序。

## 烘焙GPU 射线追踪

要通过Optix或DXR启用GPU 射线追踪，必须安装上面建议的驱动程序。

<b>DXR</b>需要以下最低配置：

* <b>Windows 10</b>版本1809，有关详细信息，请参阅[此页面](https://experienceleague.adobe.com/zh-hans/docs/substance-3d/bakers/features/gpu-raytracing)
* <b>具有Pascal体系结构的GPU</b> (Nvidia GeForce 10XX)

>[!TIP]
>
> GPU 射线追踪可在专用的光线追踪硬件（例如NVIDIA GeForce RTX或NVIDIA Quadro RTX GPU）上以最佳方式运行。

## 使用平板电脑

<b>Windows</b>上的Tablet用户应应用以下页面中描述的设置以获得最可靠的体验： [配置笔和平板电脑](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-painter/using/technical-support/configuring-pens-and-tablets)。

## 语言

软件界面提供以下语言版本：

* 德语(Deutschland)
* 英语（美国）
* 西班牙语（西班牙）
* Français（法国）
* 意大利语（意大利）
* 葡萄牙语（巴西）
* 日本語（日本)
* 한국어(한국)
* 简体中文（中国)
