---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/function-graphs/variables.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer函数图表中使用变量来高效地存储和重用值。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 变量
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# 变量

>[!NOTE]
>
> 有关创建和使用变量节点的信息，请参阅&#x200B;*[变量节点部分](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)*。

## 定义

如果你不懂编程，你可能会对变量的概念很熟悉。

如果不是，这里有一个简单的定义：

>[!NOTE]
>
> 变量只是具有包含值的特定名称的“容器”。
> 
> 可以使用变量中包含的值，方法是用变量的名称调用该值。

## 变量的类型

在Substance 3D Designer中，有两个变量系列：数字和布尔值。

## 数值变量

数值变量基本上是数字。 但我们明确区分了两种数字：

* 整数： 0 | 1 | -1 | 203568等……
* 浮动：0.23 | 1.0 | -0.3546 |等……

>[!WARNING]
>
> Designer会明确区分整数与浮点：默认情况下，您不能一起操作它们。
> 
> 幸运的是，您可以使用&#x200B;*到整数*&#x200B;或到浮点节点来执行类型转换。

### 同一变量中的多个数值

根据需要，最多可以在同一变量中累积4个数值。

同样，所有值必须来自同一类型。

要执行此操作，您可以在所有这些数值之间进行选择：

![](../../assets/image2015-12-18-14-10-36.png)

## 布尔型

Boolean是纯二进制值，这意味着它的值只能是&#x200B;*True*&#x200B;或&#x200B;*False*（也可以说0或1）。
