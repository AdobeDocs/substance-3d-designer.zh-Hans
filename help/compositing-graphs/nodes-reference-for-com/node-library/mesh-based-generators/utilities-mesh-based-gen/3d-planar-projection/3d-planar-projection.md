---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/3d-planar-projection.html"
breadcrumb-title: ''
description: 使用“3D平面投影”节点，使用平面投影进行纹理映射，将纹理投影到网格曲面上。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > 3D Planar Projection
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D平面投影
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# 3D平面投影

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-planar-gray.png)![](../../../../../../assets/3d-planar.png)

## 3D平面投影（颜色）

**在：** *基于网格的生成器**/Utilities*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

根据烘焙网格数据（“位置”和“世界法线图”）执行平面投影。 允许您跨接缝投影和放置贴花，而不依赖于原始UV映射。

## 参数

### 输入

* **位置图**： *颜色输入*&#x200B;烘焙位置图
* **世界空间法线**： *颜色输入*&#x200B;烘焙世界空间法线图
* **投影纹理**： *颜色输入*&#x200B;输入纹理以投影到目标上。

### 参数

* **定位**
  * **项目输入**：*UV位置，世界空间位置*&#x200B;选择投影位置是在2D/UV中还是在3D/世界空间中设置。
  * **目标UV位置**：\
    仅使用“UV位置输入”，最适用于在“位置”地图上的2D视图中选取点。
  * **目标位置**： *（颜色值）*仅使用世界空间位置输入，可让您定义精确的3D坐标。
  * **目标正常**： *（颜色值）*
  * **旋转**： *0.0 - 1.0\
    沿投影纹理的法线轴旋转投影纹理。*
  * **缩放**： *0.0 - 1.0*\
    设置投影纹理的全局比例。
  * **大小**： *0.0 - 2.0*&#x200B;对投影的纹理执行非均匀缩放。
* **蒙版**
  * **最大深度**： *0.0 - 1.0*&#x200B;控制投影纹理将在何时被剪切显示。
  * **深度淡化**： *0.0 - 1.0*&#x200B;将切断深度的过渡设置为突然或渐隐。
  * **法线阈值**： *-1.0 - 1.0*&#x200B;设置与投影法线不完全对齐的曲面的阈值。
  * **法向淡化**： *0.0 - 1.0*&#x200B;为不对齐的曲面设置过渡以突然或淡化。

## 示例图像

![](../../../../../../assets/3d-planar-projection-ex.gif)

</td>
</tr>
</table>
