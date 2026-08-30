---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/function-graphs/fxmaps/the-iterate-node.html"
breadcrumb-title: ''
description: 使用FXMaps中的“迭代”节点在材料中创建重复的图案和程序化的变体。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > The Iterate Node
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 迭代节点
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---


# 迭代节点

“迭代”节点允许您将象限节点的图像相乘，并且本质上是一个“复制器”节点。 深度为1的象限节点通常输出4个象限。 “迭代”节点允许您重复其输出图像，次数不限，并且每组重复项均单独处理。

“迭代”节点没有“您希望重复次数？”参数以外的其他属性。 结果是，新图像在默认情况下会直接与象限节点生成的图像重叠并混合。

Iterate节点重复收到的输入图像。 重复次数由其迭代属性定义：

使用Iterate节点的关键在于，附加到每个重复图像的任何动态函数也将被处理。 这意味着每个重复可以有自己的一组独特调整。 您可以使用“迭代”节点的“随机植入”属性来修改其工作原理。 您还可以在动态函数中访问&#x200B;*$number*&#x200B;系统变量，以确定当前呈现的重复，并相应地修改函数的结果。

例如：如果对“象限”节点中的每张图像应用随机旋转，然后将该象限节点的输出馈送到“迭代”节点的主动输入，则每个重复的图像也将具有其自身的随机旋转。

所有在象限节点上可用的相同动态特征也适用于“迭代”节点产生的重复图像。 就好像该节点在同一级别复制了象限节点，而不是添加另一个深度级别。

## 直通连接器

每个迭代节点在基节点上有两个连接器。 左连接器是传递连接器。 它收到的图像会直接传递到节点的输出连接器，并在其中与任何重复的图像混合：

请注意，无论迭代参数的设置如何，穿透图像始终保持不变。

![](the-iterate-node.resources/iterate.jpg)
