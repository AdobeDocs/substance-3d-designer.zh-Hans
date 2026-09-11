---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-designer/scripting/creating-user-interface-elements.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer Python增效工具中创建用户界面元素，以获得交互式用户体验。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Creating user interface elements
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 创建用户界面元素
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# 创建用户界面元素

Substance 3D Designer包括<b>Qt For Python</b>。 用户可以使用[UI管理器](../../scripting/scripting-api-reference/scripting-api-reference.md)类为其插件创建<b>菜单</b>、<b>对话框</b>、<b>自定义面板</b>和其他用户界面元素。

在此页面中，您可以找到在Designer中使用Qt for Python的简单示例。

有关Python的Qt的详细信息，请查看官方[文档。](https://doc.qt.io/qtforpython/index.html)

## 创建对话框

```
import sd 

from PySide2 import QtWidgets 

 

## Get the application and the UI Manager.

app = sd.getContext().getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

 

## Create a new dialog. For shortcuts to work correctly

## it is important to parent the new dialog to Designer's main window.

mainWindow = uiMgr.getMainWindow() 

dialog = QtWidgets.QDialog(parent=mainWindow) 

 

## Create a layout and some widgets.

layout = QtWidgets.QVBoxLayout() 

layout.addWidget(QtWidgets.QPushButton("Press Me")) 

dialog.setLayout(layout) 

 

## Show the dialog (non-modal).

dialog.show()
```


### 创建菜单

```
import sd 

from PySide2 import QtWidgets 

 

## Get the application and the UI Manager.

app = sd.getContext().getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

 

## Function that will be called when our menu item is selected.

def sayHello(): 

 print("Hello!") 

 

## Create a new menu.

menu = uiMgr.newMenu(menuTitle="MyMenu", objectName="doc.example.my_menu") 

## Create a new action.

act = QtWidgets.QAction("Hello", menu) 

act.triggered.connect(sayHello) 

 

## Add the action to the menu.

menu.addAction(act)
```


### 创建面板

```
import sd 

from PySide2 import QtWidgets 

 

## Get the application and the UI Manager.

app = sd.getContext().getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

 

## Create a new dock widget.

## The dock identifier is used when saving and restoring dock positions and sizes.

## For this reason, it's important that the identifier is unique.

dock = uiMgr.newDockWidget(identifier="sample.test.dock", title="New Dock") 

 

## Create a layout and add some widgets.

layout = QtWidgets.QVBoxLayout() 

dock.setLayout(layout) 

 

for i in range(0, 5): 

 layout.addWidget(QtWidgets.QPushButton("Button %s" % i))
```


### 在应用程序窗口中创建工具栏

```
import sd 

from PySide2 import QtCore, QtWidgets 

  

## Get the application and the UI Manager.

app = sd.getContext().getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

  

## Get Designer's main window.

mainWindow = uiMgr.getMainWindow() 

 

## Create our toolbar.

toolbar = QtWidgets.QToolBar() 

toolbar.addAction("Tool") 

toolbar.addAction("Bar") 

 

## Add our toolbar to Designer's window.

mainWindow.addToolBar(QtCore.Qt.TopToolBarArea, toolbar) 
```


### 在图形视图中创建工具栏

```
from functools import partial 

import sd 

 

from PySide2 import QtCore, QtGui, QtWidgets 

 

class MyGraphToolBar(QtWidgets.QToolBar): 

    def __init__(self, graphViewID, uiMgr): 

        super(MyGraphToolBar, self).__init__(parent=uiMgr.getMainWindow()) 

 

## Save the graphViewID and uiMgr for later use.

        self.__graphViewID = graphViewID 

        self.__uiMgr = uiMgr 

 

## Add actions to our toolbar.

        act = self.addAction("P") 

        act.setToolTip("Print the selected nodes to the Python console") 

        act.triggered.connect(self.__onPrintNodes) 

 

    def __onPrintNodes(self): 

        for node in self.__getSelectedNodes(): 

            print(node) 

 

    def __getSelectedNodes(self): 

## Use our saved graphViewID to retrieve the graph selection.

        return self.__uiMgr.getGraphSelectedNodesFromGraphViewID( 

            self.__graphViewID) 

 

def onNewGraphViewCreated(graphViewID, uiMgr): 

## Create our toolbar.

    toolbar = MyGraphToolBar(graphViewID, uiMgr) 

 

## Add our toolbar to the graph widget.

    uiMgr.addToolbarToGraphView( 

        graphViewID, 

        toolbar, 

        icon = None, 

        tooltip = "My Graph Toolbar") 

 

## Get the application and UI manager object.

ctx = sd.getContext() 

app = ctx.getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

 

## Register a callback to know when GraphViews are created.

uiMgr.registerGraphViewCreatedCallback( 

    partial(onNewGraphViewCreated, uiMgr=uiMgr))
```


### 在图形视图工具栏中创建动作

```
from functools import partial 

import sd 

  

from PySide2 import QtWidgets 

 

 

class MyGraphAction(QtWidgets.QAction): 

    def __init__(self, graphViewID, uiMgr): 

        super(MyGraphAction, self).__init__(parent=uiMgr.getMainWindow()) 

 

## Save the graphViewID and uiMgr for later use.

        self.__graphViewID = graphViewID 

        self.__uiMgr = uiMgr 

 

## Set up the action.

        self.setText("P") 

        self.setToolTip("Print the selected nodes to the Python console") 

        self.triggered.connect(self.__onPrintNodes) 

 

    def __onPrintNodes(self): 

        for node in self.__getSelectedNodes(): 

            print(node) 

  

    def __getSelectedNodes(self): 

## Use our saved graphViewID to retrieve the graph selection.

        return self.__uiMgr.getGraphSelectedNodesFromGraphViewID( 

            self.__graphViewID 

        ) 

 

 

def onNewGraphViewCreated(graphViewID, uiMgr): 

## Create our action.

    action = MyGraphAction( 

        graphViewID = graphViewID, 

        uiMgr = uiMgr 

    ) 

  

## Add our action to the graph toolbar.

    uiMgr.addActionToGraphViewToolbar( 

        graphViewID, 

        action 

    ) 

  

 

## Get the application and UI manager object.

ctx = sd.getContext() 

app = ctx.getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

  

## Register a callback to know when GraphViews are created.

uiMgr.registerGraphViewCreatedCallback( 

    partial(onNewGraphViewCreated, uiMgr=uiMgr))
```


### 加载使用Qt Designer创建的用户界面

>[!NOTE]
>
> Qt Designer *不包括*&#x200B;在Substance 3D Designer中。 您可以通过为操作系统安装官方Qt分发版来获得。

```
from PySide2 import QtCore, QtWidgets, QtUiTools 

 

def loadUiFile(filename, parent=None): 

    ''' 

    Loads a Qt Designer .ui file. 

    Returns a widget. 

    ''' 

    loader = QtUiTools.QUiLoader() 

    uifile = QtCore.QFile(filename) 

    uifile.open(QtCore.QFile.ReadOnly) 

    ui = loader.load(uifile, parent) 

    uifile.close() 

    return ui 

 

## Get the application and the UI Manager.

app = sd.getContext().getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

 

## Load our Qt Designer ui file.

widget = loadUiFile("MyUI.ui", parent=uiMgr.getMainWindow()) 

 

## Show our user interface. In this case we show it as a non-modal dialog,

## but we could also make it modal or create a new dock for it.

widget.show()
```
