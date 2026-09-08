---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape.html"
breadcrumb-title: ''
description: 使用“形状”节点可生成用于在Substance 3D Designer中创建图案和纹理的基本几何形状。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形状
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# 形状

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-2.png){width="128px"}

## 形状

**在：** *纹理生成器**/Patterns*

**中级**

</td>
<td style="border: 0;" valign="top">

## 描述

生成各种程序化形状，其中包含修改基础形状的选项。 形状始终具有完美插值和高精度。

尽管简单明了，但这是一个非常有用的节点：它是大多数程序化的高度图生成的构建块！ 通过将基本形状与变换节点相结合，可以创建比任何位图都更精确的完全程序化的高位图形状。

## 参数

* **拼贴**： *1 - 16*\
  设置结果应平铺的次数。
* **图案**：*方形、圆盘、抛物面、铃声、高斯、荆棘、金字塔、砖块、层次、波浪、半圆、脊状的圆、渐隐、胶囊体、锥形*、半球**\
  选择要使用的图案形状。
* **特定模式**： *0.0 - 1.0*\
  可以更改选定图案的形状。 该效果取决于所选图案。
* **缩放**： *0.0 - 1.0*&#x200B;缩放整个形状。
* **大小**： *0.0 - 1.0*&#x200B;允许在X或Y轴上进行非均匀缩放。
* **角度**： *0.0 - 1.0*&#x200B;旋转整个形状。
* **旋转45°**： *False/True*&#x200B;以预设45度旋转。
* **非正方形扩展**： *False/True*\
  启用压缩补偿并使用非正方形比例拉伸。
* **非正方形拼贴**&#x200B;**：** *False/True*启用非正方形扩展后，这将拼贴形状而不压缩。

## 示例图像

![](../../../../../../assets/shape-ex.gif)

</td>
</tr>
</table>
