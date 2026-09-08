---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-sampler.html"
breadcrumb-title: ''
description: 使用“拼贴Sampler”节点可对输入纹理中的拼贴进行采样和排列，以便在Substance 3D Designer中创建拼贴图案。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Sampler
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 平铺Sampler
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 0%

---


# 平铺Sampler

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tile-sampler.png){width="128px"}

## 平铺Sampler（颜色）

**在：** *纹理生成器**/Patterns*

**复杂**

</td>
<td style="border: 0;" valign="top">

## 描述

拼贴Sampler是终极的拼贴图案生成节点。 它是[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)的演化版本，更为复杂。 截至2017年2.1月，拼贴Sampler与[生成器](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)之间的差异已小得多。 主要的差异现在仅在七个不同的映射槽中，这些槽可用于驱动缩放、位置、旋转、大小、颜色和蒙版。 它们的效果可以单独混合。

拼贴Sampler可用于创建人工程序化图案，并可额外控制由外部输入图驱动的特定参数。

在转到“平铺Sampler”之前，请确保您熟悉[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)。 在大多数情况下，您会发现[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)已足够，您不需要增加平铺Sampler的复杂性。

## 参数

### 输入

* **图案输入1-6**： *灰度输入/彩色输入*\
  自定义图案图像，在“Pattern”参数设置为“Image Input”时使用。\
  可用输入量由&#x200B;**模式输入数字**&#x200B;参数确定。
* **缩放映射输入**： *灰度输入*&#x200B;用于驱动磁贴缩放的灰度映射。
* **位移映射输入**： *灰度输入*&#x200B;灰度映射以驱动平铺位移。
* **输入**&#x200B;旋转贴图： *灰度输入*\
  灰度映射可驱动拼贴旋转。
* **矢量图输入**： *颜色输入*\
  用于驱动非均匀缩放的彩色矢量图。
* **颜色映射输入**： *灰度输入/颜色输入*&#x200B;映射到驱动器每磁贴色调。
* **蒙版映射输入**： *灰度输入*\
  用于隐藏某些拼贴的蒙版插槽。
* **模式分布图输入**： *灰度输入*\
  用于驱动多个自定义模式输入的掩码插槽。
* **背景输入**：*灰度输入/彩色输入*&#x200B;可选的背景图像。

### 参数

* **X数量**： *0 - 64*\
  图案的X重复次数。
* **Y数量**： *0 - 64*\
  模式的Y重复次数。
* **非正方形扩展**： *False/True*\
  启用以非方形比例补偿挤压和拉伸。
* **图案**
  * **图案**：*图案输入，方形，圆盘，抛物面，贝尔，高斯，刺，金字塔，砖，渐变，波形，半铃，脊状贝尔，新月，胶囊，锥形体*\
    选择要使用的图案形状。
  * **图案输入编号**： *1 - 6*&#x200B;要随机选择的自定义图案数量。
  * **模式输入分布**： *随机，模式数，分布图*&#x200B;设置选择多个模式输入的方式。 “随机”表示选择随机类型，“模式编号”表示它们仅置入循环序列中。 分布图使用灰度图输入来驱动放置。
  * **模式输入筛选(引擎> v4)**： *双线性+ Mipmaps，双线性，最接近*
  * **特定模式**： *0.0 - 1.0*\
    可以更改选定图案的形状。 该效果取决于所选图案。
  * **特定于模式的随机**： *0.0 - 1.0*&#x200B;随机化效果取决于选定的模式。
  * **旋转**： *0、90、180、270*&#x200B;阶梯式旋转（90度）。
  * **旋转随机**： *0.0 - 1.0*&#x200B;基于每个磁贴的随机自由旋转。
  * **对称随机**： *0.0 - 1.0*&#x200B;设置应根据以下行为随机翻转/镜像的磁贴数。
  * **对称随机模式**： *水平+垂直、水平、垂直*&#x200B;确定对称镜像行为。
* **大小**
  * **大小模式**：*正常、保持比例、绝对、像素*&#x200B;设置图案大小的一般行为。\
    “法线”允许您定义阵列元素的大小。 受X和Y值的影响。\
    使用“Keep Ratio”（保持比例），可以设置受X和Y量影响的大小，但两者的X和Y比例保持不变。\
    绝对用于设置不受X和Y数量影响的绝对大小。\
    “像素”可用于设置绝对大小（以像素为单位），不受X和Y数量影响。 更改分辨率将会影响元素的大小。
  * **大小（绝对/像素）**： *0.0 - 1.0*&#x200B;更改拼贴的不均匀比例。 确切的行为取决于大小模式。
  * **大小随机**： *0.0 - 1.0*&#x200B;随机选择每个图块的比例。
  * **比例**： *0.0 - 10.0*&#x200B;设置全局图块比例。
  * **随机缩放**： *0.0 - 1.0*&#x200B;随机缩放每个图块
  * **比例图乘数**： *0.0 - 1.0*&#x200B;比例图效果中的混合。
  * **缩放矢量映射乘数**： *0.0 - 1.0*&#x200B;在缩放矢量映射的影响下混合以驱动非均匀缩放。
  * **缩放参数化影响**：*X和Y、X、Y*&#x200B;设置缩放参数化影响的轴。 用于使比例映射仅影响元素的X或Y。
* **位置**
  * **位置随机**： *0.0 - 10.0*&#x200B;在两个轴上随机分布图块位置。
  * **偏移**： *0.0 - 1.0*\
    根据“位移类型”移动拼贴。
  * **偏移类型**： *水平quincux、垂直quincux、水平全局、垂直全局*&#x200B;更改偏移操作的方向。
  * **全局偏移**： *0.0 - 1.0*&#x200B;全局偏移X轴或Y轴上的所有拼贴。
  * **位移映射强度**： *0.0 - 1.0*&#x200B;位移映射强度在偏移处的混合。
  * **位移角度**： *0.0 - 1.0*&#x200B;设置要置换的角度。
  * **矢量地图位移**： *0.0 - 1.0*&#x200B;使用矢量地图来驱动位移和角度。
* **旋转**
  * **旋转**： *0.0 - 1.0*&#x200B;全局旋转所有拼贴。
  * **旋转随机**： *0.0 - 1.0*&#x200B;每块随机旋转。
  * **旋转贴图乘数**： *0.0 - 1.0*&#x200B;以对每个拼贴旋转的旋转贴图效果进行混合。
  * **矢量映射乘数**： *0.0 - 1.0*&#x200B;使用矢量映射来驱动每个磁贴旋转。
* **颜色**
  * **蒙版映射阈值**： *0.0 - 1.0*&#x200B;何时开始隐藏拼贴的蒙版映射阈值。
  * **蒙版映射反转**： *False/True*&#x200B;反转蒙版映射效果。
  * **蒙版图采样技术**： *图案中心，图案定界框（较慢）*隐藏操作应通过单点确定还是通过定界框确定。 避免导致奇怪效果的游离像素。
  * **蒙版随机**： *0.0 - 1.0*&#x200B;随机蒙版与蒙版映射并行工作。
  * **反转蒙版**： *False/True*&#x200B;反转随机蒙版。
  * **混合模式**： *Add/Sub， Max (Tile Sampler) /* Add/Sub， Blend Blend* (Tile Sampler Color)*混合模式，用于背景上的拼贴和彼此之间的拼贴。
  * **颜色**： *（灰度值）/（颜色值）*纯色、全局拼贴颜色。
  * **颜色/明亮度随机**： *0.0 - 1.0*&#x200B;颜色随机化，每块。
  * **颜色参数化模式**： *颜色输入、缩放、行索引、行索引、图案索引（平铺Sampler）*\
    */ *色图、缩放、线索引、行索引、图案索引、图案中心位置、图案中心位置(RG)球面大小(B) （拼贴Sampler颜色）**设置颜色随机化的精确程度。
  * **颜色参数化乘数**： *0.0 - 1.0*&#x200B;以上参数化效果中的混合。
  * **颜色参数化影响（仅限Alpha）：** **RGB+Alpha，仅限RGB，仅限Color**&#x200B;设置参数化如何影响颜色。
  * **全局不透明度（仅灰度）**： *0.0 - 1.0*&#x200B;设置全局磁贴不透明度。
  * **背景颜色**： *（灰度值） / （颜色值）*设置纯背景颜色。
  * **反向渲染顺序**： *False/True*&#x200B;反向渲染顺序以从后到前。

## 示例图像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/tilesampler-ex2.png" width="256px"/></div> |
| --- |
|  |

*示例显示参数如何由输入图（图案分布、缩放、旋转）驱动。*

</td>
</tr>
</table>
