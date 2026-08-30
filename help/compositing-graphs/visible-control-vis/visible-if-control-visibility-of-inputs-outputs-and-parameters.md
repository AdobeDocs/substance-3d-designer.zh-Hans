---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/visible-if-control-visibility-of-inputs-outputs-and-parameters.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer中使用可见表达式根据条件控制参数可见性。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exposing a parameter > Visible if expressions
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 表达式可见
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 1%

---


# 表达式可见

“Visible if”表达式允许您<b>控制图形中输入、输出和参数的可见性</b>。

在[公开参数](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)时，您可能需要根据其他参数的状态隐藏或显示参数或节点连接器。 例如，仅当布尔参数按钮设置为`true`时才会显示滑块，因为否则它不会产生任何效果，并且可能会混淆用户。

为此，您可以将&#x200B;*逻辑表达式*&#x200B;输入到以下属性的<b>Visible if</b>属性中：

* 图形的[输入参数](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)；
* 图形的[输入](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)节点；
* 图形的[输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)节点。

![切换输入参数可见性](visible-if-control-visibility-of-inputs-outputs-and-parameters.resources/visible-if-example.gif "切换输入参数可见性"){width="512px"}

如果逻辑表达式的计算结果为`true`，则在表示当前图表的所有[实例节点](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)中显示参数、输入或输出。 否则，它是&#x200B;*隐藏*。

如果说明这些条件的逻辑表达式有效，则可能出现复杂条件。

>[!NOTE]
>
> 注意事项
> 
> * 此功能&#x200B;*仅*&#x200B;影响是否在用户界面中显示参数或连接器，并且&#x200B;*对图形的计算和结果没有影响*。
> * 当向“Visible if”语句中使用的任何参数公开或应用函数时，这些语句将&#x200B;*忽略*，默认为“true”。

>[!IMPORTANT]
>
> 虽然此功能在Substance 3D生态系统中运行，但某些集成可能不支持该功能。 如果不支持，可视性条件默认为`true`。

## 正在写入“Visible if”表达式

### 访问输入参数

任何可见如果表达式都需要使用至少一个输入，可通过以下语法来完成：

```
input.identifier 

input["identifier"]
```


>[!WARNING]
>
> **标识符**&#x200B;必须是现有输入参数的&#x200B;**标识符**&#x200B;属性的&#x200B;*精确*&#x200B;名称，并且类型必须是&#x200B;*区分大小写*。 您&#x200B;*不能*&#x200B;通过参数的标签引用参数。\
>  如果引用的参数不存在，或逻辑表达式无效，则在&#x200B;**Visible if**&#x200B;属性上显示&#x200B;*警告*。

### 可用的运算符

“显示条件”字段接受以下参数：

* 布尔值、浮点和整数输入。
* `true`和`false`值（区分大小写，无大写！）
* `.x` ：访问子参数
* `&&`<b> </b>：和
* `||`<b> </b>：或
* `!`<b> </b>：不
* `<`<b>、</b>`>`<b>、</b>`<=`<b>、</b>`>=`<b>、</b>`==`<b>、</b>`!=`：比较
* `()` ：括号

### 必须始终计算布尔值

Visible If表达式用作“IF”语句的条件，这意味着它必须始终生成`true`或`false`。

* 布尔值可直接作为条件求值。 带有布尔值的简单按钮仅需要此项。 请参阅以下示例，第一个案例；
* 非布尔型参数通常需要&#x200B;*比较*&#x200B;操作。 比较运算符请参阅上文，示例请参阅下文；
* 一些非布尔值可以是&#x200B;*truthy*&#x200B;或&#x200B;*falsy*，这意味着它们可以评估为`true`个，共`false`个 — 例如， 整数值`0`的计算结果为false。

## 示例

| 条件(“If”) | 公式 | 注释 |
| --- | --- | --- |
| True | ` input["my_input"]   input.my_input `  ` input["my_input"] == true   input.my_input == true ` | my\_input是布尔值 |
| False | ` !input["my_input"]   !input.my_input `  ` input["my_input"] == false   input.my_input == false `  ` input["my_input"] != true   input.my_input != true ` | my\_input是布尔值 |
| 低于 | ` input["my_input"] < 3   input.my_input < 3 ` | my\_input是整数值 |
| 等于 | ` input["param1"] == 2   input.param1 == 2 ` | param1是浮点值或整数值 |
| 低于 | ` input["my_input"].y < 3   input.my_input.y < 3 ` | my\_input是一个包含一个或多个组件的浮点值或整数值 — 例如，float2(x， y)， integer3(x， y， z) |
| 或 | ` input["param1"] \|\| input["param2"]   input.param1 \|\| input.param2 ` | param1和param2是布尔值 |
| 与 | ` input["param1"] > 0 && input["param2"] > 1   input.param1 > 0 && input.param2 > 1 ` | param1和param2是浮点值或整数值 |
