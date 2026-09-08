---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dust.html"
breadcrumb-title: ''
description: 使用Dust根据网格几何形状生成Dust累积蒙版，用于创建逼真的Dust和颗粒效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dust
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 5%

---


# Dust

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/dust.png){width="128px"}

<b>在</b>中基于网格的生成器>蒙版生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版表示在遮蔽的降低区域中以及仅在面部朝上的区域中积累的Dust。 需要正确的烘焙原子氧和世界空间法线才能工作。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>环境遮蔽</b> <i>灰度输入</i> | 用于Dust放置的已烘焙贴图。 必填！ |
| <b>世界空间正常</b> <i>颜色输入</i> | 用于Dust放置的已烘焙贴图。 必填！ |
| <b>杂色</b> <i>灰度输入</i> | 自定义Dust映射（可选），仅在“覆盖杂色”设置为True时出现。 |
| <b>蒙版（可选）</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>级别</b> <i>0.0 - 1.0</i> | 设置Dust的总量。 |
| <b>对比度</b> <i>0.0 - 1.0</i> | 调整Dust的对比度。 |
| <b>遮蔽数量</b> <i>0.0 - 1.0</i> | 设置AO的影响；被遮挡区域将出现更多Dust。 |
| <b>噪声不透明度</b> <i>0.0 - 1.0</i> | 设置灰尘区域中可见的噪声量。 |
| <b>覆盖噪声</b> <i>False/True</i> | 设置为使用自定义Dust映射输入。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/dust-ex.gif" />
        </td>
    </tr>
</table>
