---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/preview-paths.html"
breadcrumb-title: ''
description: 使用“预览路径”节点在2D视图中可视化路径数据以进行调试和验证。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Preview Paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 预览路径
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4034c519f3367597b09165c267379fd8ac4e7062
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---


# 预览路径

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](../../../../../../assets/preview-paths-icon.png "节点图标")

<b>在：</b>样条和路径工具>路径工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

在给定背景上跟踪路径的段和顶点。 每条路径一种随机颜色。

您将获得与[蒙版到路径](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)的<b>预览</b>输出类似的结果，但包含更多选项。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>背景</b> <i>颜色</i> | 顶部有显示路径的背景图像。 这还可以控制渲染大小。 |
| <b>路径</b> <i>颜色</i> | 已编码段路径的列表。 将此输入连接到[路径蒙版](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)的结果或连接到另一个路径处理节点。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>显示转角</b> <i>布尔值</i> | 在每个顶点上显示一个标记为“拐角”（叠加混合）的正方形。 |
| <b>显示顶点</b> <i>布尔值</i> | 在每个顶点上显示圆形形状（叠加混合）。 角仍显示为正方形。 |
| <b>段Thickness(px)</b> <i>浮动</i> | 调整渲染段的Thickness（以像素为单位）。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![节点示例1](../../../../../../assets/PathsToSpline-Variant2-Before_1.jpg "节点示例1")

</td>
<td style="border: 0;" valign="top">

![节点示例2](../../../../../../assets/PathsToSpline-Variant1-Before_1.jpg "节点示例2")

</td>
</tr>
</table>
