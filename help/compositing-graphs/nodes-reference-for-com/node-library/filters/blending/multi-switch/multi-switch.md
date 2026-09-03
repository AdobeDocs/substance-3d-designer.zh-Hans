---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/multi-switch.html"
breadcrumb-title: ''
description: 使用多交换机纹理基于条件纹理选择的选择器在多个输入节点之间切换。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Multi Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多交换机
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# 多交换机

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-switch.resources/multi-switch-01.png){width="128px"}

![](multi-switch.resources/multi-switch-02.png){width="128px"}

<b>英寸：</b>滤镜>混合

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

充当切换框，仅传递由“输入选择”参数定义的输入。 因此，如果连接了两个输入，则根据用户的选择，将只返回其中一个输入（未修改）。

对于在图形中添加许多不同的选项非常有用。 结合[公开](../../../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)（最好作为下拉列表），可以进行大量自定义。

重要提示：请确保使用适用于您的输入的版本！ 对颜色输入使用“多开关”，对灰度输入使用“多开关灰度”。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>输入1-20</b> <i>颜色输入</i> |  |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>输入数字</b> <i>2 - 20</i> | 要公开的输入值。 重要提示：在数量减少时不要删除连接！ |
| <b>输入选择</b> <i>1 - 20</i> | 要作为结果返回的输入。 |
