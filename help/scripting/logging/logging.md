---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/scripting/logging.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer Python增效工具中实施日志记录以进行调试和监控。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Logging
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 记录
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 4%

---


# 记录

我们建议使用标准Python的日志模块进行日志记录。

<b>sd</b>模块包含用于将日志记录重定向到Designer控制台的助手类。

## 登录到Designer的控制台面板

```
import logging 

import sd 

 

 

## Create a logger.

logger = logging.getLogger("MyLogger") 

 

 

## Add a handler to redirect logging to Designer's console panel.

ctx = sd.getContext() 

logger.addHandler(ctx.createRuntimeLogHandler()) 

 

 

## Do not propagate log messages to Python's root logger.

logger.propagate = False 

 

 

## Set the default log level if needed.

logger.setLevel(logging.DEBUG) 

 

 

## Use the logger

logger.info("Info message") 

logger.warning("Warning message") 

logger.error("Error message")
```
