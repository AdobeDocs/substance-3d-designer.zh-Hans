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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 1%

---


# Hash函数

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![哈希节点：图标](../../../../../assets/hash-icon.png "哈希节点：图标"){width="200px"}

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

<b>哈希11：</b>浮点→浮点

<b>哈希14：</b>浮点→浮点4

<b>哈希21：</b>浮点2→浮点

<b>哈希22：</b>浮点2→浮点2

</td>
<td style="border: 0;" valign="top">

<b>哈希24：</b>浮点2→浮点4

<b>Hash31：</b>浮点3→浮点

<b>哈希32：</b>浮点3→浮点2

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

![哈希14示例](../../../../../assets/hash14-example.png "哈希14示例"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![哈希32示例](../../../../../assets/hash32-example.png "哈希32示例"){zoomable="yes"}

</td>
</tr>
</table>
