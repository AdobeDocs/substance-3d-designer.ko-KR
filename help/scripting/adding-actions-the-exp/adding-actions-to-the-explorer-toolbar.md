---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/adding-actions-to-the-explorer-toolbar.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 Python 스크립팅을 사용하여 탐색기 도구 모음에 사용자 정의 동작을 추가하는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Adding actions to the Explorer toolbar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 탐색기 도구 모음에 동작 추가
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 0%

---


# 탐색기 도구 모음에 동작 추가

플러그인은 <b>SDUIMgr</b> 클래스에서 사용할 수 있는 콜백과 메서드를 사용하여 *사용자 지정 동작*&#x200B;을 <b>탐색기</b> 도구 모음에 추가할 수 있습니다.

## 샘플 탐색기 도구 모음 작업 플러그인

```
import sd 

 

import os 

from functools import partial 

 

from PySide2 import QtWidgets 

 

explorerCreatedCallbackID = None 

explorerSelectionChangedCallbackIDs = [] 

 

def onActionTriggered(explorerID, uiMgr): 

    '''Called when the user clicks on the toolbar icon.''' 

 

    print("Selected items:") 

    print("---------------") 

    for item in uiMgr.getExplorerSelection(explorerID): 

        print(item) 

    print("n") 

 

def explorerSelectionChanged(explorerID, uiMgr, action, originalExplorerID): 

    '''Called when the selection in the explorer panel changes.''' 

 

## Ignore callbacks for other explorer panels.

    if explorerID != originalExplorerID: 

        return 

 

    print("Explorer selection changed, id = %s" % explorerID) 

 

## Enable or disable the action depending on the explorer selection.

    selection = uiMgr.getExplorerSelection(explorerID) 

    action.setEnabled(len(selection) != 0) 

 

def explorerCreated(explorerID, uiMgr): 

    '''Called when a new explorer panel is created.''' 

 

    print("Explorer created, id = %s" % explorerID) 

 

## Warning: It is important to parent the action to some Qt object.

## If the action is not parented, Python will garbage collect it.

    act = QtWidgets.QAction("P", parent=uiMgr.getMainWindow()) 

    uiMgr.addActionToExplorerToolbar(explorerID, act) 

    act.setToolTip("Print explorer selection to the console") 

    act.triggered.connect(partial(onActionTriggered, explorerID=explorerID, uiMgr=uiMgr)) 

 

## Register a selection changed callback to update the action enabled state.

    global explorerSelectionChangedCallbackIDs 

    explorerSelectionChangedCallbackIDs.append(uiMgr.registerExplorerSelectionChangedCallback( 

        partial(explorerSelectionChanged, uiMgr=uiMgr, action=act, originalExplorerID=explorerID))) 

 

## Set initial enabled / disabled state.

    explorerSelectionChanged(explorerID, uiMgr, act, explorerID) 

 

def initializeSDPlugin(): 

    ctx = sd.getContext() 

    app = ctx.getSDApplication() 

    uiMgr = app.getQtForPythonUIMgr() 

 

## Register an explorer created callback to add actions to newly created explorer toolbars.

    global explorerCreatedCallbackID 

    explorerCreatedCallbackID = uiMgr.registerExplorerCreatedCallback(partial(explorerCreated, uiMgr=uiMgr)) 

 

def uninitializeSDPlugin(): 

    ctx = sd.getContext() 

    app = ctx.getSDApplication() 

    uiMgr = app.getQtForPythonUIMgr() 

 

## Unregister all callbacks.

    global explorerCreatedCallbackID 

    uiMgr.unregisterCallback(explorerCreatedCallbackID) 

 

    global explorerSelectionChangedCallbackIDs 

    for callbackID in explorerSelectionChangedCallbackIDs: 

        uiMgr.unregisterCallback(callbackID)
```
