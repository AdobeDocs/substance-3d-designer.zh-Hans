---
source-git-commit: ec58342925d3e608b0180b67a1e20ffaeb1f306a
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---
# CLAUDE.md

当使用此存储库中的代码时，此文件为Claude Code (claude.ai/code)提供了指导。

# Substance 3D Designer文档

此存储库包含Substance 3D Designer的文档。 没有应用程序代码、生成步骤或测试套件 — 存储库&#x200B;*是*&#x200B;内容，在Markdown中编写并在[Adobe Experience League](https://experienceleague.adobe.com/docs/substance3d-designer.html?lang=en)上发布。

# 存储库结构

* `help/` — 所有文档内容，按目录进行组织。
* `help/guide/TOC.md` — 目录。 每个条目都是指向页面的Markdown文件的相对链接（根位于`/help/...`）。 `TOC.md`还包含页树元数据（`user-guide-title`、`breadcrumb-title`、`nudge`、节锚点，如`{#section-id}`）。
* `help/assets/` — 共享、非页面特定的图像（例如，跨页面重复使用的应用程序图标）。
* `help/glossary/glossary.md` — 单个大型术语表页面，按字母顺序排列，使用锚点范围(`<span id="term"></span>`)进行组织，用于通过`#term`片段进行交联。
* `metadata.md` — 存储库级别的前台内容（云/解决方案/产品ID、`git-repo`等） 每`TOC.md`继承一次。 仅对存储库范围的元数据更改进行编辑；页面特定的元数据属于页面自己的头条。
* `redirects.csv`、`linkcheckexclude.json`、`markdownlint_custom.json`、`pipeline.opts` — 发布pipeline配置（重定向、链接检查异常、lint规则覆盖、管道选项）。
* `fix-image-names.py` — 一次性实用程序，使用括号后缀重命名`help/assets`个图像（例如，`foo(1).png`→`foo_1.png`），并重写每个Markdown引用以匹配。 不是任何常规工作流程的一部分；仅在此类文件名再次出现时手动运行。

## 文件夹/目录约定

对于`help/guide/TOC.md`中的每个条目：
* `help/`下有一个对应的文件夹，与目录遵循相同的嵌套。
* 该文件夹包含一个Markdown文件，该文件名为页面标题的kebab-case版本。
* 如果页面已定制了媒体（图像、GIF、视频），则它位于名为`<md-file-name>.resources`的同级子文件夹中。

添加或移动页面时，请同时更新`TOC.md`和文件夹布局，它们必须保持同步。

## 页面前页

常规内容页面使用前端内容块，例如：

```yaml
---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/<section>/<page>.html"
breadcrumb-title: ""
description: <one/two sentence SEO description>
helpx_creative_field: ""
helpx_description: Designer > <Section> > <Page>
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: <Page title>
user-guide-description: ""
user-guide-title: ""
---
```

保持`description`准确而简洁 — 它用于SEO/搜索片段。

# 内容创作规则

* 英语是真理的来源；所有其他语言都是从英语翻译过来的。
* 指向其他文档页面的所有链接都必须是&#x200B;**相对**&#x200B;链接；指向外部资源的所有链接都必须是&#x200B;**绝对**&#x200B;链接。
* 使用Experience League的自定义扩展/gotcha在GitHub风格的Markdown中编写内容，记录在[此处](https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown)。 具体内容请使用`write-experience-league-markdown`技能（如果存在）。
* 每个提交的更改都会通过CI中的自动Lint检查和链接验证（请参阅下文） — 在假定应用了规则或链接需要修复之前，请检查`markdownlint_custom.json`和`linkcheckexclude.json`。

# 验证/CI

* `.github/workflows/validate-articles.yml`在PR上运行并推送到`main`（并通过`retest`个PR注释），调用共享的`Adobe-Enterprise-Docs/workflows`可重用工作流以链接Markdown并验证链接。 此存储库中没有本地等效脚本 — CI是通过/失败的实际来源。
* `.github/workflows/mirror.yml`在推送时将`main`镜像到公共存储库；它是基础结构，而不是内容更改需要触及的内容。
* `markdownlint_custom.json`扩展共享的`markdownlint.json`规则集并禁用多个与Experience League的自定义标记扩展（例如内联HTML、非标准强调）冲突的规则(MD005、MD007、MD018、MD032、MD033、MD034、MD037、MD040)。 不要“修复”内容以满足这些已禁用的规则。
* `linkcheckexclude.json`将链接检查器应跳过的链接模式（当前为`example.com`/`example-end.com`）列入白名单。

# 工作惯例

* 这是包含大量发行说明的文档 — 发行说明位于`help/release-notes/`下，每个版本有一个文件夹（例如，`version-16-0`），以及`all-changes`和`old-versions`聚合页面。 添加新版本时，请按照现有版本文件夹作为模板进行操作。
