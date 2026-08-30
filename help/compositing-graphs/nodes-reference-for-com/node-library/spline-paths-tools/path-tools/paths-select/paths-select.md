---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-select.html"
breadcrumb-title: ''
description: 使用“路径选择”节点可根据条件从路径列表中选择和过滤特定路径。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 路径选择
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---


# 路径选择

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](paths-select.resources/paths-select-icon.png "节点图标")

<b>在：</b>样条和路径工具>路径工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

在路径中包含的多条路径之间隔离一条路径。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>标签</b> <i>类型</i> | 已编码段路径的列表。 将此输入连接到[路径蒙版](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)的结果或连接到另一个路径处理节点。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>路径</b> <i>颜色</i> | “路径”仅通过一条路径输入。 您可以使用[预览路径](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)了解结果所代表的内容，使用其他路径处理节点，或将其输入到[样条路径](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)以进一步将其处理为样条。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>选择模式</b> <i>整数</i> | 用于选择路径的方法：<br>*— 按ID：*&#x200B;从索引与<b>路径ID</b>中指定的路径匹配的列表中选择路径；<br>*— 按长度：*&#x200B;选择长度大于或小于<b>目标长度</b>中指定的阈值的路径。 |
| <b>路径ID</b> <i>整数</i> （在<b>选择模式</b>设置为&#x200B;*按ID*&#x200B;时可用） | 所选路径的索引。<br>大于<b>路径&#x200B;*中路径数的值会导致*</b>&#x200B;输出为空。 |
| <b>长度是否大于或小于？</b> <i>布尔值</i> （在<b>选择模式</b>设置为&#x200B;*按长度*&#x200B;时可用） | 控制所选内容的长度应包含还是大于或小于<b>目标长度</b>。 |
| <b>目标长度</b> <i>Float</i> （在<b>选择模式</b>设置为&#x200B;*按长度*&#x200B;时可用） | 用于选择样条的长度阈值。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-select.resources/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="paths-select.resources/PathsSelect-Variant1.jpg" alt="PathsSelect-Variant1">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-select.resources/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="paths-select.resources/PathsSelect-Variant2.jpg" alt="PathsSelect-Variant2">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
