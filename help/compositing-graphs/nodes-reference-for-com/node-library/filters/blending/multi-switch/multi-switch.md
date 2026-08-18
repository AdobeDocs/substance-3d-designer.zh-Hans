---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/multi-switch.html"
breadcrumb-title: ''
description: 使用多切换节点根据条件纹理选择的选择器在多个输入纹理之间切换。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Multi Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多交换机
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---


# 多交换机

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-switch-greyscale.png){width="128px"}

![](../../../../../../assets/multi-switch.png){width="128px"}

## Multi Switch（灰度）

**范围：** *滤镜/混合*

**简单**

</td>
<td style="border: 0;" valign="top">

## 描述

充当切换框，仅传递由“输入选择”参数定义的输入。 因此，如果连接了两个输入，则根据用户的选择，将只返回其中一个输入（未修改）。

对于在图表中添加许多不同的选项非常有用。 结合[公开](../../../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)（最好作为下拉列表），可以进行大量自定义。

重要提示：请确保使用适用于您的输入的版本！ 对颜色输入使用“多开关”，对灰度输入使用“多开关灰度”。

## 参数

### 输入

* **输入1-20**： *颜色输入*

### 参数

* **输入数字**： *2 - 20*&#x200B;要显示的输入量。 重要提示：在数量减少时不要删除连接！
* **输入选择**： *1 - 20*&#x200B;作为结果返回的输入。

## 示例图像

</td>
</tr>
</table>
