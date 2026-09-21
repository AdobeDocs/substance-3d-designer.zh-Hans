---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/working-with-3d-scenes/extracting-materials-values-and-textures.html"
breadcrumb-title: ""
description: 从3D场景中提取材料属性，以便在Substance图形中使用，执行材料创建工作流程。
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Extracting materials values and textures
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 提取材料值和纹理
user-guide-description: ""
user-guide-title: ""
source-git-commit: b1404a9f03e3156f5fba0e499bbe41dbc79b7308
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%
---

# 提取材料值和纹理

可以提取材料的属性以用于Substance图形。

## 从纹理新建图形

“从纹理输入创建图形”操作可创建一个新的Substance图形，其中包含材料使用的所有纹理

使用此操作时发生一些问题：

* 将在所选位置创建一个以材料命名的Substance图形。
* 为材料使用的每个纹理创建[位图资源](../../resources/bitmap-resource/bitmap-resource.md)，该位图资源放置在“资源”文件夹下以材料命名的文件夹中。
* 在该图形中，为每个位图资源创建[位图](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)节点，并使用纹理自动连接到在材料属性之后配置的[输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)节点。
* 如果使用同一纹理的每个通道来驱动不同的材料属性（该技术称为[通道打包](../../glossary/glossary.md)），则会自动添加[灰度转换](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/grayscale-conversion/grayscale-conversion.md)节点以选择适当的通道。
* 图形会自动连接到该材料，并且只有在图形中进行编辑后，其外观才能更改。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![从纹理输入创建图形 — “3D 视图”视口中的操作](extracting-materials-values-and-textures.resources/createGraphFromTexturesActionViewport.png "从纹理输入创建图形 — “3D 视图”视口中的操作"){zoomable="yes"}

*视口中的操作*

</td>
<td style="border: 0;" valign="top">

![从纹理输入创建图形 — “材料”菜单中的操作](extracting-materials-values-and-textures.resources/createGraphFromTexturesActionMaterials.png "从纹理输入创建图形 — “材料”菜单中的操作"){zoomable="yes"}

*材料菜单中的操作*

</td>
<td style="border: 0;" valign="top">

![从纹理输入创建图形 — “属性”停靠区中的操作](extracting-materials-values-and-textures.resources/createGraphFromTexturesActionProps.png "从纹理输入创建图形 — “属性”停靠区中的操作"){zoomable="yes"}

*属性停放中的操作*

</td>
</tr>
</table>

![从纹理创建图形的结果](extracting-materials-values-and-textures.resources/createGraphFromTexturesResult.png "从材料纹理创建图形的结果"){zoomable="yes"}

*从纹理创建图形的结果*

+++演示
![从纹理输入创建图形 — 演示](extracting-materials-values-and-textures.resources/createGraphFromTextures.gif "从纹理输入创建图形 — 演示"){zoomable="yes"}



+++

>[!TIP]
>
> 您可以将光标放在对象上并按<b>Shift+LMB</b>以选择对象，从而在视口中快速而直接地访问该动作。 然后点击“RMB”（人民币）访问该动作的上下文菜单。

>[!NOTE]
>
> 对于使用&#x200B;*嵌入纹理*&#x200B;的格式（例如：USDZ），需要在磁盘上提取和复制纹理。 这会导致执行额外的步骤，以选择提取纹理的位置。

## 提取纹理

“将纹理提取到图形”操作可在现有图形中为素材所使用的纹理创建新的位图节点。

使用此操作时发生一些问题：

* 为素材使用的纹理创建[位图资源](../../resources/bitmap-resource/bitmap-resource.md)，并将其放置在“Resources”文件夹下以素材命名的文件夹中。
* 在选定的图形中，将为该位图资源创建[位图](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)节点，并自动连接到使用该纹理在材质属性之后配置的[输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)节点。

如果图形中已存在为素材属性&#x200B;*配置的输出*，则&#x200B;*不会创建任何节点*，只会执行位图资源创建。

例如：将“基色”属性的纹理提取到已承载为“基色”配置的输出节点的图表将导致未在图形中创建节点。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![将纹理提取到图形 — 在属性停放区中操作](extracting-materials-values-and-textures.resources/extractTextureAction.png "将纹理提取到图形 — 在属性停放区中操作"){zoomable="yes"}

在“属性”停放中对材质属性执行的操作

</td>
<td style="border: 0;" valign="top">

![将纹理提取到图形 — “选择目标图形”对话框](extracting-materials-values-and-textures.resources/extractTextureSelectGraph.png "将纹理提取到图形 — “选择目标图形”对话框"){zoomable="yes"}

“选择目标图表”对话框

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

![纹理提取的结果](extracting-materials-values-and-textures.resources/extractTextureResult.png "纹理提取的结果"){zoomable="yes"}

纹理提取的结果

+++演示
![将纹理提取到图形 — 演示](extracting-materials-values-and-textures.resources/extractTextureToGraph.gif "将纹理提取到图形 — 演示"){zoomable="yes"}



+++

“将纹理提取为资源”操作只会为素材所使用的纹理创建位图资源，并将它放在“资源”文件夹下以素材命名的文件夹中。

>[!NOTE]
>
> 对于使用&#x200B;*嵌入的纹理*&#x200B;的格式（例如：USDZ），需要在磁盘上提取和复制纹理。 这会导致额外的步骤，即选择提取纹理的位置。

## 提取值

“将值提取到图形”操作可为素材属性值在现有图形中创建新的[值处理器](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)节点。

使用此操作时发生一些问题：

* 在选定的图形中，为该属性值创建了一个[值处理器](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)节点，并自动连接到在该素材属性之后配置的[输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)节点。
* 在值处理器节点的[Substance函数图形](../../function-graphs/function-graphs.md)中，创建与值类型匹配的[常量节点](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md)，并将其设置为设置为设置为图形输出的提取值。

如果图形中已存在为素材属性&#x200B;*配置的输出*，则&#x200B;*不会创建任何节点*。

例如：将“各向异性级别”属性的值提取到已承载为“各向异性级别”配置的输出节点的图形将导致未在图形中创建节点。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![将值提取到图形 — 属性停放中的动作](extracting-materials-values-and-textures.resources/extractValueAction.png "将值提取到图形 — 属性停放中的动作"){zoomable="yes"}

在“属性”停放中对材质属性执行的操作

</td>
<td style="border: 0;" valign="top">

![将值提取到图形 — “选择目标图形”对话框](extracting-materials-values-and-textures.resources/extractValueSelectGraph.png "将值提取到图形 — “选择目标图形”对话框"){zoomable="yes"}

“选择目标图表”对话框

</td>
<td style="border: 0;" valign="top">

![将值提取到图形 — 值处理器节点函数中的常量节点](extracting-materials-values-and-textures.resources/extractValueResult2.png "将值提取到图形 — 值处理器节点函数中的常量节点"){zoomable="yes"}

值处理器节点函数中的常量节点

</td>
</tr>
</table>

![值提取的结果](extracting-materials-values-and-textures.resources/extractValueResult.png "值提取的结果"){zoomable="yes"}

值提取的结果

+++演示
![将值提取到图形 — 演示](extracting-materials-values-and-textures.resources/extractValueToGraph.gif "将值提取到图形 — 演示"){zoomable="yes"}



+++
