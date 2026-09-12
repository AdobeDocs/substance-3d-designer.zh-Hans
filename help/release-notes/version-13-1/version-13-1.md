---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-13-1.html"
breadcrumb-title: ''
description: 查看Substance 3D Designer版本13.1的发行说明，了解节点图形改进和AxF导出支持。
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 13.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 版本 13.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: e540abf8ed046d72f116e9e43ae0743c5ae39c24
workflow-type: tm+mt
source-wordcount: '1289'
ht-degree: 1%

---


# 版本 13.1

<b>Substance 3D Designer 13.1</b>向节点图添加了许多生活质量改进（主要针对帧），以增强素材创建体验。 此外还添加了AxF导出，为使用AxF格式的用户提供了互操作性工作流程。

*发行日期：2023年12月12日*

![Substance 3D Designer 13.1横幅](version-13-1.resources/24-library-hero-1920x620.png "Substance 3D Designer 13.1横幅")

## 框架改进

框架是使图表井井有条并且可读的必备工具。 这就是我们决定在新版本中对它们进行润色的原因。

### 自动扩展

随着图形的增长，可能需要重新排列帧的内容。 节点可能会移动以便为添加留出空间，也可能需要将内容隔开更多以提高可读性。 为了方便进行这些调整，现在可以在移动包含的对象时自动扩展帧：在移动对象时随时按住<b>Shift</b>，以便自动调整帧边框来将该对象保留在其边界内。

![自动扩展](version-13-1.resources/autoexpand.gif)

### 使尺寸适合内容

在图表中进行调整时，框架可能不会再顺畅地适应其内容。 这个新命令允许您自动调整帧的位置和大小，以便通过填充一个中等网格单元来调整其内容的范围。 如果框架具有描述，则会对其进行调整，以尽可能使用描述旁边的任何空白空间。

![fitsize](version-13-1.resources/fitsize.gif)

### 增强说明

得益于HTML代码，现在可以在框架的描述中包含设置格式的文本。 这同样适用于注释。

![richtext](version-13-1.resources/description-3.png)

### <b>...还有更多！</b>

许多事情都经过了重新考虑，例如归属规则更可容忍，交互区域可轻松调整框架大小，对齐规则不会使网格上的节点不对齐，以及视觉方面可带来一些新鲜感。 可随时访问框架的[文档](../../interface/the-graph-view/graph-items/frame/frame.md)以了解更多信息。

## 生活质量改善

* <b>节点菜单改进： </b>为了节省搜索所需节点的时间，我们对节点菜单进行了一些改进。 现在搜索更宽容了，即使没有完美匹配项，搜索也会为您提供结果。 此外，您现在可以使用向上箭头直接访问列表中的最后一个元素。
* <b>节点放置： </b>如果您希望为图表绘制完美的布局，那么这两个细微的更改将取悦您！ 将节点从一个图形复制/粘贴到另一个图形时，粘贴的节点现在与主网格对齐。 当在长链接上添加节点时，这个节点现在将被置于该链接可见部分的中间，以便使其在任何情况下都可见。
* <b>2D视图选项： </b>如果您是[2D视图](../../interface/2d-view/2d-view.md)的密集型用户，则可以节省时间，因为现在保存了“显示棋盘”、“保留视图大小”、“使用物理尺寸”和“显示拼贴”等选项，因此当您创建新的2D视图时，甚至当您重新启动Designer时，都无需再次设置它们。

## AxF导出

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![AxF文件图标](version-13-1.resources/axf-file-icon.png "AxF文件图标")

</td>
<td width="100.00%" style="border: 0;" valign="top">

AxF是来自[X-Rite](https://www.xrite.com/axf)的格式。 它提供了一种在整个数字设计工作流程中使用数字数据捕捉、存储、编辑和传达复杂材料特征的方法。 在早期版本的Designer中，您可以[导入AxF文件](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md)，然后改进拼贴或添加程序效果，但之后您只能将更改导出为新的.sbsar文件。

在此新版本中，我们引入了就地编辑AxF素材的可能性，然后[将您的更改导出](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md)为导入的AxF文件中的新图层。

</td>
</tr>
</table>

![导出AxF](version-13-1.resources/exportaxf.gif)

## API

最后，此13.1版本通过添加另外两种可能性继续改进了Python API：

* <b>“Visible if”属性： </b>您现在可以为图形参数、输入和输出设置此属性。
* <b>图形输入/输出顺序：</b>使用sdsbscompcraph：：reorderGraphInput和sdsbscompcraph：：reorderGraphOutput来根据需要组织参数。

>[!NOTE]
>
> Designer 13.1是基于Qt5的最新主要版本，后续主要版本将升级到Qt6。 这可能会影响您的自定义插件。

## 发行说明

### 13.1.0

*（2023年12月12日发布）*

### 已添加

* [帧]自动扩展
* [框架]更改规则，以定义对象何时属于框架
* [框架]禁用框架描述的文本缩放
* [框架]调整大小以适合内容
* [帧]新的默认、悬停和选定状态
* [帧]对齐到大网格
* [Frames]支持框架描述的HTML代码
* [帧]更新交互区域
* [帧]更新视觉长宽比
* [图形]在可见链接的中间而不是链接的中间创建节点
* [图形]如果项目是所选内容中唯一具有属性的项目，则显示项目的属性
* [图表]删除图表中注释的“缩放”选项
* [Graph]执行复制/粘贴操作时，对齐主网格上的节点
* [UX]允许在“节点”菜单和“库”搜索中进行模糊搜索
* [UX]使“节点”菜单列表循环N
* [AxF]支持AxF导出
* [AxF]在Linux上禁用AxF
* [API]使用Python API设置图形参数、输入和输出的“显示条件”属性
* [API]使用Python API设置图形I/O的顺序
* [依赖项]更新提升到1.80.0
* [依赖项]将OpenSubdiv更新到3.5.x
* [依赖项]将FBX SDK更新到2020.3
* [依赖项]将NGL更新为1.35.0.20
* [色彩管理]添加对OCIO ICC显示器的支持
* [色阶]添加重置直方图的方法
* [Python]无法导入QtForPython时向用户发出警告
* [2D视图]保存视图选项的状态
* [3D视图]将位置技术添加到网格信息着色器
* [导出]添加“保存设置”按钮以保存对导出选项的更改

### 修复

* [3D视图]无法将纹理指定给MDL材质的texture\_2d类型的输入
* [AxF]模板列表中的图形标识符可以为空白
* [AxF]默认情况下，Substance图形模板字段为空
* [Content]Atlas Scatter：特定情况下的错误行为
* [Content]Flood Fill映射器：当所有形状都具有相同的Bbox大小时，输出为空
* [内容] FloodFill to Position：在某些情况下，不精确伪像
* [Content] “BaseColor/Metallic/Roughness converter”节点中的“Specular”输出不正确
* [内容]在非方形垂直图像中无法进行“蒙版到路径”处理
* [内容]缺少对输入值、输入灰度、输入颜色和输出节点的说明
* [Content] Set和Sequence节点缺少说明
* [内容]形状飞溅：“飞溅数据2”输出中出现不精确伪像
* [引擎]值处理器中的布尔值始终计算为“False”（仅限Apple Silicon）
* [资源管理器]操作系统之间的工具栏按钮顺序不一致
* [帧]使用CTRL功能键移动帧时，不抓取节点
* [渐变映射]“全部重置”选项还应重置渐变构件
* [GraphRender]在预览模式下调整时，某些节点呈现黑色
* [图形]调整默认布尔值时，“输入值”预览停滞在“False”状态（仅限Apple Silicon）
* [图表]框架不会移动靠近框架边缘的点节点
* [互操作性]发送至Substance 3D Stager后，重新发送图标未更新
* [MDL]无法更改此参数所在的节点中的粗糙度
* [MDL] “AxF到金属粗糙度”模板中的连接无效
* [UI] “导出输出”窗口可以最小化（仅限Windows）
* [UI]使用显示缩放时，图像在“关于”屏幕中显示为像素化
* [UI]图形工具栏中的节点对齐工具可创建多个撤消步骤

### 已知问题

* [AxF OpenGL着色器]各向异性分布的Ward不正确
* [AxF OpenGL着色器]不正确的默认粗糙度
* [AxF OpenGL着色器]着色基准旋转不正确
* [AxF OpenGL着色器]半球以下光线检测不正确
* [AxF OpenGL着色器]错误贡献检测
* [AxF]导出时“Specular颜色”映射值不正确
* [AxF]在“导入AxF”对话框中无法正确显示预览和纹理
* [AxF]属性“cc无折射”未正确地注入到AxF模板中
