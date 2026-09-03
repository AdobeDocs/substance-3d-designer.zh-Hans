---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-combine.html"
breadcrumb-title: ''
description: 使用“法线组合”节点组合多个法线图，用于分层表面细节和细节。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Combine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 普通组合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 4%

---


# 普通组合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-combine.resources/normal-combine-01.png){width="128px"}

<b>英寸：</b>滤镜>法线图

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

“法线组合”以数学上正确的方式合并两个法线映射的细节。

它类似于其他2D图像编辑软件中众所周知的“叠加”方法，但在内部的工作方式略有不同（三个选项）。

</td>
</tr>
</table>

这是向已烘焙贴图添加2D生成的法线映射细节的最佳、最正确方法。

如果要混合两个正常映射而不合并其细节（例如，使用蒙版），则应使用[正常混合](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-blend/normal-blend.md)。

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>正常2</b> <i>颜色</i> | 描述 |
| <b>正常1</b> <i>颜色</i> | 描述 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>技术</b> *整数* | 设置要使用的内部混合技术，以速度换取质量。<br><br>*— 白化（低质量）<br>*&#x200B;通道混合器（高质量）<br>*面向细节（高质量）* |

## 示例
