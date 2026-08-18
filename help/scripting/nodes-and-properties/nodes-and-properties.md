---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/nodes-and-properties.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer Python增效工具中创建和操纵节点和属性。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Nodes and properties
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 节点和属性
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 1%

---


# 节点和属性

[SDNode](../../scripting/scripting-api-reference/scripting-api-reference.md)类使用户能够获取有关特定节点的信息，可使用[SDProperty](../../scripting/scripting-api-reference/scripting-api-reference.md)*<b></b>*类访问哪些属性。 所有这些都可以读取或修改。

可用的节点信息包括：

* 定义
* 标识符
* 位置
* 定界框
* 属性（作为列表）
* 正在引用的资源

## 访问节点及其属性

```
import sd 

## Import the required classes.

from sd.api.sdproperty import SDPropertyCategory 

from sd.api.sdvalueserializer import SDValueSerializer 

  

## Get and print information regarding the selected nodes.

def printSelectedNodesInfo(nodes): 

    for node in nodes: 

        definition = node.getDefinition() 

        nodeId = node.getIdentifier() 

  

        print("node %s, id = %s" % (definition.getLabel(), nodeId)) 

  

## Create a list of each property category enumeration item.

        categories = [ 

            SDPropertyCategory.Annotation, 

            SDPropertyCategory.Input, 

            SDPropertyCategory.Output 

        ] 

  

## Get node properties for each property category.

        for category in categories: 

            props = definition.getProperties(category) 

  

## Get the label and identifier of each property.

            for prop in props: 

                label = prop.getLabel() 

                propId = prop.getId() 

  

## Get the connection for the currently accessed property.

                if prop.isConnectable(): 

                    connections = node.getPropertyConnections(prop) 

  

                    if connections: 

                        print("Propery %s is connected!!!" % label) 

                        continue 

  

## Get the current and default values for the currently accessed property.

                value = node.getPropertyValue(prop) 

                valueDefault = prop.getDefaultValue() 

     

                value = SDValueSerializer.sToString(value) if value else "None" 

                valueDefault = SDValueSerializer.sToString(valueDefault) if valueDefault else "None" 

 

                print("Property - %sn  id = %sn  value = %sn  default = %s" % ( 

                    label, 

                    propId, 

                    value, 

                    valueDefault 

                 ))
```


### 访问节点输入标识符和类型

```
import sd 

## Import the required classes.

from sd.api import sduimgr 

from sd.api.sdproperty import * 

 

## Access a node in the current graph, and its properties.

graph = uiMgr.getCurrentGraph() 

node = graph.getNodeFromId('<Replace this text with the node ID>') 

nodeProps = node.getProperties(SDPropertyCategory.Input) 

 

## List node identifiers and types in console.

for i in range(len(nodeProps)): 

 print(nodeProps[i].getId()) 

 print(nodeProps[i].getType())
```


### 访问节点位置和定界框

```
import sd



app = sd.getContext().getSDApplication()



uiMgr = app.getUIMgr()

currentGraph = uiMgr.getCurrentGraph()



## Works reliably if there is only one Graph View

currentGraphViewID = uiMgr.getGraphViewIDAt(0)



for node in currentGraph.getNodes():

    

## Position is accessed directly through the node

    nodePosition = node.getPosition()

## Bbox is accessed through the UI manager and the Graph View ID

    nodeBbox = uiMgr.getGraphNodeBBox(currentGraphViewID, node)

    

    print(f"""

    

{node.getDefinition().getLabel().upper()}

  UID: {node.getIdentifier()}

  Position:

    * Center X: {nodePosition.x}

    * Center Y: {nodePosition.y}

  Bounding box:

    * Top-left X: {nodeBbox.x}

    * Top-left Y: {nodeBbox.y}

    * Width: {nodeBbox.z}

    * Height: {nodeBbox.w}

""")
```
