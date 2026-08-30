---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random.html"
breadcrumb-title: ''
description: 使用“拼贴随机”节点创建随机拼贴图案，这些图案具有有机纹理效果的程序变化。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 拼贴随机
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 7%

---


# 拼贴随机

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tile-random.resources/tile-random.png){width="128px"}

<b>英寸：</b>生成器>图案

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

“拼贴随机”生成程序拼贴图案，该图案在拼贴形状中的混乱程度略高于其对应图案[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)。 它通过随机地将某些拼贴拆分为较小的拼贴来实现此目的。 我们建议您先找到Tile Generator方法，然后再处理“平铺随机”，因为许多概念是相似的。

如果目标是外观较旧、组织性较差的模式，则使用“平铺随机”而不是[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)。 但是，它具有它的限制，因此考虑使用[平铺Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)来满足任何其他高级需求。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>模式输入</b> <i>灰度输入（颜色输入）</i> | 自定义图案图像，在“Pattern”参数设置为“Image Input”时使用。 |
| <b>背景输入</b> <i>灰度输入（颜色输入）</i> |  |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>X数量</b> <i>1 - 64</i> | 图案的X重复次数。 |
| <b>Y数量</b> <i>1 - 64</i> | 模式的Y重复次数。 |
| <b>非正方形扩展</b> <i>False/True</i> | 启用以非方形比例补偿挤压和拉伸。 |
| <b>图案</b> |  |
| <b>图案</b> <i>图案输入，方形，磁盘，抛物面，铃声，高斯，荆棘，金字塔，砖块，层次，波形，半圆，脊状的圆，新月，胶囊体，锥形</i> | 选择要使用的图案形状。 |
| <b>图像输入筛选(引擎> v4)</b> <i>双线性+ Mipmaps，双线性，最接近</i> |  |
| <b>特定图案</b> <i>0.0 - 1.0</i> | 可以更改选定图案的形状。 该效果取决于所选图案。 |
| <b>模式特定的随机</b> <i>0.0 - 1.0</i> | 随机化效果取决于选择的模式。 |
| <b>旋转</b> <i>0， 90， 180， 270，随机水平，随机垂直</i> | 设置以90度步长旋转，可选随机化。 |
| <b>旋转随机</b> <i>0.0 - 1.0</i> | 添加随机自由旋转。 |
| <b>对称随机</b> <i>0.0 - 1.0</i> | 通过选定的对称随机模式随机镜像某些图案。 此值越高，镜像的图案就越多。 |
| <b>对称随机模式</b> <i>水平+垂直，水平，垂直</i> | 确定对称随机度大于0时的镜像行为。 |
| <b>拆分</b> |  |
| <b>模式</b> <i>无、自动、自动水平、自动垂直、随机h+v</i> | 设置有关如何拆分拼贴的规则。 |
| <b>阈值</b> <i>0.0 - 1.0</i> | 调整门槛大小以确定何时拆分拼贴。 |
| <b>乘数</b> <i>0 - 10</i> | 拆分乘数。 该值越大，拆分的次数就越多。 |
| <b>大小</b> |  |
| <b>随机X</b> <i>0.0 - 1.0</i> | 在X轴上随机化不均匀缩放。 |
| <b>随机Y</b> <i>0.0 - 1.0</i> | 在Y轴上随机化不均匀缩放。 |
| <b>间隙</b> |  |
| <b>模式</b> <i>相对于最小砖块，相对于最大砖块</i> | 设置间隙相对于砖块大小。 |
| <b>金额</b> <i>0.0 - 1.0</i> | 设置砖块之间的间隙大小。 |
| <b>形状</b> |  |
| <b>缩放</b> <i>0.0 - 1.0</i> | 全局缩放每个磁贴。 |
| <b>随机缩放</b> <i>0.0 - 1.0</i> | 基于每个磁贴的随机缩放。 |
| <b>旋转</b> <i>0.0 - 1.0</i> | 每个拼贴的全局旋转。 |
| <b>旋转随机</b> <i>0.0 - 1.0</i> | 基于每个拼贴随机旋转。 |
| <b>旋转约束</b> <i>False/True</i> | 限制缩放比例，以便旋转的拼贴从不重叠。 |
| <b>位置</b> |  |
| <b>偏移</b> <i>0.0 - 1.0</i> | 全局移动或平移拼贴，仅在X轴上滑动 |
| <b>随机偏移</b> <i>0.0 - 1.0</i> | 仅在X轴上随机选择每个磁贴的偏移量 |
| <b>随机</b> <i>0.0 - 1.0</i> | 随机调整位置，拼贴在X和Y轴上移动。 |
| <b>随机约束</b> <i>False/True</i> | 限制缩放，使拼贴触摸，但不重叠。 显着降低随机位置效果的色调。 |
| <b>颜色</b> |  |
| <b>颜色</b> <i>（灰度值）/（颜色值）</i> | 设置所有拼贴的纯色。 |
| <b>颜色随机</b> <i>0.0 - 1.0</i> | 基于每个拼贴随机应用颜色。 |
| <b>颜色参数化</b> <i>无，区域，大小x，大小y</i> | 使颜色变化取决于这些设置之一。 |
| <b>颜色参数化强度</b> <i>0.0 - 1.0</i> | 以上参数化效果的乘数。 |
| <b>颜色参数化效果（仅适用于颜色）</b> <i>RGB+Alpha，仅限RGB，仅限Alpha</i> | 确定仅颜色参数化效果。 |
| <b>背景颜色</b> <i>（灰度值）/（颜色值）</i> | 设置纯背景色。 |
| <b>混合模式</b> <i>Add/Sub，Max/Add/Sub，混合（颜色）</i> | 设置背景拼贴的混合模式。 |
| <b>蒙版</b> |  |
| <b>随机</b> <i>0.0 - 1.0</i> | 随机开始遮盖拼贴。 该值越大，显示的拼贴就越多。 |
| <b>反转</b> <i>False/True</i> | 反转蒙版结果。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="tile-random.resources/tile-random-1.png" />
        </td>
    </tr>
</table>
