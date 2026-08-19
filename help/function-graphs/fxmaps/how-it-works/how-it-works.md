---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/function-graphs/fxmaps/how-it-works.html"
breadcrumb-title: ''
description: 了解FXMaps如何在Substance 3D Designer中应用函数图表到纹理以实现过程效果。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > How it works
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 工作原理
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 2%

---


# 工作原理

了解FX-Map图表的工作方式是掌握这一强大功能的关键。

FX-Map图形可以包含三种FX-Map节点类型中的一种或多种：象限、迭代和交换机。 在这些节点中，您最常使用的节点是象限，迭代节点紧邻着象限。

“参数集”节点是FX-Maps的原动机。 FX-Maps依赖的核心区域会创建四叉树图，但不会显示为一个核心区域。 从视觉上看，四叉树图以马尔可夫链的形式显示。

在渲染FX地图时，简化的FX地图图表将“展开”以看起来像大树形图表。 引擎从上到下从左到右走过整个四叉树。

FX-Map节点不会盲目地复制和粘贴其图像。 在渲染每个图像时，将运行其拥有的任何动态函数。 这些函数将影响节点渲染的每个图像。 因此，可以为每个单独的图像赋予随机旋转、比例因子或许多其他调整。
