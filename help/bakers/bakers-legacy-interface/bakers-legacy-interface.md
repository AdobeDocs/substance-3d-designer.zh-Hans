---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/bakers/bakers-legacy-interface.html"
breadcrumb-title: ''
description: 了解适用于熟悉旧版本的用户的Baker的旧版界面。
helpx_creative_field: ""
helpx_description: Designer > Bakers > Bakers Legacy Interface
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Baker旧版界面
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 4%

---


# Baker旧版界面

以下是6.0.4之前的[Adobe Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)版本中可用的Baker界面的说明。

## 概述

![](bakers-legacy-interface.resources/image2017-3-13-9-33-40.png)

Baker面板分为四个部分：

### 1：场景

![](bakers-legacy-interface.resources/image2017-3-13-9-35-53.png)

用于定义烘焙过程中涉及的网格部分。

版本6中的新功能，您还可按材料选择：

![](bakers-legacy-interface.resources/image2017-3-13-9-45-26.png)

### 2：Baker

![](bakers-legacy-interface.resources/image2017-3-13-9-46-26.png)

按![](bakers-legacy-interface.resources/image2017-3-13-9-47-47.png)按钮可将所需的Baker添加到处理列表中

>[!NOTE]
>
> 烘焙按列表顺序（从上到下）处理：如果您要在另一个烘焙流程中重用烘焙的结果（如法线图），这可能非常重要

通过单击Baker布局中的“+”，可以在堆叠中添加Baker（您可以在堆叠中放置任意数量的Baker）。

.![](bakers-legacy-interface.resources/image2017-3-13-9-52-8.png)

按![](bakers-legacy-interface.resources/image2017-3-13-9-54-33.png)可以从列表中删除烘焙进程

您可以通过选择烘焙进程并使用![](bakers-legacy-interface.resources/image2017-3-13-9-55-33.png)对烘焙进程列表重新排序

### 3：Baker参数

![](bakers-legacy-interface.resources/image2017-3-13-13-24-0.png)

此部分显示当前所选Baker的特定选项。

### 4：公共参数

![](bakers-legacy-interface.resources/image2017-3-13-13-28-12.png)

显示Baker之间共享的参数。

>[!NOTE]
>
> 默认情况下，更改这些参数之一将影响所有Baker，但勾选所有Baker通用的覆盖参数除外：在这种情况下，更改将在当前Baker的本地进行。

* **资源名称**&#x200B;字段允许您根据需要更改生成的位图的名称。
* **使用“文件格式”**&#x200B;下拉列表可以更改默认的文件格式（Windows或OS/2位图格式“BMP”）。
* **&#x200B;**&#x200B;**将**&#x200B;资源放入网格特定的文件夹复选框可让您选择生成的位图是存储在模型所在的级别，还是存储在名为“Resources”的新子文件夹中。
* **方法**&#x200B;允许您定义新位图资源是应链接还是嵌入到Substance包中。
* **文件夹**&#x200B;允许您定义保存映射的位置。

按“Baker”窗口右下角的“确定”按钮将开始烘焙过程。

版本6中的新功能：现在，您可以使用“取消”按钮取消烘焙过程：

![](bakers-legacy-interface.resources/image2017-3-13-13-50-4.png)
