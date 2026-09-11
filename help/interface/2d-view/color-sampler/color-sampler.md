---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/interface/2d-view/color-sampler.html"
breadcrumb-title: ''
description: 使用2D 视图中的Color Sampler工具从纹理中取样颜色，以实现精确的颜色匹配。
helpx_creative_field: ""
helpx_description: Designer > Interface > 2D view > Color sampler tool
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 颜色取样器工具
user-guide-description: ''
user-guide-title: ''
source-git-commit: c7bf2522b15bef308d1471ca234c6619091f95fc
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---


# 颜色取样器工具

![颜色取样器工具](color-sampler.resources/color-sampler-demo.png "颜色取样器工具"){zoomable="yes"}

使用Color Sampler工具，您可以在微调参数或切换2D 视图时<b>跟踪[节点](../../../interface/2d-view/2d-view.md)中特定像素</b>的值。

它将一个大头针放在视口中并对该位置的像素的颜色和位置进行采样。

## 使用工具

请按照以下步骤访问和使用工具：

1. 单击2D 视图工具栏中的![](color-sampler.resources/color-sampler-information-button.png) <b>“信息”</b>按钮，以打开“信息”程序坞和工具栏
1. 单击“信息”工具栏中的![](color-sampler.resources/color-sampler-tool-icon.png) <b>彩色Sampler工具</b>按钮
1. 在视口中，单击要采样的特定像素以放置![](color-sampler.resources/color-sampler-pin-icon.png) <b>大头针</b>
1. 检查信息坞的专用部分中的取样值
1. 使用完工具后，单击![](color-sampler.resources/color-sampler-remove-pin.png) <b>“删除”</b>按钮以从视口中删除该大头针。\
   您也可以通过单击大头针上的人民币并在上下文菜单中选择“删除”操作将其删除。

下面演示了该工具的实际运行：

![颜色取样器：使用工具](color-sampler.resources/color-sampler-demo.gif "颜色取样器：使用工具"){zoomable="yes"}

*单击以放大*

+++复制取样RGBA值
要复制采样值，您可以单击大头针上的人民币，然后在上下文菜单中选择“复制RGBA值”操作。

可以使用颜色缩略图</b>将复制的值<b>粘贴到参数中。

也可以将“信息”面板中的颜色缩览图直接拖放到这些参数的颜色缩览图上。

![颜色取样器：复制RGBA值](color-sampler.resources/color-sampler-demo-copy-rgba-values.gif "颜色取样器：复制RGBA值"){zoomable="yes"}



*单击以放大*

+++

## 采样信息

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

信息分为三种类型和两种格式。

* <b>样本值</b>存储在图像的每个RGBA通道中：\
  变量\* /浮点
* HSV表示形式中的<b>取样颜色</b>：\
  8位整数/浮点
* 像素的<b>位置</b> （以像素数和规范化的图像空间表示）：\
  整数/浮点

</td>
<td width="33.33%" style="border: 0;" valign="top">

![采样信息](color-sampler.resources/color-sampler-information.png "采样信息"){zoomable="yes"}

</td>
</tr>
</table>

此值取决于图像使用的位深度。 在Substance图中，位深度由<b>输出格式</b>控制 [基本参数](../../../compositing-graphs/graph-parameters/graph-parameters.md)。

可用的位深度包括：

* <b>8位整数：</b>介于0到255之间的256整数值。
* <b>16位整数：</b>介于0到65,535之间的65,536整数值。
* <b>HDR低精度（16位）</b>：使用16位编码的浮点值。
* <b>HDR高精度（32位）</b>：使用32位编码的浮点值。 这是Designer中可用的最高精度。
