---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/scripting/using-threads.html"
breadcrumb-title: ''
description: Aprenda a utilizar subprocesos en las secuencias de comandos de Substance 3D Designer Python para el procesamiento y el rendimiento en paralelo.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using threads
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Uso de subprocesos
user-guide-description: ''
user-guide-title: ''
source-git-commit: e49409eb4835f6a6c9f17713511e07b7afa38028
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# Uso de subprocesos

Es posible que los complementos <b>creen subprocesos</b> mediante el módulo de subprocesos de Python *o* Qt para las clases relacionadas con subprocesos de Python.

Esto puede resultar útil para realizar operaciones de E/S o procesamiento en segundo plano mientras se ejecuta Designer.

Es importante tener en cuenta que la mayoría de las clases y métodos de la API Python de Designer *solo* se pueden llamar desde el <b>subproceso de aplicación principal</b>. Por lo tanto, si desea realizar cualquier modificación en cualquier gráfico que esté abierto actualmente en Designer, debe realizarlas desde el subproceso de la aplicación principal.

Una posible solución es usar <b>QThread</b> y <b>conexiones en cola</b>, como en el siguiente ejemplo:

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
