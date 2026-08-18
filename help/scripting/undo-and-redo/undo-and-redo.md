---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/undo-and-redo.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer Python脚本中实现用于用户操作的撤消和重做功能。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Undo and redo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 还原和重做
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---


# 还原和重做

使用<b>SDHistoryUtils.UndoGroup</b>类，用户可以&#x200B;*对操作进行分组*，以便在一个命令中&#x200B;*撤消或重做*&#x200B;所有操作。

这些组由用户&#x200B;*命名*，将在用户界面的还原/重做列表中按该名称显示。  这使得大量操作更易于管理。

```
import sd 

from sd.api.sdhistoryutils import * 

 

## Get the application and package manager objects.

cxt = sd.getContext() 

app = cxt.getSDApplication() 

pkgMgr = app.getPackageMgr() 

 

## Group one or more changes into an undo group.

with SDHistoryUtils.UndoGroup("My Undo Group"): 

## Create two new packages.

    pkgMgr.newUserPackage() 

    pkgMgr.newUserPackage()
```
