---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/grunge-rust-fine.html"
breadcrumb-title: ''
description: 使用铁锈精细节点生成精细的铁锈图案，用于为金属添加腐蚀和风化效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Grunge Rust Fine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 铁锈正常
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 1%

---


# 铁锈正常

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/grungerustfine.jpg){width="200px"}

**位置：** *纹理生成器* */杂色*

**简单**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

**铁锈Fine**&#x200B;节点会生成类似于精细污渍铁锈叠加的污渍映射。

</td>
</tr>
</table>

## 参数

* **平衡** *浮动*&#x200B;调整暗值和亮值之间的平衡。
* **对比度** *浮动*&#x200B;调整图像的对比度。
* **反转** *布尔值*&#x200B;使用`1-x`操作反转图像的输出。
* **非正方形扩展***布尔值*&#x200B;启用以非方形比率补偿挤压和拉伸。
* 高级
  * **基础污渍对比度** *浮动*&#x200B;调整用作铁锈基础的污渍纹理的对比度。
  * **基本变形强度** *浮动*&#x200B;调整应用于污渍映射的变形效果的强度，该映射用作铁锈的基础。
  * **条纹强度***浮动*&#x200B;调整基本污渍纹理上叠加的较亮条纹和斑点的强度。
  * **杂色强度***浮动*&#x200B;调整应用于基本污渍纹理的杂色强度。
  * **锐化强度***浮动*&#x200B;调整全局锐化效果的强度。

## 示例图像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/grungerustfine-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/grungerustfine-variant.jpg){width="256px"}

</td>
</tr>
</table>
