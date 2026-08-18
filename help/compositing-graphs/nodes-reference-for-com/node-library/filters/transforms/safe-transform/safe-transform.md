---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/safe-transform.html"
breadcrumb-title: ''
description: 使用安全变换节点可应用变换，同时保留纹理边界并避免伪影。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Safe Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 安全变换
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# 安全变换

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

## 安全变换（灰度）

**英寸：** *筛选器/变换*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

[转换2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)的拼贴安全版本。 允许您在不破坏拼贴的情况下进行缩放、旋转和偏移，并且不会由于小的偏移和旋转而丢失像素细节（失去清晰度/锐度）。

当需要最大控制或完美锐化时，变换噪声非常有用。

## 参数

* **拼贴**： *1 - 16*&#x200B;通过拼贴来缩小输入。
* **偏移模式**： *手动，随机*&#x200B;切换到随机偏移，而不是手动定义的偏移。
* **偏移**： *0.0 - 1.0*\
  移动或转换结果。 确保像素对齐且没有插值。
* **旋转**： *0.0 - 1.0*&#x200B;沿角度旋转输入。
* **平铺安全旋转**： *False/True*&#x200B;确定旋转的行为，即它是否应该对齐到不会模糊任何像素的安全值。
* **对称**： *无、X、Y、X+Y*
* **背景颜色**： *（颜色值）（仅限颜色版本）*
* **Mipmap模式**： *自动，手动*&#x200B;确定Mipmapping模式。 将此选项设置为“手动”可获得更锐利的结果。
* **多级渐远纹理级别**： *0 - 10*&#x200B;当Mipmap模式设置为“手动”时，这将允许您选择其他Mipmap。

## 示例图像

|  |
| --- |
| 没有附加到此页面的图像。 |

</td>
</tr>
</table>
