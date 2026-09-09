---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-grayscale.html"
breadcrumb-title: ''
description: 使用“漫射灰度”节点可应用灰度漫射效果，以创建平滑的颜色过渡和混合。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 漫射灰度
user-guide-description: ''
user-guide-title: ''
source-git-commit: 07f136ebd89fbe737b6c042f1275bd348b2be514
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 3%

---


# 漫射灰度

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](diffusion-grayscale.resources/diffusion-grayscale-icon.png){width="200px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据提供的&#x200B;**蒙版**&#x200B;图像输入，将漫射过程应用于&#x200B;**源**&#x200B;图像输入中的值，在值之间创建平滑渐变。

只有来自与蒙版匹配的像素的值会被扩散；其他像素不会参与结果。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>源</b> <i>灰度</i> | 要扩散的图像。 |
| <b>蒙版</b> <i>灰度</i> | 漫射蒙版：白色像素在<i>源</i>中取样，并以黑色像素扩散。 图像应该是黑白的。 如果蒙版包含渐变，则截止值为0.5。 |
| <b>强度</b> <i>灰度</i> | 在本地定义漫射过程应用的强度。 此地图应该为<i>对比图</i>，才能产生显着的效果。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>迭代</b> <i>0.0 - 64.0</i> | 要执行的迭代数（越高越好，但速度越慢）。 有用的值在[8， 48]范围内。<br>请注意，如果您不寻找数学正确性，则低值会很合适，甚至更好。 |
| <b>距离</b> <i>0.0 - 1.0</i> | 调整漫射的最大距离。 |
| <b>启用仿色</b> <i>True/False</i> | 控制每个通道的采样方法。 抖动允许以较少的次数收敛，但会引入杂色。<br>如果没有它，则每个刀路的速度会更快，但需要更多的刀路才能获得平滑的结果，而不会出现带状伪影。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-01-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-01a-after.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-01b-after.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-02-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-02-after.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-02-render.jpg" />
        </td>
    </tr>
</table>
