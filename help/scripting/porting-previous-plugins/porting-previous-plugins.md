---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/scripting/porting-previous-plugins.html"
breadcrumb-title: ''
description: 了解如何将插件从以前版本的Substance Designer移植到当前的Python API。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Porting previous plugins
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 移植以前的增效工具
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# 移植以前的增效工具

由于为支持适用于Python的Qt所做的更改，**以前的增效工具将不再工作**。\
尤其请注意以下事项：

## 插件加载和卸载

现在，在应用程序<b>启动</b>时加载插件，在应用程序<b>退出</b>时卸载插件。\
因此，插件已&#x200B;*不需要*&#x200B;从“*sdplugins.Plugin*”继承。

有关详细信息，请查看[插件基础知识](../../scripting/plugin-basics/plugin-basics.md)部分。

## 创建用户界面元素

插件&#x200B;*不再需要*&#x200B;来定义“*sdplugins.PluginDesc*”。\
相反，增效工具可以使用<b>新的[UI管理器](../scripting-api-reference/scripting-api-reference.md#ui-manager-sduimgr)对象</b>和<b>Qt for Python</b>来创建它们需要的任何用户界面元素。

您可以在[创建用户界面元素](../../scripting/creating-user-interface/creating-user-interface-elements.md)部分中找到小代码示例。

## 替换位置上下文的使用

已将“*SDLocationContext*”类&#x200B;*从Python API中删除*。\
增效工具可以使用<b>[UI管理器](../scripting-api-reference/scripting-api-reference.md#ui-manager-sduimgr)对象</b>访问当前活动的图形和选区。

可在[访问图表和选区](../../scripting/accessing-graphs-and-sel/accessing-graphs-and-selections.md)部分中找到一些示例。
