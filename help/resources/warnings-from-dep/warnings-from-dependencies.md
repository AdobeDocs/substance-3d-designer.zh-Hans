---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/warnings-from-dependencies.html"
breadcrumb-title: ''
description: 了解来自Substance 3D Designer中资源依赖项的警告以及如何解决这些警告。
helpx_creative_field: ""
helpx_description: Designer > Resources > Warnings from dependencies
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 依赖项中的警告
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1245'
ht-degree: 0%

---


# 依赖项中的警告

此页面列出了Substance 3D Designer中的依赖项可能触发的警告和错误消息，并且提供了针对每个警告和错误消息的常见故障诊断步骤。

依赖项是Substance 3D文件(SBS)引用的&#x200B;*其他文件*。 它们包括[资源](../../resources/resources.md)和[图形实例](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)节点引用的其他Substance 3D文件。

## ![（错误）](../../assets/error.svg)无效的依赖包

无法加载依赖关系包，因为它缺失、已损坏或与正在使用的Designer版本不兼容。

<b>！[(tick)](../../assets/check.svg)解决方案</b>

有两个主要方法可纠正此问题：

1. <b>成功加载依赖项</b>

   检查依赖项包是否存在于警告消息中指定的位置。 如果没有，请找到该文件并将其放回该位置，或重新创建它。 如果文件存在，*尝试在Designer中加载它*，并查找与该包相关的任何警告或错误。 请参阅这些特定问题的故障排除步骤并相应地进行修复。

   然后，通过在[资源管理器](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)面板中单击主机包上的RMB，并在上下文菜单中选择<b>重新加载</b>选项来重新加载该主机包。

   ![“无效的依赖包”解决方案1](../../assets/warnings-dep-invalid-dependent-pkg.gif "“无效的依赖包”解决方案1")
1. <b>在包中重新定位依赖项</b>

   可以使用[依赖关系管理器](../../interface/dependency-manager/dependency-manager.md)重新定位依赖关系。 单击[资源管理器](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)面板中的主机包上的RMB，然后在上下文菜单中选择<b>依赖关系管理器</b>选项。

   在“依赖管理器”的列表中查找缺失的依赖项，单击该依赖项上的人民币，然后选择<b>迁移……</b>选项。 使用文件浏览器对话框查找依赖关系包，然后单击<b>打开</b>。

   然后，通过在[资源管理器](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)面板中单击主机包上的RMB，并在上下文菜单中选择<b>重新加载</b>选项来重新加载该主机包。

   ![“无效的依赖包”解决方案2](../../assets/warnings-dep-invalid-dependent-pkg-2.gif "“无效的依赖包”解决方案2")

## ![（错误）](../../assets/error.svg)检查别名&#x200B;*&#39;X&#39;*&#x200B;是否在项目中定义

正在从警告中报告的别名下的Substance 3D文件(SBS)数据中[别名](../../interface/preferences-window/project-settings/project-settings.md)的位置加载包的某个依赖项或资源，尽管当前[项目文件](../../interface/preferences-window/project-settings/project-settings.md)中未定义该别名。

<b>！[(tick)](../../assets/check.svg)解决方案</b>

[项目文件](../../interface/preferences-window/project-settings/project-settings.md)中至少应有一个定义警告中报告的别名。

![“检查别名是否已定义”解决方案](../../assets/warnings-dep-alias.gif "“检查别名是否已定义”解决方案")

## ![（错误）](../../assets/error.svg)找不到与此资源匹配的文件

找不到与[位图资源](../../resources/bitmap-resource/bitmap-resource.md)的&#x200B;*UDIM模板*&#x200B;匹配的文件。

<b>！[(tick)](../../assets/check.svg)解决方案</b>

如果链接了[位图资源](../../resources/bitmap-resource/bitmap-resource.md)，并且Designer在其文件名中检测到&#x200B;*UDIM命名分类*，例如`my_texture_0x1.png`中的`0x1`，则它提议将其链接为&#x200B;*UDIM模板*，以便[位图](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)节点在Designer中使用UDIM工作流程时，能够&#x200B;*使用该分类自动将*&#x200B;切换到UDIM集中的其他位图。 在这种情况下，Designer以&#x200B;*不同方式*&#x200B;链接位图资源，这考虑了UDIM编号模板。

有两个主要方法可纠正此问题：

1. <b>还原文件</b>

   转到资源的<b>文件路径</b>属性指定的位置，并检查模板之后的文件是否存在。 如果没有，请恢复或重新创建它们。

   ![“没有与资源解决方案1](../../assets/warnings-dep-udim-2.gif "匹配的文件”没有与资源解决方案1")匹配的文件
1. <b>重新定位文件</b>

   如果移动或重命名了文件，请通过单击[资源管理器](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)面板中的资源项上的RMB来重新定位文件，然后选择<b>重新定位</b>选项将该资源链接到一组同类型UDIM图像&#x200B;*第一个文件*。

   ![“没有与资源解决方案2](../../assets/warnings-dep-udim.gif "匹配的文件”没有与资源解决方案2")匹配的文件

## ![（错误）](../../assets/error.svg)未找到链接的文件

链接资源引用的文件在其<b>文件路径</b>属性指定的位置不存在。

<b>！[(tick)](../../assets/check.svg)解决方案</b>

有两个主要方法可纠正此问题：

1. <b>还原文件</b>

   转到资源的<b>文件路径</b>属性指定的位置，并检查该文件是否存在。 如果没有，请恢复或重新创建它。

   ![“未找到链接的文件”解决方案1](../../assets/warnings-dep-file-not-found.gif "“未找到链接的文件”解决方案1")
1. <b>重新定位文件</b>

   如果该文件已被移动或重命名，请通过单击[资源管理器](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)面板中的资源项上的RMB将其重新定位，然后选择<b>重新定位</b>选项以将该资源链接到另一个相同类型的文件。

   ![“未找到链接的文件”解决方案2](../../assets/warnings-dep-file-not-found-2.gif "“未找到链接的文件”解决方案2")

## ![（错误）](../../assets/error.svg)未找到色彩空间

[位图资源](../../resources/bitmap-resource/bitmap-resource.md)引用的色彩空间在当前[色彩管理](../../color-management/color-management.md)环境中找不到。 这可以是ICC配置文件，也可以是OCIO配置中的色彩空间。

<b>！[(tick)](../../assets/check.svg)解决方案</b>

“色彩空间”属性的选项列表会自动填充可用的有效色彩空间。 将该资源的色彩空间值更改为列表中的任何其他条目。

或者，将该色彩空间添加到当前的[色彩管理](../../color-management/color-management.md)环境，然后重新启动Designer。 这可以是ICC配置文件，也可以是OCIO配置中的色彩空间。

>[!NOTE]
>
> 仅当使用&#x200B;**旧版**&#x200B;以外的色彩管理模式（类似于禁用色彩管理）时，才会触发此警告。 您可以在[项目设置](../../interface/preferences-window/project-settings/project-settings.md)的&#x200B;**色彩管理**&#x200B;部分中启用色彩管理。

![“未找到色彩空间”解决方案](../../assets/warnings-dep-color-space.gif "“未找到色彩空间”解决方案")

## ![（错误）](../../assets/error.svg)未找到引用资源

在警告中报告的位置找不到分配给[3D网格资源](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/3d-mesh-resource-200574577.html)的UV磁贴的图形。

<b>！[(tick)](../../assets/check.svg)解决方案</b>

有两个主要方法可纠正此问题：

1. <b>还原图形</b>

   在[资源管理器](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)面板中检查<b>UV磁贴</b>列表中指定的图形的包内容。 如果它不存在，请恢复或重新创建它。

   ![“未找到引用资源”解决方案1](../../assets/warnings-dep-udim-graph-2.gif "“未找到引用资源”解决方案1")
1. <b>选择其他图形</b>

   将包中的另一个图形分配给UV图块。

   ![“未找到引用资源”解决方案1](../../assets/warnings-dep-udim-graph.gif "“未找到引用资源”解决方案2")

## 多次分配![（错误）](../../assets/error.svg)个UV磁贴

[3D网格资源](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/3d-mesh-resource-200574577.html)的UV磁贴被多次分配给[Substance图形](../../compositing-graphs/substance-compositing-graphs.md)。

<b>！[(tick)](../../assets/check.svg)解决方案</b>

对于3D网格资源的每个UV集，请确保<b>UV磁贴</b>列表中没有&#x200B;*存在*&#x200B;以上的UDIM索引。

已多次分配![&#39;UV磁贴&#39;解决方案](../../assets/warnings-dep-udim-same.gif "&#39;已多次分配&#39;UV磁贴&#39;解决方案")

## ![（错误）](../../assets/error.svg)无效的UV磁贴

[3D网格资源](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/3d-mesh-resource-200574577.html)列出的UV磁贴未在网格中定义或已损坏。

<b>！[(tick)](../../assets/check.svg)解决方案</b>

对于3D网格资源的每个UV集，请确保<b>UV磁贴</b>列表中的所有项都引用链接资源中&#x200B;*存在*&#x200B;的UDIM。

>[!NOTE]
>
> 此警告无法通过用户界面触发，因为它&#x200B;*仅*&#x200B;列出了在链接的资源中检测到的UDIM。 仅直接修改Substance 3D文件(SBS) **&#x200B;中的数据，会导致触发此警告。

![“无效的UV磁贴”解决方案](../../assets/warnings-dep-udim-invalid.gif "“无效的UV磁贴”解决方案")
