---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/scripting/plugin-basics.html"
breadcrumb-title: ''
description: 了解为Substance 3D Designer创建Python插件以扩展应用程序功能的基础知识。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Plugin basics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 增效工具基础知识
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# 增效工具基础知识

增效工具是定义<b>initializeSDPlugin()</b>函数的Python文件或Python模块。

加载插件时调用<b>initializeSDPlugin()</b>函数。\
在此函数中，您可以创建用户界面元素、注册回调以及您可能需要的任何其他功能。

或者，该插件可以定义一个<b>uninitializeSDPlugin()</b>函数，该函数将在卸载该插件时调用。\
您可以使用此功能释放资源、关闭网络连接和进行类似操作。

```
## Plugin entry point. Called by Designer when loading a plugin.

def initializeSDPlugin(): 

 print("Hello!") 

 

## If this function is present in your plugin,

## it will be called by Designer when unloading the plugin.

def uninitializeSDPlugin(): 

 print("Bye!")
```
