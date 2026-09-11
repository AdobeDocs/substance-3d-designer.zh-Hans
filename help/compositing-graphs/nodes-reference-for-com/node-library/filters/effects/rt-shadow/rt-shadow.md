---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-shadow.html"
breadcrumb-title: ''
description: 使用“RT阴影”节点计算来自几何的实时阴影信息，以创建动态光照效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Shadows
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: RT阴影
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# RT阴影

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![RT阴影节点图标](rt-shadow.resources/rt-shadow.png "RT阴影节点图标")

<b>英寸：</b>滤镜>效果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

从高度图输入生成光线跟踪阴影。

由于计算时间，不应将此节点与CPU (SSE)引擎结合使用。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>示例</b> <i>整数</i> | 用于计算阴影的光线数。<br>较高的值可提供更平滑和更精确的结果，但会降低性能。 |
| <b>模式</b> <i>整数</i> | 在曲面上绘制阴影的方法。 |
| <b>Height比例</b> <i>Float</i> | 输入高度图强度的乘数。 |
| <b>光源位置</b> <i>Float2</i> | 围绕曲面的球面上的光源位置： <br><br>- <b>X</b>：水平位置，按匝数排列；<br>- <b>Y</b>：垂直位置，其中0.5为顶点，0/1为地平线。 |
| <b>光照强度</b> <i>Float</i> | 光源的强度。 |
| <b>光源大小</b> <i>Float2</i> | （在<b>模式</b>设置为<i>底纹</i>时可用）矩形光源的大小。 |
| <b>光度（柔和阴影）</b> <i>Float</i> | <b>光线大小</b>对光线方向的贡献的乘数。<br>值越大，阴影越平滑。 |
| <b>保持光照在水平线之上</b> <i>布尔值</i> | 如果<b>光照位置</b>的设置方式将光线放置在地平线以下，则此参数可防止光线越过该阈值，这意味着Y值会被固定在[0；1]范围内。 |
| <b>阴影不透明度</b> <i>Float</i> | 在表面上绘制的阴影不透明度的乘数。 |
| <b>阴影衰减</b> <i>Float</i> | 一个乘数，用来衰减阴影离主光栅越远的部分。<br>值为0时产生均匀的阴影（仍然应用柔和的阴影）。 |
| <b>最大阴影长度</b> <i>Float</i> | 阴影可从其光栅绘制的最大距离。<br>值为0时不会产生明显的阴影。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/RTShadows-01.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/RTShadows-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/RTShadows-03.jpg" />
        </td>
    </tr>
</table>
