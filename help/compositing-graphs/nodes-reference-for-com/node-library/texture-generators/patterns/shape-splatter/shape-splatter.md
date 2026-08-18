---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter.html"
breadcrumb-title: ''
description: 使用“形状飞溅”节点可以跨纹理散点形状，以创建程序性图案和细节。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形状飞溅
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 0%

---


# 形状飞溅

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-splatter.png){width="128px"}

## 形状飞溅

**英寸：** *纹理生成器**/Patterns*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

一个非常复杂的节点，旨在与伴随的节点[“形状飞溅混合”](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-blend/shape-splatter-blend.md)、[“形状飞溅到蒙版”](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-to-mask/shape-splatter-to-mask.md)和[“形状飞溅数据提取”](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-data-ext/shape-splatter-data-extract.md)结合使用。 用于以类似于[平铺Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)或[生成器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)的方式飞溅形状，但采用动态、非破坏性的流程，允许通过类似于[Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)的多级系统来控制每个步骤。 而Flood Fill从外部源获取基本输入映射，形状飞溅器会一步生成映射和后续数据，作为[Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)的一种更高级的版本。

它的主要用途是允许将形状放置在Height地图上并受其驱动，然后从Splatter Data生成各种地图。 例如，在景观上放置岩石、树枝和树叶，由各种地图面向和驱动。 然后可以将不同的映射用于Height、正常、基色、粗糙度以及任何其他通道，而所有这些映射仍然基于相同的共享Splatter数据。

## 参数

### 输入

* **背景Height**： *灰度输入*&#x200B;背景Height，用于放置拼贴并驱动各种效果。
* **图案1-8**： *灰度输入**可选图案*
* **图案分布**： *灰度输入*&#x200B;灰度映射到
* **形状缩放**： *灰度输入*&#x200B;用于驱动拼贴缩放的灰度映射。
* **形状旋转**： *灰度输入*&#x200B;用于驱动磁贴旋转的灰度映射。
* **Height偏移**： *灰度输入*&#x200B;灰度映射，用作平铺Height的偏移。
* **Height比例**： *灰度输入*&#x200B;灰度映射，用作平铺Height的偏移。
* **蒙版随机**： *灰度输入*\
  用于遮盖节点效果的遮罩槽。
* **矢量图**： *颜色输入*&#x200B;用于驱动拼贴定位和旋转的颜色矢量图。

### 参数

* **X数量**： *1 - 64*\
  图案的X重复次数。
* **Y数量**： *1 - 64*\
  图案的Y重复次数。
* **图案**
  * **模式输入编号**： *1 - 8*&#x200B;设置要使用的不同模式数量。 解锁新的图案输入插槽。
  * **模式分布模式**： *随机，模式索引，行索引，列索引*&#x200B;设置如何确定要使用的模式。 随机或按图案、行或列。
  * **图案分布图乘数**： *0.0 - 1.0*&#x200B;设置可选分布图对图案放置的影响。
  * **图案旋转**： *0， 90， 180， 270*&#x200B;设置预设，图案旋转90度。
  * **图案旋转随机**： *0.0 - 1.0*&#x200B;设置图案的随机90度步长旋转量。
* **大小**
  * **缩放**： *0.0 - 5.0*\
    设置每个拼贴的统一比例。
  * **随机缩放**： *0.0 - 1.0*&#x200B;随机对每个图块进行统一缩放。
  * **无重叠缩放**： *0.0 - 1.0*&#x200B;统一但仅向下随机缩放，以避免重叠拼贴。 不应与前两个参数一起使用。
  * **比例图乘数**： *0.0 - 1.0*&#x200B;设置比例图的影响。
  * **大小**： *0.0 - 1.0*&#x200B;允许对拼贴进行不均匀缩放。
  * **Bg斜率的大小比例**： *0.0 - 1.0*&#x200B;将背景图斜率（正常计算）用于非均匀缩放拼贴。 模拟透视变形。
  * **大小与X/Y数量比率**： *0.0 - 1.0*&#x200B;非均匀缩放，以补偿X和Y数量中的不同比率。
* **位置**
  * **位置随机**： *0.0 - 2.0*&#x200B;每个磁贴的随机偏移位置。
  * **随机分布**： *Gaussian， Uniform*&#x200B;设置用于前一个参数的计算。 不会带来太大的差别，因为数字越大，影响越明显。 高斯分布更均匀。
  * **矢量映射乘数**： *0.0 - 1.0*&#x200B;矢量输入映射对偏移的影响。
  * **水平偏移**： *-2.0 - 2.0*&#x200B;全局水平偏移。
  * **垂直偏移**： *-2.0 - 2.0*&#x200B;全局垂直偏移。
  * **越界选项**： *缩放形状、约束位置*&#x200B;拼贴显示为越界时要执行的操作。
* **旋转**
  * **旋转**： *0.0 - 1.0*&#x200B;全局旋转所有拼贴。
  * **旋转随机**： *0.0 - 1.0*&#x200B;每块随机旋转。
  * **从背景斜率旋转**： *0.0 - 1.0*&#x200B;使用背景图斜率（正常计算）旋转拼贴。 可用于使斜率上的形状向上或向下指向。
  * **旋转贴图乘数**： *0.0 - 1.0*&#x200B;以对每个拼贴旋转的旋转贴图效果进行混合。
  * **矢量映射乘数**： *0.0 - 1.0*&#x200B;混合每磁贴旋转的旋转贴图效果。
* **Height**
  * **Height比例自动调整**： *False/True*&#x200B;相对于背景自动调整Height范围，而不是定义绝对范围。 允许更少或更多的控制。
  * **Height偏移**： *-1.0 - 1.0*&#x200B;在Height范围内统一偏移/移动所有拼贴的修饰符。
  * **Height偏移随机**： *0.0 - 1.0*&#x200B;基于每个磁贴随机更改Height偏移。
  * **Height偏移映射多路复用器**： *0.0 - 1.0*&#x200B;设置偏移映射影响的修饰符。
  * **Height缩放**： *0.0 - 1.0*&#x200B;用于在Height范围内统一缩放/扩展所有拼贴的修饰符。 与抵消相反的是，这会使图像值更加泾渭分明，如对比度。
  * **Height比例随机**： *0.0 - 1.0*&#x200B;基于每个图块随机更改Height比例。
  * **Height的比例映射乘数**： *0.0 - 1.0*&#x200B;用于设置比例映射影响的修饰符。
  * **符合背景**： *0.0 - 1.0*&#x200B;影响拼贴与背景的混合。 不符合表示高图保持刚性，符合以下背景形状。 比如对叶子和棍子都有好处。
  * **平滑匹配的背景**： *0.0 - 2.0*&#x200B;对上一个效果使用平滑值，以避免不正确或极端变化。
  * **从背景斜率倾斜**： *0.0 - 1.0*&#x200B;由背景斜率驱动的调整/斜率平铺Height（正常计算）。
  * **背景Smoothness**： *0.0 - 2.0*&#x200B;对上一个效果使用平滑值，以避免出现不正确或极端的变化。
  * **挖剪黑色像素**： *False/True*&#x200B;切换以忽略拼贴基底形状中的全黑色(0)像素。
  * **拼合图案库**： *False/True*&#x200B;调整拼贴与背景混合的行为：拼贴将与背景交叉(False)，或者较低时覆盖背景。
* **蒙版**
  * **蒙版随机**： *0.0 - 1.0*&#x200B;随机隐藏拼贴。 此值越高，拼贴消失得越多。
  * **蒙版随机映射乘数**： *0.0 - 1.0*&#x200B;何时开始隐藏蒙版映射的阈值。
  * **来自Bg斜率的蒙版**： *-1.0 - 1.0*&#x200B;使用背景图斜率（正常计算）来隐藏拼贴。

## 示例图像

</td>
</tr>
</table>
