---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/gradient-radial.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---


# 径向渐变

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/gradient-radial.png){width="128px"}

## 径向渐变

**英寸：** *纹理生成器**/Patterns*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

类似于[渐变圆形](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-circular/gradient-circular.md)，创建由两个自定义点以径向方式定义的灰度渐变过渡。 过渡从a到b，由中心点和半径定义。 请记住，结果并不总是平铺的。

## 参数

* **形状： *半球，圆锥***确定过渡轮廓。 圆锥是锐化的线性过渡，半球是柔和的并在中间是圆的。
* **点1**：\
  渐变的中心点。 白手起家。
* **点2**：\
  用于确定渐变范围的半径点。 结尾为黑色。
* **非正方形扩展**： *False/True*\
  启用使用非方形比率补偿挤压和拉伸。

</td>
</tr>
</table>
