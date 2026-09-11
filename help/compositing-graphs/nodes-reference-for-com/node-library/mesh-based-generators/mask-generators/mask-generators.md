---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators.html"
breadcrumb-title: ''
description: 访问Substance 3D Designer中的蒙版生成器节点，以根据网格几何形状和属性创建蒙版。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 遮罩生成器
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%

---


# 遮罩生成器

此类别包含一系列黑白蒙版生成节点。 它们会根据已烘焙贴图信息生成蒙版，然后可以用于混合材料和其他效果。 这些Substance Painter类似于[智能蒙版](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/features/smart-materials-and-masks)和[生成器](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/content/creating-custom-effects/generators)。

所有这些节点都需要[个已烘焙贴图，](../../../../../bakers/bakers.md)，因为没有[个已烘焙贴图](../../../../../bakers/bakers.md)，结果不会很多。

主要预期用途是将这些蒙版生成器用于[多渠道材料](../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/material-filters.md)。 蒙版生成后，将用作[混合](../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-blend/material-blend.md)的混合蒙版。

此类别中有一些有趣的节点是：

* [滴落铁锈](../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/dripping-rust/dripping-rust.md)
* [边缘损坏](../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-damages/edge-damages.md)
* [从下到上](../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/bottom-to-top/bottom-to-top.md)
* [蒙版生成器](../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/mask-builder/mask-builder.md)
