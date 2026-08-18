---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-uv.html"
breadcrumb-title: ''
description: 使用“扩散UV”节点在UV空间中应用扩散效果，以创建平滑的颜色过渡和混合。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion UV
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 扩散UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 1%

---


# 扩散UV

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-icon.png){width="200px"}

**范围：** *滤镜/效果*

**中级**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 描述

根据提供的&#x200B;**蒙版**&#x200B;图像输入，对&#x200B;**源**&#x200B;图像输入中的UV坐标应用扩散过程，并在&#x200B;**源**&#x200B;的值之间插入坐标。

只有来自与蒙版匹配的像素的UV会扩散；其他像素不会参与结果。

请注意，拼贴处理方式特殊：当拼贴处于&#x200B;*启用*&#x200B;状态（默认情况下是这种情况）时，相邻坐标的平均值可以超过0/1限制。

例如，如果U坐标值在一个像素上为0.1，在另一个像素上为0.8，则平均值将是0.95而不是0.45，因为假设了&#x200B;*坐标拼贴*。 这与实际像素位置无关：坐标值在整个图像上的处理方式相同。

使用此滤镜处理&#x200B;*纹理变形*&#x200B;时，这可能会导致不希望出现的结果。 如果发生这种情况，请确保蒙版定义的“控制曲线/点”的间距不超过&#x200B;*半个纹理*。

</td>
</tr>
</table>

## 参数

* **迭代**： *0.0 - 64.0*&#x200B;要执行的扩散迭代次数（越高越好，但速度越慢）。 有用的值在[8， 48]范围内。\
  请注意，如果您不寻求数学正确性，则低值会更优秀。

## 输入

* **源** *颜色*\
  UV扩散。 请注意，在此筛选器中以特殊方式处理拼贴（请参阅&#x200B;*描述*）。
* **蒙版***灰度*&#x200B;扩散蒙版：白色像素在&#x200B;*源*&#x200B;中取样，并以黑色像素扩散。 图像应该是黑白的。 如果蒙版包含渐变，则截止值为0.5。

## 示例图像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01a-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01a-after.jpg){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01b-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01b-after.jpg){width="256px"}

</td>
</tr>
</table>
