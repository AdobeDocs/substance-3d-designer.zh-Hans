---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/safe-transform.html"
breadcrumb-title: ''
description: 使用安全变换节点可以应用变换，同时保留纹理边界并避免伪影。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Safe Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 安全变换
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 5%

---


# 安全变换

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](safe-transform.resources/safe-transform.png)

![](safe-transform.resources/safe-transform-grayscale.png)

<b>英寸：</b>筛选器>变换

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

拼贴安全版本的[变换2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)。 允许您在不中断拼贴的情况下进行缩放、旋转和偏移，并且不会由于小的偏移和旋转而丢失像素细节（失去清晰度/锐度）。

当需要最大程度地控制或完美锐化时，可用于噪声。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>平铺</b> <i>1 - 16</i> | 通过拼贴输入来缩小它。 |
| <b>偏移模式</b> <i>手动，随机</i> | 切换到随机偏移而不是手动定义的偏移。 |
| <b>偏移</b> <i>0.0 - 1.0</i> | 移动或转换结果。 确保像素已捕捉且未插值。 |
| <b>旋转</b> <i>0.0 - 1.0</i> | 沿角度旋转输入。 |
| <b>磁贴安全旋转</b> <i>False/True</i> | 确定旋转的行为，以及它是否应捕捉到不会模糊任何像素的安全值。 |
| <b>对称</b> <i>无、X、Y、X+Y</i> |  |
| <b>背景颜色</b> <i>（颜色值）（仅限颜色版本）</i> |  |
| <b>镜像转换模式</b> <i>自动，手动</i> | 确定mipmapping模式。 将此选项设置为“手动”可获得更锐利的结果。 |
| <b>多级渐远纹理级别</b> <i>0 - 10</i> | 当镜像转换模式设置为“手动”时，您可以选择其他镜像转换。 |
