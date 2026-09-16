---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/transformation-2d.html"
breadcrumb-title: ""
description: 使用变换 2D节点可将2D变换应用于纹理，包括平移、旋转和缩放。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Transformation 2D
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 2D 变形
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 5%
---

# 2D 变形

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![原子节点：变换 2D](transformation-2d.resources/comp_transformation_1.png "原子节点：变换 2D"){width="100%"}

<b>进入：</b>个原子节点

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

将 2D 变换矩阵应用于图像：平移、旋转、缩放、对称和剪切。

这非常类似于Photoshop中的变换(Ctrl-T)或使用Substance 3D Painter中的2D映射操纵器。

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="transformation-2d.resources/transformation2d-tooltip.gif" alt="transformation-2d工具提示" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>

这是一个非常有用且应用广泛的节点，它可以增加拼贴、去除拼贴、将图像放置在特定位置、拉伸或挤压输入等。

但是，它不能完美匹配某些应用，因此以下节点可能值得关注： [安全变换](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/safe-transform/safe-transform.md)、[非方形变换](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/non-square-transform/non-square-transform.md)、[四次变换](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/quad-transform/quad-transform.md)和[梯形变换](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/trapezoid-transform/trapezoid-transform.md)。


>[!TIP]
>
> 正在禁用拼贴
> 
> 将“拼贴模式”[基本参数](../../../../glossary/glossary.md)的[继承方法](../../../../glossary/glossary.md)设置为“绝对”，然后允许您将参数值设置为“无拼贴”：
> 
> ![](transformation-2d.resources/tilingmode.png)

>[!NOTE]
>
> 节点属性中缩放和旋转的值相对于当前变换&#x200B;*为*，在单击“应用”按钮之前，不会应用于2D 视图。


## 参数

|  |  |
| --- | --- |
| <b>变换矩阵</b> *Float4* | 打开基础转换矩阵以直接编辑。 允许您更改旋转和缩放。 也可以通过2D 视图中的线框进行调整。   警告：它们不直接与视图相关，而是可在步骤中应用的相对调整。 |
| <b>偏移</b> *Float2* | 定义图像的二维位移。 用于更改位置或偏移还可以通过2D 视图中的线框进行调整。   与2D 视图输出直接相关。 |
| <b>镜像转换模式</b> *整数* | 允许您切换到手动[镜像转换](../../../../glossary/glossary.md)级别，这将使用纹理筛选减少图像中的伪影。 |
| <b>多级渐远纹理级别</b> *整数* | 设置要使用的[镜像转换](../../../../glossary/glossary.md)级别。     *当“镜像转换模式”设置为“手动”时可用* |
| <b>遮罩颜色</b> *Float4* | 禁用变换拼贴时用作背景的颜色。 即，设置当变换的输入不覆盖输出的区域时使用的颜色。   如果使用的是RGBA颜色，则可以使其透明。 |
| <b>筛选</b> *整数* | 设置使用的缩减像素采样方法。 当多级渐远纹理级别减少时，效果并不特别好。 |

## 输入连接器

|  |  |
| --- | --- |
| <b>输入</b> *灰度/颜色*&#x200B;主要 | 要变换的图像。 |


## 示例

*即将推出。*
