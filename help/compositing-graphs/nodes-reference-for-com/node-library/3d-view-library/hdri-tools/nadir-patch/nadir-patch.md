---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/nadir-patch.html"
breadcrumb-title: ''
description: 使用Nadir Patch节点修补HDRI全景图的低点区域，以修复环境图中的底部伪影。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Nadir Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nadir Patch
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9aaf135d4c336ea0cff865524ad1ccd5dcc225bd
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 5%

---


# Nadir Patch

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](nadir-patch.resources/panorama-nadir-patch.png){width="200px"}

<b>进入：</b>3D 视图>HDRI 工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点提供了在球面映射图像的中心地面点（最低点）上进行修补的功能。 它可以用来隐藏或“仿制”一个丑陋的低谷，或者可见的相机或三脚架。 它的工作方式类似于[仿制修补](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)，但可以对球面映射的图像进行调整。 用户选择图像中其他位置的一个点，即在最低点克隆并混合进来的点。 只需单个HDRI即可处理其他外部输入，但可以将外部蒙版用作修补效果的Alpha。

可以使用[Nadir Extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/nadir-extract/nadir-extract.md)快速检查和验证效果。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>输入</b> <i>颜色输入</i> |  |
| <b>蒙版输入</b> <i>灰度输入</i> | 用于遮盖修补的可选蒙版插槽。 像阿尔法一样运作。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>启用</b> <i>False/True</i> | 启用或禁用修补效果。 |
| <b>显示助手</b> <i>False/True</i> | 显示或隐藏助手行，用于调试目的。 |
| <b>Thickness</b> <i>0.0 - 1.0</i> | 助手行的Thickness。 |
| <b>修补缩放</b> <i>0.0 - 1.0</i> | 全局一致的补丁缩放。 同时影响源和目标。 |
| <b>修补程序大小</b> <i>0.0 - 1.0</i> | 曲面片大小不均匀。 |
| <b>修补程序旋转</b> <i>0.0 - 1.0</i> | 修补的旋转。 影响源和目标。 |
| <b>修补Alpha</b> <i>平滑方形，高斯，蒙版输入</i> | 设置用于混合修补与背景的Alpha值。 |
| <b>修补硬度</b> <i>0.0 - 1.0</i> | 设置Alpha的硬度/对比度。 |
| <b>源旋转偏移</b> <i>0.0 - 1.0</i> | 仅对修补源进行旋转。 |
| <b>位置坐标</b> |  |
| <b>源位置</b> | 源的位置。 具有2D视图中的手柄。 |
| <b>修补程序位置</b> | 目标的位置。 具有2D视图中的手柄。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="nadir-patch.resources/nadir-patch-ex.gif" />
        </td>
    </tr>
</table>
