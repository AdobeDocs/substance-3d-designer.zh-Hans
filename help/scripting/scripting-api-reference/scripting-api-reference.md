---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/scripting/scripting-api-reference.html"
breadcrumb-title: ''
description: 访问完整的Substance 3D Designer Python脚本API参考，了解增效工具开发。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Scripting API reference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 脚本API参考
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '1251'
ht-degree: 0%

---


# 脚本API参考

本页介绍API的主要概念。

有关更多详细信息，请参阅应用程序附带的文档，可在<b>帮助> Python API文档……</b>中访问这些文档。在本文档中，对模块名称（位于下方的括号中）执行<b>快速搜索</b>以轻松查找其定义。

## 上下文

上下文(*Context*)对象是API</b>的<b>主要入口点。 它是用户第一次使用“*sd*”模块中的方法“<b>*getContext()*</b>”获取它时创建的。

此对象允许实质上<b>检索应用程序</b> (*SDApplication*)对象。

## 应用程序(SDApplication)

应用程序(*SDApplication*)是允许<b>访问主API管理器</b>的对象，例如：

* 管理应用程序所有<b>包</b>的<b>包</b>管理器(*SDPackageMgr*)；
* 管理应用程序所有<b>模块</b>的<b>模块</b>管理器(*SDModuleMgr*)；
* <b>UI </b>管理器(*SDUIMgr*)，可以在应用程序窗口中创建<b>菜单和停靠站</b>。

可以在发生某些事件时调用的应用程序中注册<b>回调</b>。

## 包管理器(SDPackageMgr)

此对象管理应用程序的所有包<b>包</b>。 包显示在“<b>*资源管理器*</b>”组件中。

通过它，您可以：

* <b>创建</b>新包；
* <b>加载/卸载</b>包；
* <b>保存</b>包；
* <b>查找</b>包。

## 包(SDPackage)

包(*SDPackage*)是<b>资源集合</b> (*SDResource*)。

包的内容可以通过“*SDPackageMgr*”对象<b>存储</b>到扩展名为<b>.sbs</b>的文件。 此对象允许您<b>检索</b>特定资源。

要<b>创建</b>特定资源，请参阅相关对象静态方法(例如：“*SDSBSCompGraph.sNew()*”)。

软件包还包含元数据词典(SDMetadataDict)。 您可以在[此处](../../package-metadata/package-metadata.md)找到有关元数据的更多信息。

## 资源(SDResource)

资源(*SDResource*)是可由其他资源<b>引用</b>的对象。

有多个资源<b>类型</b>：

* 文件夹(*SDResourceFolder*)；
* 图形(*SDGraph*)；
* 位图(*SDResourceBitmap*)；
* SVG图像(*SDResourceSVG*)；
* 字体(*SDResourceFont*)；
* 场景(*SDResourceScene*)；
* BSDF测量(*SDResourceBSDFMeasurement*)；
* 光源配置文件(*SDResourceLightProfile*)。

资源可以从以下项下的静态方法“*sNew()*”中<b>创建</b>：

* 一个包裹；
* 文件夹。

一个资源可以有多个<b>属性</b> (*SDProperty*)。

## UI管理器(SDUIMgr)

UI管理器允许<b>在Substance Designer的主窗口（如<b>菜单</b>、<b>停靠站</b>）中创建用户界面元素</b>，并允许在发生用户界面相关事件时调用<b>回调</b>。

此外，UI管理器有权访问<b>当前活动图形</b>和活动图形<b>选区</b>。

## 图形(SDGraph)

图形(*SDGraph*)是包含以下内容的对象：

* <b>节点</b>(*SDNode*)；
* <b>图形对象</b> (*SDGraphObjects*)；
* <b>属性</b>(*SDProperty*)。

图形类型有4种：

* 图形(*SDSBSCompGraph*)
* 函数图形(*SDSBSFunctionGraph*)Substance
* FXMap图形(*SDSBSFxMapGraph*)Substance

一个图形可以有一个或多个<b>输出</b>节点。 输出节点表示图形的<b>结果</b>。

图形的所有可用节点都可以使用“*getNodeDefinitions()*”方法<b>检索</b>。

可以使用方法“*newNode()*”创建<b>新节点</b>。

可以使用方法“*newInstanceNode()*”从资源(*SDResource*)创建新的<b>实例</b>节点。

## 节点(SDNode)

节点(*SDNode*)表示对对象执行的<b>操作</b>。

可从以下位置创建它：

* <b>定义</b> (*SDDefinition*) (请参见“*SDGraph.newNode()”*)；
* <b>资源</b> (*SDResource*) (请参见“*SDGraph.newInstanceNode()”*)。

一个节点可以有多个<b>属性</b>。

节点有多个<b>类型</b>：

* *<b>SDSBSCompNode</b>*：Substance 图形的节点(*SDSBSCompGraph*)；
* *<b>SDSBSFunctionNode</b>*：Substance 函数图形的节点(*SDSBSFunctionGraph*)；
* *<b>SDSBSFxMapNode</b>*：SubstanceFXMap图形(*SDSBSFxMapGraph*)的节点；

## 图形对象(SDGraphObjects)

图形对象(*SDGraphObject*)是<b>向图形添加附加信息</b>的对象，但在图形评估过程中&#x200B;<b>*未*&#x200B;将其考虑在内</b>。

图形对象有<b>3种类型</b>：

* <b>大头针</b> (*SDGraphObjectPin*)
* <b>注释</b> (*SDGraphObjectComment*)
* <b>帧</b> (*SDGraphObjectFrame*)

请参阅这些对象上的静态方法“*sNew()*”，以了解有关如何<b>创建</b>这些对象的详细信息。

## 属性(SDProproperty)

属性(*SDProperty*)是<b>描述</b>了<b>另一个对象</b>（图形、节点、资源等）的属性。

它属于特定的<b>类别</b> (*SDPropertyCategory*)：

* <b>输入</b>：分类对象的输入属性，通常<b>会影响当前对象执行的操作</b>；
  * 例如：图形中统一颜色节点的属性“*color*”是输入属性；
* <b>输出</b>：分类对象的输出属性。 它用于标识对象的<b>结果</b>；
* <b>批注</b>：将&#x200B;<b>*不*&#x200B;影响由对象执行的操作</b>的属性分类；
  * 例如：图形的“*标签*”是批注属性，因为它不影响图形计算。

它包含以下<b>成员</b>：

* <b>Id</b>：属性在其类别上下文中的标识符；
* <b>类型</b>：当前属性支持的类型。 某些属性可以支持&#x200B;*多个*&#x200B;类型：“*int*”、“*float*”等；
  * 例如：“*sbs：:function:：add*”节点的输入属性可以支持不同的类型：“*int”*、“*int2”*、“*int3”*、“*int4”*、“*float”*、“*float2”*、“*float3”*、“*float4”等；*
* <b>类别</b>：属性所属的类别（输入、输出、批注）；
* <b>标签</b>：属性的标签，仅用于显示&#x200B;**；
* <b>描述</b>：属性的描述；
* <b>DefaultValue</b>：默认值；
* <b>IsConnectable</b>：指示是否可以对此属性执行连接(*SDConnection*) *SDConnection*；
* <b>isReadyOnly</b>：指示属性是否为只读。 如果为true，则与其关联的值&#x200B;*不*&#x200B;可修改；
* <b>isVariadic</b>：如果为true，则此属性将被表示为对象上的&#x200B;*多个*&#x200B;属性；
* <b>isPrimary</b>：指示指定的属性是否为控制某些其他属性的&#x200B;*主体*&#x200B;属性。 *注意：*&#x200B;此操作特定于Substance *合成*&#x200B;节点(*SDSBSCompNode*)。

示例：

* “*sbs：:compositing:：input*”节点的属性：

<table data-preserve-html="true"><colgroup><col style="width: 276.0px;"/><col style="width: 129.0px;"/><col style="width: 283.0px;"/></colgroup><tbody><tr><th colspan="3" style="text-align: center;">sbs：:compositing:：input</th></tr><tr><td style="text-align: left;"><strong>输入</strong></td><td style="text-align: left;"><strong>注释</strong></td><td style="text-align: left;"><strong>输出</strong></td></tr><tr><td>$outputsize</td><td>标签</td><td><p>unique_filter_output （可连接）</p></td></tr><tr><td>$format</td><td>描述</td><td><br/></td></tr><tr><td>$pixelsize</td><td>标识符</td><td><br/></td></tr><tr><td>$pixelration</td><td>userdata</td><td><br/></td></tr><tr><td>$拼贴</td><td>群组</td><td><br/></td></tr><tr><td>$randomseed</td><td>visibleif</td><td><br/></td></tr><tr><td><p>bitmapresourcepath</p></td><td>使用情况</td><td><br/></td></tr></tbody></table>

* “*sbs：:compositing:：blend*”节点的属性：

<table data-preserve-html="true"><colgroup><col style="width: 278.0px;"/><col style="width: 129.0px;"/><col style="width: 283.0px;"/></colgroup><tbody><tr><th colspan="3" style="text-align: center;">sbs：:compositing:：blend</th></tr><tr><td style="text-align: left;"><strong>输入</strong></td><td style="text-align: left;"><strong>注释</strong></td><td style="text-align: left;"><strong>输出</strong></td></tr><tr><td>$outputsize</td><td><br/></td><td>unique_filter_output （可连接）</td></tr><tr><td>$format</td><td><br/></td><td><br/></td></tr><tr><td>$pixelsize</td><td><br/></td><td><br/></td></tr><tr><td>$pixelration</td><td><br/></td><td><br/></td></tr><tr><td>$tiling</td><td><br/></td><td><br/></td></tr><tr><td>$randomseed</td><td><br/></td><td><br/></td></tr><tr><td>source.连接器（可连接）</td><td><br/></td><td><br/></td></tr><tr><td><p>destination.连接器（可连接）</p></td><td><br/></td><td><br/></td></tr><tr><td>不透明度。连接器（可连接）</td><td><br/></td><td><br/></td></tr><tr><td>不透明度多项</td><td><br/></td><td><br/></td></tr><tr><td colspan="1">混合模式</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr><tr><td colspan="1">colorblending</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr><tr><td colspan="1">蒙版矩形</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr></tbody></table>

## 类型(SDType)

类型(*SDType*)包含值<b>类型</b>的信息，例如：

* <b>Id</b>：类型的标识符；
* <b>Modifier</b>：类型修饰符，可以是“*SDTypeModifier”* <b>枚举</b>值之一：
  * *自动*；
  * *统一*：每个操作计算值&#x200B;*一次*；
  * *变化*：每个操作计算值&#x200B;*次*（例如：每个纹理）。

定义了多种类型，例如：

* <b>枚举</b> (*SDTypeEnum*)：描述一个<b>枚举</b>类型及其所有属性；
* <b>结构</b> (*SDTypeStruct*)：描述一个<b>结构</b>类型及其所有属性；
* <b>数组</b> (*SDTypeArray*)：描述<b>数组</b>。
* 等。

有关详尽列表，请参阅Substance Designer的&#x200B;*Python API文档*。

## 值(SDValue)

值(*SDValue*)是<b>将</b>封装为&#x200B;*基类型*&#x200B;值的对象。

例如：

* “<b>*SDValueInt*</b>”对象封装“*int*”值；
* “<b>*SDValueFloat4*</b>”对象封装“*float4*”值；
* 等。

基类型值通常可以是使用“<b>get()</b>”方法检索的<b></b>，但此值可以取决于已返回的“*SDValue“*”的&#x200B;*类型*。

## 连接(SDConnection)

连接(*SDConnection*)表示两个不同<b>节点</b>的两个不同<b>属性</b>之间的<b>链接</b>。

它包含：

* <b>目标节点</b>；
* 目标节点的<b>目标属性</b>；

所有<b>连接操作</b>都在节点上执行：

* <b>正在创建</b>新连接，请参阅“*SDNode.newPropertyConnection()*”
* <b>删除</b>现有连接，请参阅“*SDNode.deletePropertyConnection()*”
* <b>检索</b>属性的连接，请参阅“*SDNode.getPropertyConnections()*”

## 模块(SDModule)

模块是<b>定义和类型的集合</b>。

它允许方便地检索有关可创建的节点以及枚举和结构的所有信息。

它包含：

* 在模块管理器(*SDModuleMgr*)的上下文中唯一的<b>标识符</b> (*Id*)；
* <b>定义</b>的列表(*SDDefinition*)；
* <b>类型</b>的列表(*SDType*)。

## 定义(SDDefinition)

定义(*SDDefinition*)对象包含有关基于<b>属性</b> （“*SDNode“*”等）的特定<b>对象</b>的定义的信息。

它包含：

* <b>Id</b>：定义的标识符；
* <b>标签</b>：定义的标签；
* <b>描述</b>：定义的描述；
* <b>属性</b>：所有可用属性&#x200B;*类别*&#x200B;的属性(*SDPropertyCategory*)。
