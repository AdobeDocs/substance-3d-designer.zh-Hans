---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/baking-issues.html"
breadcrumb-title: ''
description: 查找在Substance 3D Designer中与烘焙纹理相关的技术问题的故障排除步骤。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Baking issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 烘焙问题
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---


# 烘焙问题

此页面列出了与Substance 3D Designer中的[烘焙纹理](../../bakers/bakers.md)相关的技术问题，并提供了针对每个问题的故障排除步骤。

## 本页内容

“按名称匹配”不起作用

## “按名称匹配”不起作用

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>![（错误）](baking-issues.resources/error.svg)问题</b>

当“匹配”选项设置为“按网格名称”时，匹配似乎未应用，或者在所有场景对象间未一致应用。

<b>![（刻度）](baking-issues.resources/check.svg)建议的步骤</b>

在Designer 14.1及更低版本中，使用其&#x200B;*父*&#x200B;对象的名称匹配低多边形和高多边形对象 — 在大多数情况下，使用其父级变换。

自Designer 15.0起，直接使用&#x200B;*几何*&#x200B;对象的名称。

</td>
<td style="border: 0;" valign="top">

![场景树中的几何对象及其父对象](baking-issues.resources/baking-issues-01.png "场景树中的几何对象及其父对象"){zoomable="yes"}

</td>
</tr>
</table>

要获得预期匹配项，您可能需要走两条路：

* 调整几何对象的名称以应用匹配名称。
* 通过在项目设置中调整[“名称筛选模式”选项](../../interface/preferences-window/project-settings/project-settings.md)，恢复到行为或以前的Designer版本：
  1. 转到编辑>首选项>项目
  1. 选择列表中的最后一个项目文件
  1. 在项目文件列表下方，选择“Bakers”选项卡
  1. 将“名称筛选模式”设置为“父名称（旧版）”
