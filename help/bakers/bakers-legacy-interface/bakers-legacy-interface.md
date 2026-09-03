---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/bakers/bakers-legacy-interface.html"
breadcrumb-title: ''
description: 了解适用于熟悉旧版本的用户的Substance 3D Designer面包师的旧版界面。
helpx_creative_field: ""
helpx_description: Designer > Bakers > Bakers Legacy Interface
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 面包师旧版界面
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 3%

---


# 面包师旧版界面

以下是6.0.4之前的[Adobe Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)版本中可用的烘焙器界面的说明。

## 概述

![](bakers-legacy-interface.resources/bakers-legacy-interface-01.png)

烘焙面板分为四个部分：

### 1：场景

![](bakers-legacy-interface.resources/bakers-legacy-interface-02.png)

允许您定义网格的哪一部分参与烘焙过程。

第6版中的新增功能，您还可通过材质进行选择：

![](bakers-legacy-interface.resources/bakers-legacy-interface-03.png)

### 2：面包师

![](bakers-legacy-interface.resources/bakers-legacy-interface-04.png)

按![](bakers-legacy-interface.resources/bakers-legacy-interface-05.png)按钮可将所需的面包师添加到处理列表中

>[!NOTE]
>
> 烘焙按列表顺序（从上到下）处理：如果您要在另一个烘焙过程中重复使用烘焙结果（如法线图），这可能非常重要

单击面包师布局中的“+”图标可将面包师添加到栈叠中（您可以将任意数量的面包师放在栈叠中）。

.![](bakers-legacy-interface.resources/bakers-legacy-interface-06.png)

通过按![](bakers-legacy-interface.resources/bakers-legacy-interface-07.png)，可以从列表中移除烘焙过程

您可以通过选择烘焙过程并使用![](bakers-legacy-interface.resources/bakers-legacy-interface-08.png)对烘焙过程列表重新排序

### 3：烘焙参数

![](bakers-legacy-interface.resources/bakers-legacy-interface-09.png)

此部分显示当前所选烘焙的特定选项。

### 4：公共参数

![](bakers-legacy-interface.resources/bakers-legacy-interface-10.png)

显示面包师之间共享的参数。

>[!NOTE]
>
> 默认情况下，更改其中一个参数将影响所有面包师，但勾选所有面包师通用的“覆盖参数”除外：在这种情况下，更改将仅针对当前面包师。

* **资源名称**&#x200B;字段允许您根据需要更改生成的位图的名称。
* **使用“文件格式”**&#x200B;下拉列表可以更改默认的文件格式（Windows或OS/2位图格式“BMP”）。
* **&#x200B;**&#x200B;**将**&#x200B;资源放入网格特定的文件夹复选框允许您选择生成的位图是存储在模型所在的级别，还是存储在名为“Resources”的新子文件夹中。
* **方法**&#x200B;允许您定义新位图资源是应链接还是嵌入到Substance包中。
* **文件夹**&#x200B;允许您定义保存映射的位置。

按烘焙窗口右下角的“确定”按钮将开始烘焙过程。

版本6中的新功能：您现在可以使用取消按钮取消烘焙过程：

![](bakers-legacy-interface.resources/bakers-legacy-interface-11.png)
