---
name: write-experience-league-markdown
description: |
  用于编写在Adobe Experience League上发布的Markdown内容的语法规则、自定义扩展和gotchas。 每当创建或编辑此存储库（或任何其他Experience League内容存储库）中的帮助/下的任何页面（标题、链接、图像、表格、注释/警告块、UICONTROL/DNL标签、视频嵌入、锚点和已知渲染缺陷）时，请使用此技能。 来源： https://experienceleague.adobe.com/zh-hans/docs/contributor/contributor-guide/writing-essentials/markdown
source-git-commit: ed17c57a1aa9669a602d4523bdef20cd7d82db75
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 4%
---

# 书写Experience League标记

Experience League通过自定义管道渲染GitHub风格的Markdown
具有自己的扩展和渲染奇特。 标准GFM大部分有效，但
以下项目是特定于Experience League的 — 请确定它们是否正确且包含内容
lint/link-check CI失败，或在实时站点上错误地渲染。

## 标题

* `#`到`#####`（级别1-5）。 页面的`title`首页内容是
有效级别0；正文中的第一个Markdown标题应为
单个`# Level 1`标题与页面标题匹配（或密切匹配）。
* 不要随意跳过级别；微型目录是从标题生成的。

## 文本格式

* `**bold**`, `*italic*`, `***bold and italic***`.
* 用反斜杠（`\*`、`\_`等）转义文本特殊字符。
* 标题/标题中的&#x200B;**和/或**&#x200B;必须写出(`and`)或编码为
  `&amp;` — 标题中的原始`&`可能会中断分析。
* 用作文本（非实HTML）的&#x200B;**尖括号**&#x200B;必须经过编码：
  `<placeholder>`→`&lt;placeholder&gt;`。
* 从文字处理器粘贴的&#x200B;**智能引号**&#x200B;必须经过编码，不能保留为
文本卷形字符：左双`&#8220;`，右双`&#8221;`，
撇号/右单`&#8217;`。

## 列表

* 编号列表：使用`1.`（或`1)`）启动每个项目 — GitHub/Experience
联盟自动编号，而不考虑键入的字面数字。
* 项目符号列表：使用`*`、`-`或`+`，但&#x200B;**不要混合项目符号字符
在同一列表/文档**&#x200B;中。
* `TOC.md`列表嵌套一致地使用`+` — 遵循现有文件的
项目符号样式，而不是引入其他样式。

## 链接

* 内部交叉引用必须是指向&#x200B;**&#x200B;**
目标`.md`文件： `[Overview](../../overview.md)`。
* 外部引用必须是&#x200B;**绝对**&#x200B;个URL。
* 将锚点添加到另一页的标题/范围：附加`#anchor-id`，例如，
  `[Mesh](../../glossary/glossary.md#mesh)`.
* 页面内锚点声明为标题（自动嵌套）或
紧接在术语前面的显式`<span id="anchor-id"></span>` (HTML) / `{: #anchor-id}` (Markdown) —
请参阅`help/glossary/glossary.md`，了解此存储库中使用的模式。
* `TOC.md`节锚点在标题/列表后使用`{#section-id}`语法
标签，例如`Getting started{#getting-started}`。

## 图像

尽可能使用Markdown图像语法：

```markdown
![Alt text](path/to/image.png "Optional hover text")
```

* `![...]`文本需要可访问的替代文本。 保持简洁并做好
不使用下划线；应改用空格或连字符。
* 图像路径可以相对于Markdown文件，也可以是根目录相对路径，例如
作为`/help/assets/shared-image.png`。 页面特定的图像属于
同级`<page-name>.resources/`文件夹(例如，
  `<page-name>.resources/image.png`). `help/assets/`是旧共享文件夹；
  请勿在此处添加新的特定于页面的图像。
* 可选的图像查询参数可以控制CDN处理：
  `?width=750&format=png&optimize=medium`. 将这些参数保留在图像上
  URL，在任何属性块之前。
* 在关闭`)`之后立即添加图像属性：
  `![Alt text](image.png "Hover text"){width="300" align="center"}`.
  `width`是视图区域的像素值或百分比；图像缩放
按比例分配。 支持的对齐值为`center`和`right`。
  不支持`valign`。
* 使用`modal="regular"`或`zoomable="yes"`使图像点击缩放：
  `![Alt text](image.png){width="100" zoomable="yes"}`. 不合并
  单击以缩放图像链接；以超链接为准。
* 要将图像链接到另一页，请在标记链接中绕排图像：
  `[![Alt text](image.png)](../target/target.md)`.
* 对于大图像，在实际使用时请至少提供640像素的源宽度。
除非需要，否则不要使用超过约2000像素，并保持图像文件低于
可能为5 MB。 管道接受最大100 MB的文件，但文件超过
20 MB未通过验证，文章通常应包含不超过
100张图像（一些更旧的指导说是200张；使用更严格的限制）。

仅在Markdown无法表示所需布局(如
特殊表或自定义内联演示文稿。 支持的HTML图像表单
为：

```html
<img src="image.png" alt="Alt text" />
```

* 始终提供有意义的`alt`属性，并使用相对或
根目录相对`src`与Markdown图像一致。
* 对于保留的内联HTML内的HTML图像，请添加
  `data-preserve-html="true"`到包含的标记(当需要
  周围标记。 例如：

  ```html
  <div data-preserve-html="true" align="center">
    <img src="my-page.resources/preview.gif" alt="Preview" />
  </div>
  ```

* 要为HTML图像启用点击缩放，请使用
  `<img>`标记上的`class="modal-image"`。
* 不要使用不支持的HTML属性或依赖`valign`；更喜欢Markdown
宽度和对齐方式的属性。

## 表

偏好使用原生Markdown表来表示普通的表格内容：

```markdown
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

* 在桌子前放一行空白。 标记表至少需要一个
标题行和一个正文行；对于单行或无标题行使用HTML表
表。
* 每个标头分隔符单元格中至少使用三个连字符，并且保留不变
每行中的管道字符数。 退出文本管道为`\|`或
  `&vert;`.
* 根据需要使用分隔符行中的对齐标记：
  左对齐、居中对齐和右对齐的`|---|:---:|---:|`。
* 分段和HTML的Markdown表格单元格支持内嵌格式
基本列表。 将`<p>`用于单独的段落，`<br>`用于换行，以及
  `<ul>`/`<ol>`包含`<li>`个列表项。 加
  `data-preserve-html="true"`在需要HTML元素时内嵌
  周围的存储库标记。

  ```markdown
  | Header | Details |
  |---|---|
  | Text | First paragraph.<p>Second paragraph.<br>New line.<ul><li>Item</li></ul> |
  ```

* 避免使用非常宽和非常高的表格；这些表格难以导航。
请小心处理表中的内联代码，因为长代码可能会强制
列宽不成比例。
* 要为Markdown表选择表布局，请在
表，用空白行分隔：

  ```markdown
  {style="table-layout:fixed"}
  ```

  当长文本或代码需要灵活时，请使用`table-layout:auto`（默认值）
  列宽。 将`fixed`用于平衡列，例如包含
  大小相近的图像。

当Markdown无法表示所需结构时，请使用HTML表，例如
省略标题、将单元格与范围合并、平衡列或对齐
单元格中的内容：

```html
<table style="table-layout:fixed">
  <tr>
    <th>Property</th>
    <th>Value</th>
  </tr>
  <tr>
    <td align="center">Example</td>
    <td>Details</td>
  </tr>
</table>
```

* 支持的表元素包括`<table>`、`<tbody>`、`<thead>`、`<tfoot>`、
  `<tr>`、`<th>`、`<td>`、`<col>`和`<colgroup>`以及受支持的
内联元素，如`<p>`、`<br>`、`<b>`、`<i>`、`<ul>`、`<ol>`和
  `<li>`.
* 不要在HTML表内使用Markdown语法。 例如， Markdown
注释、图像和链接可以按字面渲染；请改用HTML语法。
  `UICONTROL`和`DNL`本地化标记是例外。
* 在下列情况下，请在单元格上使用`align="left"`、`align="center"`或`align="right"`
需要。 HTML表不能包含嵌套表。
* 在开始标记上设置HTML表布局：
  `<table style="table-layout:auto">`或
  `<table style="table-layout:fixed">`.
* 对于无边框的一行HTML表，请使用
  `<tr style="border: 0;">`.

## 代码

* 内联代码：单个回退。
* 带围栏的块：三重backticks，语法为可选语言
突出显示（` `&#x200B;``python `、` ``&#x200B;`javascript `等）。

## 注释/警告块

自定义块引号语法，每个块一种类型，空白块引号行介于
标签和正文：

```markdown
>[!NOTE]
>
>This is a standard NOTE block.

>[!TIP]
>
>This is a standard TIP.

>[!IMPORTANT]
>
>This is an IMPORTANT note.
```

支持的类型： `NOTE`、`TIP`、`IMPORTANT`、`CAUTION`、`WARNING`、
`ADMINISTRATION`, `AVAILABILITY`, `PREREQUISITES`, `ERROR`, `INFO`, `SUCCESS`.

## 视频嵌入

Experience League不支持在`[!VIDEO]`块中直接嵌入MP4或YouTube视频。 如果需要动画预览，请改用页面的同级`.resources`文件夹中的GIF，并根据需要使用内联HTML使其居中。

```markdown
<div data-preserve-html="true" align="center">
  <img src="my-page.resources/my-preview.gif" alt="My preview" />
</div>
```

请勿将`[!VIDEO]`用于本地MP4文件、远程MP4文件或YouTube URL — 发布管道会拒绝它们，并且CI失败。

## UICONTROL标签

以内嵌方式换行UI元素名称（按钮标签、菜单项、字段名称）
定位管道知道要检查平移的字符串并掉落
如果不存在任何标签，请返回英文标签：

```markdown
Click [!UICONTROL Save] to apply changes.
Go to [!UICONTROL Tools] > [!UICONTROL Settings].
```

对于指导文本（菜单）中引用的每个文本UI标签，均使用它
项目、按钮名称、对话框标题、面板名称)。

## DNL标记（“不本地化”）

包装产品名称、第三方功能名称或任何必选短语
永远不要由机器平移：

```markdown
Use [!DNL Adobe Analytics] to track metrics.
The [!DNL Target] implementation requires configuration.
```

在此存储库中，请将其用于产品名称，例如`[!DNL Substance 3D Designer]`。
`[!DNL Substance 3D Sampler]`等，在每页首次/突出显示的提及上，
与现有页面一致。

## 内联HTML

允许原始HTML(此存储库的`markdownlint_custom.json`禁用MD033
仅能通过IP地址来可靠地保留
标签携带`data-preserve-html="true"`时的管道。 保留内联HTML
对于普通标记无法表示的情况(表单元格内的图像/列表，
`<span id="...">`个锚点)，而不是作为Markdown的一般替代项。

## 前页

请参阅AGENTS.md的“Page front matter”（页面前页）部分，了解使用的确切数据块
此存储库中的常规内容页面，以及存储库级别的`metadata.md`
继承的字段。