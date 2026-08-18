---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/iray.html"
breadcrumb-title: ''
description: 在Substance 3D Designer 3D视图中使用光线渲染器，以实现基于物理的材质预览和逼真的光照效果。
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > Iray
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Iray
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '2159'
ht-degree: 1%

---


# Iray

本页介绍了[Substance 3D Designer](https://www.adobe.com/cn/products/substance3d-designer.html)的3D视图面板中提供的Iray渲染器，该渲染器提供了交互式路径跟踪，可使用CPU和/或GPU加速（仅限Nvidia GPU）进行逼真的渲染。

>[!WARNING]
> 
> Iray渲染器和所有相关功能已从Designer 16.0.0版中移除。
> 
> 在此处了解详情： [MDL图表和Iray生命周期结束](../../../technical-issues/mdl-graph-iray-eol/mdl-graph-iray-eol.md)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 概述

<b>Iray</b>是一种高度&#x200B;*交互式*&#x200B;且基于物理的直观渲染技术，它通过模拟光线和材料的物理行为来生成&#x200B;*逼真的图像*。 在[Nvidia Iray](https://www.nvidia.com/en-us/design-visualization/iray/)网页上了解更多信息。

</td>
<td style="border: 0;" valign="top">

[![NVIDIA Iray徽标](../../../assets/iray-logo.jpg)](https://www.nvidia.com/en-us/design-visualization/iray/)

</td>
</tr>

<tr style="border: 0;">
<td style="border: 0;" valign="top">

由于3D视图使用Iray的&#x200B;*逐行渲染器*，因此只要对每个像素执行了至少一个样本，就会生成图像。 在执行采样迭代时，图像会&#x200B;*自动更新*，从而使初始粗糙图像在每次迭代时变得&#x200B;*更清晰*。

渲染器在[3D视图](../../../interface/3d-view/3d-view.md)面板中可用：打开<b>渲染器</b>菜单，然后选择<b>Iray</b>选项以将该3D视图面板中使用的渲染器切换为Iray。\
切换到Iray渲染器&#x200B;*会更改某些3D视图菜单中的可用选项*。 这些更改将在下面的<b>3D视图</b>部分中说明。

默认情况下，一旦选择了光线渲染器，即会开始渐进式渲染。 渲染进程将一直运行，直到满足下列条件中的&#x200B;*一个*：

* 执行的最大样本数&#x200B;**
* 符合&#x200B;*渲染时间限制*

请参阅此页面的<b>渲染器</b>部分，了解有关调整这些条件的更多信息。

</td>
<td style="border: 0;" valign="top">

![使用Iray渲染的中世纪城堡墙材料](../../../assets/iray-overview.png "使用Iray渲染的中世纪城堡墙材料")

*材质：[中世纪城堡](https://helpx.adobe.com/substance-3d/unlisted/assets/allassets/2b3f6eca9a6b6ab19d263d8b77819df431c3c973.html)**，作者[Mark Foreman](https://www.artstation.com/oggyart)**，可在我们的[Substance 3D资源](https://helpx.adobe.com/substance-3d/unlisted/assets.html)**库*&#x200B;中使用

</td>
</tr>
</table>

>[!WARNING]
>
> 任何时间只能运行&#x200B;*一个* Iray渲染实例。\
> 这意味着当3D视图面板使用此渲染器时，**渲染器**&#x200B;菜单在其他3D视图面板中&#x200B;*处于禁用状态*，并且这些菜单默认为&#x200B;**OpenGL**&#x200B;渲染器。

## 3D视图选项

<a name="scene"></a>

### 场景

在<b>场景</b>菜单中选择<b>编辑</b>选项，以在<b>属性</b>面板中查找特定于Iray的场景属性。

* <b>已启用：</b>当设置为&#x200B;*False*&#x200B;时，将隐藏该对象，并且&#x200B;*不再向场景提供*

显示组件

* <b>可见</b>：设置为&#x200B;*False*&#x200B;时，对象处于隐藏状态，但&#x200B;*仍对场景有贡献*，即反射光线、吸收光线和投影阴影

网格显示组件

* 细分
  * <b>方法</b>：用于在程序上将网格细分为更精细的几何形状的方法
    * *无*：未应用细分
    * *参数*：将网格细分为`4^x`个三角形，其中`x`是此参数指定的值
    * *长度*：细分网格，直到所有边缘的长度（在对象空间中）都小于“最小长度”参数指定的值
  * <b>最小长度</b>：细分网格，直到所有边的长度都低于对象空间中的此指定值（仅适用于&#x200B;*Length*&#x200B;方法）
  * <b>数字</b>：应该应用于网格的细分迭代次数（仅适用于&#x200B;*参数*&#x200B;方法）

>[!WARNING]
>
> 在渲染之前和期间，细分网格&#x200B;*会以指数方式增加其处理时间*。 我们建议在输入值时保持&#x200B;*保守*。\
> 请注意在Parameter方法中使用&#x200B;*高* **数字**&#x200B;值，在Length方法中使用&#x200B;*低* **最小长度**&#x200B;值。

![场景选项](../../../assets/iray-scene-subdivision.gif "场景选项")

<a name="materials"></a>

### 材质

由于Iray依赖于NVIDIA开发的[MDL着色模型](https://www.nvidia.com/en-us/design-visualization/technologies/material-definition-language/)，因此可用于场景素材的素材将替换为Designer加载的MDL库。 此库使用以下源生成：

* Designer安装中包含的MDL文件
* 在加载的[项目文件](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)中由用户](../../../interface/preferences-window/project-settings/project-settings.md)列出的[目录中找到了MDL文件
* [NVIDIA vMaterials](https://developer.nvidia.com/vmaterials)库（如果已安装）

>[!NOTE]
>
> 要更深入地了解MDL着色模型，请查看由NVIDIA编写和维护的[MDL手册](http://mdlhandbook.com/)。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

加载的MDL素材的累积列表位于<b>素材</b>菜单下，任何列出的素材子菜单下，如右侧的图像所示。

此外，如果在Designer中加载了[MDL图形](../../../mdl-graphs/creating-an-mdl-graph/creating-an-mdl-graph.md)，则它可以应用于场景中的任何材质。 此时，它将被添加到可用的MDL材料列表中。

此菜单中的其他重要选项包括：

* 选择<b>编辑</b>选项以访问<b>属性</b>面板中MDL的&#x200B;*公开输入*，并根据需要调整素材
* 使用<b>加载……</b>选项，您可以&#x200B;*手动加载任何MDL文件*，这些文件将添加到累积列表中并应用于场景
* <b>导出预设……</b>选项可打开<b>导出MDL材质预设</b>对话框，使用此对话框可使用3D视图中应用的当前设置导出预设MDL文件

</td>
<td style="border: 0;" valign="top">

![材质菜单](../../../assets/iray-mdl-list.png "材质菜单")

</td>
</tr>
</table>

>[!NOTE]
>
> 加载&#x200B;**MDL图形**&#x200B;时，3D视图渲染器将&#x200B;*自动切换到&#x200B;**Iray***以加载并应用它。

<a name="camera"></a>

### 相机

关于相机设置，OpenGL和Iray之间的主要区别在于如何管理&#x200B;*字段深度*。 实际上，Iray作为物理上精确的渲染器，视相机的&#x200B;*光圈*&#x200B;而定，场地深度会“自然”发生。

选择“光线渲染器”后，摄像机属性中会显示下列参数：

* <b>焦距</b>：离焦点的相机的距离 — 即图像最清晰的地方
* <b>光圈直径</b>：驱动相机光圈的值。 此值越低，图像元素在焦点之前和之后就越锐利 — 用更简单的术语来说，此值控制场效果深度的强度

![相机设置](../../../assets/camera-dof.png "相机设置")

<a name="environment"></a>

### 环境

打开<b>环境</b>菜单并选择<b>编辑</b>选项，以在<b>属性</b>面板中显示环境属性。

可使用以下属性：

圆顶

* <b>圆顶类型</b>：设置场景周围的对象，环境纹理投影在该对象上
  * *无限球体*：无限球形环境
  * *地面*：无限球形环境，但具有纹理地面
  * *球形*：自定义半径的有限大小的球形圆顶
  * *带地面的球体*：具有自定义半径的有限大小的球状穹顶，其中环境下半部分投影到分割球体上部和下部的平面上
  * *带地面的方框*：自定义宽度、Height和长度的有限大小的方框状穹顶，其中环境下半部分投影到分割方框上下部分的平面上
* <b>旋转角度</b>：控制圆盖绕&#x200B;*Y轴*&#x200B;旋转的角度
* <b>半径</b>：球体的半径（仅适用于&#x200B;*球体*&#x200B;和&#x200B;*具有地面*&#x200B;圆顶类型的球体）
* <b>宽度</b>：方框的宽度（仅适用于具有地面&#x200B;*圆盖类型的*&#x200B;方框）
* <b>Height</b>：方框的Height（仅适用于具有地面&#x200B;*圆盖类型的*&#x200B;方框）
* <b>长度</b>：框的长度（仅适用于具有地面&#x200B;*圆盖类型的*&#x200B;框）
* <b>可视化</b>：启用有限大小环境几何的假颜色叠加。 这可用于将几何与拍摄的环境映射的投影对齐（仅适用于&#x200B;*球体*、*具有地面的球体*&#x200B;和&#x200B;*具有地面*&#x200B;穹顶类型的方框）

>[!NOTE]
>
> 对于有限大小的圆顶，所有场景几何都应被&#x200B;*圈在*&#x200B;圆顶内。

圆顶地面\
以下参数适用于&#x200B;*地面*、*有地面的球体*&#x200B;和&#x200B;*有地面的方框*&#x200B;穹顶类型：

* **地面**：启用地平面
* **位置**：有限圆盖原点的位置（也适用于&#x200B;*球体*&#x200B;圆盖类型）
* **反射率**：地面反射的不透明度和色调，其中黑色表示反射不可见
* **光泽**：地面反射的光泽
* **阴影强度**：投射在地面上的阴影的不透明度
* **纹理缩放**：控制地面上环境纹理投影的大小（也适用于&#x200B;*球体*&#x200B;圆顶类型）

其中一些设置的影响说明如下：

+++显示环境


<table>
  <tr>
    <td>
      <img src="../../../assets/iray-environment-hidden.png" alt="图像 — 环境隐藏">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../assets/iray-env-visible.png" alt="图像 — 环境可见">
      <br><i>之后</i>
    </td>
  </tr>
</table>



![Iray — 环境已隐藏](../../../assets/iray-environment-hidden.png "Iray — 环境已隐藏")

![Iray — 环境可见](../../../assets/iray-env-visible.png "Iray — 环境可见")

+++

+++启用地平面


<table>
  <tr>
    <td>
      <img src="../../../assets/iray-env-infinite-sphere.png" alt="射线 — 仅限无限球体">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../assets/iray-env-sphere-ground.png" alt="Iray — 带地平面的无限球体">
      <br><i>之后</i>
    </td>
  </tr>
</table>



![Iray — 仅限无限球体](../../../assets/iray-env-infinite-sphere.png "Iray — 仅限无限球体")

![Iray — 具有地平面的无限球体](../../../assets/iray-env-sphere-ground.png "Iray — 具有地平面的无限球体")

+++

+++旋转环境
![旋转环境](../../../assets/iray-env-rotation.gif "旋转环境")



+++

+++调整地平面
![地面反射](../../../assets/iray-env-ground-options.gif "地面反射")



+++

+++调整无限球体
![环境缩放（球体）](../../../assets/iray-env-sphere-radius.gif "环境缩放（球体）")



+++

+++调整封闭框
![环境缩放（多维数据集）](../../../assets/iray-env-box-dimensions.gif "环境缩放（多维数据集）")



+++

<a name="display"></a>

### 显示

这些选项在渲染的图像顶部显示&#x200B;*文本叠加*，其中包含有关渲染的有用信息。

* <b>已用时间</b>：渲染的持续时间（秒）。 满足任一结束条件时，此计时器和渲染进程都将停止
* <b>迭代</b>：执行的采样迭代数。 当满足任一结束条件时，此计数器和渲染进程都将停止
* <b>渲染方法</b>：使用的渲染路径。 在本地计算机上的大多数用途是使用Photoreal
* <b>分辨率</b>：有效的渲染分辨率。 如果相机属性中的“使用窗口分辨率”选项设置为“假”，则会自动调整图像的比例以匹配分辨率比率
* <b>场景统计信息</b>：与渲染场景相关的统计信息列表，其中包括三角形计数和材质计数以及其他数据

![显示选项](../../../assets/iray-display-data.png "显示选项"){width="512px"}

<a name="renderer"></a>

### 渲染器

打开<b>渲染器</b>菜单并选择<b>编辑</b>选项，以在<b>属性</b>面板中显示渲染器属性。

渐进渲染

* <b>最小采样数</b>：在考虑停止逐行渲染的条件之前，要计算的每个像素的最小采样数
* <b>最大采样数</b>：如果已经渲染了每个像素的此样本数，则自动停止逐行渲染
* <b>最大时间（秒）</b>：渐进渲染应在秒后自动终止
* <b>已启用焦散取样器</b>：通过专用焦散取样器增加默认取样器。 焦散线是光线穿过不透明对象的结果，因此仅当将支持半透明的[MDL](../../../mdl-graphs/creating-an-mdl-graph/creating-an-mdl-graph.md)材质应用于场景中的任何对象时才需要
* <b>已启用Firefly滤镜</b>：启用萤火虫滤镜，该滤镜使用预定义的算法，在渲染过程中移除计算图像中的萤火虫。 Firefly是视觉伪影，图像中的&#x200B;*孤立像素*&#x200B;比其相邻像素明显亮&#x200B;**，并且是光线样本不足，无法准确确定光线分布的结果
* 帖子降噪器\
  Iray渲染器使用[NVIDIA Optix AI-Accelerated Denoiser](https://developer.nvidia.com/optix-denoiser)算法对正在渲染的图像进行迭代的高质量去噪。

  * <b>已启用</b>：使预定义的&#x200B;*降噪算法*&#x200B;能够在设置的渲染迭代中触发，并在渲染的&#x200B;*结束*&#x200B;之前处于活动状态
  * <b>开始迭代</b>：如果启用降噪器，则此选项设置降噪过程开始时的迭代。 这可以防止降噪器的性能开销影响交互性，例如，在移动摄像机时。 此外，由于迭代收敛性不强，前几代迭代往往不适合作为降噪器的输入，导致结果不理想。

以下图像比较演示了其中一些设置的影响：

+++焦散取样器


<table>
  <tr>
    <td>
      <img src="../../../assets/iray-renderer-none.png" alt="图像 — 基本渲染">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../assets/iray-renderer-caustics.png" alt="Iray — 已启用焦散取样器">
      <br><i>之后</i>
    </td>
  </tr>
</table>



![Iray — 基本渲染](../../../assets/iray-renderer-none.png "Iray — 基本渲染")

![Iray — 焦散取样器已启用](../../../assets/iray-renderer-caustics.png "Iray — 焦散取样器已启用")

+++

+++Firefly过滤器


<table>
  <tr>
    <td>
      <img src="../../../assets/iray-renderer-caustics.png" alt="图像 — Firefly滤镜已禁用">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../assets/iray-renderer-caustics-fireflies.png" alt="Iray — 已启用Firefly滤镜">
      <br><i>之后</i>
    </td>
  </tr>
</table>



![Iray -Firefly滤镜已禁用](../../../assets/iray-renderer-caustics.png "Iray -Firefly滤镜已禁用")

![Iray — 已启用Firefly滤镜](../../../assets/iray-renderer-caustics-fireflies.png "Iray — 已启用Firefly滤镜")

+++

+++后降噪器


<table>
  <tr>
    <td>
      <img src="../../../assets/iray-renderer-caustics-fireflies.png" alt="Iray — 禁用降噪后功能">
      <br><i>之前</i>
    </td>
    <td>
      <img src="../../../assets/iray-renderer-caustics-fireflies-denoiser-180.png" alt="Iray — 启用降噪后功能">
      <br><i>之后</i>
    </td>
  </tr>
</table>



![Iray — 后降噪器已禁用](../../../assets/iray-renderer-caustics-fireflies.png "Iray — 后降噪器已禁用")

![Iray — 启用后降噪器](../../../assets/iray-renderer-caustics-fireflies-denoiser-180.png "Iray — 启用后降噪器")

+++

*材质：厚玻璃MDL* *在NVIDIA的MDL核心定义* *中可用*

## 硬件加速

Iray渲染器专门在NVIDIA GPU上提供硬件加速，具有下列优势：

* 显着提升渲染速度
* [Optix AI加速去噪](https://developer.nvidia.com/optix-denoiser)（请参阅本页<b>渲染器</b>部分中的“Post-denoiser”）

您可以在[首选项](../../../interface/preferences-window/preferences-window.md)窗口的<b>3D视图</b>部分中选择Iray应用于渲染的硬件，如右侧的图像所示。

检测到支持的GPU时，将列在此部分中，默认情况下为&#x200B;*自动选择*，并且未选择CPU。 任何手动更改都会覆盖此自动行为，因此您的自定义更改将保存以供将来会话使用。

>[!NOTE]
>
> 如果检测到并列出了支持的GPU，我们强烈建议&#x200B;*将CPU保留为未选择*，因为使用CPU进行Iray渲染会对应用程序的整体性能和响应产生&#x200B;*显着影响*。

>[!WARNING]
>
> GPU硬件加速使用[NVIDIA CUDA](https://developer.nvidia.com/cuda-zone)技术。 确保您的&#x200B;*图形驱动程序是最新的*，以实现最佳兼容性和可靠性。 在[此处](https://www.nvidia.com/Download/index.aspx?lang=en-us)查找您的NVIDIA GPU的最新驱动程序。\
> 对于多GPU配置，建议&#x200B;*禁用SLI*，并仅选择一个GPU以获得最佳可靠性。

![Iray首选项](../../../assets/iray-preferences-hardware.png "Iray首选项")
