---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-uv.html"
breadcrumb-title: ''
description: 使用“UV”节点在UV空间中应用漫射效果，以创建平滑的颜色过渡和混合。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion UV
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 2%

---


# UV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-icon.png){width="200px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据提供的&#x200B;**蒙版**&#x200B;图像输入，对&#x200B;**源**&#x200B;图像输入中的UV坐标应用漫射处理，并在&#x200B;**源**&#x200B;的值之间插入坐标。

只有来自与蒙版匹配的像素的UV会扩散；其他像素不会参与结果。

请注意，拼贴处理方式特殊：当拼贴为&#x200B;*已启用*（默认情况下处于启用状态）时，相邻坐标的平均值可以超过0/1限制。

例如，如果U坐标值在一个像素上为0.1，在另一个像素上为0.8，则平均值将是0.95而不是0.45，因为假定坐标的&#x200B;*拼贴*。 这与实际像素位置无关：坐标值在整个图像上的处理方式相同。

使用此滤镜处理&#x200B;*纹理变形*&#x200B;时，这可能导致不良结果。 如果发生这种情况，请确保您的蒙版定义的“控制曲线/点”的纹理长度间隔不超过&#x200B;*一半*。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>源</b> <i>颜色</i> | UV扩散。 请注意，在此筛选器中以特殊方式处理拼贴（请参阅<i>描述</i>）。 |
| <b>蒙版</b> <i>灰度</i> | 漫射蒙版：白色像素在<i>源</i>中取样，并以黑色像素扩散。 图像应该是黑白的。 如果蒙版包含渐变，则截止值为0.5。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>迭代</b> <i>0.0 - 64.0</i> | 要执行的迭代数（越高越好，但速度越慢）。 有用的值在[8， 48]范围内。<br>请注意，如果您不寻找数学正确性，则低值会很合适，甚至更好。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/diffusion-uv-01a-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/diffusion-uv-01a-after.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/diffusion-uv-01b-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/diffusion-uv-01b-after.jpg" />
        </td>
    </tr>
</table>
