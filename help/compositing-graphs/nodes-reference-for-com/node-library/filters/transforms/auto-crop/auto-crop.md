---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/auto-crop.html"
breadcrumb-title: ''
description: 使用“自动裁剪”节点自动裁剪纹理，以移除空边框并优化纹理尺寸。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Auto Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 自动裁剪
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---


# 自动裁剪

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocropgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocropcolor.png){width="200px"}

</td>
</tr>
</table>

<b>英寸：</b>筛选器>变换

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

**自动裁剪**&#x200B;节点调整&#x200B;**输入**，以便其内容可以放在图像的&#x200B;*中心*&#x200B;而不调整大小，或调整到图像的&#x200B;*范围*。

图像的内容由符合&#x200B;**X**&#x200B;和&#x200B;**Y**&#x200B;的&#x200B;*第一个和最后一个像素*&#x200B;的框定义，这些像素的值是&#x200B;*大于0*（即非黑色）。 **颜色**&#x200B;版本允许您从RGB和Alpha通道中选择用于定义该框。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>模式</b> <i>整数</i> | 设置应应用的裁剪方法： <br><br>- <i>裁剪方形</i>：裁剪图像以使形状位于可完全包含它的最小<i>方形</i>图像的中心<br>- <i>裁剪自动</i>：裁剪图像以使形状位于可完全包含它的最小<i>方形或非方形</i>图像的中心<br>- <i>适合（保持比例）</i>：在保持图像大小的同时，将图像调整到图像的<i>全宽</i> <i>比例</i>（即宽长比）<br>- <i>填充(拉伸)</i>：将图像大小调整为图像的<i>全宽</i> |
| <b>使用Alpha</b> <i>布尔值</i> | 使用<b>输入</b>的Alpha 通道来确定图像内容的<i>边界</i>以进行裁剪。 设置为<i>False</i>时，将改用黑色像素。<br><br><i>注意：</i>此参数仅在节点的<b>Color</b>版本中可用。 |
| <b>筛选模式</b> <i>整数</i> | 定义在像素<i>插值</i>时，如何处理采样结果：<br><br>- <i>最接近</i>：将对完全相同的<i>相同</i>值（更快）<br>- <i>双线性</i>：将对结果应用双线性的滤镜，以获得<i>更平滑</i>的外观<br>- <i>自动</i>：根据所选的<b>模式</b>进行裁剪，使用上述两种模式中最合适的模式 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/autocrop-demo-01-resized.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/autocrop-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/autocrop-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/autocrop-variant4.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/autocrop-variant3.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/autocrop-node.png" />
        </td>
    </tr>
</table>
