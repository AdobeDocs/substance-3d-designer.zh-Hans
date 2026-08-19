---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/nadir-patch.html"
breadcrumb-title: ''
description: 使用Nadir Patch节点修补HDRI全景图的最低区域，以修复环境映射中的底部伪影。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Nadir Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nadir Patch
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 1%

---


# Nadir Patch

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-nadir-patch.png){width="200px"}

## Nadir Patch

**位置：** *3D视图/HDRI 工具*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

此节点提供了在球面映射图像的中心地点（最低点）上进行修补的功能。 它可以用来隐藏或“仿制”一个丑陋的谷底，或可见的相机或三脚架。 它的工作方式类似于[仿制修补程序](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)，但可以对球面映射的图像进行调整。 用户选择图像中其他位置的一个点，即在最低点克隆并混合进来的点。 只需单个HDRI即可处理其他外部输入，但可以将外部蒙版用作修补效果的Alpha。

可以使用[Nadir Extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/nadir-extract/nadir-extract.md)快速检查和验证效果。

## 输入

* **输入**： *颜色输入*
* **蒙版输入**：*灰度输入*\
  用于遮盖修补的可选蒙版插槽。 像阿尔法一样运作。

## 参数

* **启用**： *False/True*\
  启用或禁用修补效果。
* **显示帧帮助程序**： *False/True*\
  显示或隐藏辅助线以进行调试。
* **帧Thickness**： *0.0 - 1.0*\
  帮助线的Thickness。
* **修补程序缩放**： *0.0 - 1.0*\
  全局一致的补丁缩放。 同时影响源和目标。
* **修补程序大小**： *0.0 - 1.0*\
  曲面片大小不均匀。
* **修补程序旋转**： *0.0 - 1.0*\
  修补的旋转。 影响源和目标。
* **修补Alpha**： *平滑方形，高斯，蒙版输入*\
  设置用于混合修补与背景的Alpha值。
* **修补硬度**： *0.0 - 1.0*\
  设置Alpha的硬度/对比度。
* **源旋转偏移**： *0.0 - 1.0*\
  仅对修补源进行旋转。
* **位置坐标**
  * **源位置**：\
    源的位置。 具有2D视图中的手柄。
  * **修补程序位置**：\
    目标的位置。 具有2D视图中的手柄。

## 示例图像

![](../../../../../../assets/nadir-patch-ex.gif)

</td>
</tr>
</table>
