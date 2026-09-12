---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-15-1.html"
breadcrumb-title: ''
description: 查看Substance 3D Designer版本15.1的发行说明，了解新增功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 15.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 版本15.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: fde9d7a455c1c7b366323c119f4c1f9a2c114952
workflow-type: tm+mt
source-wordcount: '1719'
ht-degree: 0%

---


# 版本15.1

Substance Designer15.1提供了一个完全改版的图表创建窗口，其中包含直接样本访问、改进的噪声节点以实现更大的创意可能性、节点菜单中条理分明的类别等等。

*发行日期：2025年12月11日*

![Designer 15.1横幅](version-15-1.resources/bannerweb.png)

## 改进图表创建

在此版本中，[图形创建窗口](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md)已<b>进行了全面重新设计</b>，以增强Substance 3D Designer中的初始用户体验。 此更新的主要目标是简化模板选择流程，从而允许用户高效地确定最适合其需求的模板。

缩略图提供了针对预期素材类型的即时<b>视觉参考</b>，而详细的工具提示提供了所有相关信息。 为了改进组织，模板现在被分类为特定<b>类别</b>，例如材料、过滤器和扫描处理。

尽管主界面已升级，但用户仍可访问以前的视图，包括列表、包和目录选项。

[了解详情](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md)

![重新设计新图形窗口](version-15-1.resources/newgraph.png){zoomable="yes"}

## 嵌入样本

随着我们重新设计的图表创建窗口的启动，我们直接在软件中添加了各种[<b>示例素材</b>](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md)。 此增强功能用于响应您有关更好地访问学习资源的请求。

![新的示例图形创建窗口](version-15-1.resources/GraphSample.png){zoomable="yes"}

为了满足这一需求，我们使用了织物（包括皮革和缎面）、木材、金属、塑料、陶瓷等材料样本。 这些示例旨在帮助您轻松启动项目并熟悉Substance 3D Designer中可用的主要系列节点

每个图形都带有<b>批注</b>，经过精心组织，并包含最少的节点，使其尽可能易于理解。

您可以在创建新Substance图表时访问“物料抽样”类别中的抽样，也可以使用方便的“转到抽样”按钮直接从主屏幕访问抽样。

除了这些基础素材之外，我们还提供了<b>高级示例</b>来演示如何更有效地使用<b>FX映射和像素处理器</b>功能。

[了解详情](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md)

![Substance Designer中的木质样本](version-15-1.resources/samplegraph.png){zoomable="yes"}

## 新增噪声

噪声在多数图形中起着至关重要的作用，因此我们重点研究了此版本中的几项关键增强功能，以改进其功能和可用性。

在此更新中，我们引入了<b>对非拼贴场景的更好支持</b>，从而确保杂色图案按预期运行，而无需强制拼贴。 以前，在禁用拼贴时，会强制噪声节点拼贴或生成错误的结果。

大多数噪音现在包含<b>新参数</b>，为用户提供了更好的创意控制。 这些附加选项使图表作者能够在其工作流程中微调噪声的外观和行为。

最后，位深度<b>不再硬锁定到16位</b>。 您现在可以覆盖单个节点实例上的位深度设置，以便在需要时获得更高的细节和动态范围，或优化图形以提高性能。

请参阅下面的[发行说明](#release-notes)中更新的噪声的完整列表。

示例： [细胞1](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md) [云彩2](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/clouds-2/clouds-2.md) [方向划痕](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-scratches/directional-scratches.md) [水汽噪声1](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/moisture-noise/moisture-noise.md)

![方向无序噪声](version-15-1.resources/directionaldisorder.gif){zoomable="yes"}

## 节点菜单中的层次结构

为了应对在广泛的库中定位特定节点的挑战，我们在“节点”菜单中引入了类别。

由于节点数量庞大，很难快速找到所需的节点。 为了简化此过程，已在图形级别实现新的[<b>组</b>属性](../../compositing-graphs/graph-parameters/graph-parameters.md)。 定义此属性后，它用于组织和排序搜索结果。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![使用类别1](version-15-1.resources/search1-2.png){zoomable="yes"}进行节点搜索

</td>
<td style="border: 0;" valign="top">

![使用类别2](version-15-1.resources/search2.png){zoomable="yes"}进行节点搜索

</td>
</tr>
</table>

## 默认输出

当节点有多个[输出](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)时，不能在2D视图中同时显示所有输出，也不能将它们作为节点缩略图显示。 在这些情况下，主流准则是使用第一个连接的引脚，或者，如果没有连接，默认使用第一个输出。

但是，这种方法不一定能产生最佳结果。 例如，在某些Spline节点中，第一个连接的销通常表示样条坐标数据，这不适合预览目的。

为了解决此问题，引入了默认输出属性。 此功能允许图形作者<b>指定默认应显示的输出</b>，从而增强节点使用的直观性，并有助于更清楚地了解所创作的图形。

播放下图，查看默认输出定义前后的差异。

[了解详情](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)

<table>
  <tr>
    <td>
      <img src="version-15-1.resources/defaultouput2.png" alt="defaultouput2">
      <br><i>之前</i>
    </td>
    <td>
      <img src="version-15-1.resources/defaultouput1.png" alt="在默认输出中，缩览图始终是相关的。">
      <br><i>之后</i>
    </td>
  </tr>
</table>

## “Is defined”节点

使用函数图表时，您可能需要确定图表内是否存在[变量](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)。

例如，通过检测变量的缺失，可以提供回退值，从而确保函数的行为符合预期，而无需显式设置每个输入。 因此我们添加了[“已定义”节点](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)。

[了解详情](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)

![已定义节点](version-15-1.resources/isdefined.png){zoomable="yes"}

## 发行说明

### 15.1.0

*（2025年12月11日发布）*

### 已添加

* [NewGraph]重新处理新的图形窗口
* [新图形]添加材料样本和高级样本
* [NewGraph]为模板数据（类别和副标题）的图表添加新属性
* [NewGraph]删除输出格式选项
* [内容]添加哈希函数
* [Content]向函数添加调色板。sbs
* [内容]各向异性杂色v2：添加默认输出格式，添加无序
* [内容]对节点和参数标签应用句首大写
* [内容] BnW污点1 v2：添加默认输出格式，不支持拼贴
* [内容] BnW污点2 v2：添加默认输出格式，不支持拼贴
* [内容] BnW污点3 v2：添加默认输出格式，不支持拼贴
* [内容]细胞1、2、3、4 v2：添加默认输出格式，无拼贴支持，无序选项
* [内容] Cloud 1 v2：添加默认输出格式，不支持拼贴
* [内容] Cloud 2 v2：添加默认输出格式，不支持拼贴
* [内容] Cloud 3 v2：添加默认输出格式，不支持拼贴
* [内容]蒙版v2的颜色
* [内容]定向噪声1 v2：添加默认输出格式，不支持拼贴
* [内容]定向噪声2 v2：添加默认输出格式，不支持拼贴
* [内容]定向噪声3 v2：添加默认输出格式，不支持拼贴
* [内容]定向噪声4 v2：添加默认输出格式，不支持拼贴
* [内容]方向划痕v2：添加默认输出格式，不支持拼贴
* [内容]Dirt1 v2：添加默认输出格式，不支持拼贴
* [内容]Dirt2 v2：添加默认输出格式，不支持拼贴
* [内容]Dirt3 v2：添加默认输出格式，不支持拼贴
* [内容]Dirt4 v2：添加默认输出格式，不支持拼贴
* [内容]Dirt5 v2：添加默认输出格式，不支持拼贴
* [内容]Dirt渐变v2：添加默认输出格式，新的无序选项
* [Content]分形求和基础v2：添加默认输出格式、无序、不支持拼贴
* [内容]分形求和1、2、3、4 v2：添加默认输出格式
* [内容]高斯杂色v2：添加默认输出格式，不支持拼贴
* [内容]高斯污点1&amp;2 v2：添加默认输出格式，不支持拼贴
* [内容]凌乱的纤维1、2、3 v2：添加默认输出格式，不支持拼贴，无顺序选项
* [内容]水汽杂色v2：添加默认输出格式，不支持拼贴
* [内容]新的“水气噪声2”节点
* [内容]噪声：更新以添加默认输出格式
* [内容] Perlin噪声v2：添加默认输出格式，不支持拼贴
* [内容]形状映射器：添加筛选模式
* [内容] UV映射器：添加筛选模式
* [内容]波形1 v2：使用默认输出格式+新选项
* [内容]白噪声v2：使用默认输出格式，添加分布选项
* [烘焙]仅显示来自所选网格的UV
* [面包师]添加选项以选择按名称匹配几何的方法
* [面包师]删除面包师后，选择最接近的面包师
* [烘焙师] UDIM：定义要烘焙的UV磁贴列表
* [Bakers]将烘焙SDK更新到3.15.4
* [3D视图/场景浏览器]右键单击基本美元时，应避免选择基本美元
* [色彩管理]支持ACES 2.0
* [合成图形]允许将输出节点设置为“默认输出”
* [Cooker]移除有关函数实例的非连接输入的警告†
* [函数] Add isDefined运算符
* [Graph]在节点菜单中根据“group”属性对项目进行分组
* [Graph]改进缩览图渲染

### 修复

* [3D视图]当连接到环境或baseColor时，L16灰度纹理显示为红色色调
* [3D视图]更改无素材的场景的素材绑定会创建新的“默认”素材
* [3D视图]特定OBJ网格的计算法线不正确
* [3D视图]在Pathtracer中加载时，SBSSCN中的自定义环境不可见
* [3D视图]旋转已禁用的环境时，控制台中出现错误
* [3D视图]Specular level未正确应用
* [3D视图]使用Eclair光栅器时Specular edge color不起作用
* [3D视图]用户添加的材质未应用于默认场景
* [3D视图]&#x200B;[烘焙]材质颜色在覆盖后或使用“颜色”烘焙器时过暗
* [3D视图]&#x200B;[烘焙]FBX文件无材质颜色
* [Bakers]无法正确检测到FBX文件中的素材颜色
* [Bakers]在JSON预设导出中，“recompute\_tangents”选项始终为“false”
* [Bakers] CLI：通过JSON文件连续运行同一烘焙器时崩溃
* [Bakers]更新“color-generator”参数不适用于“灰度”
* [内容]路径蒙版：非方形比例失败
* [内容]PBR 渲染/图标渲染器：Specular瓣功能不正确
* [内容]样条路径：默认情况下，将“输出大小”设置为“相对于父代”
* [内容]点列表：当数据纹理不是方形时，点的顺序不正确
* [内容]样条映射器：随机情况下出现1像素线故障
* [Content]样条映射器：在某些情况下，当Thickness为0时，拉伸的UV
* [Graph]删除函数子图的输出时崩溃
* [Graph]可在只读包中更改输入节点颜色类型
* [Graph]在只读包中可以更改主要输入
* [属性]颜色预览构件的颜色与sRGB按钮状态不匹配
* [场景]无法加载大于2 GB的OBJ文件
* [UI]重新启动后，控制台和依赖项管理器停靠状态未恢复

### 已知问题

* [Baker]使用某些特定的NVIDIA驱动程序烘焙期间崩溃
* [3D视图] OpenGL：某些导入的场景可能无法渲染
* [3D视图]路径跟踪器：在启用镶嵌/位移的情况下更新纹理时，性能缓慢
* [3D视图]某些颜色素材属性在覆盖时未正确进行颜色管理
* [3D视图]无法正确支持带有动画基元的场景
* [3D视图]尚不支持具有多个UDims的网格
* [3D视图]不支持具有多个UV的网格，这可能会导致材质渲染无效
* [3D视图] AMD显卡不支持路径跟踪器
