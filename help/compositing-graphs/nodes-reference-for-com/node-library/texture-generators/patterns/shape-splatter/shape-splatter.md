---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter.html"
breadcrumb-title: ''
description: 使用“形状飞溅”节点可在纹理间散点形状，以创建程序化的图案和细节。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 形状飞溅
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 7%

---


# 形状飞溅

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-splatter.resources/shape-splatter.png){width="128px"}

<b>进入：</b>纹理生成器>图案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

非常复杂的节点，旨在与伴随的节点[“形状飞溅”混合](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-blend/shape-splatter-blend.md)、[“形状飞溅到蒙版”](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-to-mask/shape-splatter-to-mask.md)和[“形状飞溅数据提取”](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-data-ext/shape-splatter-data-extract.md)结合使用。 用于以类似于[平铺Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)或[生成器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)的方式飞溅形状，但采用动态、非破坏性的流程，允许通过类似于[Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)的多级系统来控制每个步骤。 而Flood Fill从外部源获取基本输入图，形状飞溅器会一步生成地图和后续数据，是一种更高级的[Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)版本。

它的主要用途是允许将形状放置在高度图上并由其驱动，然后从Splatter Data生成各种地图。 例如，在景观上放置岩石、树枝和树叶，由各种地图面向和驱动。 然后，可以将不同的映射用于Height、正常、基色、粗糙度和任何其他通道，而所有这些映射仍然基于相同的共享Splatter Data。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>背景Height</b> <i>灰度输入</i> | 背景Height，用于放置拼贴并驱动各种效果。 |
| <b>图案1-8</b> <i>灰度输入</i> | 可选模式 |
| <b>模式分布</b> <i>灰度输入</i> | 灰度映射到 |
| <b>形状缩放</b> <i>灰度输入</i> | 灰度映射可驱动磁贴缩放。 |
| <b>形状旋转</b> <i>灰度输入</i> | 灰度映射可驱动拼贴旋转。 |
| <b>Height偏移</b> <i>灰度输入</i> | 用作拼贴Height偏移量的灰度映射。 |
| <b>Height比例</b> <i>灰度输入</i> | 用作拼贴Height偏移量的灰度映射。 |
| <b>蒙版随机</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 |
| <b>矢量图</b> <i>颜色输入</i> | 用于驱动磁贴定位和旋转的彩色矢量图。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>X数量</b> <i>1 - 64</i> | 图案的X重复次数。 |
| <b>Y数量</b> <i>1 - 64</i> | 图案的Y重复次数。 |
| <b>图案</b> |  |
| <b>模式输入编号</b> <i>1 - 8</i> | 设置要使用的不同图案的数量。 解锁新的图案输入插槽。 |
| <b>模式分发模式</b> <i>随机，模式索引，行索引，列索引</i> | 设置如何确定要使用的模式。 随机或按图案、行或列。 |
| <b>模式分布图乘数</b> <i>0.0 - 1.0</i> | 设置可选分布图对图案放置的影响。 |
| <b>图案旋转</b> <i>0, 90, 180, 270</i> | 设置预设，图案旋转90度。 |
| <b>图案旋转随机</b> <i>0.0 - 1.0</i> | 设置图案的随机90度步长旋转量。 |
| <b>大小</b> |  |
| <b>缩放</b> <i>0.0 - 5.0</i> | 设置每个拼贴的统一比例。 |
| <b>随机缩放</b> <i>0.0 - 1.0</i> | 随机化每个拼贴的均匀比例。 |
| <b>缩放无重叠</b> <i>0.0 - 1.0</i> | 统一但仅向下随机缩放，以避免重叠的拼贴。 不应与前两个参数一起使用。 |
| <b>缩放映射乘数</b> <i>0.0 - 1.0</i> | 设置比例尺地图的影响。 |
| <b>大小</b> <i>0.0 - 1.0</i> | 允许拼贴缩放不均匀。 |
| <b>来自Bg斜率的大小比例</b> <i>0.0 - 1.0</i> | 将背景图斜率（计算法线）用于不均匀缩放的拼贴。 模拟透视变形。 |
| <b>大小与X/Y量的比率</b> <i>0.0 - 1.0</i> | 用于补偿X和Y量中不同比例的非均匀缩放。 |
| <b>位置</b> |  |
| <b>位置随机</b> <i>0.0 - 2.0</i> | 每个拼贴的随机偏移位置。 |
| <b>随机分布</b> <i>高斯，一致</i> | 设置用于前一个参数的计算。 不会带来太大的差别，因为数字越大，影响越明显。 高斯分布更均匀。 |
| <b>矢量映射乘数</b> <i>0.0 - 1.0</i> | 矢量输入图对偏移量的影响。 |
| <b>水平偏移</b> <i>-2.0 - 2.0</i> | 全局水平偏移量。 |
| <b>垂直偏移</b> <i>-2.0 - 2.0</i> | 全局垂直偏移。 |
| <b>越界选项</b> <i>缩放形状，约束位置</i> | 拼贴显示为越界时要执行的操作。 |
| <b>旋转</b> |  |
| <b>旋转</b> <i>0.0 - 1.0</i> | 全局旋转所有拼贴。 |
| <b>旋转随机</b> <i>0.0 - 1.0</i> | 为每个拼贴随机旋转。 |
| <b>从背景斜率旋转</b> <i>0.0 - 1.0</i> | 使用背景图斜率（正常计算）旋转拼贴。 可用于使斜率上的形状向上或向下指向。 |
| <b>旋转贴图乘数</b> <i>0.0 - 1.0</i> | 旋转贴图对每拼贴旋转的影响下的混合。 |
| <b>矢量映射乘数</b> <i>0.0 - 1.0</i> | 旋转贴图对每拼贴旋转的影响下的混合。 |
| <b>Height</b> |  |
| <b>Height比例自动调整</b> <i>False/True</i> | 相对于背景自动调整Height范围，而不是定义绝对范围。 允许更少或更多的控制。 |
| <b>Height偏移</b> <i>-1.0 - 1.0</i> | 用于在Height范围内均匀地偏移/移动所有拼贴的修改量。 |
| <b>Height偏移随机</b> <i>0.0 - 1.0</i> | 基于每个拼贴随机更改Height偏移。 |
| <b>Height偏移映射多路复用器</b> <i>0.0 - 1.0</i> | 用于设置偏移图影响的修饰符。 |
| <b>Height比例</b> <i>0.0 - 1.0</i> | 在Height范围内统一缩放/扩展所有拼贴的修改量。 与抵消相反的是，这会使图像值更加泾渭分明，如对比度。 |
| <b>随机Height缩放</b> <i>0.0 - 1.0</i> | 基于每个拼贴随机更改Height比例。 |
| <b>Height的比例映射乘数</b> <i>0.0 - 1.0</i> | 用于设置“比例图”影响的修饰符。 |
| <b>遵从背景</b> <i>0.0 - 1.0</i> | 影响拼贴与背景的混合。 不符合表示高图保持刚性，符合以下背景形状。 比如对叶子和棍子都有好处。 |
| <b>平滑匹配的背景</b> <i>0.0 - 2.0</i> | 为上一个效果设置平滑值，以避免不正确或极端变化。 |
| <b>从背景斜率倾斜</b> <i>0.0 - 1.0</i> | 调整/斜率由背景Height驱动的拼贴斜率（正常计算）。 |
| <b>后台Smoothness</b> <i>0.0 - 2.0</i> | 为上一个效果设置平滑值，以避免不正确或极端变化。 |
| <b>抠图黑色像素</b> <i>False/True</i> | 切换以忽略拼贴基础形状中的全黑色(0)像素。 |
| <b>拼合图案库</b> <i>False/True</i> | 调整拼贴与背景的混合行为：拼贴将与背景相交(False)，或者较低时覆盖背景。 |
| <b>蒙版</b> |  |
| <b>蒙版随机</b> <i>0.0 - 1.0</i> | 随机隐藏拼贴。 此值越高，拼贴消失得越多。 |
| <b>掩码随机映射乘数</b> <i>0.0 - 1.0</i> | 何时开始隐藏拼贴对蒙版图进行主动变更。 |
| <b>来自Bg斜率的蒙版</b> <i>-1.0 - 1.0</i> | 使用背景图斜率（正常计算）隐藏拼贴。 |
