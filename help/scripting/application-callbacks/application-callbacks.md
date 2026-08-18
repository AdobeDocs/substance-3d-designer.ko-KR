---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/scripting/application-callbacks.html"
breadcrumb-title: ''
description: Substance 3D Designer Python 플러그인의 애플리케이션 콜백을 사용하여 애플리케이션 이벤트에 응답하는 방법에 대해 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Application callbacks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 응용 프로그램 콜백
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---


# 응용 프로그램 콜백

특정 이벤트가 발생할 때 Designer에서 호출할 응용 프로그램 개체에 <b>파이썬 콜백</b>을 등록할 수 있습니다.

메뉴 및 단추와 같은 사용자 인터페이스 개체는 <b>Qt for Python</b> 라이브러리를 사용하여 콜백을 트리거할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소 만들기](../../scripting/creating-user-interface/creating-user-interface-elements.md)를 참조하세요.

```
import sd 

 

## Our callbacks.

def onBeforeFileLoadedCallback(filePath): 

    print("Before file loaded, file: %s" % filePath) 

 

def onAfterFileLoadedCallback(filePath, succeed, updated): 

    print("After file loaded, file: %s, succeed: %s, updated: %s" % (filePath, succeed, updated)) 

     

def onBeforeFileSavedCallback(filePath, parentPackagePath): 

    print("Before file saved, file: %s, parentPackage: %s" % (filePath, parentPackagePath)) 

 

def onAfterFileSavedCallback(filePath, succeed): 

    print("After file saved, file: %s, succeed: %s" % (filePath, succeed)) 

 

## Get the application.

app = sd.getContext().getSDApplication() 

 

## Register our callbacks.

beforeFileLoadedCallbackID = app.registerBeforeFileLoadedCallback(onBeforeFileLoadedCallback) 

afterFileLoadedCallbackID = app.registerAfterFileLoadedCallback(onAfterFileLoadedCallback) 

beforeFileSavedCallbackID = app.registerBeforeFileSavedCallback(onBeforeFileSavedCallback) 

afterFileSavedCallbackID = app.registerAfterFileSavedCallback(onAfterFileSavedCallback) 

 

## Unregister callbacks when no longer needed.

app.unregisterCallback(beforeFileLoadedCallbackID) 

app.unregisterCallback(afterFileLoadedCallbackID) 

app.unregisterCallback(beforeFileSavedCallbackID) 

app.unregisterCallback(afterFileSavedCallbackID)
```
