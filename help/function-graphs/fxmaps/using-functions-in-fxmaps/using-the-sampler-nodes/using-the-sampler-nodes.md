---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/using-the-sampler-nodes.html"
breadcrumb-title: ''
description: 了解如何在FXMaps中使用Sampler节点对纹理进行采样和创建过程素材变化。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Using the Sampler nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用Sampler节点
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# 使用Sampler节点

![](using-the-sampler-nodes.resources/using-the-sampler-nodes-01.jpg)

取样器节点可用于对插入到fx-map节点的图像输入中的像素值进行取样。 采样值然后可以用于使用函数驱动任何参数。

## 简单示例

在本示例中，创建了一组象限节点，以生成图案网格。 将在最后一个象限的不透明度/明亮度参数中创建函数。

![](using-the-sampler-nodes.resources/using-the-sampler-nodes-02.jpg){width="300px"}![](using-the-sampler-nodes.resources/using-the-sampler-nodes-03.jpg){width="300px"}

采样节点以float2输入作为采样坐标(x， y)。 在此示例中，我们使用$pos变量：对于每个图案，像素值在连接到FxMap节点的第一个图像输入的图案位置采样。

“样本灰色”节点返回0， 1范围中的float1值。

“示例颜色”节点返回0， 1范围中的float4 (rgba)值。

## 高级示例

这里，我们将采样值与常量(0.3)进行比较。 如果取样值大于0.3，则函数返回1，否则返回0。

![](using-the-sampler-nodes.resources/using-the-sampler-nodes-04.jpg){width="300px"}![](using-the-sampler-nodes.resources/using-the-sampler-nodes-05.jpg){width="300px"}

## 下载示例

[![SBS文件图标](using-the-sampler-nodes.resources/using-the-sampler-nodes-06.png){width="64px"}](https://shared-assets.adobe.com/link/d5f9adf3-0bb5-49a1-4eb9-a0506d4f3f32)
