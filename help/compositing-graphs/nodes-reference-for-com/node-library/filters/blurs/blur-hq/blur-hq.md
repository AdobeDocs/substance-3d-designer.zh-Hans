---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/blur-hq.html"
breadcrumb-title: ''
description: 使用“Blur HQ”（模糊HQ）节点对纹理应用高质量的模糊效果，获得平滑、专业的模糊效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Blur HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 模糊 HQ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 5%

---


# 模糊 HQ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/blur-hq-1.png){width="128px"}

![](../../../../../../assets/blur-hq-grayscale.png){width="128px"}

## 模糊HQ（灰度）

**范围：** *滤镜/模糊*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

对结果执行“高品质高斯模糊”。 质量比[标准原子盒模糊](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) [好得多。](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)

重要提示：请确保使用适用于您的输入的版本！ 对颜色输入使用“模糊总部”，对灰度输入使用“模糊总部”。

## 参数

* **强度**： *0.0 - 16.0*\
  模糊的强度（半径）。 此值越高，模糊效果越明显。
* **质量**： *0 - 1*&#x200B;增加内部取样量可获得更高质量，同时降低计算速度。

## 示例图像

![](../../../../../../assets/hqblur-example.gif)

</td>
</tr>
</table>
