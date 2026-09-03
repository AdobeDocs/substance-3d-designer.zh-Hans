---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/emboss-with-gloss.html"
breadcrumb-title: ''
description: 使用“光泽浮雕”节点创建带有光泽映射的浮雕效果，为纹理添加深度和光泽。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Emboss With Gloss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 光泽浮雕
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 6%

---


# 光泽浮雕

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](emboss-with-gloss.resources/emboss-with-gloss-01.png){width="128px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

在颜色和Height输入上执行添加光泽（Specular反射）的浮雕效果。 实质上根据Height信息为图像添加仿制的烘焙光照。 对于某些需要烘焙到纹理中的光照的纹理样式很有用。

有关包含更多选项的版本，请参阅[Uber浮雕](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md)。 还有更简单的原子版本的[浮雕](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md)。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>颜色</b> <i>颜色输入</i> |  |
| <b>Height</b> <i>灰度输入</i> |  |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>突出显示颜色</b> <i>（颜色值）</i> | Specular高亮的颜色。 |
| <b>阴影颜色</b> <i>（颜色值）</i> | 在阴影/无光照区域中使用的颜色。 |
| <b>光泽</b> <i>0.0 - 0.5</i> | 光泽度高光大小。 |
| <b>强度</b> <i>0.0 - 10.0</i> | 高光的强度。 |
| <b>光线角度</b> <i>0.0 - 1.0</i> | （虚假）光的入射角。 |
