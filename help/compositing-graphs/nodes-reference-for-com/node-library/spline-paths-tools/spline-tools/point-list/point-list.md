---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/point-list.html"
breadcrumb-title: ''
description: 使用“点列表”节点创建和管理用于样条和路径生成的点列表。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Point List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 点列表
user-guide-description: ''
user-guide-title: ''
source-git-commit: 29dd2e6adc826f63ee26defc0032b0e52d4e30fb
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 1%

---


# 点列表

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](point-list.resources/point-list-icon.png "节点图标")

<b>In：</b>样条和路径工具>样条曲线工具

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

生成由样条遍历的点的列表。

如果将现有的点列表提供给<b>点</b>输入，则生成的列表将附加到输入列表中。

</td>
</tr>
</table>

>[!TIP]
>
> 此节点可用于向[样条（多边形二次）](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md)节点提供点以生成样条。

>[!IMPORTANT]
>
> <b>点列表</b>和<b>点数</b>连接器&#x200B;*不兼容*&#x200B;与<b>样条坐标</b>、<b>样条数据</b>和<b>样条量</b>连接器不兼容，因为它们依赖于不同的数据。

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>预览</b> <i>灰度</i> | 以灰度图像形式预览点。 |
| <b>点列表输入</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的输入点列表：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> -Height<br><b>A</b> — 压缩数据：<br> *整数部分：Smoothness；<br> *分数部分：Thickness。 |
| <b>点数输入</b> <i>整数</i> | 输入点的数量。 |

<a name="outputs"></a>

## 输出

|  |  |
|:---|:---|
| <b>预览</b> <i>灰度</i> | 以灰度图像形式预览点。 |
| <b>点列表</b> <i>颜色</i> | 以彩色图像的RGBA通道编码的点的输出列表：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> -Height<br><b>A</b> — 压缩数据：<br> *整数部分：Smoothness；<br> *分数部分：Thickness。 |
| <b>点数</b> <i>整数</i> | 输出点数。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>点数</b> <i>整数</i> | 生成的点数。 |
| <b>全局Smoothness调整</b> <i>浮动</i> | 对所有点的Smoothness值应用统一的偏移。<br>生成的Smoothness值被固定在[0；1]范围内。 |
| <b>点属性</b> |  |
| <b>p#属性</b> <i>浮点3</i> | 设置p#点的属性。<br>*-Height：*&#x200B;调整较低值表示较低或较深位置的点的Height；<br>*-Smoothness：*&#x200B;在p#处偏移样条平滑化的开始，其中值0产生硬轨迹，值1产生完全平滑的轨迹；<br>*-Thickness：*&#x200B;在p#处调整样条的Thickness。 Thickness由特定的Spline节点使用。 |
| <b>点坐标</b> |  |
| <b>p#</b> <i>浮点2</i> | 设置p#点在纹理空间中的位置。 |
| <b>预览</b> |  |
| <b>显示标签</b> <i>布尔值</i> | 在“预览”输出中，每个点旁边都显示该点的名称。 |
| <b>标签大小</b> <i>浮动</i>（在“显示标签”设置为“True”时可用） | 纹理空间中每个点的标签大小，其中0.1是纹理宽度的十分之一。 |
| <b>显示点数</b> <i>布尔值</i> | 在“预览”输出中显示点。 |
| <b>点大小</b> <i>浮动</i>（在“显示点数”设置为“True”时可用） | 纹理空间中的点的半径，其中0.1是纹理宽度的十分之一。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![节点示例1](point-list.resources/PointList-Variant1.jpg "节点示例1")

</td>
<td style="border: 0;" valign="top">

![节点示例2](point-list.resources/PointList-Demo1.gif "节点示例2")

</td>
</tr>
</table>
