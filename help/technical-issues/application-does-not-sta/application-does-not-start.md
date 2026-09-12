---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/application-does-not-start.html"
breadcrumb-title: ''
description: 解决阻止Substance 3D Designer启动的问题，并找到启动该应用程序的解决方案。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Application does not start
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 应用程序不启动
user-guide-description: ''
user-guide-title: ''
source-git-commit: 734525cdd187aac666168f8a9e1f9e49f3dad03e
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 1%

---


# 应用程序不启动

本页列出了Substance 3D Designer无法正确启动的常见原因，并针对每个原因提供了按操作系统分组的故障排除步骤：

[Designer 15.0及更高版本](#version-15-0)

[Windows 10/11](#windows-10-11)

[Windows 7/8/8.1](#windows-7-8)

[Linux](#linux)

## Designer 15.0及更高版本

<b>![（错误）](application-does-not-start.resources/error.svg)问题</b>

在同时具有集成GPU (iGPU)和独立GPU (dGPU)的系统上，无法启动版本15.0及更高版本的Designer。

<b>![（刻度）](application-does-not-start.resources/check.svg)建议的步骤</b>

更新iGPU的图形驱动程序。 您可以在此处找到最新的驱动程序： [Intel](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)  | [AMD](https://www.amd.com/en/support/download/drivers.html)

## Windows 10/11

**![（错误）](application-does-not-start.resources/error.svg)问题**

Substance 3D Designer在使用Windows 10或Windows 11的系统上无法启动。

**![（刻度）](application-does-not-start.resources/check.svg)建议的步骤**

由于在许可证验证过程中使用了&#x200B;*过时* `libeay32.dll`库，旧版本的Designer可能无法在Windows 10或Windows 11上启动。

您可以尝试用&#x200B;*更新版本*&#x200B;替换库，例如在[此处](https://support.networkoptix.com/hc/en-us/articles/115015730007-Nx-Software-crashes-due-to-libeay32-dll-on-Windows)分发的版本（为32位Windows选择文件），步骤如下：

1. 在Designer的安装目录中找到`libeay32.dll`文件
1. 如果将来需要恢复文件，请将文件备份到安全位置
1. 用更新后的版本替换文件
1. 启动Designer

>[!WARNING]
>
> 不支持的配置
> 
> 不支持Windows 10。 您可以在[系统要求](../../getting-started/system-requirements/system-requirements.md)页面上了解更多信息。
> 
> 不支持维护期之外的Designer版本。 如果对系统进行了重大更改（例如操作系统升级），这些版本可能无法再可靠地运行。

## Windows 7/8/8.1

**![（错误）](application-does-not-start.resources/error.svg)问题**

Substance 3D Designer在使用Windows 7、Windows 8或Windows 8.1的系统上无法启动。

**![（刻度）](application-does-not-start.resources/check.svg)建议的步骤**

作为版本&#x200B;**11.3.0**&#x200B;更新的一部分，我们升级了多个库、工具和SDK，其中&#x200B;*破坏了与Windows 10以下版本的Windows的兼容性*。

我们&#x200B;*强烈*&#x200B;建议升级到Windows 10，因为Microsoft本身不再支持以前版本的Windows供主流使用（请参阅[此处](https://www.microsoft.com/en-us/windows/windows-7-end-of-life-support-information)和[此处](https://docs.microsoft.com/en-us/lifecycle/faq/windows#windows-8.1)）。 因此，继续使用这些版本会出现&#x200B;*安全问题*。\
如果无法升级到Windows 10，请&#x200B;*不要更新*&#x200B;您安装的Designer *过去*&#x200B;版本&#x200B;**11.2.2**。

>[!WARNING]
>
> 不支持的配置
> 
> 请注意，Windows 7、Windows 8和Windows 8.1 *未正式受支持*。 您可以在[系统要求](../../getting-started/system-requirements/system-requirements.md)页面上了解更多信息。

## Linux

<b>![（错误）](application-does-not-start.resources/error.svg)问题</b>

关闭主屏幕并显示主窗口时崩溃。

<b>![（刻度）](application-does-not-start.resources/check.svg)建议的步骤</b>

Designer无法加载Python组件，因为它加载系统的<b>libffi.so</b>库，而不是它自己的库。

为确保Designer加载其自己的库，请在Designer的安装目录下使用此命令，将`%command%`替换为运行Designer的命令：

```
LD_PRELOAD=./plugins/pythonsdk/lib/python3.11/lib-dynload/libffi.so.6 %command%
```


请注意，Python版本号取决于正在运行的Designer版本：

* 低于14.0.0： python3.9
* 低于12.1.0： python3.7

+++Steam启动选项
从Steam启动Designer的Linux用户可以在Designer的启动选项中设置LD\_PRELOAD命令，如下所示。

完成此操作后，Designer可能会在Steam中正常启动，以供将来所有会话使用。

![蒸汽启动选项](application-does-not-start.resources/steam_linux_launch_option.jpg "蒸汽启动选项")



+++

**![（错误）](application-does-not-start.resources/error.svg)问题**

Designer的Steam版本无法启动，并且不生成错误消息。

**![（刻度）](application-does-not-start.resources/check.svg)建议的步骤**

您可以通过记录Steam应用程序来获取错误消息。

按照[此处](https://github.com/ValveSoftware/steam-for-linux/issues/7114#issuecomment-629634260)的建议，完全关闭Steam，然后从终端运行以下命令（或为此命令创建快捷键）：

```
steam 2>&1 | tee /path/to/logfile
```


<b>![（错误）](application-does-not-start.resources/error.svg)问题</b><b>e</b>

无法加载`<b>xcb</b>`插件。 命令行中显示以下消息：

```
qt.qpa.plugin: Could not load the Qt platform plugin "xcb" in "" even though it was found. 

This application failed to start because no Qt platform plugin could be initialized. Reinstalling the application may fix this problem. 

 

Available platform plugins are: minimal, offscreen, xcb. 

 

Aborted (core dumped)
```


**![（刻度）](application-does-not-start.resources/check.svg)建议的步骤**

缺少某些必需的包。 从Designer的安装目录运行以下命令：

```
ldd libQt5XcbQpa.so.5
```


在打印的列表中检查报告为`not found`的任何包，然后为每个缺失的包运行以下命令：

```
apt-get install <package-name>
```


E.g.

```
apt-get install libxcb-xinput0
```


<b>![（错误）](application-does-not-start.resources/error.svg)问题</b>

启动Designer时发生此错误：

```
error while loading shared libraries: libcrypt.so.1: cannot open shared object file: No such file or directory
```


Designer加载的系统库与Designer自己的<b>libcrypto.so.1.1</b>库不兼容。

<b>![（刻度）](application-does-not-start.resources/check.svg)建议的步骤</b>

从Designer安装目录中删除<b>`libcrypto.so.1.1`</b>库，以便改用系统的库。

>[!NOTE]
>
> 仅当系统有自己的libcrypto.so.1库时，此解决方法才有效。 在最近的分发中，可能需要安装兼容包，如<b>libxcrypt-compat</b>。

<b>![（错误）](application-does-not-start.resources/error.svg)问题</b>

在使用&#x200B;*基于Arch*&#x200B;的Linux分发版本的系统上，Substance 3D Designer无法启动。

**![（刻度）](application-does-not-start.resources/check.svg)建议的步骤&#x200B;*(![（警告）](application-does-not-start.resources/warning.svg)不稳定，仅限AMD GPU！)***

尝试安装&#x200B;**progl**（属于[AMDGPU-PRO](https://wiki.archlinux.org/title/AMDGPU_PRO)驱动程序），并通过它启动Designer。 您可以使用应用程序启动命令中的`progl`前缀执行此操作：

```
progl <designer-application-path>
```


请注意，`progl`可能不稳定。 因此，应将此作为&#x200B;*最后手段*&#x200B;来尝试。

>[!WARNING]
>
> 请注意，基于Arch的Linux发行版&#x200B;*不受支持*。 您可以在[系统要求](../../getting-started/system-requirements/system-requirements.md)页面上了解更多信息。
