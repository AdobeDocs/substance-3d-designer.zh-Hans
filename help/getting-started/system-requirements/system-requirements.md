---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/getting-started/system-requirements.html"
breadcrumb-title: ""
description: 查看Substance 3D Designer的系统要求，确保您的计算机满足必要的规格。
helpx_creative_field: ""
helpx_description: Designer > Getting started > System requirements
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 系统要求
user-guide-description: ""
user-guide-title: ""
source-git-commit: aeb517a0def4b5bc2de723633f8932dfc03f052c
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%
---

# 系统要求

以下是应用程序支持的硬件和系统的列表：

## 按平台划分的系统配置

### Windows

|             | 最小 | 推荐 | 最佳 |
|:------------|:---------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| **操作系统** | Windows 11（64位）23H2版 | Windows 11（64位）24H1版 | Windows 11（64位）24H2版 |
| **CPU** | Intel Core i5<br>AMD Ryzen 5 | Intel Core i7<br>AMD Ryzen 7 | Intel Core i9<br>AMD Ryzen 9 |
| **GPU** | NVIDIA GeForce RTX 2060 Super<br>NVIDIA Quadro RTX 4000<br>AMD Radeon RX 5700 XT<br>AMD Radeon Pro W5700 | NVIDIA GeForce RTX 3080<br>NVIDIA Quadro RTX A4000<br>AMD Radeon RX 6800 XT<br>AMD Radeon Pro W7700 | NVIDIA GeForce RTX 4090<br>NVIDIA Quadro RTX 5000 Ada代<br>AMD Radeon RX 7900 XTX<br>AMD Radeon Pro W7800 |
| **VRAM** | 8 GB | 16 GB | 24 GB |
| **RAM** | 16 GB | 32 GB | 64 GB |
| **存储空间** | 具有30 GB可用空间的固态硬盘 | 具有50 GB可用空间的固态硬盘 | 具有70 GB可用空间的固态硬盘 |

### macOS

|             | 最小 | 推荐 | 最佳 |
|:------------|:----------------------------------|:----------------------------------|:----------------------------------|
| **操作系统** | macOS14 Sonoma | macOS26 Tahoe | macOS26 Tahoe |
| **CPU** | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| **GPU** | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| **RAM** | 16 GB | 32 GB | 64 GB |
| **存储空间** | 具有30 GB可用空间的固态硬盘 | 具有50 GB可用空间的固态硬盘 | 具有70 GB可用空间的固态硬盘 |

### Linux

| 企业 | 蒸汽 |
|:------------------|:-------------|
| RHEL 8</br>RHEL 9 | Ubuntu 22.04 |

## 一般建议

* 为了在舒适的条件下工作，我们建议使用分辨率大于1 Mega像素且宽于1280像素的显示器。
* 许多Substance应用程序依靠OpenSSL 1.1.1来与RHEL8/9兼容。 对于具有较新OpenSSL版本的系统，您需要手动提供它。
* 为了在&#x200B;**macOS 10.15 Catalina**&#x200B;上运行，仅对&#x200B;*个版本&#x200B;**2019.x**&#x200B;及更高版本进行了公证。*
* 如果OpenGL 3.3上下文可用，则可以&#x200B;**远程桌面**&#x200B;连接。 它将在&#x200B;**Nvidia Quadro**&#x200B;上工作，但在Nvidia GeForce上工作&#x200B;*而不是*，因为它仅提供OpenGL 1.4上下文。 如果这是一个问题，我们建议使用替代解决方案，例如&#x200B;**VNC/Teamviewer**。
* **Steam**&#x200B;版本用户应&#x200B;*禁用* Designer的&#x200B;**Steam叠加**，因为它可能会在活动时导致性能问题。

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
> 在GPU上执行繁重的计算时（例如，渲染复杂图形、3D视图渲染、从3D视图中导出场景等），为获得最佳整体稳定性，强烈建议确保&#x200B;**超时检测和恢复(TDR)**&#x200B;值与我们文档的[本页](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash)中的建议相匹配。

## 不支持的配置

**Windows**

* 不支持虚拟机。
* 不支持Windows Server。

**macOS**

* 不支持基于Intel的macOS系统。
* 仅支持官方Apple配置。
* eGPU当前不受支持，可能存在稳定性问题。

**Linux**

* 不支持Linux上的Mesa驱动程序。

**任何平台**

* x86-64 (Intel、AMD) CPU不支持集成GPU。
* 不支持将Designer与拦截Designer对图形驱动程序的调用的第三方软件结合使用。 此类软件包括：
  * 后期处理喷射器，例如应用相机分级、颜色效果的重新着色器……
  * 屏幕叠加，例如自定义十字线、GPU性能度量、视频流的外观……

## 最低GPU驱动程序版本

下表列出了运行无问题的应用程序所需的最低GPU驱动程序版本。 此列表可能会随新版本发布而发生更改。

要下载新驱动程序，请参阅： [GPU具有过时的驱动程序](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-has-outdated-drivers)。

| 操作系统 | NVIDIA | AMD | Intel |
|:------------|:-----------------------------|:-----------------------------------------|:------------|
| **Windows** | GeForce 451.48 Quadro 451.48 | Radeon 19.7.1 Radeon Pro / FirePro 18.Q4 | 15.33 |
| **Linux** | 535.129.03 | Radeon 23.20 Pro 23.Q3 | 不支持 |

>[!NOTE]
>
> 在&#x200B;**macOS**&#x200B;上，GPU驱动程序由操作系统本身提供。 更新到最新版本的操作系统以访问最新驱动程序。

## 烘焙GPU 射线追踪

要通过Optix或DXR启用GPU 射线追踪，必须安装上面建议的驱动程序。

**DXR**&#x200B;需要以下最低配置：

* **Windows 10**&#x200B;版本1809，有关详细信息，请参阅[此页面](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing)
* **具有Pascal体系结构的GPU** (Nvidia GeForce 10XX)

>[!TIP]
>
> GPU 射线追踪可在专用的光线追踪硬件（例如NVIDIA GeForce RTX或NVIDIA Quadro RTX GPU）上以最佳方式运行。

## 使用平板电脑

**Windows**&#x200B;上的Tablet用户应应用以下页面中描述的设置以获得最可靠的体验： [配置笔和平板电脑](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/configuring-pens-and-tablets)。

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
