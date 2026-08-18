---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/scripting/creating-user-interface-elements.html"
breadcrumb-title: ''
description: Substance 3D Designer Python 플러그인에서 인터랙티브한 사용자 경험을 위한 사용자 인터페이스 요소를 만드는 방법에 대해 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Creating user interface elements
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 사용자 인터페이스 요소 만들기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# 사용자 인터페이스 요소 만들기

Substance 3D Designer에는 Python용 <b>Qt</b>가 포함됩니다. 사용자는 [UI 관리자](../../scripting/scripting-api-reference/scripting-api-reference.md)클래스를 사용하여 플러그인에 대한 <b>메뉴</b>, <b>대화 상자</b>, <b>사용자 지정 패널</b> 및 기타 사용자 인터페이스 요소를 만들 수 있습니다.

이 페이지에서는 Designer 내에서 Python용 Qt를 사용하는 간단한 예를 확인할 수 있습니다.

Python용 Qt에 대한 자세한 내용은 공식 [설명서](https://doc.qt.io/qtforpython/index.html)를 확인하십시오.

## 대화 상자 만들기

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


### 메뉴 만들기

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


### 패널 만들기

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


### 응용 프로그램 창에서 도구 모음 생성

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


### 그래프 보기에서 도구 모음 만들기

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


### 그래프 보기 도구 모음에서 작업 만들기

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


### Qt Designer을 사용하여 생성된 사용자 인터페이스 로드

>[!NOTE]
>
> Qt Designer이 Substance 3D Designer에 *포함되지 않음*&#x200B;입니다. 운영 체제에 대한 공식 Qt 배포를 설치하면 얻을 수 있습니다.

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
