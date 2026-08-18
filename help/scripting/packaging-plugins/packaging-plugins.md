---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/scripting/packaging-plugins.html"
breadcrumb-title: ''
description: 了解如何打包适用于Substance 3D Designer的Python增效工具以进行分发和安装。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Packaging plugins
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 打包插件
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 3%

---


# 打包插件

## 增效工具包内容

包是单个文件，内部为zip存档文件，包含一个&#x200B;**pluginInfo.json**&#x200B;文件，其中包含有关插件的元数据。

插件代码以及插件工作所需的任何其他文件或资源。

**PluginInfo.json条目：**

| 条目 | 描述 | 默认值 | 注释 |
| --- | --- | --- | --- |
| 元数据\_格式\_版本 | 元数据文件的格式。 | 1 | 必需。当前必须设置为1。 |
| 名称 | 插件名称。 |  | 必需。必须与包含插件代码的Python模块的名称匹配 |
| 版本 | 插件版本。 |  | 可选。 |
| 作者 | 插件作者。 |  | 可选。 |
| email | 插件作者的电子邮件。 |  | 可选。 |
| min\_designer\_version | 增效工具工作所需的应用程序的最低版本。 | 2019.2 | 可选。 |
| 平台 | 运行插件的平台。 | 任何 | 可选。对于包含编译代码的插件，此条目可用于在不支持的平台上禁用插件。可能的值： win、linux、osx、any。 |

## 创建新的插件包项目

我们提供了[Cookiecutter](https://cookiecutter.readthedocs.io/en/latest/)模板项目以简化插件包项目的创建。

您可以直接使用它，也可以根据需要进行修改。

可在<b>plugins/tools/pkgplugintemplate</b>下的应用程序目录中找到模板。

1. <b>如果系统中尚未安装Python，请安装它</b>

   Cookiecutter与Python 2和Python 3兼容
1. <b>如果尚未安装Cookiecutter，请安装它</b>

   通常，这可以使用pip来完成：

   ```
   pip install cookiecutter
   ```


   有关安装Cookiecutter的替代方法或有关Cookiecutter的详细信息，请访问<https://cookiecutter.readthedocs.io/en/latest/installation.html>查看文档
1. <b>创建新的插件包项目</b>

   在终端窗口中运行：

   ```
   cookiecutter path/to/pkgplugintemplate -o path/to/new/project
   ```


   填写所需信息。 新项目将在指定目录中创建。
1. <b>开发完成后打包您的插件</b>

   在终端窗口中运行：

   ```
   python makepackage.py
   ```

1. 将在Build目录中生成插件包
