---
name: write-experience-league-markdown
description: ""
Source: https://experienceleague.adobe.com/zh-hans/docs/contributor/contributor-guide/writing-essentials/markdown
source-git-commit: e44437dcecf30714ffe5274c91135d84a0360aa7
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 6%

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
紧接在术语前面的显式`<span id="anchor-id"></span>` —
请参阅`help/glossary/glossary.md`，了解此存储库中使用的模式。
* `TOC.md`节锚点在标题/列表后使用`{#section-id}`语法
标签，例如`Getting started{#getting-started}`。

## 图像

* `![Alt text](path/to/image.png "Optional hover title")`.
* 支持可选的大小/优化查询参数：
  `![Adobe logo](my-page.resources/logo.png?width=750&format=png&optimize=medium)`.
* **替代文本不得包含下划线** — 它们不能正确呈现；
请改用连字符或空格。
* 特定于页面的图像位于同级`<page-name>.resources/`文件夹中
相对引用的`.md`旁边的(例如
  `<page-name>.resources/image.png`). `help/assets/`是旧版共享
  文件夹 — 不要在那里添加新图像（请参见CLAUDE.md）。

## 表

* 竖线分隔，带有连字符标题分隔符行：

  ```markdown
  | Header | Another header | Yet another header |
  |--- |--- |--- |
  | row 1 | column 2 | column 3 |
  | row 2 | row 2 column 2 | row 2 column 3 |
  ```

* 表前必须有一个空白行，否则它不会呈现为表。
* 表格不能完全容纳多段落内容或复杂块内容
单元格 — 此存储库需要在表格单元格内显示图像/列表(例如，
比较表（在`overview.md`中），它回退到内联HTML
(`<div>`、`<b>`、`<ul>`/`<li>`)，每个都有`data-preserve-html="true"`
标记，这样管道就不会将其剥离。 遵循现有模式，
无需发明新的内联HTML。

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

```markdown
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

## UICONTROL标签

以内嵌方式换行UI元素名称（按钮标签、菜单项、字段名称）
本地化管道知道要检查已翻译的字符串并下降
如果不存在任何标签，请返回英文标签：

```markdown
Click [!UICONTROL Save] to apply changes.
Go to [!UICONTROL Tools] > [!UICONTROL Settings].
```

对于指导文本（菜单）中引用的每个文本UI标签，均使用它
项目、按钮名称、对话框标题、面板名称)。

## DNL标记（“不本地化”）

包装产品名称、第三方功能名称或任何必选短语
永远不要机器翻译：

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

请参见CLAUDE.md的“页面前页”部分，了解使用的确切块
此存储库中的常规内容页面，以及存储库级别的`metadata.md`
继承的字段。