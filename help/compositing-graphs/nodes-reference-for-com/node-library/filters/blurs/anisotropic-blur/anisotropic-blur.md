---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/anisotropic-blur.html"
breadcrumb-title: ''
description: 使用“各向异性模糊”节点应用方向模糊效果，以创建运动模糊和条纹效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Anisotropic Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 各向异性模糊
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 1%

---


# 各向异性模糊

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/anisotropic-blur-grayscale.png){width="128px"}

![](../../../../../../assets/anisotropic-blur.png){width="128px"}

## 各向异性模糊（灰度）

**范围：** *滤镜/模糊*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

执行高品质的[方向模糊](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-blur/directional-blur.md)，只需一些设置即可自定义外观。 也称为“运动模糊”。

重要提示：请确保使用适用于您的输入的版本！ 对颜色输入使用“各向异性模糊”，对灰度输入使用“各向异性模糊灰度”。

## 参数

* **强度**： *0.0 - 16.0*&#x200B;模糊的强度（半径）。 此值越高，模糊效果越明显。
* **各向异性**： *0.0 - 1.0*&#x200B;模糊的方向性。 将此值设置为0.0与执行常规模糊相同。
* **角度**： *0.0 - 1.0*&#x200B;设置模糊方向的角度。
* **质量**： *0 - 1*&#x200B;在[方框模糊](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)和内部总部模糊之间切换。 以速度换取质量。

## 示例图像

![](../../../../../../assets/aniso-blur-example.gif)

</td>
</tr>
</table>
