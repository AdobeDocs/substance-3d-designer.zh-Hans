---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/technical-issues/python-issues.html"
breadcrumb-title: ''
description: 解决Substance 3D Designer中的Python脚本问题，包括增效工具和API问题。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Python issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Python问题
user-guide-description: ''
user-guide-title: ''
source-git-commit: 21af965a075e8c119d16922f15b867da99c21397
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# Python问题

本页列出了与Substance 3D Designer的[Python API](../../scripting/scripting.md)以及Python中实现的功能相关的技术问题，并提供了相应的故障排除步骤。

Python中实现的功能包括[资源管理器](../../interface/the-explorer-window/the-explorer-window.md)工具栏中的[Publish](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)/[发送到](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md)操作，以及用于删除图表中未使用的节点的工具。

## “QtForPython”模块无法加载

<b>![（错误）](python-issues.resources/error.svg)问题</b>

无法加载“QtForPython”Python模块，这会导致缺少Python中实现的功能，如[节点](../../interface/the-explorer-window/the-explorer-window.md)工具栏中的[Publish](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)/[发送到](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md)资源管理器，以及用于移除图形中未使用的节点的工具。

此外，许多[Python插件](../../scripting/plugin-basics/plugin-basics.md)将无法加载或无法按预期工作。

<b>![（刻度）](python-issues.resources/check.svg)建议的步骤</b>

Designer安装的QtForPython及其依赖项与系统上的现有安装之间可能存在冲突。

删除[QtForPython](https://doc.qt.io/qtforpython-5/index.html) ([PySide2](https://pypi.org/project/PySide2/))和[Shiboken2](https://pypi.org/project/shiboken2/)的任何其他系统安装。

或者，您也可以考虑使用Python *虚拟环境*&#x200B;或&#x200B;*包管理器*（例如[rez](https://github.com/AcademySoftwareFoundation/rez)），而不是在系统范围内安装QtForPython。
