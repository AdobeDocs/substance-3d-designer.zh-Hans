---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/switch.html"
breadcrumb-title: ''
description: 使用“Switch Node”（切换纹理）根据条件纹理选择的蒙版在两个输入节点之间进行切换。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 切换
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 3%

---


# 切换

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](switch.resources/switch-01.png){width="128px"}

![](switch.resources/switch-02.png){width="128px"}

<b>英寸：</b>滤镜>混合

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

简单的双位置开关节点。 根据Switch参数设置返回Input 1或Input 2。 未修改结果。 有关更高级的版本，请参阅[Multi Switch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md)。

在图形中公开布尔型(True/False)选择非常有用，在该选项中，您只需要一个按钮，而无需使用复杂的下拉列表来选择整个选项。

重要提示：请确保使用适用于您的输入的版本！ 对颜色输入使用“切换”，对灰度输入使用“切换灰度”。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>输入1 (True)</b> <i>彩色或灰度输入</i> |  |
| <b>输入2 (False)</b> <i>彩色或灰度输入</i> |  |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>切换</b> <i>False/True</i> | 在输入1 (True)和输入2 (False)之间切换。 |
