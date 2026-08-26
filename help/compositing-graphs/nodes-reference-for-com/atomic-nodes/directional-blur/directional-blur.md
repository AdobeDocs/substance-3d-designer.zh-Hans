---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/directional-blur.html"
breadcrumb-title: ''
description: 使用方向模糊节点沿特定方向应用模糊效果，以创建运动模糊和条纹效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Directional blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 定向模糊
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 9%

---


# 定向模糊

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子节点：方向模糊](../../../../assets/comp_dirmotionblur_1.png "原子节点：方向模糊"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

根据强度图在指定方向上应用模糊。

此节点执行的操作类似于在输入上执行运动模糊。 与常规“[模糊](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)”节点（在所有方向上均等模糊）不同，“方向模糊”沿用户定义的角度工作。

</td>
</tr>
</table>

与“模糊”类似，它也是一种更快且低质量的操作。 [各向异性模糊](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md)中提供了扩展的、更高质量的替代项，具有性能折中

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

## 方向模糊和各向异性模糊

以下图像显示了方向模糊和[各向异性模糊](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md)对相同输入形状的影响，参数相似。 “各向异性模糊”已设置为完全各向异性和高质量。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>方向模糊</b>

![方向模糊比较](../../../../assets/dirblur-01.png "方向模糊比较"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

<b>各向异性模糊</b>

![各向异性模糊比较](../../../../assets/aniso-01.png "各向异性模糊比较"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 参数

</td>
<td style="border: 0;" valign="top">

### 输入连接器

</td>
<td style="border: 0;" valign="top">

### 输出连接器

</td>
<td style="border: 0;" valign="top">

### 示例

</td>
</tr>
</table>

## 参数

|  |  |
| --- | --- |
| <b>强度</b> *浮动* | 设置模糊半径（以像素为单位）。 |
| <b>角度</b> *浮动* | 模糊效果的方向（顺时针旋转次数），从水平方向开始 — 即方向矢量(1， 0)。 |

## 输入连接器

|  |  |
| --- | --- |
| <b>输入</b> *灰度/颜色* [主要](../../../../glossary/glossary.md) | 要处理的图像。 |

## 输出连接器

|  |  |
| --- | --- |
| <b>输出</b> *灰度/颜色* |  |

## 示例

*即将推出。*
