---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-vertex-processor-simple.html"
breadcrumb-title: ''
description: 使用Paths顶点处理器简单节点处理带有简化转换选项的路径顶点。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Vertex Processor Simple
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Paths顶点处理器简单
user-guide-description: ''
user-guide-title: ''
source-git-commit: f9ae596767e754b5c0f62ed6bdb6f16dd33bb799
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---


# Paths顶点处理器简单

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](paths-vertex-processor-simple.resources/paths-vertex-processor-simple-icon.png "节点图标")

<b>在：</b>样条和路径工具>路径工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

对输入<b>顶点</b>的路径位置应用变换。

1. 编辑<b>逐顶点函数</b>参数函数；
1. 使用<b>GetFloat2</b>节点&#x200B;*顶点.pos*&#x200B;变量；
1. 对此值执行一些操作（例如，将其乘以以缩放路径）；
1. 将计算结果设置为输出。

</td>
</tr>
</table>

可以使用输入图像并从函数中进行取样。 必须首先连接输入，才能从函数中对其进行取样。 （请注意，第一个输入是&#x200B;*图像1*！）\
您也可以访问&#x200B;*顶点.corner*(bool)和&#x200B;*path.id*(float)变量。

>[!TIP]
>
> 对于高级用户，[路径格式规范](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md)解释了如何将路径数据编码为彩色图像，并提供了直接处理此数据的提示。

>[!NOTE]
>
> 另请参阅[路径顶点处理器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md)。

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>路径</b> <i>颜色</i> | 已编码段路径的列表。 将此输入连接到[路径蒙版](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)的结果或连接到另一个路径处理节点。 |
| <b>输入#</b> <i>彩色/灰度</i> | 应在<b>逐顶点函数</b>参数函数中采样的图像的输入。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>路径</b> <i>颜色</i> | 变换路径。 您可以使用[预览路径](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)了解结果所代表的内容，使用其他路径处理节点，或将其输入到[样条路径](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)以进一步将其处理为样条。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>图像输入计数</b> <i>整数</i> | 用于连接应在<b>逐顶点函数</b>参数函数中采样的图像的可见<b>输入#</b>输入连接器数。<br>设置完所有所需的样本后，可通过将此参数的值减回0来隐藏未使用的大头针。<br>如果需要更多输入，请改用[Paths顶点处理器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md)。 |
| <b>逐顶点函数</b> <i>Float2</i> | 应用于每个顶点的函数。 必须返回新的顶点位置。<br>有关指导信息，请参阅此页面中的<b>描述</b>部分。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![节点示例2](paths-vertex-processor-simple.resources/PathsVertexProcessor-Demo2.gif "节点示例2")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
