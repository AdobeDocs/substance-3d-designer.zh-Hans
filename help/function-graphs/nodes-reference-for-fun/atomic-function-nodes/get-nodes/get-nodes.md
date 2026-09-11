---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/get-nodes.html"
breadcrumb-title: ''
description: 访问Substance 3D Designer函数图形中的Get节点以检索变量值和数据。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 变量
user-guide-description: ''
user-guide-title: ''
source-git-commit: f28a2ba2531cfc4456744ff151432ed8308275ec
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 6%

---


# 变量

变量是<b>存储值</b>以便稍后获取（<b>获取</b>）和/或修改值（<b>设置</b>）的一种方法。

![函数Substance- Get float](get-nodes.resources/assign-getfloat.gif "函数图形Substance- Get float"){zoomable="yes"}

Get节点实质上就是获取一个动态变量，然后从Get节点的输出返回该变量以便在函数中使用。 这些Get节点形成在[图形参数](../../../../compositing-graphs/graph-parameters/graph-parameters.md)和[参数函数](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)中定义的输入参数之间的链接。

每次使用Get节点时，必须从下拉菜单中选择一个可用值。 获取节点将<b>获取相应类型的值</b>。 这意味着，您只能在Get节点的菜单中看到有效选项，而不能选取无效选项。 如果变量不可用，则表示存在类型不匹配

存在多个<b>“系统”变量</b>：不能自行声明的预定义的特殊变量。 这些变量非常重要，对于下面的节点，会列出可用的系统变量。

当参数为[公开](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)时，它包括对其应用一个参数函数，该函数仅包含正确类型的Get节点。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 获取

</td>
<td style="border: 0;" valign="top">

### 设置

</td>
<td style="border: 0;" valign="top">

### Is defined

</td>
</tr>
</table>

## 获取

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![获取浮点2 — 图标](get-nodes.resources/fn_variables_getfloat2.png "获取浮点2 — 图标"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

这些节点允许您获取在当前作用域&#x200B;*中存在*&#x200B;的变量的值。

在“属性”停放区中设置要提取的变量的名称。

</td>
</tr>
</table>

“获取”节点存在一些需要注意的限制：

* <b>它们已键入</b>，因此需要确保变量包含与节点类型相同的值。 “控制台”中报告类型不匹配。
* <b>它们不检查当前作用域中是否存在变量</b>。 控制台中报告未找到的变量。
* 在使用控制流节点（如“序列”）的复杂函数中，请注意设置并获取变量的<b>顺序</b>。 当Designer检测到“设置之前”的情况时，会在控制台中报告该情况。

>[!NOTE]
>
> 内置变量
> 
> 多个“Get”节点将提供内建变量以根据当前上下文访问现有值 — 例如：像素处理器中的当前像素位置、节点的当前拼贴模式……
> 
> 所有内置变量都列在[此专用页](../../../../function-graphs/variables/system-variables/system-variables.md)中。

### 获取节点

+++float
![获取浮动 — 图标](get-nodes.resources/fn_variables_getfloat.png "获取浮动 — 图标"){width="200px"}



获取浮点

![获取浮点2 — 图标](get-nodes.resources/fn_variables_getfloat2.png "获取浮点2 — 图标"){width="200px"}



获取浮点 2

![获取浮点3 — 图标](get-nodes.resources/fn_variables_getfloat3.png "获取浮点3 — 图标"){width="200px"}



获取浮点 3

![获取浮点4 — 图标](get-nodes.resources/fn_variables_getfloat4.png "获取浮点4 — 图标"){width="200px"}



获取浮点 4

+++

+++整数
![获取整数 — 图标](get-nodes.resources/fn_variables_getint.png "获取整数 — 图标"){width="200px"}



获取整数

![获取整数2 — 图标](get-nodes.resources/fn_variables_getint2.png "获取整数2 — 图标"){width="200px"}



获取整数 2

![获取整数3 — 图标](get-nodes.resources/fn_variables_getint3.png "获取整数3 — 图标"){width="200px"}



获取整数 3

![获取整数4 — 图标](get-nodes.resources/fn_variables_getint4.png "获取整数4 — 图标"){width="200px"}



获取整数 4

+++

+++其他
![获取布尔值 — 图标](get-nodes.resources/fn_variables_getboolean.png "获取布尔值 — 图标"){width="200px"}



获取布尔

![获取字符串 — 图标](get-nodes.resources/fn_variables_getstring.png "获取字符串 — 图标"){width="200px"}



获取字符串

+++

## 设置

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![设置：节点图标](get-nodes.resources/fn_variables_set.png "设置：节点图标"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

文本

</td>
</tr>
</table>

## Is defined

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![已定义：节点图标](get-nodes.resources/fn_variables_isdefined.png "已定义：节点图标"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

文本

</td>
</tr>
</table>
