---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/light.html"
breadcrumb-title: ''
description: 使用光照节点可根据网格光照条件生成蒙版，以创建逼真的材质变化。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 光线
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 9%

---


# 光线

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/light-2.png){width="128px"}

<b>在</b>中基于网格的生成器>蒙版生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)中的[智能蒙版](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)。

此蒙版与其他生成器稍有不同：它完全执行基于世界空间正常映射的假光照，返回黑白“光图”蒙版。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>水平角度</b> <i>0.0 - 1.0</i> | 设置伪光的水平角度。 |
| <b>垂直角度</b> <i>0.0 - 1.0</i> | 设置伪光的垂直角度。 |
| <b>高光光泽度</b> <i>0.0 - 0.999</i> | 设置突出显示区域的衰减跨页。 |
| <b>高光级别</b> <i>0.0 - 1.0</i> | 设置高亮区域的亮度级别。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/light-ex.gif" />
        </td>
    </tr>
</table>
