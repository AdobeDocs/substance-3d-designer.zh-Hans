---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/point-list.html"
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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# 点列表

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](../../../../../../assets/point-list-icon.png "节点图标")

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
> <b>点列表</b>和<b>点数</b>连接器&#x200B;*不兼容*，它们与<b>样条坐标</b>、<b>样条数据</b>和<b>样条量</b>连接器不兼容，因为它们依赖于不同的数据。

## 输入连接器

<b>预览&#x200B;</b>*灰度*&#x200B;以灰度图像形式预览点。

<b>点列表输入</b> *颜色*\
以彩色图像的RGBA通道编码的输入点列表：\
<b>R</b> - X位置\
<b>G</b> - Y位置\
<b>B</b> -Height\
<b>A</b> — 打包的数据：\
*整数部分：Smoothness；\
*小数部分：Thickness。

<b>点数输入</b> *整数*\
输入点的数量。

## 输出连接器

<b>预览&#x200B;</b>*灰度*&#x200B;以灰度图像形式预览点。

<b>点列表&#x200B;</b>*颜色*\
以彩色图像的RGBA通道编码的点的输出列表：\
<b>R</b> - X位置\
<b>G</b> - Y位置\
<b>B</b> -Height\
<b>A</b> — 打包的数据：\
*整数部分：Smoothness；\
*小数部分：Thickness。

<b>点数&#x200B;</b>*整数*\
输出点数。

## 参数

<b>点数</b> *整数*&#x200B;生成的点数。

<b>全局Smoothness调整</b> *浮动*&#x200B;对所有点的Smoothness值应用统一的偏移。\
得到的Smoothness值被固定在[0；1]范围内。

+++点属性
<b>p#属性</b> *Float3*&#x200B;设置p#点的属性。\
*-Height：*&#x200B;调整较低值表示较低或较深位置的点的Height；\
*-Smoothness：*&#x200B;在p#处偏移样条平滑化的开始，其中0值产生硬轨迹，1值产生完全平滑轨迹；\
*-Thickness：*&#x200B;在p#处调整样条的Thickness。 Thickness由特定的Spline节点使用。

+++

+++点坐标
<b>p#</b> *Float2*&#x200B;设置纹理空间中p#点的位置。

+++

+++预览
<b>显示标签</b> *布尔值*\
在“预览”输出中，每个点旁边都显示该点的名称。

<b>标签大小</b> *浮动*（在“显示标签”设置为“True”时可用）\
纹理空间中每个点的标签大小，其中0.1是纹理宽度的十分之一。

<b>显示点数</b> *布尔值*\
在“预览”输出中显示点。

<b>点大小</b> *浮动*（在“显示点数”设置为“True”时可用）\
纹理空间中的点的半径，其中0.1是纹理宽度的十分之一。

+++

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![节点示例1](../../../../../../assets/PointList-Variant1.jpg "节点示例1")

</td>
<td style="border: 0;" valign="top">

![节点示例2](../../../../../../assets/PointList-Demo1.gif "节点示例2")

</td>
</tr>
</table>
