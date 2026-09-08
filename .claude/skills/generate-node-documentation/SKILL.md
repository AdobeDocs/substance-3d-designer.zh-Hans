---
name: generate-node-documentation
description: ""
source-git-commit: 475af5f27b827f66289993dbd8367904c1baf42b
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 4%

---


# 正在生成节点文档

此存储库中的每个叶节点引用页都遵循一个一致结构。 此
技能就是这种结构的规格。 一个典型的、充分运作的例子是
`.../node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md` —
如有疑问，请打开并镜像它。

此技能仅覆盖节点页&#x200B;*结构*。 对于基本Experience LeagueMarkdown
(注释/警告块、相对与绝对链接、UICONTROL/DNL、图像查询参数、
lint gotchas)遵循`write-experience-league-markdown`技能。

## 节点页所在的位置（文件夹/目录约定）

* 在匹配的类别/子类别路径下，每个节点有一个文件夹，例如：
  `.../node-library/<category>/<subcategory>/<node-name>/<node-name>.md`.
* 该文件夹被命名为kebab-case节点标题；它包含&#x200B;**一个** `.md`文件
名字相同。
* 页面的所有嵌入媒体（图标、图像、GIF）都位于&#x200B;**的同级中
  `.md`旁边的`<node-name>.resources/`文件夹&#x200B;**被引用了
  相对路径（例如`<node-name>.resources/<file>.png`）。 不要将节点页指向以下位置
  共享`help/assets/`文件夹 — 这是正在逐步淘汰的旧模式；新的和
  已编辑的页面使用自己的`.resources`文件夹。
* 每个页面在`help/guide/TOC.md`中都有一个对应的条目。 添加或移动
页面，同时更新`TOC.md`和文件夹布局（请参阅CLAUDE.md的文件夹/目录）
公约)。

## 前页

节点页使用&#x200B;**最小**&#x200B;块 — 只有`title`和痕迹样式
`description`. (这与的11字段旧版块CLAUDE.md文档不同，
常规内容页面。)

```yaml
---
title: "Shape splatter v2"
description: "Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Generator > Pattern > Shape splatter v2"
---
```

## 车身结构

从上到下，前面的内容都非常重要：

### &#x200B;1. H1标题

单个`# <Node title>` — 每页正好有一个H1。

### &#x200B;2. 图标/说明表

一个HTML表，一行，两个单元格。 左侧单元格(`33.33%`)包含图标，然后
`In:` breadcrumb；右单元格(`100.00%`)包含`## Description`和散文。

```html
<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![<Node title> icon](<node-name>.resources/<node-name>.png "<Node title>")

<b>In:</b> <Category> &gt; <Subcategory>

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

<Description prose.>

</td>
</tr>
</table>
```

说明单元格散文约定：
* 用`<br><br>`分隔段落（单元格内的原始空白行不可靠）。
* 内联强调为`<b>…</b>` / `<i>…</i>`。
* 导入辅助元素在句首使用`<i>Note:</i>` / `<i>Tip:</i>`。
* 将`&gt;`用于`In:`行中的`>`（它在HTML内）。 选择类别/
子类别名称来自节点本身；不要发明它们。

### &#x200B;3. 可选标注

`>[!INFO]`、`>[!TIP]`、`>[!NOTE]`等。在&#x200B;**之后**转到图标/说明表(不是
（在单元格内）。 根据`write-experience-league-markdown`技能的语法。

### &#x200B;4. 输入

仅在节点具有输入大头针时才包含。 在标题前面加一个锚点。

```markdown
<a name="inputs"></a>

## Inputs

|  |  |
|:---|:---|
| <b>Background height</b> <i>Grayscale</i> | The base height map in which shapes are scattered.<br><br>The contribution is controlled by the <b>Background input opacity</b> parameter. |
```

* 两列，空标题行，`|:---|:---|`对齐方式。
* 每个输入一行：左单元格`<b>Name</b> <i>Type</i>`，右单元格说明。
* 类型标志符是HTML斜体 — `<i>Type</i>` — 不是标记`*Type*`。

### &#x200B;5. 输出

形状与输入相同，具有`<a name="outputs"></a>` + `## Outputs`。 仅在以下情况下包含
node记录不同的输出（许多节点具有单个隐式输出并忽略此输出）
部分 — 不要发明一个)。

对于打包的多通道输出，使用`<br>`分隔通道并缩进
具有`&nbsp;`的子点(请参阅
参考)：

```markdown
| <b>Splatter UVW</b> | <b>R</b> - U component of the shapes' UVs.<br><b>G</b> - V component of the shapes' UVs.<br><b>B</b> - The shapes' height. (W)<br><b>A</b> - Packed data:<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- <i>Integer part:</i> The shapes' unique identifier. |
```

### &#x200B;6. 参数

相同的表格形状，具有`<a name="parameters"></a>` + `## Parameters`。 忽略全部
节（如果节点没有参数）(从不发出空表或“无参数”。
行)。

* **已分组的参数**：发出一个生成标签行，其右单元格为空，位于
组的行：

  ```markdown
  | <b>Positioning</b> |  |
  | <b>Project Input</b> <i>UV Position, World Space Position</i> | Choose whether the projection position is set in 2D/UV or in 3D/World space. |
  ```

* **枚举/多选项值**：将描述单元格内的选项作为
  `<br>`分隔的虚线列表：

  ```markdown
  | <b>Position distribution mode</b> <i>Integer</i> | The method of distributing the shapes:<br><br>- <b>2D grid:</b> A simple uniform grid.<br>- <b>Poisson disc:</b> Randomly offsets grid cells to prevent overlaps.<br>- <b>Uniform:</b> An even distribution of a set number of shapes. |
  ```

### &#x200B;7. 示例

仅在有示例图像/GIF时才包含。 使用HTML库表格；一个 `<td>`
包含可选字幕的每张图像；在3张图像后绕排到新的`<tr>`。 媒体路径
指向页面的`.resources`文件夹。

```html
## Examples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="./<node-name>.resources/<file>.gif" /><br><i>Caption</i>
        </td>
        <td style="border: 0; background: transparent">
            <img src="./<node-name>.resources/<file2>.jpg" /><br><i>Another caption</i>
        </td>
    </tr>
</table>
```

将部分填充的最后一行中的尾随单元格留空(`<td …></td>`)，而不是
重排。 如果源中没有，请省略字幕。

## 规范类型值

重用节点自己的类型措辞；典型值： `Grayscale`、`Color`、`Integer`、
`Float`, `Float2`, `Float3`, `Float4`, `Integer2`, `Boolean`, `Grayscale Input`,
`Color Input`, `(Color value)`, `(Grayscale value)`. 不要发明或“标准化”类型
节点实际上并不使用。

## 表单元格规则

* 表单元格内没有原始新行 — 使用`<br>` (和`<br><br>`之间的连接行
段落)。
* 单元格内的强调为`<b>`/`<i>`，类型标记始终为`<i>Type</i>`。
* 用`&nbsp;`序列缩进嵌套子点。

## 规则/不该做的事

* **不要伪造**节点没有的输入、输出或参数；省略
部分。 请勿改写、总结或去除现有的技术内容 — 仅限
重新设置格式。
* **保持链接相对**&#x200B;于其他`.md`页面；外部链接绝对。
* 将旧页面编辑为以下格式时&#x200B;**丢弃旧版摘要**：困难标记
(`**Simple**` / `**Intermediate**` / `**Complex**`)，冗余 `## <Title>`
图标单元格内的副标题，存根句子，如“没有附加图像
以及先前迁移的剩余空导航/包装表。
* 每页&#x200B;**一个H1**；节使用`##`和Inputs/Outputs/Parameters锚点
(`inputs` / `outputs` / `parameters`)必须位于其标题之前，以便跨页
  `#inputs`个链接解析。
* 在添加、重命名或移动页面时&#x200B;**保持`TOC.md`的同步**。
