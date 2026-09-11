---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/technical-issues/parameters-not-working-as-expected.html"
breadcrumb-title: ''
description: 解决图形参数无法按预期工作的问题，并找到解决方案。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Parameters not working as expected
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 参数未按预期方式工作
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 5%

---


# 参数未按预期方式工作

本页列出了在Substance 3D Designer中参数无法按预期工作的常见原因，并且提供了相应的故障排除步骤。

## 参数在预览模式下不起作用且已发布Substance 3D资源(SBSAR)

<b>！[（错误）](../../assets/error.svg)问题</b>

在Designer中使用[预览模式](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)时，或在该图形之外的Substance 3D资源(SBSAR) [已发布](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)的参数列表中，图形的某些公开参数&#x200B;*未列出*。

<b>！[(tick)](../../assets/check.svg)建议的步骤</b>

缺少的参数可能是[静态参数](../../glossary/glossary.md)，在图形&#x200B;*被烹调*&#x200B;后&#x200B;*无法动态编辑*，即经过处理以便快速高效地运行其算法。 每次&#x200B;*编辑*&#x200B;或&#x200B;*发布*&#x200B;图形时，都会在Designer中执行烹饪操作。 受此类限制影响的参数列于本文档的[公开参数](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)页的[限制](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)部分。

因此，静态参数在Designer中可见且可编辑，但在发布的Substance 3D资源中&#x200B;*隐藏*。 在发布到Substance 3D资源之前，可使用[预览模式](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)查看这些限制是否有效。

以下是静态参数的列表：

| 节点 | 参数 |
| --- | --- |
| 所有节点 | 拼贴模式像素比率 |
| [统一颜色](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md) | 颜色模式 |
| [像素处理器](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) | 颜色模式 |
| [混合](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) | 混合模式裁剪区域 |
| [FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) | 混合模式 |
| [象限](../../function-graphs/fxmaps/the-quadrant-node/the-quadrant-node.md) | 图案输入图像Alpha输入图像筛选 |

## 应用于参数的Substance函数图形的结果不正确

<b>！[（错误）](../../assets/error.svg)问题</b>

应用于Substance参数的Node函数图形在使用负整数时不会输出期望值。

<b>！[(tick)](../../assets/check.svg)建议的步骤</b>

当前不支持负整数。 作为解决方法，请使用[整数2](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md)值中的负整数，然后使用[节点](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md)Swizzle 整数提取该值。
