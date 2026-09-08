---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-splitter.html"
breadcrumb-title: ''
description: 使用Atlas Splitter节点将纹理图集分割成单独的纹理，用于处理扫描的材料。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Splitter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas Splitter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---


# Atlas Splitter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![节点图标](../../../../../../assets/atlas-splitter.png "节点图标")

<b>进入：</b>个材质筛选器/扫描处理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

采用贴图集图像输入，并将所有单独的元素拆分为&#x200B;*单独的素材*。

它还可以用于重新组织和移动所有元素到网格中。

该节点作为[Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)节点的高级应用程序工作。

</td>
</tr>
</table>

## 参数

<b>网格视图</b> *布尔值*\
在网格中显示所有检测到的形状。

<b>网格不透明度</b> *浮动*\
在“网格视图”为True时设置网格线的不透明度。 调试选项

<b>网格选区不透明度</b> *浮动*\
如果网格视图为True，则设置网格选区突出显示的不透明度。 调试选项

<b>自动缩放</b> *布尔值*\
自动缩放形状以适合网格单元格。

<b>自动裁剪</b> *布尔值*\
根据最大的形状自动裁剪输出大小，以最大限度地减少空白空间。

<b>形状选区</b> *整数*\
在网格视图中设置突出显示哪个单元格，在网格视图之外设置返回哪个单元格。

<b>忽略小于</b>的形状 *浮动*\
忽略对角线大小小于指定值的形状。

<b>自动旋转</b> *布尔值*\
根据其定界框大小比例自动旋转形状。

<b>旋转</b> *浮动*\
全局形状旋转角度

<b>输入法线格式</b> *整数*\
设置输入法线的格式。 设置错误的格式将导致错误的结果。

<b>缩小不透明度蒙版</b> *整数*\
缩小不透明度蒙版以移除潜在的杂色或孤立像素。 它防止了不需要形状的检测，并且还提高了性能。

<b>扩展宽度</b> *浮动*\
在除“正常”和“Height”以外的所有声道上，应用基于“不透明度”蒙版的膨胀效果。

<b>启用其他输入</b> *布尔值*\
对于未涵盖的任何其他地图，提供“用户1”和“用户2”的输入和设置。

<b>自定义背景颜色</b> *布尔值*\
允许您选择自定义背景色，而不是该图层内容的膨胀。

<b>Base color背景色</b> *Float3*\
为Base color自定背景色。

<b>正常背景色</b> *Float3*\
为法线图自定背景色。

<b>金属背景色</b> *Float*\
金属的自定背景色。

<b>粗糙度背景色</b> *Float*\
用于粗糙度的自定背景色

<b>Height背景色</b> *Float*\
用于Height的自定背景色

<b>用户1背景颜色</b> *Float*\
自定义“用户1”映射的自定义BG颜色

<b>用户2背景颜色</b> 自定义“用户1”映射的&#x200B;*Float*&#x200B;自定义BG颜色

## 示例
