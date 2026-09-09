---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-blend.html"
breadcrumb-title: ''
description: 使用“法向混合”节点将法线图混合在一起，以便在表面细节之间创建平滑的过渡。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 正常混合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 3%

---


# 正常混合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-blend.resources/normal-blend.png){width="128px"}

<b>在</b>个筛选器中>法线图

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

“正常混合”允许您将两个正常映射与一个可选蒙版混合，同时确保所有值保持正常化。 它与[原子混合节点](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)没有太大区别，但添加了正常映射的内部计算。

普通混合不适用于组合（叠加）正常映射，后者顶部映射将细节添加到底部映射。 为此，请改用[普通合并](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-combine/normal-combine.md)。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>NormalFG</b> <i>颜色输入</i> | 前景/顶部正常映射。 |
| <b>NormalBG</b> <i>颜色输入</i> | 背景/底部正常映射。 |
| <b>蒙版</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 可以使用“使用蒙版”参数切换。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>不透明度</b> <i>0.0 - 1.0</i> | 在前景和背景之间混合不透明度 |
| <b>使用蒙版</b> <i>False/True</i> | 启用或禁用蒙版图。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-blend.resources/normalblend-ex.gif" /><br><i>（.gif格式在示例中引入了仿色，应用程序内结果平滑）</i>
        </td>
    </tr>
</table>
