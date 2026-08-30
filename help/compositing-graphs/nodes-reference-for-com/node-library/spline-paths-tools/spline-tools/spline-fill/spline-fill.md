---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-fill.html"
breadcrumb-title: ''
description: 使用“样条填充”节点，用纹理或颜色填充由封闭样条定义的区域。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Fill
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 样条填充
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---


# 样条填充

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](spline-fill.resources/spline-fill-icon.png "节点图标")

<b>In：</b>样条和路径工具>样条曲线工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

用纯白色填充输入样条的内部。 外墙上全是纯黑色。

开放样条由起点到终点用直线封闭。 样条交叉的交叉点通过反转这些交叉点处的线的内部和外部侧来解决。

</td>
</tr>
</table>

>[!IMPORTANT]
>
> 建议不要在[0， 1]拼贴之外的样条上使用此节点。 这种情况下，充填过程是不可靠的。

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>样条坐标</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的输入样条点的坐标：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> -Height<br><b>A</b> — 压缩数据：<br> — 符号：样条是闭合（负）或开放（正）；<br> -绝对值：Thickness+ 1。 |
| <b>样条数据</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的输入样条的其他数据。<br><b>R</b> -正切X<br><b>G</b> -正切Y<br><b>B</b> — 未使用<br><b>A</b> — 未使用 |
| <b>样条量</b> <i>整数</i> | 输入样条的数量。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>输出</b> <i>灰度</i> | 在纯黑色背景上使用纯白色填充输入样条的结果图像。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-fill.resources/SplineFill-Variant1-Before.jpg" alt="SplineFill-Variant1-Before">
      <br><i>之前</i>
    </td>
    <td>
      <img src="spline-fill.resources/SplineFill-Variant1-After.jpg" alt="样条填充 — 变量1-After">
      <br><i>之后</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![节点示例2](spline-fill.resources/SplineFill-Demo.gif "节点示例2")

</td>
</tr>
</table>
