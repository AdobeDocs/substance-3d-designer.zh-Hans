---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/bakers.html"
breadcrumb-title: ''
description: 了解如何使用Substance 3D Designer生成器将基于网格的信息计算到纹理文件中。
helpx_creative_field: ""
helpx_description: Designer > Bakers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 烘焙
user-guide-description: ''
user-guide-title: ''
source-git-commit: 583588c4e12e3d0857c2b16200945e36ea523151
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---


# 烘焙

烘焙是指&#x200B;**将基于网格的信息传递到纹理**&#x200B;的操作。 然后，着色器和/或Substance滤镜读取这些信息，以生成更高级的效果或纹理。

>[!NOTE]
>
> 要了解有关烘焙的更多信息，请参阅[烘焙文档](https://experienceleague.adobe.com/zh-hans/docs/substance-3d/bakers/home)。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

可以通过[资源管理器](../interface/the-explorer-window/the-explorer-window.md)窗口中的网格文件访问烘焙窗口。 右键单击网格名称并选择“**烘焙模型信息**”以打开烘焙窗口。

</td>
<td width="33.33%" style="border: 0;" valign="top">

3D场景资源的上下文菜单中的![“烘焙模式信息”选项](bakers.resources/sd-mesh-right-click.png " 3D场景资源的上下文菜单中的“烘焙模式信息”选项")

</td>
</tr>
</table>

![烘焙窗口](bakers.resources/sd-window-overview.png "烘焙窗口")

## 概述

烘烤窗分为若干面板，如下所述。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 要烘焙的元素

此面板控制将使用低多边形网格的哪一部分进行烘焙。

它列出了在低多边形网格文件中找到的几何。 缺省情况下，该列表基于在文件中找到的单个材料，但在相关时可将其切换到子网格。 您可以取消选中在烘焙过程中应忽略的元素。

</td>
<td style="border: 0;" valign="top">

![](bakers.resources/sd-mesh-selection.png)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 输出

此面板控制烘焙纹理将位于何处。

</td>
<td style="border: 0;" valign="top">

![](bakers.resources/sd-output.png)

</td>
</tr>
</table>

| *参数* | *描述* |
| --- | --- |
| **方法** | 控制烘焙纹理将与Substance包一起存储的方式。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>嵌入</strong> ：烘焙纹理存储在具有特定命名的Substance包旁边的子文件夹中。</li><li data-preserve-html="true"><strong>已链接</strong>（默认） ：烘焙纹理存储在定义的文件夹中，然后引用到Substance包中。</li></ul> |
| **文件夹** | 存储烘焙纹理时的位置。 单击三点式按钮打开一个文件对话框并选择导出文件夹。右侧将显示一个复选标记，指示文件夹是否实际存在。 |
| **名称** | 烘焙纹理的命名约定。 单击三点式按钮以打开下拉列表并插入其他占位符（品牌名称、自定义、材质、网格）。 |
| **示例** | 模拟文件名以测试命名约定。 |
| **将资源放入网格特定的文件夹** | 如果启用，烘焙纹理将保存在名为网格文件的文件夹中。 |

### 高清网格

此面板控制高多边形网格列表和相关设置。 有关详细信息，请参阅[常用参数](https://experienceleague.adobe.com/zh-hans/docs/substance-3d/bakers/bakers-settings/common-parameters)。

![高清网格](bakers.resources/sd-high.png "高清网格")

### 默认值

有关详细信息，请参阅[常用参数](https://experienceleague.adobe.com/zh-hans/docs/substance-3d/bakers/bakers-settings/common-parameters)。

![默认值](bakers.resources/sd-default-values.png "默认值")

### 面包师渲染列表和设置

**面包师渲染列表**&#x200B;可供您选择生成哪种烘焙纹理。 默认情况下，该列表为空。

* **添加新的面包师：**&#x200B;单击“添加面包师”按钮。
* **删除面包机：**&#x200B;在列表中选择面包机，然后单击“删除面包机”按钮。
* **将面包机移动到顶部：**&#x200B;在列表中选择面包机，然后单击“拉至顶部”按钮。
* **向下移动面包机：**&#x200B;在列表中选择面包机，然后单击“下移”按钮。

默认情况下，继承中的每个面包师都使用默认值（请参阅上文）。 例如，可以通过单击面包机行上的单元格来覆盖大小（分辨率）。 这适用于行中的其他设置。

单击列表中的面包机时，“面包机参数”视图将使用其特定参数更新。

要了解有关特定参数的详细信息，请参阅： [面包师设置](https://experienceleague.adobe.com/zh-hans/docs/substance-3d/bakers/bakers-settings/bakers-settings)。

![面包师渲染列表](bakers.resources/sd-baker-list.png "面包师渲染列表")
