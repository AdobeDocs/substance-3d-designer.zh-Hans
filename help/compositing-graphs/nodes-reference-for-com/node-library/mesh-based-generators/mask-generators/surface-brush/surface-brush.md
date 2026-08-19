---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/surface-brush.html"
breadcrumb-title: ''
description: 使用“表面画笔”节点根据表面方向生成蒙版，用于创建定向风化和磨损效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Surface Brush
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 表面画笔
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---


# 表面画笔

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/surface-brush.png){width="128px"}

## 表面画笔

**英寸：** *基于网格的生成器**/蒙版生成器*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版代表对象表面上金属刷的有趣效果，被对象几何形状和AO遮蔽。

## 参数

### 输入

* **正常世界空间**： *颜色输入*
* **曲率**： *灰度输入*\
  用于内部效果和蒙版的已烘焙贴图。
* **环境遮蔽**： *灰度输入*\
  用于内部效果和蒙版的已烘焙贴图。
* **位置**： *灰度输入*
* **蒙版（可选）**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。

### 参数

* **级别**： *0.0 - 1.0*\
  设置全局效果级别，逐渐显示。
* **对比度**： *0.0 - 1.0*\
  调整结果的对比度。
* **Scratches长度**： *0.0 - 8.0*&#x200B;设置划痕的长度。 较小的值更像点，较高的值则为长条纹。
* **遮挡轴**： *X、Y、Z、无*&#x200B;应接收划痕的对象的轴。 不会改变划痕的方向。
* **遮挡轴强度**： *0.0 - 1.0*&#x200B;轴遮蔽效果的强度。
* **遮蔽**： *0.0 - 1.0*&#x200B;遮挡划痕时AO的强度。
* **锐化强度**： *0.0 - 1.0*&#x200B;设置应用到划痕的后锐化量。

## 示例图像

![](../../../../../../assets/surface-brush-ex.gif)

</td>
</tr>
</table>
