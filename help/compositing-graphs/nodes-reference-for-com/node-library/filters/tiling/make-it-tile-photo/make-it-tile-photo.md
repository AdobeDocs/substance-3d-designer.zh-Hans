---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-photo.html"
breadcrumb-title: ''
description: 使用“制作平铺照片”节点将照片转换为无缝的纹理以创建材料。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Photo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 为其拼贴照片
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 9%

---


# 为其拼贴照片

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/make-it-tile-photo.png)

![](../../../../../../assets/make-it-tile-photo-grayscale.png)

<b>在</b>个筛选器中>拼贴

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点为由于非连续边缘而不可能平铺的任何图像提供了边缘修复功能。 它不会影响输入图像边缘之外的任何内容。 如果要以不同的方式调整缩放或平铺，请查看[使其平铺修补](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-patch/make-it-tile-patch.md)。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>蒙版变形H</b> <i>-100.0 - 100.0</i> | 在水平轴中引入变形，以避免未定义的过渡。 |
| <b>蒙版变形V</b> <i>-100.0 - 100.0</i> | 在垂直轴上引入变形，以避免未定义的过渡。 |
| <b>蒙版大小H</b> <i>0.0 - 1.0</i> | 设置过渡边水平到达的距离。 |
| <b>蒙版大小V</b> <i>0.0 - 1.0</i> | 设置过渡边缘垂直达到的距离。 |
| <b>蒙版精度H</b> <i>0.0 - 1.0</i> | 设置过渡的水平平滑程度。 |
| <b>蒙版精度V</b> <i>0.0 - 1.0</i> | 设置过渡的垂直平滑程度。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/mit-photo-ex.png" />
        </td>
    </tr>
</table>
