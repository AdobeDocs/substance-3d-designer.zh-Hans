---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-vertex-processor.html"
breadcrumb-title: ''
description: 使用“路径顶点处理器”节点可使用高级选项变换和处理路径顶点。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Vertex Processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 路径顶点处理器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 1%

---


# 路径顶点处理器

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](paths-vertex-processor.resources/paths-vertex-processor-01.png "节点图标")

<b>在：</b>样条和路径工具>路径工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

对输入<b>顶点</b>的路径位置应用变换。

该节点的使用方法如下：

1. 编辑<b>逐顶点函数</b>参数函数；
1. 使用<b>Get Float2</b>节点获取；*vertex.pos*、*prev.pos*&#x200B;和/或&#x200B;*next.pos*&#x200B;变量
1. 对这些值执行一些操作（例如，乘以它们以缩放路径）；
1. 将计算结果设置为输出。

</td>
</tr>
</table>

在查询&#x200B;*prev.pos*&#x200B;或&#x200B;*next.pos*&#x200B;之前，请确保设置适当的<b>访问的上一个顶点</b>和<b>访问的下一个顶点</b>值\
您还可以添加输入图像并从函数中对其进行取样。 必须首先连接输入，才能从函数中对其进行取样。 （请注意，第一个输入是&#x200B;*图像1*！）\
您还可以访问&#x200B;*prev[2].pos*(Float2)、*next[2].pos*(Float2)、*path.corner*(bool)和&#x200B;*顶点.id*(float)变量。

>[!TIP]
>
> 对于高级用户，[路径格式规范](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md)解释了如何将路径数据编码为彩色图像，并提供了直接处理此数据的提示。

>[!NOTE]
>
> 另请参阅[路径顶点处理器简单](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor-1/paths-vertex-processor-simple.md)。

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>路径</b> <i>颜色</i> | 已编码段路径的列表。 将此输入连接到[路径蒙版](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)的结果或另一个&#x200B;*路径*&#x200B;处理节点。 |
| <b>输入#</b> <i>彩色/灰度</i> | 应在<b>逐顶点函数</b>参数函数中采样的图像的输入。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>路径</b> <i>颜色</i> | 变换后的路径。 您可以使用[预览路径](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)了解结果所代表的内容，使用其他路径处理节点，或将其输入到[样条路径](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)以进一步将其处理为样条。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>以前访问的顶点</b> <i>整数</i> | 使用此参数将允许您使用<b>节点</b>参数函数中的<b>Get</b>逐顶点函数，获取路径上的上一个顶点(*prev.pos*)和上一个上一个顶点(*prev[2].pos*)的位置。 |
| <b>下一个顶点已访问</b> <i>整数</i> | 使用此参数将允许您使用<b>节点</b>参数函数中的<b>Get</b>逐顶点函数，获取以下顶点沿路径(*next.pos*)和以下顶点(*next[2].pos*)的位置。 |
| <b>图像输入计数</b> <i>整数</i> | 用于连接应在<b>逐顶点函数</b>参数函数中采样的图像的可见<b>输入#</b>输入连接器的数量。<br>设置完所有所需的样本后，可通过将此参数的值减回0来隐藏未使用的大头针。 |
| <b>逐顶点函数</b> <i>浮点2</i> | 应用于每个顶点的函数。 必须返回新顶点位置。<br>有关指导信息，请参阅此页面中的<b>描述</b>部分。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![节点示例2](paths-vertex-processor.resources/paths-vertex-processor-02.gif "节点示例2")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
