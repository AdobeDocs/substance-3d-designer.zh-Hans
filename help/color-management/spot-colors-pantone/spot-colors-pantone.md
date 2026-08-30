---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/color-management/spot-colors-pantone.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer中使用Pantone专色，以便在打印和设计工作流程中实现准确的颜色匹配。
helpx_creative_field: ""
helpx_description: Designer > Color Management > Spot Colors (Pantone)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 专色(Pantone)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---


# 专色(Pantone)

专色是选择颜色的替代模式。 Substance 3D Designer可让您从色标簿中选择颜色，从而匹配现有的色彩管理和复制系统，而不是标准的RGB或HSV拾色器。 这可让您确保Designer中使用的数字颜色与所生产的产品的数字颜色非常匹配。

目前，专色提供了17本Pantone书籍。

## 色彩管理

由于专色用于准确的颜色重现和匹配，因此开始工作之前，您必须为Designer设置[色彩管理](../../color-management/color-management.md)。 专色最好与<b>Adobe 颜色引擎(ACE)</b>色彩管理配合使用，而不是OCIO。 它们可以在旧版模式下工作，但如果您没有针对显示器进行sRGB校准，则无法确保正确显示它们。

简言之，设置专色的色彩管理包括以下步骤：

* 通过生成或获取适当的ICC配置文件来校准监视。
* 在Designer的首选项中启用带Adobe 颜色引擎(ACE)的色彩管理。
* 设置2D和3D视图以使用显示器中的适当配置文件。
* 重新启动以使更改生效。
* 验证Designer与其他Adobe应用程序（如Adobe Illustrator或Photoshop）之间的颜色是否匹配。 第一本Pantone书籍《纯色涂层纸》中的颜色“<b>Pantone Rhodamine Red C</b>”是一个很好的测试用例，因为如果色彩管理不正确，该颜色可能会发生显着变化。

>[!WARNING]
>
> **缩略图颜色**
> 
> 节点缩略图&#x200B;*默认情况下不进行色彩管理*，因此在2D视图中仅会显示具有正确配置文件的信任颜色。 可以在项目的色彩管理下的首选项中启用缩略图色彩管理，但性能略有下降。

## 使用专色

### 从RGB切换到专色

即使设置了色彩管理，拾色器默认情况下仍然为RGB或HSV拾色器。 您需要手动将它们切换为专色。 此设置按参数存储，在公开参数时甚至还会继续存储。

1. 单击RGB色板旁边的![](spot-colors-pantone.resources/image2021-1-25-9-40-40.png) <b>拾色器类型</b>按钮。
1. 从下拉列表中选择任意<b>色标簿</b>，而不是<b>RGB颜色</b>。
1. ![](spot-colors-pantone.resources/image2021-1-25-9-40-25.png) <b>拾色器类型</b>的图标将更改，且其界面将更改为<b>专色</b>模式。

![切换到专色模式](spot-colors-pantone.resources/spot-switch.gif "切换到专色模式"){width="512px"}

### 选择和查找专色

有几种方式可以在色标簿中查找和选择专色。

* 您可以使用书籍页面两侧的![](spot-colors-pantone.resources/image2021-1-25-10-40-28.png) ![](spot-colors-pantone.resources/image2021-1-25-10-40-53.png) <b>左右箭头</b>在页面之间翻转。 您还可以单击并拖动页面显示，以在页面之间滚动。
* 您可以从当前页面中单击任何颜色来选取它。 通常，有更多的颜色可用，需要向下滚动一点。
* 您可以使用搜索栏按名称或编号搜索颜色。 这种搜索只匹配书中的颜色名称，没有复杂的逻辑；搜索“灰色”只会得到名称中包含“灰色”字样的结果，您不会看到任何名称中仅包含数字的灰色颜色。
* 要为色标簿获取更大、更易于使用的界面，请单击![](spot-colors-pantone.resources/image2021-1-25-10-39-18.png) <b>滴管</b>图标和![](spot-colors-pantone.resources/image2021-1-25-10-40-28.png) <b>向左箭头</b>之间的颜色预览框。

![浏览专色](spot-colors-pantone.resources/spot-choose.gif "浏览专色"){width="512px"}

### 选取和转换专色

可以使用![](spot-colors-pantone.resources/image2021-1-25-10-39-18.png) <b>滴管</b>工具选取专色。 在专色模式下，这意味着将取样的RGB转换为当前选定书籍中匹配最接近的专色。

Designer的<b>滴管</b>工具可在屏幕上的任何位置使用，没有任何限制，因此这意味着您可以使用Designer作为专色转换工具。

切换色标簿，甚至从专色色标簿切换回RGB，会将当前颜色转换为最匹配的颜色。 这意味着您可以在书籍之间转换颜色，然后再转换回RGB。

>[!WARNING]
>
> 在画册之间转换专色是一项有损操作。 进行往返转换通常不会得到与最初使用的颜色相同的颜色！

![选取和转换专色](spot-colors-pantone.resources/spot-pick.gif "选取和转换专色"){width="512px"}
