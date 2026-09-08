---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/path-2d-transform.html"
breadcrumb-title: ''
description: 使用“路径2D变换”节点通过平移、旋转和缩放操作来变换路径。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Path 2D Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 路径二维变换
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4034c519f3367597b09165c267379fd8ac4e7062
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 2%

---


# 路径二维变换

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](../../../../../../assets/path-2d-transform-icon.png "节点图标")

<b>在：</b>样条和路径工具>路径工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

使用线框变换路径。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>路径</b> <i>颜色</i> | 已编码段路径的列表。 将此输入连接到[路径蒙版](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)的结果或连接到另一个路径处理节点。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>路径</b> <i>颜色</i> | 变换后的路径。 您可以使用[预览路径](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)了解结果所代表的内容，使用其他路径处理节点，或将其输入到[样条路径](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)以进一步将其处理为样条。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>转换矩阵</b> <i>浮点4</i> | 应用于样条的变换矩阵。 有三种编辑矩阵参数的模式可用：<br>*— 变换Gizmo：*&#x200B;当选择Spline 2D变换节点时，调整[2D 视图](../../../../../../interface/2d-view/2d-view.md)中显示的线框手柄；<br>*— 旋转/拉伸：*&#x200B;单独控制样条的旋转和拉伸。 请注意，这些值始终相对于当前变换应用。 例如，将50%宽度应用两次会产生25%宽度；<br>*— 矩阵值：*&#x200B;单击<b>编辑矩阵值</b>按钮以直接输入矩阵的原始数值。 |
| <b>偏移</b> <i>浮点2</i> | 将位置偏移应用于X（水平）和Y（垂直）中的样条。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/Paths2DTransform-Variant1.jpg" alt="Paths2DTransform-Variant1">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../../../../assets/Paths2DTransform-Variant2.jpg" alt="Paths2DTransform-Variant2">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
