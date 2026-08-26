---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/getting-started/activation-and-licenses.html"
breadcrumb-title: ''
description: 了解如何激活Substance 3D Designer并管理用于访问所有特性和功能的许可证。
helpx_creative_field: ""
helpx_description: Designer > Getting started > Activation and licenses
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 激活和许可证
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 1%

---


# 每个应用程序类型的激活流程

激活过程取决于您购买或有权访问Designer的位置：

| 版本 | 激活过程 |
| --- | --- |
| Creative Cloud 桌面版 | 请参阅[HelpX文档](https://helpx.adobe.com/cn/support/substance-3d-designer.html)中的专用页面。 如果有任何问题，[Creative Cloud文档](https://helpx.adobe.com/cn/creative-cloud/user-guide.html)可能会提供其他答案。 |
| 蒸汽 | 直接从Steam库中启动产品。 |
| Substance（独立） | 请参阅下述激活流程。 |

## 激活步骤（Substance版本）

### 使用激活向导

有三种选择可用：

* <b>评估此产品</b>：旧版试用不再可用。 您可以改为在[此处](https://www.adobe.com/creativecloud/3d-augmented-reality.html)或使用Creative Cloud桌面版为每个Substance 3D应用程序开始30天试用。 每个试用都独立于其他Substance 3D应用程序，因此您可以一次试用一个应用程序或一次试用所有应用程序。
* <b>使用许可证文件进行激活</b>：在2022年9月30日之前，使用从[Substance 3D网站](https://store.substance3d.com/user)上的帐户页面下载的许可证文件(<b>\*.key</b>)激活产品。
* <b>使用您的帐户激活</b>：旧版Substance帐户无法再用于激活。

>[!IMPORTANT]
>
> 要使用“激活向导”安装许可证文件，请确保以管理员身份运行Designer并暂时禁用防病毒软件。

![激活向导](../../assets/activation-wizard.png "激活向导")

### 手动激活

您可以通过将license.key文件放入以下文件夹来手动激活Designer：

<table data-preserve-html="true">
<colgroup> <col/> <col/> <col/> <col/> </colgroup><tbody><tr><th style="text-align: left;">Platform</th>
<th style="text-align: left;">版本</th>
<th colspan="2" style="text-align: left;">路径</th>
</tr><tr><td rowspan="4" style="text-align: left;"><b>Windows</b></td>
<td rowspan="2" style="text-align: left;"><b>11.2</b>或更高版本</td>
<td style="text-align: left;">AppData &gt;本地</td>
<td style="text-align: left;">C:\Users\用户\[用户名]\AppData\Local\Adobe\Adobe Substance 3D Designer</td>
</tr><tr><td style="text-align: left;">AppData &gt;漫游</td>
<td style="text-align: left;">C:\Users\用户\[用户名]\AppData\Roaming\Adobe\Adobe Substance 3D Designer</td>
</tr><tr><td rowspan="2" style="text-align: left;"><b>11.1</b>或更低</td>
<td style="text-align: left;">AppData &gt;本地</td>
<td style="text-align: left;">C:\Users\用户\[用户名]\AppData\Local\Allegorithmic\Substance Designer</td>
</tr><tr><td style="text-align: left;">AppData &gt;漫游</td>
<td style="text-align: left;">C:\Users\用户\[用户名]\AppData\Roaming\Allegorithmic\Substance Designer</td>
</tr><tr><td rowspan="2" style="text-align: left;"><b>Mac</b></td>
<td style="text-align: left;"><b>11.2</b>或更高版本<br/>
</td>
<td colspan="2" style="text-align: left;">/用户/[用户名]/资源库/Application Support/Adobe/Adobe Substance 3D Designer</td>
</tr><tr><td style="text-align: left;"><b>11.1</b>或更低<br/>
</td>
<td colspan="2" style="text-align: left;">/用户/[用户名]/资源库/Application Support/Allegorithmic/Substance Designer</td>
</tr><tr><td rowspan="2" style="text-align: left;"><b>Linux</b></td>
<td style="text-align: left;"><b>11.2</b>或更高版本</td>
<td colspan="2" style="text-align: left;">/home/[用户名]/.local/share/Adobe/Adobe Substance 3D Designer</td>
</tr><tr><td style="text-align: left;"><b>11.1</b>或更低<br/>
</td>
<td colspan="2" style="text-align: left;">/home/[用户名]/.local/share/Allegorithmic/Substance Designer</td>
</tr></tbody></table>

>[!NOTE]
>
> 上述路径中的某些目录可能默认处于隐藏状态。 在文件资源管理器中手动键入路径，或者显示隐藏的文件以查看它们。

>[!IMPORTANT]
>
> 确保该文件名为&#x200B;**license.key**，否则应用程序将无法找到它。

### 环境变量

您可以使用[环境变量](../../pipeline-and-project-con/environment-variables/environment-variables.md)覆盖Designer为<b>license.key</b>文件检查的位置。
