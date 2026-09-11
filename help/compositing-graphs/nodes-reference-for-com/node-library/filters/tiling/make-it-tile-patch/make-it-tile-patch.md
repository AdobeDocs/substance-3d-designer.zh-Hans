---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-patch.html"
breadcrumb-title: ''
description: 使用Make It Tile Patch节点可对输入图像进行修补并创建无缝拼贴纹理。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使其拼贴贴贴面
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 8%

---


# 使其拼贴贴贴面

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](make-it-tile-patch.resources/make-it-tile-patch.png)

![](make-it-tile-patch.resources/make-it-tile-patch-grayscale.png)

<b>在</b>个筛选器中>拼贴

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

此节点是基于网格的半随机拼贴。 它接受输入修补程序并四处盖印，尝试根据您的设置将它转换为拼贴图像，而不会重复过多。

当您有一小块纹理并希望从中创建较大尺寸的拼贴纹理时，非常有用。

请记住，这不同于[Make-It-Tile Photo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md)，后者主要修复边缘。

要对整个素材执行此操作，请参阅[智能自动拼贴](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/smart-auto-tile/smart-auto-tile.md)。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>蒙版大小</b> <i>0.0 - 1.0</i> | 盖印修补时使用的圆形蒙版的大小。 |
| <b>蒙版精度</b> <i>0.0 - 1.0</i> | 蒙版的衰减/Smoothness精度。 |
| <b>蒙版变形</b> <i>-100.0 - 100.0</i> | 在蒙版边缘引入变形。 适合避免曲面片之间平滑、未定义的过渡。 |
| <b>图案大小宽度</b> <i>0.0 - 1000.0</i> | 将修补的宽度更改得不均匀。 |
| <b>图案大小Height</b> <i>0.0 - 1000.0</i> | 更改曲面片的Height不均匀。 |
| <b>无序</b> <i>0.0 - 1.0</i> | 引入了平移随机性，略微移动斑块。 |
| <b>大小变化</b> <i>0.0 - 100.0</i> | 引入蒙版的大小变化。 |
| <b>八度音阶</b> <i>0 - 6</i> | 这是确定总体大小的主控件。 |
| <b>旋转</b> <i>-360.0 - 360.0</i> | 预旋转修补。 |
| <b>旋转变化</b> <i>0.0 - 360.0</i> | 为每个修补图章引入随机旋转。 |
| <b>背景颜色</b> <i>（颜色值）</i> | 设置没有显示修补的区域的背景色。 |
| <b>颜色变化</b> <i>0.0 - 1.0（仅限颜色版本）</i> | 引入每个修补的颜色变化。 |
| <b>明度变化</b> <i>（仅限灰度版本）</i> | 引入每个修补的明度变化。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="make-it-tile-patch.resources/patch-ex.gif" />
        </td>
    </tr>
</table>
