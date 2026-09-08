---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random.html"
breadcrumb-title: ''
description: 使用“拼贴随机”节点创建具有程序化变化的随机拼贴图案，用于有机纹理效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 拼贴随机
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---


# 拼贴随机

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tile-random.png){width="128px"}

## 平铺随机（颜色）

**在：** *生成器/图案*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

拼贴随机生成程序化的拼贴图案，该图案在拼贴形状中的混乱程度略高于其对应图案[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)。 它通过随机地将某些拼贴拆分为较小的拼贴来实现此目的。 我们建议您先找到Tile Generator方法，然后再处理“平铺随机”，因为许多概念是相似的。

如果目标是外观较旧、组织性较差的模式，则使用“平铺随机”而不是[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)。 但是，它具有它的限制，因此考虑使用[平铺Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)来满足任何其他高级需求。

## 参数

### 输入

* **图案输入**： *灰度输入（颜色输入）*\
  自定义图案图像，在“Pattern”参数设置为“Image Input”时使用。
* **背景输入**： *灰度输入（颜色输入）*

### 参数

* **X数量**： *1 - 64*\
  图案的X重复次数。
* **Y数量**： *1 - 64*\
  模式的Y重复次数。
* **非正方形扩展**： *False/True*\
  启用压缩补偿并使用非正方形比例拉伸。
* **图案**
  * **图案**：*图案输入，方形，磁盘，抛物面，铃声，高斯，荆棘，金字塔，砖块，层次，波形，半圆，脊状的圆，新月，胶囊体，锥形*\
    选择要使用的图案形状。
  * **图像输入筛选(引擎> v4)**： *双线性+ Mipmaps，双线性，最接近*
  * **特定模式**： *0.0 - 1.0*\
    可以更改选定图案的形状。 该效果取决于所选图案。
  * **特定于模式的随机**： *0.0 - 1.0*&#x200B;随机化效果取决于选定的模式。
  * **旋转**： *0， 90， 180， 270，随机水平，随机垂直*&#x200B;设置90度步长旋转，可选随机化。
  * **旋转随机**： *0.0 - 1.0*&#x200B;添加随机自由旋转。
  * **对称随机**： **0.0 - 1.0**&#x200B;按所选对称随机模式随机镜像某些图案。 此值越高，镜像的图案就越多。
  * **对称随机模式**： *水平+垂直、水平、垂直*&#x200B;确定对称随机大于0时的镜像行为。
* **拆分**
  * **模式**： *无、自动、自动水平、自动垂直、随机h+v*&#x200B;设置拆分拼贴的规则。
  * **阈值**： *0.0 - 1.0*&#x200B;何时拆分磁贴的阈值大小。
  * **乘数**： *0 - 10*&#x200B;拆分乘数。 该值越大，拆分的次数就越多。
* **大小**
  * **随机X**： *0.0 - 1.0*&#x200B;在X轴上随机化非均匀缩放。
  * **随机Y**： *0.0 - 1.0*&#x200B;在Y轴上随机化非均匀缩放。
* **间隙**
  * **模式**： *相对于最小砖块，相对于最大砖块*&#x200B;设置砖块大小间隙相对于。
  * **数量**： *0.0 - 1.0*&#x200B;设置砖块之间的间隙大小。
* **形状**
  * **缩放**： *0.0 - 1.0*&#x200B;对所有图块进行全局缩放。
  * **随机缩放**： *0.0 - 1.0*&#x200B;基于每个磁贴的随机缩放。
  * **旋转**： *0.0 - 1.0*&#x200B;每个磁贴的全局旋转。
  * **旋转随机**： *0.0 - 1.0*&#x200B;基于每个拼贴随机旋转。
  * **旋转约束**： *False/True*&#x200B;约束缩放，以使旋转的拼贴从不重叠。
* **位置**
  * **偏移**： *0.0 - 1.0*\
    全局移动或平移磁贴，仅在X轴上滑动
  * **随机偏移**： *0.0 - 1.0*&#x200B;随机分布每块偏移，仅在X轴上滑动
  * **随机**： *0.0 - 1.0*&#x200B;随机化位置，拼贴在X和Y轴上移动。
  * **随机约束**： *False/True*&#x200B;约束缩放，使拼贴触摸，但不重叠。 显着降低随机位置效果的色调。
* **颜色**
  * **颜色**： *（灰度值） / （颜色值）*为所有拼贴设置纯色。
  * **颜色随机**： *0.0 - 1.0*&#x200B;基于每个拼贴随机化颜色。
  * **颜色参数化**： *无，区域，大小x，大小y*&#x200B;使颜色变化取决于这些设置之一。
  * **颜色参数化强度**： *0.0 - 1.0*&#x200B;上述参数化效果的乘数。
  * **颜色参数化效果（仅适用于Alpha）：** **RGB+Alpha、仅限RGB、仅限颜色**&#x200B;确定仅限颜色参数化效果。
  * **背景颜色**： *（灰度值） / （颜色值）*设置纯背景颜色。
  * **混合模式**：*添加/子集，最大值/*&#x200B;添加/子集，混合（颜色）**为背景上的拼贴设置混合模式。
* **蒙版**
  * **随机**： *0.0 - 1.0*&#x200B;随机开始遮盖拼贴。 该值越大，显示的拼贴就越多。
  * **反转**： *False/True*\
    反转蒙版结果。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/tile-random-1.png" width="256px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
