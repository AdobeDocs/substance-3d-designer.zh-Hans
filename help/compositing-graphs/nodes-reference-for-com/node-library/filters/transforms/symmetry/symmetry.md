---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry.html"
breadcrumb-title: ''
description: 使用对称节点通过沿指定轴镜像纹理来创建对称阵列。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 对称
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 7%

---


# 对称

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](symmetry.resources/symmetry-01.png){width="128px"}

<b>英寸：</b>筛选器>变换

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

对输入图像执行各种对称操作。 可用于使几何形状对称。

此节点与[镜像](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md)非常相似，但具有对混合模式的额外控制。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>对称模式</b> <i>镜像Y，镜像X，左对角，右对角，镜像X/Y，镜像X /镜像Y，左对角/右对角，右对角/左对角，8</i> | 选择对称几何模式。 |
| <b>传输模式</b> <i>0 - 6</i> | 选择对称混合模式：复制、添加、去除、正片叠底、添加子集、最大值、最小值。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="symmetry.resources/symmetry-02.png" />
        </td>
    </tr>
</table>
