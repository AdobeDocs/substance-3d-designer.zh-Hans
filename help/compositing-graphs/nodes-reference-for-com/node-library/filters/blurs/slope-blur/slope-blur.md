---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/slope-blur.html"
breadcrumb-title: ''
description: 使用“斜率模糊”节点可应用基于Height映射斜率的定向模糊效果来创建运动模糊。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Slope Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 斜率模糊
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 1%

---


# 斜率模糊

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/slope-blur.png){width="128px"}

![](../../../../../../assets/slope-blur-grayscale.png){width="128px"}

## 斜率模糊（灰度）

**范围：** *滤镜/模糊*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

执行高级、高质量模糊，其中各向异性/方向由灰度“斜率映射”驱动。 按照斜率映射的斜率将其想象为斜率模糊效果，就像它是高度映射一样，类似于[方向变形](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md)（它基于内部变形）。

这是Designer中最有趣、最强大的模糊之一。 它可用于实现一些非常有趣和意料之外的效果，如碎裂和风化边缘，或污迹和泄漏Dirt或铁锈。

重要提示：请确保使用适用于您的输入的版本！ 对彩色输入使用“斜率模糊”，对灰度输入使用“斜率模糊灰度”。

## 参数

### 输入

* **斜率**： *灰度输入*&#x200B;斜率映射到各向异性的驱动角度。 理想情况下，应包含倾斜渐变；严苛、锐利的过渡将无法很好地发挥作用！

### 参数

* **样本**： *0 - 32*&#x200B;样本量，会影响品质，但会牺牲速度。
* **强度**： *0.0 - 16.0*\
  模糊量或强度。
* **模式**：*模糊，最小，最大*|\
  后续模糊刀路的混合模式。 “模糊”的行为更像标准[各向异性模糊](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md)，而“最小值”将“去除”现有区域，“最大值”将“去除”白色区域。

## 示例图像

![](../../../../../../assets/slopeblur01.gif)

![](../../../../../../assets/slopeblur02.gif)

</td>
</tr>
</table>
