---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dirt.html"
breadcrumb-title: ''
description: 使用Dirt根据网格曲率、位置和遮蔽生成Dirt累积蒙版。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 污垢
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 7%

---


# 污垢

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dirt.resources/dirt-01.png){width="128px"}

<b>在</b>中基于网格的生成器>蒙版生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白色蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版基于烘焙的AO和曲率表示边缘和角落中遮挡和凹陷的Dirt。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>弯曲</b> <i>灰度输入</i> | 用于内部效果和蒙版的已烘焙贴图。 必填！ |
| <b>环境遮蔽</b> <i>灰度输入</i> | 用于内部效果和蒙版的已烘焙贴图。 必填！ |
| <b>污渍输入</b> <i>灰度输入</i> | 自定义污渍映射输入，可选，由参数启用。 |
| <b>蒙版（可选）</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 |
| <b>世界空间正常</b> <i>颜色输入</i> | 仅用于三平面。 |
| <b>位置</b> <i>颜色输入</i> | 仅用于三平面。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>Dirt级别</b> <i>0.0 - 1.0</i> | Dirt量的主控件。 |
| <b>Dirt对比度</b> <i>0.0 - 1.0</i> | 控制蒙版中Dirt的主对比度。 |
| <b>污渍量</b> <i>0.0 - 1.0</i> | 设置Dirt的脏乱程度。 设置为0可达到完美平滑Dirt。 |
| <b>边缘蒙版</b> <i>0.0 - 1.0</i> | 要从凸起边缘移除的Dirt量（基于弯曲图）。 |
| <b>使用自定义污渍</b> <i>False/True</i> | 允许使用自定义污渍映射输入，而不是内置污渍。 |
| <b>污渍比例</b> <i>1 - 16</i> | 设置污渍细节的拼贴比例。 |
| <b>使用三平面</b> <i>False/True</i> | 使用[三平面投影](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md)进行污渍映射，删除接缝。 |
| <b>三平面混合对比度</b> <i>0.001 - 1.0</i> | 设置三平面投影的对比度。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dirt.resources/dirt-02.gif" />
        </td>
    </tr>
</table>
