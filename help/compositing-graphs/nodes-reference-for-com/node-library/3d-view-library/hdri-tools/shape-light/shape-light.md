---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/shape-light.html"
breadcrumb-title: ''
description: 使用“形状光”节点将自定形状的光源添加到HDRI环境，以实现创意光照效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Shape Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形状光照
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---


# 形状光照

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-shape.png){width="200px"}

## 形状光照

**位置：** *3D视图/HDRI 工具*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

生成球面投影的矩形形状。 形状变换由变换小工具驱动。

## 输入

* **背景图像输入**： *颜色输入*&#x200B;要在其上合成生成的光的可选背景。
* **形状图像输入**：*颜色输入*&#x200B;要映射到球面光的可选图像。 仅在“形状颜色模式”设置为“图像输入”时使用。

## 参数

* **形状矩阵**
  * **矩阵**： *（转换矩阵）*\
    结果的变换控件。 可以通过直接与画布交互来修改结果。
  * **偏移**： *-2.0 - 2.0*\
    移动或转换结果。 可以通过直接与画布交互来修改结果。
* **形状**： *矩形，磁盘*\
  选择要置入的形状。
* **形状颜色模式**：*RGB、色温（开氏温度）、图像输入*\
  选择用来设置形状颜色的方法。 “Image Input（图像输入）”允许使用第二个输入插槽。
* **颜色**： *（颜色值）*\
  仅当“形状颜色模式”设置为“RGB”时。 为形状选取颜色。
* **形状温度**： *800.0 - 20000.0*\
  仅在“形状颜色模式”设置为“色温”时。 设置形状颜色的开氏值。
* **形状图像输入灰度系数**： *sRGB，线性*\
  仅当“形状颜色模式”设置为“图像输入”时。 确定如何解释形状图像输入。
* **形状曝光(EV)**： *0.0 - 10.0*\
  为生成的形状设置曝光值，使其与背景图像曝光值完美匹配。
* **形状硬度**： *0.0 - 1.0*\
  设置形状边缘的硬度。
* **热点曝光(EV)**： *0.0 - 10.0*\
  设置中心热点的曝光度。 请注意，这在RGB模式下不是很可见。
* **热点大小**： *0.0 - 1.0*\
  中心热点的大小。
* **热点衰减**： *0.0 - 1.0*\
  中心热点的衰减。
* **热点位置**： *0.0 - 1.0*\
  中心热点的X和Y位置。
* **启用后台输入**： *False/True*\
  切换可选背景图像的使用。 复合图像在背景之上生成了光照。
* **背景颜色**： *（颜色值）*\
  如果未使用背景输入，请在此处设置纯色背景值。
* **背景灰度系数**： *sRGB，线性*&#x200B;如果使用背景输入，请设置如何解释背景输入。

## 示例图像

![](../../../../../../assets/shape-light-ex.gif)

</td>
</tr>
</table>
