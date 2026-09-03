---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/function-graphs/what-is-a-function.html"
breadcrumb-title: ''
description: 了解Substance 3D Designer中的功能以及如何使用它们创建可重用的节点网络。
helpx_creative_field: ""
helpx_description: "Designer > Function graphs > What is a function "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: '什么是函数 '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# 什么是函数？

Substance 3D Designer中的函数允许用户使用以编程语言找到的逻辑生成结果。

但是，Designer中的函数不会使用代码行，而是使用相同的节点方法。 乍一看，函数图形看起来非常类似于常规图形。

![](what-is-a-function.resources/what-is-a-function-01.png)

在以下两种主要情况下，您可能会遇到函数：

* 控制参数的结果
* 如果您编辑像素处理器

## 控制参数的结果

在Substance 3D Designer中，任何参数都可以由函数控制。

![](what-is-a-function.resources/what-is-a-function-02.png)

因此，您可以想象图形各部分之间的规则和依赖关系，以获得独特的结果。

例如，您可以决定混合节点的不透明度为变形节点强度的一半：

![](what-is-a-function.resources/what-is-a-function-03.gif)

事实上，您可能已经创建了一些不知名的功能：

如果公开了参数，则自动创建了一个函数和一个变量：该函数包含捕获新创建变量值的get float节点：

![](what-is-a-function.resources/what-is-a-function-04.gif)
