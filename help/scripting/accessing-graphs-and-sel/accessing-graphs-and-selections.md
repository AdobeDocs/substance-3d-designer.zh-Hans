---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/accessing-graphs-and-selections.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer Python脚本中访问和处理图表和节点选择。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Accessing graphs and selections
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 访问图表和选区
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# 访问图表和选区

<b>SDApplication</b>类包含一些有用的方法，可让您访问&#x200B;*当前活动的*&#x200B;图形以及图形内的&#x200B;*当前选择*。

```
import sd 

 

## Get the application and UI manager object.

ctx = sd.getContext() 

app = ctx.getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

 

## Get the current graph.

g = uiMgr.getCurrentGraph() 

print("The current graph is %s" % g) 

 

## Get the currently selected nodes.

selection = uiMgr.getCurrentGraphSelectedNodes() 

for node in selection: 

 print("Node %s" % node)
```


使用<b>graphViewID</b>可访问在&#x200B;*特定*&#x200B;图形视图中显示的图形。

在创建自定义图形视图工具栏时，此方法非常有用。 [创建用户界面元素](../../scripting/creating-user-interface/creating-user-interface-elements.md)一章中的<b>在图形视图中创建工具栏</b>示例提供了更多详细信息。
