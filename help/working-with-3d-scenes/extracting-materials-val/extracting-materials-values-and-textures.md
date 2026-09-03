---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/working-with-3d-scenes/extracting-materials-values-and-textures.html"
breadcrumb-title: ''
description: 从3D场景提取素材属性，以用于素材创建工作流程的Substance图表。
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Extracting materials values and textures
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 提取素材值和纹理
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 0%

---


# 提取素材值和纹理

可以提取材料的属性以用于Substance图。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 从纹理新建图表

</td>
<td style="border: 0;" valign="top">

### 提取纹理

</td>
<td style="border: 0;" valign="top">

### 提取值

</td>
</tr>
</table>

## 从纹理新建图表

“从纹理输入创建图形”操作可创建新的Substance图形，其中包含材质使用的所有纹理

使用此操作时发生一些问题：

* 将在所选位置创建以材料命名的Substance图形。
* 为素材使用的每个纹理创建[位图资源](../../resources/bitmap-resource/bitmap-resource.md)，并将其放置在“Resources”文件夹下以素材命名的文件夹中。
* 在图形中，为每个位图资源创建[位图](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)节点，并使用纹理自动连接到在材质属性之后配置的[输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)节点。
* 如果使用同一纹理的每个通道来驱动不同的素材属性（该技术称为[通道打包](../../glossary/glossary.md)），则会自动添加[灰度转换](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/grayscale-conversion/grayscale-conversion.md)节点以选择适当的通道。
* 图形会自动连接到材料，并且直到您在图形中进行编辑之后，其外观才应改变。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![从纹理输入创建图形 — “3D视图”视口中的操作](extracting-materials-values-and-textures.resources/extracting-materials-values-and-textures-01.png "从纹理输入创建图形 — “3D视图”视口中的操作"){zoomable="yes"}

*3D视图视口中的操作*

</td>
<td style="border: 0;" valign="top">

![从纹理输入创建图形 — “材质”菜单中的操作](extracting-materials-values-and-textures.resources/extracting-materials-values-and-textures-02.png "从纹理输入创建图形 — “材质”菜单中的操作"){zoomable="yes"}

*“材质”菜单中的操作*

</td>
<td style="border: 0;" valign="top">

![从纹理输入创建图形 — “属性”停放中的操作](extracting-materials-values-and-textures.resources/extracting-materials-values-and-textures-03.png "从纹理输入创建图形 — “属性”停放中的操作"){zoomable="yes"}

*属性停放中的操作*

</td>
</tr>
</table>

![从素材纹理创建图形的结果](extracting-materials-values-and-textures.resources/extracting-materials-values-and-textures-04.png "从素材纹理创建图形的结果"){zoomable="yes"}

*从素材纹理创建图形的结果*

+++演示
![从纹理输入创建图形 — 演示](extracting-materials-values-and-textures.resources/extracting-materials-values-and-textures-05.gif "从纹理输入创建图形 — 演示"){zoomable="yes"}



+++

>[!TIP]
>
> 您可以将光标放在对象上并按<b>Shift+LMB</b>以选择对象，从而在3D视图视口中快速而直接地访问该动作。 然后点击“RMB”（人民币）访问该动作的上下文菜单。

>[!NOTE]
>
> 对于使用&#x200B;*嵌入的纹理*（例如：USDZ）的格式，需要在磁盘上提取和复制纹理。 这会导致额外的步骤，即选择提取纹理的位置。

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

![将纹理提取到图形 — 在属性停放区中操作](extracting-materials-values-and-textures.resources/extracting-materials-values-and-textures-06.png "将纹理提取到图形 — 在属性停放区中操作"){zoomable="yes"}

在“属性”停放中对材质属性执行的操作

</td>
<td style="border: 0;" valign="top">

![将纹理提取到图形 — “选择目标图形”对话框](extracting-materials-values-and-textures.resources/extracting-materials-values-and-textures-07.png "将纹理提取到图形 — “选择目标图形”对话框"){zoomable="yes"}

“选择目标图表”对话框

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

![纹理提取的结果](extracting-materials-values-and-textures.resources/extracting-materials-values-and-textures-08.png "纹理提取的结果"){zoomable="yes"}

纹理提取的结果

+++演示
![将纹理提取到图形 — 演示](extracting-materials-values-and-textures.resources/extracting-materials-values-and-textures-09.gif "将纹理提取到图形 — 演示"){zoomable="yes"}



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

例如：将“Anisotropy level”属性的值提取到已承载为“Anisotropy level”配置的输出图形的节点将导致在图形中未创建任何节点。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![将值提取到图形 — 属性停放中的动作](extracting-materials-values-and-textures.resources/extracting-materials-values-and-textures-10.png "将值提取到图形 — 属性停放中的动作"){zoomable="yes"}

在“属性”停放中对材料属性执行的操作

</td>
<td style="border: 0;" valign="top">

![将值提取到图形 — “选择目标图形”对话框](extracting-materials-values-and-textures.resources/extracting-materials-values-and-textures-11.png "将值提取到图形 — “选择目标图形”对话框"){zoomable="yes"}

“选择目标图表”对话框

</td>
<td style="border: 0;" valign="top">

![将值提取到图形 — 值处理器节点函数中的常量节点](extracting-materials-values-and-textures.resources/extracting-materials-values-and-textures-12.png "将值提取到图形 — 值处理器节点函数中的常量节点"){zoomable="yes"}

值处理器节点函数中的常量节点

</td>
</tr>
</table>

![值提取的结果](extracting-materials-values-and-textures.resources/extracting-materials-values-and-textures-13.png "值提取的结果"){zoomable="yes"}

值提取的结果

+++演示
![将值提取到图形 — 演示](extracting-materials-values-and-textures.resources/extracting-materials-values-and-textures-14.gif "将值提取到图形 — 演示"){zoomable="yes"}



+++
