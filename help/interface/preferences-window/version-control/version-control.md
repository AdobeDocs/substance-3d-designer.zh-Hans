---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/preferences-window/version-control.html"
breadcrumb-title: ''
description: 在Substance 3D Designer首选项中配置版本控制设置，以便与Git和其他系统集成。
helpx_creative_field: ""
helpx_description: Designer > Interface > Preferences window > Version control
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 版本控制
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---


# 版本控制

>[!IMPORTANT]
>
> Substance 3D Designer版本<b>14.0.0</b>将Perforce支持升级为<b>Python 3</b>。
> 
> 确保相应地调整其他脚本和版本控制环境。

Designer提供了[Perforce](https://www.perforce.com/) (P4)版本控制系统的Python集成。

集成将自定义“版本控制”子菜单添加到[资源管理器](../../../interface/the-explorer-window/the-explorer-window.md)中的包的上下文菜单中，并添加自定义图标以匹配P4中的包状态。

## 正在准备P4

在[P4V](https://www.perforce.com/products/helix-core-apps/helix-visual-client-p4v)中，记下工作区名称和路径，如下所示：

![P4V工作区信息](../../../assets/p4v-workspace-strings.jpg "P4V工作区信息"){zoomable="yes"}

在任何文本编辑器或IDE中，打开位于Designer安装中的以下脚本：“*tools/version\_control/perforce.py*”。

在第19行上，编辑系统上可执行<b>&#39;p4&#39;的位置</b>的路径。\
在下面的示例中，此路径为“*c：/Program Files/Perforce/p4.exe*”。

```
## Editable variables

cPerforceP4AbsPath = os.path.abspath("c:/Program Files/Perforce/p4.exe")

cVerbose = False
```


## Designer中的设置

版本控制在[项目设置](../../../interface/preferences-window/project-settings/project-settings.md)中配置，可在Designer的[首选项](../../../interface/preferences-window/preferences-window.md)中找到。

项目设置中的![“版本控制”选项卡](../../../assets/p4v-project-settings.jpg "项目设置中的“版本控制”选项卡"){zoomable="yes"}

1. 转到“编辑>首选项”
1. 转到“项目”，选择目标[项目文件](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)，然后转到“版本控制”选项卡
1. 选中“已启用版本控制”
1. 在“工作区”部分中填写此信息：

   * <b>名称：</b>输入您之前从P4V检索到的“工作区名称”
   * <b>路径：</b>输入您之前从P4V检索到的“工作区路径”

![Designer中的P4设置：工作区](../../../assets/p4v-project-settings-workspace.jpg "Designer中的P4设置：工作区"){zoomable="yes"}

### 设置动作

这些操作将显示在资源管理器中包的上下文菜单中。 有与大多数版本控制工具概念匹配的预定义操作：

* 可根据需要更改所有操作标签。
* 所有操作都需要脚本才能有效。

您可以使用：

* 一个脚本&#x200B;*每个*&#x200B;操作
* 一个用于&#x200B;*所有*&#x200B;操作的脚本

Designer的安装中提供了所有操作的入门脚本：“*tools/version\_control/perforce.py*”。

>[!IMPORTANT]
>
> 包需要保存在“工作区路径”下（例如“*f：/Dev/perforce*”下）才可用

1. 在<b>操作</b>组中，单击<b>添加</b>操作的“……”按钮
1. 在Designer安装中选择以下脚本：“*tools/version\_control/perforce.py*”
1. 应为所有其他操作自动设置脚本。

![Designer中的P4设置：操作](../../../assets/p4v-project-settings-actions.jpg "Designer中的P4设置：操作"){zoomable="yes"}

### 设置自定义操作

由于所有版本控制工具都各不相同，并且包含许多功能，因此我们允许用户添加自定义操作。

1. 单击“添加项目”
1. 填写新动作的标签，并设置其脚本路径

### 设置脚本解释器

1. 在“解释器”部分，单击“添加项目”
1. 设置脚本文件的扩展名或后缀，以及解释器可执行文件的路径
1. 编辑perforce.py脚本以更新“p4”二进制文件的位置

![Designer中的P4设置：解释器](../../../assets/p4v-project-settings-interpreters.jpg "Designer中的P4设置：解释器"){zoomable="yes"}

## 如何使用版本控制

1. 创建新包
1. 将包保存在“工作区路径”目录下
1. 单击程序包上的RMB：您现在可以访问“版本控制”子菜单
1. 根据工作区中包文件的状态，有几种操作可用：

   * <b>添加：</b>将文件标记为“ToAdd”
   * <b>提交：</b>提交所选包。 此操作将显示一个对话框，用于指定更改消息（请参阅下文）
   * <b>还原：</b>还原修改。 此操作会显示一个对话框，用于选择要恢复的文件（请参阅下文）
   * <b>签出：</b>将文件从仓库签出
   * <b>获取上一个版本：</b>从仓库检索最新版本
   * <b>刷新状态：</b>刷新包文件状态

   <table>
   <tr style="border: 0;">
   <td style="border: 0;" valign="top">

   ![“提交”对话框](../../../assets/p4v-submit.jpg "“提交”对话框"){zoomable="yes"}

   </td>
   <td style="border: 0;" valign="top">

   ![“恢复”对话框](../../../assets/p4v-revert.jpg "“恢复”对话框"){zoomable="yes"}

   </td>
   </tr>
   </table>

>[!NOTE]
>
> 所有操作都支持多选
> 
> 对于使用只读文件权限来限制修改的P4和其他版本控制工具，用户必须先签出包，然后才能进行修改。
> 
> 无法在SD中修改只读包文件。

根据程序包的状态，程序包将包含以下图标：

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![包图标：最新](../../../assets/p4-up-to-date.png "包图标：最新")

最新

</td>
<td style="border: 0;" valign="top">

![包图标：已签出](../../../assets/p4-checked-out.png "包图标：已签出")

已签出

</td>
<td style="border: 0;" valign="top">

![包图标：已添加](../../../assets/p4-added.png "包图标：已添加")

标记为添加

</td>
<td style="border: 0;" valign="top">

![包图标：不在仓库中](../../../assets/p4-not-in-depot.png "包图标：不在仓库中")

不在仓库中

</td>
</tr>
</table>

请注意，非最新包标有警告符号。

## 动作脚本

因此，将生成每个操作执行的命令：

my\_script <b>*WorkspaceName WorkspacePath ActionName[ActionArgs]*</b>

<b>工作区名称：</b>工作区的名称

<b>WorkspacePath：</b>工作区根目录的路径

<b>ActionName：</b>操作名称：

* *添加：*&#x200B;用于“添加”操作
* *签出：*&#x200B;以执行“签出”操作
* *提交：*&#x200B;以进行“提交”操作
* 用于“还原”操作的&#x200B;*还原：*
* *get\_last\_version：*&#x200B;用于“获取最新版本”操作
* 用于“获取状态”操作的&#x200B;*get\_status：*

在项目设置中设置标签，使用“ ”字符替换为“\_”，例如：“My Action”=>“My\_Action”。

操作的<b>ActionArgs：</b>个参数：

* *-desc*：“提交”操作使用的说明字符串
* *-files：*&#x200B;文件列表
* *-files\_list：*&#x200B;包含每行文件列表的文本文件

<b>get\_status</b>：根据指定文件的状态返回值：

* 0：未定义的状态
* 1：不在车库中
* 2：早期版本（不是最新版本）
* 3：最新版本（最新）
* 4：已签出
* 5：已标记待添加
* 其他操作：
  * 0：成功
  * 其他：错误
