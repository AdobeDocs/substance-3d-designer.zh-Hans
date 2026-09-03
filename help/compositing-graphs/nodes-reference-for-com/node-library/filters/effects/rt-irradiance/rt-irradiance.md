---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-irradiance.html"
breadcrumb-title: ''
description: 使用“RT辐照度”节点从几何计算实时辐照度信息，以进行真实光照计算。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Irradiance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: RT辐照度
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 4%

---


# RT辐照度

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](rt-irradiance.resources/rt-irradiance-01.png){width="128px"}

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

在从环境图和emissive图生成的高度图输入上生成光线跟踪照度。 可用于将光照“烘焙”到图形内的纹理中。 用于模拟全局照明和光晕。由于计算时间的原因，不应将此节点与CPU (SSE)引擎结合使用。 返回两个映射：一个是“辐照度”输出，其中辐照度应用于材料输入；一个是仅包含计算出的辐照度值的原始辐照度映射。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>Height</b> <i>灰度输入</i> | Height是材料插槽中唯一需要的输入。 没有它，节点将无法正常工作。 |
| <b>具发射性</b> <i>颜色输入</i> | emissive应采用纯黑色不发光、任何其他彩色值都发光的格式。 Alpha将被忽略。 需要连接到此插槽或环境插槽才能看到任何结果。 |
| <b>环境</b> <i>颜色输入</i> | 使用HDR光照环境计算辐照度。 需要连接到此插槽或Emissive插槽才能看到任何结果。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>Height比例</b> <i>0.0 - 1.0</i> | 缩放以解释Height。 影响整个场景外观。 |
| <b>质量</b> <i>32光线，64光线，128光线</i> | 决定结果质量，但也影响性能。 光线越少，噪声越大。 |
| <b>计算回弹</b> <i>False/True</i> | 切换弹跳计算。 影响质量和速度。 |
| <b>环境轮换</b> <i>0.0 - 1.0</i> | 围绕旋转环境。 |
| <b>环境曝光(EV)</b> <i>-4.0 - 4.0</i> | 要用于环境的曝光度值，会影响效果的总亮度。 |
| <b>发射强度</b> <i>0.0 - 20.0</i> | 发射输入的乘数影响来自发射体的辐射强度。 |
| <b>Emissive色彩空间</b> <i>sRGB，线性</i> | 用于解释敏感输入的色彩空间。 |
| <b>原始照度Alpha中的IBL阴影</b> <i>False/True</i> | 切换是否向照片中添加阴影 |
| <b>EmissiveLOD偏差</b> <i>-1.0 - 1.0</i> | 调整emissive辐照度的质量。 值越低，噪音越大。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irradiance-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irradiance-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irradiance-04.jpg" />
        </td>
    </tr>
</table>
