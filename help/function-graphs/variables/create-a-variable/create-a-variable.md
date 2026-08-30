---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/variables/create-a-variable.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer函数图表中创建自定义变量以获取可重用的值和参数。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Create a variable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 创建变量
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---


# 创建变量

Substance 3D Designer中有多种创建变量的方法：

* 使用输入参数
* 使用Set节点。

## 使用输入参数

创建输入参数时，将创建变量并将其与它关联。 然后可以在图形的任何函数中重用此变量。

因此，一个曝光参数可能影响图表的多个部分。

## 使用Set节点

“集”节点是仅在函数图形中可用的节点：

它允许用户创建自定义变量：

* 该名称在参数中声明。
* 该值由输入定义。

### 如何使用&#x200B;*集*&#x200B;节点

使用“集”节点有些特殊：

当您声明它时，它仅在图形内可用，默认情况下实际上没有用（毕竟您已通过链接输出它的值）。

因此，必须在此图表外部声明此新变量。

为此，必须使用序列节点并执行以下步骤：

* 将实际输出节点链接到Sequence节点的“最后一个”输入
* 将Set节点链接到序列节点的“In”输入。
* 将序列设置为输出节点

完成此操作后，该变量将可在同一节点的其他函数图中使用。

>[!WARNING]
>
> 当节点由Substance Engine处理时，其参数（以及可以控制它们的函数）从上到下读取。 因此， Set节点只能通过节点参数栈栈中位于它下面的参数来访问。

>[!NOTE]
>
> 如果要创建多个变量，只需重复&#x200B;*Set*&#x200B;和&#x200B;*Sequence*&#x200B;节点创建操作，并将最后一个序列节点设置为输出节点：
> 
> ![](create-a-variable.resources/image2015-12-18-18-43-8.png)
