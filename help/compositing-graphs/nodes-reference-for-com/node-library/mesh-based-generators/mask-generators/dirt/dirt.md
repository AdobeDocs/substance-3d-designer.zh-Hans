---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dirt.html"
breadcrumb-title: ''
description: 使用Dirt根据网格曲率、位置和遮蔽生成Dirt累积蒙版。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 污垢
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 2%

---


# 污垢

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dirt.png){width="128px"}

## 污垢

**英寸：** *基于网格的生成器**/蒙版生成器*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版基于烘焙的AO和曲率表示边缘和角落中遮挡和凹陷的Dirt。

## 参数

### 输入

* **曲率**： *灰度输入*\
  用于内部效果和蒙版的已烘焙贴图。 必填！
* **环境遮蔽**： *灰度输入*\
  用于内部效果和蒙版的已烘焙贴图。 必填！
* **污渍输入**： *灰度输入*\
  自定义污渍映射输入，可选，由参数启用。
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。
* **正常世界空间**： *颜色输入*\
  仅用于三平面。
* **位置**： *颜色输入*\
  仅用于三平面。

### 参数

* **Dirt级别**： *0.0 - 1.0* Dirt量的主控件。
* **Dirt对比度**： *0.0 - 1.0*&#x200B;控制蒙版中Dirt的主对比度。
* **污渍量**： *0.0 - 1.0*&#x200B;设置Dirt的脏程度。 设置为0可达到完美平滑Dirt。
* **边缘蒙版**： *0.0 - 1.0*&#x200B;要从凸出边缘移除的Dirt量（基于曲率图）。
* **使用自定义污渍**： *False/True*&#x200B;允许使用自定义污渍映射输入，而不是内置污渍。
* **污渍比例**： *1 - 16*&#x200B;设置污渍细节的拼贴比例。
* **使用三平面**： *False/True*&#x200B;使用[三平面投影](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md)进行污渍映射，移除接缝。
* **三平面混合对比度**： *0.001 - 1.0*&#x200B;设置三平面投影的对比度。

## 示例图像

![](../../../../../../assets/dirt-ex.gif)

</td>
</tr>
</table>
