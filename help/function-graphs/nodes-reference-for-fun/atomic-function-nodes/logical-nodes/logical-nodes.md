---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/logical-nodes.html"
breadcrumb-title: ''
description: 访问Substance 3D Designer函数图形中的逻辑节点以执行布尔逻辑操作和比较。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Logical
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 逻辑
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---


# 逻辑节点

逻辑节点用于将多个条件添加到图形中：

![](logical-nodes.resources/logical-nodes-01.png)

## *和*&#x200B;节点

![](logical-nodes.resources/logical-nodes-02.png)

And节点采用两个布尔型节点作为输入：

* 如果两个输入均为True，则&#x200B;*和*&#x200B;节点的输出将为&#x200B;*True*
* 在任何其他情况下，*And*&#x200B;节点都将返回&#x200B;*False*

## *或*&#x200B;节点

![](logical-nodes.resources/logical-nodes-03.png)

“或”节点采用两个布尔型节点作为输入：

* 如果至少有一个输入为True (1)，则&#x200B;*或*&#x200B;节点的输出将为&#x200B;*True*
* 如果两个输入均为False，*或*&#x200B;节点将返回&#x200B;*False*

## *Not*&#x200B;节点

![](logical-nodes.resources/logical-nodes-04.png)

Not节点将布尔值作为输入：它将查看输入值并返回其相反值：

* *True*&#x200B;输入提供&#x200B;*False*&#x200B;输出
* *False*&#x200B;输入提供&#x200B;*True*&#x200B;输出
