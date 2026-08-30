---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/bottom-to-top.html"
breadcrumb-title: ''
description: 使用“自下而上”节点，根据网格世界位置从下至上生成渐变蒙版。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Bottom To Top
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 从下到上
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 5%

---


# 从下到上

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](bottom-to-top.resources/bottom-to-top.png){width="128px"}

<b>在</b>中基于网格的生成器>蒙版生成器

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

根据已烘焙贴图和用户设置生成黑白蒙版。 类似于[Painter](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-painter/using/home)中的[智能蒙版](https://experienceleague.adobe.com/zh-hans/docs/substance-3d-painter/using/features/smart-materials-and-masks)。

这将生成从模型底部到顶部的白色到黑色的过渡，对于进行基于几何的衰减和选择非常有用。

</td>
</tr>
</table>

<a name="inputs"></a>

## 输入

|  |  |
|:---|:---|
| <b>位置</b> <i>颜色输入</i> | 烘焙位置映射。 必填！ |
| <b>粗糙度</b> <i>灰度输入</i> | 这与PBR粗糙度无关，而是用于分解过渡的（可选）变体映射。 仅在粗糙度设置为大于0时显示。 |
| <b>蒙版（可选）</b> <i>灰度输入</i> | 用于遮盖节点效果的遮罩槽。 |

<a name="parameters"></a>

## 参数

|  |  |
|:---|:---|
| <b>级别</b> <i>0.0 - 1.0</i> | 在黑白图像之间移动结果的平均色阶，就像亮度调整一样。 |
| <b>对比度</b> <i>0.0 - 1.0</i> | 调整过渡的对比度。 |
| <b>粗糙度_变量</b> <i>0.0 - 1.0</i> | 确定用于混合变化的粗糙度映射的数量。 将此值增大到0以上可显示映射槽。 |

## 示例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="bottom-to-top.resources/bottom-to-top-ex.gif" />
        </td>
    </tr>
</table>
