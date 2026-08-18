---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/quad-transform.html"
breadcrumb-title: ''
description: 使用“四元变换”节点将四边形变换应用于纹理，以进行透视校正和变形。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Quad Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 四元变换
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 1%

---


# 四元变换

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/quad-transform-grayscale.png){width="128px"}

![](../../../../../../assets/quad-transform.png){width="128px"}

## 四元变换（灰度）

**英寸：** *筛选器/变换*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

特殊的变换节点，允许通过与四边形角点的交互来变换该形状。 允许非常具体的变换以实际操作的方式进行。

## 参数

* **p00**：左上点。
* **p01**：左下点
* **p10**：右上角。
* **p11**：右下角。
* **剔除**：*仅正面、仅背面、前后对面*&#x200B;设置交叉点时的剔除/形状隐藏。
* **启用拼贴**： *False/True*
* **背景颜色**： *（灰度值）*如果拼贴关闭，则为纯背景颜色。
* **采样**： *双线性，最接近*&#x200B;设置采样质量。

## 示例图像

![](../../../../../../assets/quad-example.gif)

</td>
</tr>
</table>
