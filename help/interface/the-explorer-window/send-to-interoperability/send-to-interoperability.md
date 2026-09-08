---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-explorer-window/send-to-interoperability.html"
breadcrumb-title: ''
description: 使用Substance 3D Designer中的发送到互操作性功能将材料导出到其他应用程序。
helpx_creative_field: ""
helpx_description: Designer > Interface > The Explorer window > Send to...  Interoperability
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 发送至...  互用性
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 1%

---


# 发送至...  互用性

![从Designer发送到Substance 3D应用程序](../../../assets/explorer-interop.png "从Designer发送到Substance 3D应用程序"){width="512px"}

Adobe Substance 3D Designer与[Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html)、[Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html)和[Substance 3D Stager](https://www.adobe.com/products/substance3d-stager.html)具有互操作性。 它允许您&#x200B;*发送*&#x200B;和&#x200B;*重新发送*&#x200B;您快速工作，从而促进整个Substance 3D生态系统的迭代。

工作流程通常如下：

1. 在[Substance图形的属性](../../../compositing-graphs/graph-parameters/graph-parameters.md)中设置<b>类型</b>属性
1. 在[资源管理器](../the-explorer-window.md)面板中，选择要发送的包
1. 在资源管理器的<b>Publish/发送</b>下拉列表中，选择目标应用程序
1. 对图表进行更改
1. 重复步骤3以重新发送包，并用您所做的更改更新现有已发送的资源

>[!WARNING]
>
> 在<b>Steam</b>版本中，互操作性功能&#x200B;*不*&#x200B;可用。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 设置图形类型

Substance图可以具有多种功能。 您必须预先定义图表的确切功能，以确保可以正确地发送图表。

在[图形属性](../../../compositing-graphs/graph-parameters/graph-parameters.md)的<b>属性</b>部分，有一个<b>类型</b>选项，下拉菜单具有以下选项：

</td>
<td style="border: 0;" valign="top">

![Substance图形的类型属性](../../../assets/type-attribute.jpg "Substance图形的类型属性")

</td>
</tr>
</table>

* 如果尚未设置，**Unspecified**&#x200B;是默认类型。 根据您发送给哪个应用程序，可能会以不同的方式对其进行解释。 例如，[Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html)将默认为材料；
* **标准材质**&#x200B;用于多通道PBR材质，带有正确标记的[输出](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)；
* **贴花材料**&#x200B;用于具有Alpha 通道的多通道PBR材料，将应用为[Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html)或[Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html)中的贴花；
* **贴图集素材**&#x200B;用于由多个贴图集图像组成的多通道PBR素材，可在Designer中的[Atlas Scatter节点](../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/atlas-scatter/atlas-scatter.md)或[Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html)中使用；
* **筛选器**&#x200B;用于通用筛选器，两者均用于[Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html)或[Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html)；
* **基于网格的生成器**&#x200B;用于多输入蒙版生成器。 此仅由[Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html)使用；
* **纹理生成器**&#x200B;用于单通道地图，如2D过程和噪声；
* **环境光**&#x200B;用于单通道光照环境，用于照亮场景和对象；
* **光照纹理**&#x200B;用于应用于物理光线的单个通道纹理。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## “发送到”菜单

发送过程涉及在幕后[将](../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)一个或多个包发布到Substance 3D资源文件(SBSAR)。

发送内容可通过以下方式执行：

* 右键单击包并打开上下文菜单中的<b>发送到……</b>子菜单，然后为目标应用程序选择<b>发送到……</b>选项；
* 单击“资源管理器”面板顶部的![](../../../assets/sendto-icon.jpg)<b>“Publish/发送”</b>按钮，然后为目标应用程序选择<b>“发送至……”</b>选项。

</td>
<td style="border: 0;" valign="top">

![资源管理器中的Publish/发送到菜单](../../../assets/explorer-sendto-displayed.jpg "资源管理器中的Publish/发送到菜单")

</td>
</tr>
</table>

### 重新发送

再次发送&#x200B;*已发送一次*&#x200B;的包到&#x200B;*同一目标*&#x200B;应用程序时，将在目标应用程序中使用新版本&#x200B;*更新资源*。

## 发送至 Player

[Substance Player](https://helpx.adobe.com/substance-3d-player/home.html)同时支持&#x200B;*3} <b>Substance 3D文件</b> (SBS)和<b>Substance 3D资源</b> (SBSAR)。*

若要发送到Player，Substance Player可执行文件需要由用户&#x200B;*手动定位*，此操作可以完成：

* 如果播放器在安装Designer后&#x200B;*从未找到*，系统提示此消息；
* 随时在<b>工具</b>菜单中，使用<b>Substance Player>查找……</b>选项。

在Player中，从Designer接收要求用户手动找到Substance 3D Designer *安装目录*，具体操作如下：

* 当系统提示自安装Player以来&#x200B;*从未找到Designer*&#x200B;时；
* 随时在<b>选项</b>菜单中，使用<b>查找Adobe Substance 3D Designer</b>选项。

>[!NOTE]
>
> 将Substance 3D文件(SBS)发送到Player时，会将Substance 3D资源(SBSAR)发布为&#x200B;*临时文件*。

## 问题

发送包时可能会遇到错误，例如：

```
Error sending package to Substance 3D Painter. Check the console for details. SBSAR export failed.
```


这通常是因为标准错误和警告所致，请修复它们来解决此问题：

* 您的图中未定义[输出](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)节点。 添加输出节点并连接一些节点；
* [函数图形](../../../function-graphs/function-graphs.md)中的[获取节点](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)中缺少变量或变量已损坏。 在受影响的节点上按&#x200B;*黄色警告徽章*&#x200B;跟踪它们。
