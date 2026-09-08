---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan-non-uniform.html"
breadcrumb-title: ''
description: 使用直方图扫描非均匀节点执行非均匀直方图扫描以实现高级颜色校正。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan Non-Uniform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 直方图扫描不均匀
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 3%

---


# 直方图扫描不均匀

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/histogram-scan-non-uniform.png){width="128px"}

<b>英寸：</b>滤镜>调整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

[直方图扫描](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)的高级版本，带有额外的控件和输入，可在每像素级别上驱动效果，而不是在整个图像中统一。 可用于实现更复杂的蒙版中的对比度和过渡。

使用它比常规[直方图扫描](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)复杂得多，因此，在尝试使用非统一版本之前，请确保您熟悉它。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>输入</b> <i>灰度输入</i> | 要修改的源结果。 |
| <b>位置图</b> <i>灰度输入</i> | 输入插槽以驱动“位置”参数。 在“使用位置输入”设置为True时激活。 有效值范围较小，具体取决于对比度映射和设置。 |
| <b>对比度图</b> <i>灰度输入</i> | 输入插槽以驱动对比度参数。 在“使用对比度输入”设置为True时激活。 有效值范围小。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>使用位置输入</b> <i>False/True</i> | 切换使用位置映射输入槽。 |
| <b>位置</b> <i>0.0 - 1.0</i> | 控制或修改映射结果以驱动位置设置。 |
| <b>使用对比度输入</b> <i>False/True</i> | 切换对比度映射输入插槽的使用。 |
| <b>对比度</b> <i>0.0 - 1.0</i> | 控制或修改映射结果以驱动对比度设置。 |
