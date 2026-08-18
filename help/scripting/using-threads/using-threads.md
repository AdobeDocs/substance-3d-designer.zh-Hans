---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/using-threads.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Designer Python脚本中使用线程进行并行处理和性能。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using threads
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用线程
user-guide-description: ''
user-guide-title: ''
source-git-commit: e49409eb4835f6a6c9f17713511e07b7afa38028
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# 使用线程

增效工具可以使用Python的线程模块&#x200B;*或* Qt为Python线程相关类<b>创建线程</b>。

这有助于在Designer运行时执行后台处理或I/O操作。

请务必注意，Designer的Python API中的大多数类和方法只能&#x200B;*从<b>主应用程序线程</b>调用*。 因此，如果要对当前在Designer中打开的任何图表进行任何修改，则必须从主应用程序线程进行修改。

一个可能的解决方案是使用<b>QThread</b>和<b>排队连接</b>，如下例所示：

```
import time 

from PySide2 import QtCore 

 

 

## Our thread object.

class TimerThread(QtCore.QThread): 

    tick = QtCore.Signal() 

 

    def run(self): 

        for i in range(0, 7): 

            print("Emitting signal from thread %s" % QtCore.QThread.currentThread()) 

            self.tick.emit() 

            time.sleep(0.5) 

 

 

## Our receiver object, created on the main thread.

class Receiver(QtCore.QObject): 

    def __init__(self, parent=None): 

        super(Receiver, self).__init__(parent) 

 

    def onTick(self): 

## This is called on the main thread. It is safe to use the sd API here.

        print("Tick received in thread %s" % QtCore.QThread.currentThread()) 

 

 

timer = TimerThread() 

receiver = Receiver() 

 

## Use QtCore.Qt.QueuedConnection to make sure that slots are called on the main thread.

## You can also use QtCore.Qt.BlockingQueuedConnection if you need to block while the slot is called.

timer.tick.connect(receiver.onTick, QtCore.Qt.QueuedConnection) 

 

## Start out thread.

timer.start()
```
