---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/3d-scene-resource.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer中导入和使用3D场景资源以进行素材预览和测试。
helpx_creative_field: ""
helpx_description: Designer > Resources > 3D scene resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 场景资源
user-guide-description: ''
user-guide-title: ''
source-git-commit: fde9d7a455c1c7b366323c119f4c1f9a2c114952
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 1%

---


# 3D 场景资源

本页介绍了Substance 3D Designer中的&#x200B;**3D场景**&#x200B;资源类型，包括其支持的文件格式以及可能的使用方式。

## 概述

可以在各种工作流程中使用3D场景资源：

* [烘焙网格图](../../bakers/bakers.md)
* 在[3D视图](../../interface/3d-view/3d-view.md)中预览[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)中的&#x200B;*纹理*

支持以下3D场景文件格式：

* [USD](https://graphics.pixar.com/usd/release/index.html) (\*.usd)
* [USDA](https://graphics.pixar.com/usd/release/index.html) (\*.usda)
* [USDZ](https://graphics.pixar.com/usd/release/index.html) (\*.usdz)
* [Autodesk FBX](https://www.autodesk.com/products/fbx/overview) (\*.fbx)
* [Wavefront OBJ](https://www.fileformat.info/format/wavefrontobj/egff.htm) (\*.obj)
* [Autodesk 3D Studio Mesh](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2022/ENU/3DSMax-Data-Exchange/files/GUID-A16ECF7F-70E5-4F9F-8EAD-35F5CFB485A2-htm.html) (\*.3ds)
* [拼贴画](https://www.khronos.org/collada/) (\*.dae)
* [Autodesk AutoCAD绘图](https://knowledge.autodesk.com/support/autocad/learn-explore/caas/CloudHelp/cloudhelp/2019/ENU/AutoCAD-Core/files/GUID-D4242737-58BB-47A5-9B0E-1E3DE7E7D647-htm.html) (\*.dxf)

## 网格存储

3D场景&#x200B;*只能*&#x200B;被链接，这意味着它们停留在磁盘上的位置，仅在应用程序中引用。

将包含3D 场景资源的包发布为[Substance 3D](https://www.adobe.com/products/substance3d/3d-augmented-reality.html)资源(SBSAR)时，网格&#x200B;*未嵌入*，但被丢弃。

## 网格图

将3D 场景链接到包是将网格图[烘焙为该场景几何形状](../../bakers/bakers.md)的唯一方法。 您可以执行以下步骤以开始使用：

* 在包上单击&#x200B;*人民币*，然后在上下文菜单中选择<b>链接>3D 网格</b>选项
* 选择任何受支持的3D 场景文件
* 如果显示<b>链接为Udim网格</b>对话框提示，请单击&#x200B;*否*，除非您要烘焙UV磁贴
* 在[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)中加载了资源后，单击资源上的&#x200B;*人民币*，然后在上下文菜单中选择<b>烘焙模型信息</b>选项
* 此时会显示[烘焙模型信息](../../bakers/bakers.md)对话框，供您设置和运行任何网格图烘焙

![网格图](3d-scene-resource.resources/bake-model-information.gif "烘焙网格图"){width="512px"}

## UDIM/UV磁贴使用情况

在链接网格资源并且该应用程序检测到它具有0-1范围之外的UV时，系统将询问您是否应将此网格视为UDIM网格（也称为UV 平铺）。 此设置以后可以更改，除非您确定正在使用UV拼贴，否则应按<b>否</b>回答。

如果UV拼贴行为处于活动状态，则烘焙的行为将有所不同，并将烘焙每个检测到的UV拼贴的纹理。

## 资源/场景与状态

该应用程序将您在3D视图中看到的内容分成两个不同的文件。 实际的3D模型或网格是资源管理器中可见的资源。 光照、相机和其他设置的设置称为“<b>状态</b>”。 可以将状态保存到外部.sbsscn文件，以便以后再次加载。 .sbsscn文件不是资源，它们是只能通过[3D 视图中的“场景”菜单加载的其他配置文件。](../../interface/3d-view/3d-view.md)
