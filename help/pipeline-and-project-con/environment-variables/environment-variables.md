---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/pipeline-and-project-configuration/environment-variables.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer中使用环境变量来配置路径和系统设置。
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Environment variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 环境变量
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 3%

---


# 环境变量

此页列出可用于覆盖应用程序的默认行为的环境变量。

| 变量 | 描述 |
| --- | --- |
| **SBS\_DESIGNER\_PYTHON\_PATH** | Designer将从中加载[Python插件](../../scripting/plugin-basics/plugin-basics.md)的路径。 |
| **SUBSTANCE\_DESIGNER\_LICENSE** | Designer应使用的许可证文件(*license.key*)的位置。   覆盖Designer [激活向导](../../getting-started/activation-and-licenses/activation-and-licenses.md)中设置的路径。  **注意：**&#x200B;旧版本可能需要使用备用变量名称：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>SUBSTANCE_DESIGNER_6_许可证</strong></li><li data-preserve-html="true"><strong>SUBSTANCE_DESIGNER_5_许可证</strong></li></ul> |
| <b>OCIO</b> | 使用OpenColorIO [色彩管理](../../color-management/color-management.md)时应使用的OCIO配置文件的路径。   在[项目设置](../../interface/preferences-window/project-settings/project-settings.md)中覆盖Designer色彩管理设置中设置的路径。 |
| **ALLEGO\_LICENSE\_IDLE\_DELAY** | 如果是多用户配置，则释放许可证席位之前的延迟秒数为7200秒（2小时）。 |
