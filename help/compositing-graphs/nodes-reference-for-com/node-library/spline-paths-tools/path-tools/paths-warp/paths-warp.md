---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-warp.html"
breadcrumb-title: ''
description: 使用“路径变形”节点沿路径曲线变形纹理，以创建弯曲和有机图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 路径变形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# 路径变形

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](paths-warp.resources/paths-warp-icon.png "节点图标")

<b>在：</b>样条和路径工具>路径工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据<b>渐变输入</b>使输入路径变形。 （与[变形](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md)节点效果相同。）

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>路径</b> <i>颜色</i> | 已编码段路径的列表。 将此输入连接到[路径蒙版](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)的结果或连接到另一个路径处理节点。 |
| <b>渐变输入</b> <i>灰度</i> | Height状输入既控制变形量，又控制变形方向。 （与[变形](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md)节点效果相同。） |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>路径</b> <i>颜色</i> | 变形路径。 您可以使用[预览路径](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)了解结果所代表的内容，使用其他路径处理节点，或将其输入到[样条路径](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)以进一步将其处理为样条。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>强度</b> <i>浮动</i> | <b>强度</b>参数设置变形的强度。 |
| <b>步骤数</b> <i>整数</i> | 使用较高的值，以多个较小的增量来变形输入路径。<br>这可以防止路径自行交叉，特别是在使用较高的<b>强度</b>值时。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-warp.resources/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="paths-warp.resources/PathsWarp-Variant1-After.jpg" alt="PathsWarp-Variant1-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-warp.resources/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="paths-warp.resources/PathsWarp-Variant2-After.jpg" alt="PathsWarp-Variant2-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![节点示例1](paths-warp.resources/PathsWarp-Demo1.gif "节点示例1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
