---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/gradient-radial.html"
breadcrumb-title: ''
description: 使用“渐变”径向节点创建从中心点辐射的径向渐变，以实现圆形颜色过渡。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Gradient Radial
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 径向渐变
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 1%

---


# 径向渐变

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](gradient-radial.resources/gradient-radial-01.png){width="128px"}

<b>进入：</b>纹理生成器>图案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

类似于[渐变圆形](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-circular/gradient-circular.md)，创建由两个自定义点以径向方式定义的灰度渐变过渡。 过渡从a到b，由中心点和半径定义。 请记住，结果并不总是平铺的。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>形状</b> <i>锥形，半球</i> | 确定过渡配置文件。 锥形是一种锐化的线性过渡，半球是柔和的，其中心是圆的。 |
| <b>点1</b> | 渐变的中心点。 白手起家。 |
| <b>点2</b> | 用于确定渐变范围的半径点。 结尾为黑色。 |
| <b>非正方形扩展</b> <i>False/True</i> | 启用使用非方形比率补偿挤压和拉伸。 |
