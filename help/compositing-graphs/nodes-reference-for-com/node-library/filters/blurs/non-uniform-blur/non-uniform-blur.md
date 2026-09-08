---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/non-uniform-blur.html"
breadcrumb-title: ''
description: 使用非均匀模糊节点在X和Y方向应用不同强度的模糊以用于各向异性效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Non Uniform Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 非均匀模糊
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---


# 非均匀模糊

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-blur-grayscale.png){width="128px"}

![](../../../../../../assets/non-uniform-blur.png){width="128px"}

## 非均匀模糊（灰度）

**范围：** *滤镜/模糊*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

执行“高品质模糊”，其中强度由输入蒙版驱动。 允许添加“各向异性”和“不对称”选项。

## 参数

### 输入

* **模糊映射**： *灰度输入*&#x200B;用于驱动效果强度的蒙版映射。

### 参数

* **强度**： *0.0 - 50.0*&#x200B;应用模糊的最大强度。 模糊映射遮盖，因此此设置对该映射的黑色区域无效。
* **各向异性**： *0.0 - 1.0*&#x200B;可以选择向模糊效果添加方向性。 由“角度”参数驱动。
* **不对称**： *0.0 - 1.0*&#x200B;选择性地向采样添加偏差。 由“角度”参数驱动。
* **角度**： *0.0 - 1.0*&#x200B;用于设置方向性和采样偏差的角度。
* **样本**： *1 - 16*&#x200B;样本量，决定质量。 乘以刀片数量。
* **刀片**： *1 -* 9\
  采样扇区的数量，决定质量。 乘以样本量。

## 示例图像

*以下示例由“模糊映射”槽中的渐变渐变（90度）驱动。*

![](../../../../../../assets/nonuniform-example.gif)

</td>
</tr>
</table>
