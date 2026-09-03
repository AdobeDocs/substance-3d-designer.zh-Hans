---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/non-uniform-blur.html"
breadcrumb-title: ''
description: 使用非均匀模糊节点在X和Y方向应用不同强度的模糊以用于各向异性效果。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Non Uniform Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 非均匀模糊
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 9%

---


# 非均匀模糊

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](non-uniform-blur.resources/non-uniform-blur-01.png){width="128px"}

![](non-uniform-blur.resources/non-uniform-blur-02.png){width="128px"}

<b>英寸：</b>滤镜>模糊

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

执行“高品质模糊”，其中强度由输入蒙版驱动。 允许添加“各向异性”和“不对称”选项。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>模糊映射</b> <i>灰度输入</i> | 用于驱动效果强度的蒙版映射。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>强度</b> <i>0.0 - 50.0</i> | 应用模糊的最大强度。 模糊映射遮盖，因此此设置对该映射的黑色区域无效。 |
| <b>各向异性</b> <i>0.0 - 1.0</i> | （可选）向模糊效果添加方向性。 由“角度”参数驱动。 |
| <b>不对称</b> <i>0.0 - 1.0</i> | 可选地向采样添加偏置。 由“角度”参数驱动。 |
| <b>角度</b> <i>0.0 - 1.0</i> | 用于设置方向性和采样偏置的角度。 |
| <b>示例</b> <i>1 - 16</i> | 样本量，决定质量。 乘以刀片数量。 |
| <b>刀片</b> <i>1 - 9</i> | 采样扇区的数量，决定质量。 乘以样本量。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="non-uniform-blur.resources/non-uniform-blur-03.gif" /><br><i>以下示例由“模糊映射”槽中的渐变渐变（90度）驱动。</i>
        </td>
    </tr>
</table>
