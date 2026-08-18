---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/font-resource.html"
breadcrumb-title: ''
description: 在Substance 3D Designer中导入并使用字体资源向素材添加文本和排版规则。
helpx_creative_field: ""
helpx_description: Designer > Resources > Font resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 字体资源
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# 字体资源

字体资源应与[原子文本节点](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)一起使用。 通过引用磁盘上的任意位置中的字体文件，这些字体允许您使用系统上未安装的字体。

>[!NOTE]
>
> **SBSAR中的字体**
> 
> 无论字体来自链接的资源还是通过使用系统安装的字体，字体始终嵌入在SBSAR中。 此方法的优势在于无需安装，并且在导出具有依赖项的SBS文件时，可以确保字体文件随附在一起。

## 使用自定义字体资源

* 右键单击包，选择<b>链接>字体</b>
* 选择.otf或.ttf文件。
* 在您的[图形](../../compositing-graphs/substance-compositing-graphs.md)中放置[文本节点](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)。
* 在<b>字体</b>属性下，任何字体资源都可在列表的顶部找到。

请注意，字体列表不会在属性打开时自动刷新。 您必须切换到另一个属性窗口并切换回“文本”节点，才能查看新链接的字体。
