---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/technical-issues/crash-when-rendering-graphs.html"
breadcrumb-title: ''
description: 在Substance 3D Designer中渲染图形时对崩溃进行疑难解答，并找到防止发生这些问题的解决方案。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Crash when rendering graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 渲染图形时崩溃
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 3%

---


# 渲染图形时崩溃

本页列出了在Substance 3D Designer中的图形呈现过程中发生的崩溃，并且提供了针对各个问题的故障排除步骤。

## TDR（仅限Windows）

<b>[![(error)](../../assets/error.svg)](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash)问题</b>

系统的<b>超时检测和恢复(TDR)</b>计时器&#x200B;*太短*，无法在图形驱动程序&#x200B;*重新启动*&#x200B;之前让Substance 3D Designer完成其当前计算。

Substance 3D Designer执行的计算可能非常密集，并且使用图形驱动程序达到其&#x200B;*在一段时间内不会对操作系统做出响应*&#x200B;的程度。\
作为一项稳定性和安全措施，操作系统&#x200B;*重新启动图形驱动程序*，缩短了计算并导致Substance 3D Designer *崩溃*。

<b>！[(tick)](../../assets/check.svg)建议的步骤</b>

TDR计时器值需要&#x200B;*增加*&#x200B;才能防止此类崩溃。 您可以按照Substance 3D Painter文档的[此页面](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash)中的说明执行此操作，这些文档也适用于Substance 3D Designer。
