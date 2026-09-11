---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/constant-nodes.html"
breadcrumb-title: ''
description: 访问Substance 3D Designer函数图形中的常量节点以定义常量值和参数。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Constant
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 常数
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4e61f5588fb279e139240ac5939d6b7e58e1027a
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 0%

---


# 常数

常量节点是一种创建静态值的方法，供内部Substance函数图形使用。 与[变量](../../../../function-graphs/variables/variables.md)不同，它们无法在外部修改。

此外，本页还提供了有关每种数据类型和常见用例的一些额外信息。

## 整数

常量整数生成整数，步骤为1。

[可以将它们转换为Float，](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md)，当执行任何比加法、减法和简单比较更复杂的操作时，建议执行此操作。

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![整数类型图标](constant-nodes.resources/fn-constant-integer.png "整数类型图标")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>整数</b>

整数具有单个组件。 它可用作建立选区的索引，例如：

* 选择一个作为下拉菜单呈现给用户的选项（请参阅[此页面](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)中的“下拉列表”）。
* 选择[多交换机](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md)节点的输入。<b></b>

>[!IMPORTANT]
>
> 参数函数中的<b>负整数</b>是&#x200B;*不受支持*。 请参阅[此页面](../../../../technical-issues/parameters-not-working/parameters-not-working-as-expected.md)的“技术问题”部分以获得解决方法。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![整数2类型图标](constant-nodes.resources/fn-constant-integer2.png "整数2类型图标")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>整数2</b>

Integer2节点生成带有(X， Y)分量的静态2分量整数向量。

整数2不常见，但用于在[Tile Generator](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)中设置X和Y 2D拼贴。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![整数3类型图标](constant-nodes.resources/fn-constant-integer3.png "整数3类型图标")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>整数3</b>

Integer3节点生成带有(X、Y、Z)分量的静态3分量整数向量。

整数3不常见，不太可能会出现。<b>\
</b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![整数4类型图标](constant-nodes.resources/fn-constant-integer4.png "整数4类型图标")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>整数4</b>

Integer4节点生成带有(X、Y、Z、W)分量的静态4分量整数向量。

整数4不常见，不太可能会出现。<b>\
</b>

</td>
</tr>
</table>

## 浮动

常数Float生成小数，而不是全数，这意味着它们始终在小数符号之后有值，可以按小于1的步长递增或递减（默认为0.01）。

[浮点数可以转换为整数](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md)，但会向上或向下舍入到最接近的整数，这意味着数据和准确性会丢失。

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![浮点类型图标](constant-nodes.resources/fn-constant-float.png "浮点类型图标")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>浮动</b>

float具有单个组件，为了简洁起见，名称中省略了(1)。 float非常常见，可用于任何需要以滑块或角度形式精确控制的值。 您可以在几乎每个Node的参数中找到它。 这也是灰度值的首选数据类型！<b></b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Float2类型图标](constant-nodes.resources/fn-constant-float2.png "Float2类型图标")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>浮点2</b>

float2节点生成静态2分量Float向量。 组件命名为X、Y。Float2非常常见，用于[采样坐标](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md)和[变换偏移](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/transforms.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Float3类型图标](constant-nodes.resources/fn-constant-float3.png "Float3类型图标")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>浮点3</b>

float3节点生成静态3分量Float向量。 组件名为X、Y、Z。Float3不常见，它主要用来表示[3D比例坐标](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md)，是一种在没有Alpha数据的情况下存储颜色的更简单方法。<b>\
</b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Float4类型图标](constant-nodes.resources/fn-constant-float4.png "Float4类型图标")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>浮点4</b>

float4生成静态4组件Float向量。组件命名为X、Y、Z、W。Float4非常常见，因为它是存储和设置[颜色信息的首选方法，其中XYZW数据表示RGBA值。](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md)<b>\
</b>

</td>
</tr>
</table>

## 其他

Substance函数图形内存在另外两种数据类型：布尔值和字符串。 在Designer版本6中，在[文本](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)节点旁引入了字符串。

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![布尔型图标](constant-nodes.resources/fn-constant-boolean.png "布尔型图标")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>布尔值</b>

布尔型是最简单的数据类型，只知道两种状态：True或False、1或0。 它用白色表示。 如果不使用[转换](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md)或使用[逻辑节点](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md)，则无法在布尔值和整数之间进行交换。 布尔非常常见，它是控制函数或图形流量的绝佳方法，典型用法是[切换节点。](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md)<b></b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![字符串类型图标](constant-nodes.resources/fn-constant-string.png "字符串类型图标")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>字符串</b>

字符串节点生成静态字符串（一段文本）。 它是Function中可用的最独特的数据类型，通常不能与其他Function节点结合使用。 其主要目标是作为[文本节点](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)的最终输出运行。

</td>
</tr>
</table>
