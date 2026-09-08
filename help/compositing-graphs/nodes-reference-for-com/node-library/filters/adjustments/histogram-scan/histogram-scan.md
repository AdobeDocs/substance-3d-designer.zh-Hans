---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan.html"
breadcrumb-title: ''
description: 使用“直方图扫描”节点扫描和分析纹理直方图，以进行颜色校正和调整。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 直方图扫描
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 7%

---


# 直方图扫描

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/histogram-scan-1.png){width="128px"}

<b>英寸：</b>滤镜>调整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

这个节点非常简单但非常有用，它提供了一种直观的方法来重新映射输入灰度图像的对比度和亮度。 可用于以动态方式“扩大”和“缩小”蒙版。

[单击此处观看关于直方图操作的Substance学院视频。](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=427s)

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>位置</b> <i>0.0 - 1.0</i> | 与亮度控制类似，移动结果的中点。 在渐变输入上使用时，这将扩展并缩小过渡点。<br><br>重要提示：默认值0表示最终结果始终为黑色，因此请尝试从0.5开始！ |
| <b>对比度</b> <i>0.0 - 1.0</i> | 调整结果的对比度。 可用于设置过渡的硬度。 |
| <b>反转位置</b> <i>False/True</i> | 反转最终结果。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/histogram-scan.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/histogram-scan2.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/histogram-scan3.gif" />
        </td>
    </tr>
</table>
