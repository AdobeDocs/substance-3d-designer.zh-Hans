---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/function-node-library/function-nodes-random/hash-functions.html"
breadcrumb-title: ''
description: 在函数图中使用散列函数根据输入坐标生成确定性随机值。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Function node library > Random > Hash
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Hash函数
user-guide-description: ''
user-guide-title: ''
source-git-commit: 81c39001686736d41614fd59247d53e6d8438def
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 1%

---


# Hash函数

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![哈希节点：图标](hash-functions.resources/hash-icon.png "哈希节点：图标"){width="200px"}

<b>In：</b>函数>随机

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

基于用作种子的输入值计算介于0和1之间的伪随机值。

标题中的数字显示值的入点和出点类型。 例如：哈希23将float2值作为输入并输出float3值。

</td>
</tr>
</table>

当Hash节点输出多个组件的值时，每个组件具有不同的伪随机值。

可用的版本及其输入类型和输出类型：

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>哈希11：</b>→Float

<b>哈希14：</b>→Float4

<b>哈希21：</b>Float2 →Float

<b>哈希22：</b>Float2 →Float2

</td>
<td style="border: 0;" valign="top">

<b>哈希24：</b>Float2 →Float4

<b>Hash31：</b>Float3→Float

<b>哈希32：</b>Float3→Float2

</td>
</tr>
</table>

## 输入连接器

|  |  |
| --- | --- |
| <b>输入</b> | 用作计算伪随机输出的种子值。 |

## 示例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![哈希14示例](hash-functions.resources/hash14-example.png "哈希14示例"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![哈希32示例](hash-functions.resources/hash32-example.png "哈希32示例"){zoomable="yes"}

</td>
</tr>
</table>
