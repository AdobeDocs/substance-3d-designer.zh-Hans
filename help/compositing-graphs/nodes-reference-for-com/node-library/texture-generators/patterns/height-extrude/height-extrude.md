---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/height-extrude.html"
breadcrumb-title: ''
description: 使用高度挤出节点凸出基于高度图的形状，以便在纹理中创建类似3D的深度效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Height Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 高度挤出
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---


# 高度挤出

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-extrude.png){width="200px"}

## 高度挤出

**在：** *纹理生成器**/Patterns*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

高度挤出从输入高度图渲染3D Z深度。 就像[形状凸出](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md)和[立方体3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md)一样，它允许您在2D 视图中旋转相机。 其主要目标是作为生成器用于从平面高图创建3D旋转形状。 然后可以将这些形状与[形状飞溅](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md)一起使用。

与[形状凸出](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md)的主要区别在于，输入图不必是二进制“alpha”类型的映射，而是全范围灰度映射。 这意味着您可以更好地控制凸出Height（有机、复杂形状），但不能控制斜面配置文件（硬表面、更简单的形状）。

## 参数

* **相机角度**：\
  相机的欧拉角，半转。 请注意，水平旋转和缩放直接应用于输入。
* **相机比例**： *0.001 - 3.0*\
  应用于输出的全局缩放。
* **Height比例**： *0.0 - 2.0*\
  将全局因子应用于输入Height值。
* **垂直偏移**： *-1.0 - 1.0*\
  向上或向下移动最终输出。
* **地面**： *关闭/打开*\
  如果地面处于关闭状态，则会显示输入为0的黑色背景，而不是类似地面的平面。
* **普通格式**： *DirectX/OpenGL*\
  **法线格式**&#x200B;参数可反转法线图的y坐标。
* **正常强度**： *0.0 - 256.0*\
  与&#x200B;**正常**&#x200B;节点的&#x200B;**强度**&#x200B;参数相同。 将其设置为256可在旋转时获得无共享的正常。

## 示例图像

</td>
</tr>
</table>
