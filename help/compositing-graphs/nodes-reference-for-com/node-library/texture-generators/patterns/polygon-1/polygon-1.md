---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/polygon-1.html"
breadcrumb-title: ''
description: 使用“多边形1”节点为几何纹理生成具有可自定义的边和属性的基本多边形图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Polygon 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多边形1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 1%

---


# 多边形1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/polygon-1-1.png){width="128px"}

## 多边形1

**英寸：** *纹理生成器**/Patterns*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

生成多边形形状，其中包含许多调整选项。 有关更简单的版本，请参阅[多边形2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/polygon-2/polygon-2.md)。

## 参数

* **边数**： *3 - 32*&#x200B;设置多边形应具有的边数。
* **爆炸**： *0.0 - 1.0*&#x200B;将多边形“切片”分开。
* **三角形大小**： *0.0 - 1.0*&#x200B;调整切片/三角形的大小。 任何调整都可能使形状分离，只有1,1。 完全连接！
* **缩放**： *0.0 - 1.0*&#x200B;将整个形状作为一个整体进行缩放。
* **自动缩放**： *False/True*&#x200B;调整缩放，使整个多边形适合视图，并使用默认参数。
* **旋转**： *0.0 - 1.0*&#x200B;旋转整个形状。
* **渐变**： *False/True*&#x200B;生成渐变切片/三角形，而不是纯色切片/三角形。 注意：启用此设置后，将变得与多边形2类似。
* **渐变反转**： *False/True*&#x200B;如果启用了“渐变”，则反转渐变方向。
* **拼贴**： *1 - 16*\
  设置结果应平铺的次数。
* **非正方形扩展**： *False/True*\
  启用以非方形比例补偿挤压和拉伸。
* **非方形拼贴**&#x200B;**：** *False/True*启用非正方形扩展功能后，这将拼贴形状而不压缩。

## 示例图像

![](../../../../../../assets/polygon-1-ex.gif)

</td>
</tr>
</table>
