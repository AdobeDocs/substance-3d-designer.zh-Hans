---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/technical-issues/cannot-create-load-a-project.html"
breadcrumb-title: ''
description: 解决在Substance 3D Designer中创建或加载项目时出现的问题并查找解决方案。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Cannot createload a project
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 无法创建加载项目
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 0%

---


# 无法创建/加载项目

本页列出了在Substance 3D Designer中创建或加载项目失败的常见原因，并针对每个原因提供了故障排除步骤。

## 应用程序太旧，无法打开URL

**![（错误）](../../assets/error.svg)问题**

**Substance 3D文件(SBS)**&#x200B;正由&#x200B;*不支持其格式*&#x200B;的Substance 3D Designer版本加载。 Substance 3D文件可能&#x200B;*保存为较新的软件版本*，该软件对这些文件使用了更新的格式。

**![（刻度）](../../assets/check.svg)建议的步骤**

随着Substance 3D Designer的发展，Substance 3D文件格式(SBS)也将不断发展。 新版本的软件通常需要&#x200B;*更新您的文件*，以便它们可以支持最新功能。

在新版本中首次&#x200B;*加载文件*&#x200B;时，将&#x200B;*提示*&#x200B;您执行此更新。

>[!WARNING]
>
> 如果在应用更新&#x200B;*后*&#x200B;保存了文件，则其格式版本也会更改。 此时，*无法再在Substance 3D Designer的早期版本*&#x200B;中加载。
> 
> 此限制也适用于[Substance Player](https://helpx.adobe.com/substance-3d-player/home.html)。

首先，检查您使用的是否是当前许可证允许的最新版本的Substance 3D Designer。 以下是每个版本的更新访问点：

* <b>Substance 3D订阅：</b>转到[Adobe Creative Cloud桌面](https://creativecloud.adobe.com/en/apps/download/creative-cloud)应用程序中“应用程序”选项卡的“更新”部分
* <b>[Substance3d.com](http://Substance3d.com)订阅：在Substance 3D Designer中提示时更新</b>，或在[订阅3d.com](http://substance3d.com)网站的[我的Substance](https://store.substance3d.com/user)部分中下载最新安装程序
* <b>Steam：</b>应用程序将默认自动更新。 您可以通过启动Substance 3D Designer或转到“下载”屏幕手动触发更新

>[!WARNING]
>
> 在保存&#x200B;*已更新的文件之前，请确保您不需要在Substance 3D Designer*&#x200B;的早期版本中加载您的文件。
> 
> 或者，您可以&#x200B;*在文件*&#x200B;的副本&#x200B;*之后*&#x200B;将其加载到新版本的Substance 3D Designer中，以便您始终有一个文件可以返回到，如果您需要使用软件的早期版本。

## 创建或加载项目时崩溃

<b>！[（错误）](../../assets/error.svg)问题</b>

创建或加载项目时崩溃通常是由初始化[3D视图](../../interface/3d-view/3d-view.md)期间出错（在设置工作区时发生）引起的。

如果系统是笔记本电脑，第三方应用程序可能会强制执行&#x200B;*电源管理计划*，以阻止3D视图使用系统的GPU。 如果其他GPU设备均无法代替自己执行任务，则可能会导致崩溃。

如果在会话之间更改&#x200B;*显示配置或缩放*，以便3D视图渲染帧在无效坐标下创建，也可能会发生崩溃。

<b>！[(tick)](../../assets/check.svg)建议的步骤</b>

考虑到导致此崩溃的多种可能原因，我们建议按顺序执行以下故障诊断步骤：

更新图形驱动程序

首先，确保图形驱动程序是最新的。 您可以在[此处](https://www.nvidia.com/Download/index.aspx?lang=en-us) (NVIDIA)、[此处](https://www.amd.com/en/support) (AMD)或[此处](https://downloadcenter.intel.com/product/80939/Graphics-Drivers) (Intel)找到您的GPU的最新版本。

强制实现最佳性能

查找任何管理您系统的&#x200B;*电源计划*&#x200B;的软件（例如，华硕军械库板条箱），尤其是当系统为笔记本电脑时。

某些电源管理应用程序可能会限制其他应用程序对系统GPU的访问，或妨碍GPU的性能，从而可能导致崩溃。 如果电源管理应用程序存在且处于活动状态，请切换到可实现最佳性能的计划。

强制使用离散GPU

如果您的系统具有&#x200B;*可切换图形*，请考虑对Substance 3D应用程序强制使用独立GPU (dGPU)。

大多数情况下，这可以通过控制GPU设置的专用应用程序实现。 例如，对于NVIDIA GPU，您可以在“NVIDIA控制面板”应用程序中执行此操作。

重置保存在注册表中的用户界面

如果崩溃是由显示配置或缩放中的更改引起的，您可以尝试删除Designer的现有注册表项，以完全重置用户界面以及其他设置。

按操作系统执行此重置的过程说明如下：

+++Windows
* 关闭Designer

关闭Designer

* 打开<b>命令提示符</b>应用程序

打开<b>命令提示符</b>应用程序

* 输入以下命令并按<b>Enter</b>：

  <b>桌面Creative Cloud</b>

  ```
  reg delete "HKEY_CURRENT_USER\Software\Adobe\Adobe Substance 3D Designer" /f
  ```


  <b>蒸汽/Substance版本</b>

  ```
  reg delete "HKEY_CURRENT_USER\Software\Allegorithmic\Substance Designer" /f
  ```


输入以下命令并按<b>Enter</b>：

<b>桌面Creative Cloud</b>

<b>蒸汽/Substance版本</b>

* 断开第二个显示器与系统的连接，然后将其连接回来（如果您&#x200B;*未*&#x200B;连接多个显示器，请忽略此步骤）

断开第二个显示器与系统的连接，然后将其连接回来（如果您&#x200B;*未*&#x200B;连接多个显示器，请忽略此步骤）

* 启动Designer，但&#x200B;*不*&#x200B;创建或打开任何项目

启动Designer，但&#x200B;*不*&#x200B;创建或打开任何项目

* 在顶部栏中，打开<b>窗口</b>菜单并选择<b>新建3D视图</b>选项

在顶部栏中，打开<b>窗口</b>菜单并选择<b>新建3D视图</b>选项

* 检查<b>3D视图</b>是否正确初始化，然后在面板顶栏的<b>场景</b>菜单中尝试不同的预览网格

检查<b>3D视图</b>是否正确初始化，然后在面板顶栏的<b>场景</b>菜单中尝试不同的预览网格

* 创建或打开材质

创建或打开材质

+++

+++macOS
* 关闭Designer

关闭Designer

* 打开<b>终端</b>应用程序

打开<b>终端</b>应用程序

* 输入以下命令并按<b>Enter</b>：

  <b>桌面Creative Cloud</b>

  ```
  rm ~/Library/Preferences/com.adobe.Adobe\ Substance\ 3D\ Designer.plist
  ```


  <b>蒸汽/Substance版本</b>

  ```
  rm ~/Library/Preferences/com.allegorithmic.Substance\ Designer.plist
  ```


输入以下命令并按<b>Enter</b>：

<b>桌面Creative Cloud</b>

<b>蒸汽/Substance版本</b>

* 断开第二个显示器与系统的连接，然后将其连接回来（如果您&#x200B;*未*&#x200B;连接多个显示器，请忽略此步骤）

断开第二个显示器与系统的连接，然后将其连接回来（如果您&#x200B;*未*&#x200B;连接多个显示器，请忽略此步骤）

* 启动Designer，但&#x200B;*不*&#x200B;创建或打开任何项目

启动Designer，但&#x200B;*不*&#x200B;创建或打开任何项目

* 在顶部栏中，打开<b>窗口</b>菜单并选择<b>新建3D视图</b>选项

在顶部栏中，打开<b>窗口</b>菜单并选择<b>新建3D视图</b>选项

* 检查<b>3D视图</b>是否正确初始化，然后在面板顶栏的<b>场景</b>菜单中尝试不同的预览网格

检查<b>3D视图</b>是否正确初始化，然后在面板顶栏的<b>场景</b>菜单中尝试不同的预览网格

* 创建或打开材质

创建或打开材质

+++
