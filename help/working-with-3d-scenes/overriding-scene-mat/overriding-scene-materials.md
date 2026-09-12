---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/working-with-3d-scenes/overriding-scene-materials.html"
breadcrumb-title: ''
description: 覆盖3D场景中的现有材料，将其替换为您自己的Substance材料以进行测试和预览。
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Overriding scene materials
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 覆盖材料
user-guide-description: ''
user-guide-title: ''
source-git-commit: fa12f0ba789f700924fa0a6f3cbc0726c5f468e9
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 0%

---


# 覆盖材料

在使用现有材料的3D场景时，需要覆盖这些材料才能将其替换为您自己的文档。

可以从头构建材料，也可以构建已[提取到场景材料](../../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md)中的Substance图形的调整版本。

![覆盖材料，对其进行微调并将其重置为其场景状态](overriding-scene-materials.resources/tweakOverriddenMaterial.gif "覆盖场景材料，对其进行微调并将其重置为其场景状态"){zoomable="yes"}

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 覆盖材料

</td>
<td style="border: 0;" valign="top">

### 重置为场景状态

</td>
<td style="border: 0;" valign="top">

### 连接的材质

</td>
</tr>
</table>

## 覆盖材料

场景中使用的任何材料都可以用您自己的版本覆盖，即新材料或已编辑的现有材料版本。

“覆盖材料”操作位于以下两个位置：

* 打开“材料”菜单并转到所需材料的子菜单
* 按下场景对象上的Shift + LMB键以将其选中，然后单击RMB键以打开其上下文菜单

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![覆盖材料 — “3D 视图”视口中的操作](overriding-scene-materials.resources/overrideMaterialActionViewport.png "覆盖材料 — “3D 视图”视口中的操作"){zoomable="yes"}

*视口中的操作*

</td>
<td style="border: 0;" valign="top">

![覆盖材料 — “材料”菜单中的操作](overriding-scene-materials.resources/overrideMaterialActionMaterials.png "覆盖材料 — “材料”菜单中的操作"){zoomable="yes"}

*材料菜单中的操作*

</td>
</tr>
</table>

在Designer（使用USD作为其内部场景描述）的上下文中，覆盖意味着&#x200B;*创建尽可能与原始文档匹配的材料副本*，并将场景网格的&#x200B;*材料绑定*&#x200B;从原始文档更改为副本。

>[!NOTE]
>
> 副本在场景中根下的“<b>材料</b>”文件夹（USD中的“Scope”）中创建，并且使用与原始文件相同的标识符加上数字后缀（例如：“rustedMetal\_0”）

这意味着两件重要的事情：

1. 原始材料绝不会发生任何更改。
1. 在Designer中完成的任何工作都将应用于该副本。

如果您想恢复原始场景的材料或执行快速前后检查，您可以通过同一“覆盖材料”操作随时打开和关闭任何覆盖

考虑到副本是为匹配原始文件而创建的，在大多数情况下，覆盖材料不应更改其外观（请参阅下面的注释），直到将Substance图形连接到它或编辑其属性为止。

>[!NOTE]
>
> 应用覆盖时，Designer会计算受影响网格的正切和二项式，这可能需要一些时间并更改这些网格的方面，特别是在这些网格没有定义的正常比例和偏差或使用其他比例和偏差时。

>[!IMPORTANT]
>
> <b>AdobeStandardMaterial</b>着色模型在Substance 3D生态系统中受支持，但不是行业标准，因此&#x200B;*可能不受第三方应用程序（如Blender）支持*。
> 
> 为实现Substance 3D应用程序外部的最佳互操作性，目前建议使用<b>UsdPreviewSurface</b>着色模型，即使该模型支持的材料属性和效果少得多。

## 重置为场景状态

如果需要恢复到材料的初始状态，同时保持其覆盖状态并且仍可对其进行编辑，则可以将任何材料副本重置为初始值。

如果修改了材料属性值，或对图形应用了纹理，该属性将恢复为初始值或纹理。

材料可以完全重置，也可以按属性重置。

使用材料子菜单或网格上下文菜单中的“将材料重置为场景状态”操作可完全重置材料。

该操作可在三个位置找到：

* 打开“材质”菜单并转到所需材质的子菜单
* 按住场景对象上的Shift + LMB键将其选中，然后单击RMB键以打开上下文菜单
* 那个材料房顶上的汉堡菜单

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![将材料重置为场景状态 — “3D 视图”视口中的操作](overriding-scene-materials.resources/resetMaterialToSceneStateActionViewport.png "将材料重置为场景状态 — “3D 视图”视口中的操作"){zoomable="yes"}

*3D视图视口中的操作*

</td>
<td style="border: 0;" valign="top">

![将材料重置为场景状态 — “材料”菜单中的操作](overriding-scene-materials.resources/resetMaterialToSceneStateActionMaterials.png "将材料重置为场景状态 — “材料”菜单中的操作"){zoomable="yes"}

*“材质”菜单中的操作*

</td>
<td style="border: 0;" valign="top">

![将材料重置为场景状态 — “Properties”停放中的操作](overriding-scene-materials.resources/resetMaterialToSceneStateActionProps.png "将材料重置为场景状态 — “Properties”停放中的操作"){zoomable="yes"}

*材料属性中的操作*

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

如果只想重置材料的某些方面，也可以在材料属性中&#x200B;*每个属性*&#x200B;使用该操作。

打开材料属性的汉堡菜单以查找“重置为默认场景状态”操作。

</td>
<td style="border: 0;" valign="top">

![重置为场景状态 — 材料属性中的操作](overriding-scene-materials.resources/resetPropertyToSceneStateAction.png "重置为场景状态 — 材料属性中的操作"){zoomable="yes"}

</td>
</tr>
</table>

## 连接的材质

同样：Designer不会直接改变场景的材料，它在场景中创建副本，并将网格绑定到该副本而不是原始文档。

另一方面，Designer在其“材料”菜单中拥有&#x200B;*自己的*&#x200B;个单独的材料列表，默认与场景的材料列表匹配。 您可以随时在该列表中添加新材料。

这是一组仅在Designer中创作和管理的&#x200B;*其他*&#x200B;数据。 然后，这些材料&#x200B;*连接到副本*，这将覆盖场景的原始材料。

![覆盖材料 — 数据示意图](overriding-scene-materials.resources/overridingMaterialsSchematic.png "覆盖材料 — 数据示意图"){zoomable="yes"}

您可以将“材料”菜单中列出的任何材料连接到Designer在场景中创建的副本：在场景浏览器中单击副本上的人民币，然后转到“连接材料”子菜单。

子菜单列出了场景中的所有材料以及您可能从“材料”菜单手动创建的任何材料。

![连接材料](overriding-scene-materials.resources/connectMaterials.gif "连接材料"){zoomable="yes"}
