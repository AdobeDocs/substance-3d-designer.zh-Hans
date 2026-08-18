---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/variables/get-a-variable-value.html"
breadcrumb-title: ''
description: 了解如何使用“获取变量”节点在Substance 3D Designer函数图中检索变量值。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Get a variable value
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 获取变量值
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---


# 获取变量值

要在函数中使用变量，您需要“调用”它，即需要将变量的值导入到函数中。

为此，您需要使用&#x200B;*Get*&#x200B;节点：

![](../../../assets/image2015-12-21-7-29-51.png)

有多种不同的Get节点：根据要导入的值类型选择正确的节点：

![](../../../assets/image2015-12-21-7-31-4.png)

## 将变量分配给Get节点

默认情况下， get节点将显示一个警告符号：这意味着它尚未链接到任何变量。

要链接变量，请转到参数，然后在“Variables/Get \*\*\*”列表中选择一个变量（\*\*\*将被替换为Get节点可以调用的值类型）。

变量名称将显示在节点中：

![](../../../assets/assign-getfloat.gif)

请注意，只有来自相同类型的Get节点的变量才会出现在列表中。

>[!WARNING]
>
> 请注意，使用&#x200B;*Set*&#x200B;节点创建的变量将不会出现在&#x200B;*Get*&#x200B;节点列表中。
> 
> 但是，您仍然可以通过在列表中手动写入名称来获取变量。
> 
> 请不要忘记，在以下情况下，您可以调用使用Set节点创建的变量：
> 
> * Get和Set节点位于控制同一节点参数的函数图中
> * 由&#x200B;*Get*&#x200B;节点图形控制的参数可能相同，或者位于参数栈栈中&#x200B;*Set*&#x200B;节点图形的参数下方。
