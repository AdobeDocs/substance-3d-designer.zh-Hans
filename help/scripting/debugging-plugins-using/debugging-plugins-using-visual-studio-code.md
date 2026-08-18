---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/debugging-plugins-using-visual-studio-code.html"
breadcrumb-title: ''
description: 了解如何使用Visual Studio代码调试Substance 3D Designer Python增效工具以实现高效开发。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Debugging plugins using Visual Studio Code
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用Visual Studio代码调试插件
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# 使用Visual Studio代码调试插件

作为许多开发人员的工作流标准，**Visual Studio Code IDE**&#x200B;可用于调试Python插件。

>[!WARNING]
>
> <b>debugpy.listen()</b>方法允许任何能够连接到指定端口的人在调试进程中执行任意代码。
> 
> 因此，应在&#x200B;*安全网络*&#x200B;上&#x200B;*<b>仅</b>*&#x200B;设置并执行调试。

为了设置Visual Studio Code与Substance 3D Designer之间的协同作用，请按照以下步骤操作：

1. 安装&#x200B;**[Visual Studio代码](https://code.visualstudio.com/)**&#x200B;和&#x200B;**[Python扩展](https://marketplace.visualstudio.com/items?itemName=ms-python.python)**。
1. 安装&#x200B;**[调试程序Python模块](https://github.com/microsoft/debugpy)**。

   >[!NOTE]
   >
   > 确保Designer中的Python解释器可以找到“*调试程序*”模块。 最简单的方法是将“*调试*”模块所在的目录添加到&#x200B;**PYTHONPATH**&#x200B;环境变量。 另一种方法是在脚本中修改sys.path ，将路径添加到调试模块。
1. 启动应用程序，打开Python编辑器并&#x200B;**运行以下代码**：

   ```
   import sys 
   
   
   
   debugpy_path = '/path/to/debugpy/module' 
   
   debugpy_port = 5678 
   
   designer_py_interpreter = '/path/to/python/executable/bundled/in/designer' 
   
   
   
   if not debugpy_path in sys.path: 
   
       sys.path.append(debugpy_path) 
   
   
   
   import debugpy 
   
   
   
   debugpy.configure(python=designer_py_interpreter) 
   
   debugpy.listen(debugpy_port)
   ```

1. 在Visual Studio代码中，打开您的项目并创建一个&#x200B;**launch.json**&#x200B;文件。 在文件中添加以下内容：

   ```
   { 
   
       "name": "Attach to Designer", 
   
       "type": "python", 
   
       "request": "attach", 
   
       "port": <port number used in the script above>, 
   
       "host": "127.0.0.1" 
   
   }
   ```

1. 单击<b>调试</b>图标，根据需要创建或编辑调试器配置。
1. 选择&#x200B;**Python：附加到Designer**&#x200B;配置，然后单击&#x200B;**开始调试**。

   您现在应该能够设置断点，逐步执行代码，并使用Visual Studio代码调试器的所有其他功能。
