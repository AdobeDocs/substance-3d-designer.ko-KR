---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/scripting/plugin-basics.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 응용 프로그램 기능을 확장하기 위해 Python 플러그인을 만드는 기본 사항을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Plugin basics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 플러그인 기본 사항
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# 플러그인 기본 사항

플러그인은 Python 파일 또는 <b>initializeSDPlugin()</b> 함수를 정의하는 Python 모듈입니다.

플러그인이 로드되면 <b>initializeSDPlugin()</b> 함수가 호출됩니다.\
이 함수에서는 사용자 인터페이스 요소를 만들고 콜백 및 필요한 기타 기능을 등록할 수 있습니다.

선택적으로 플러그인은 플러그인이 언로드될 때 호출되는 <b>uninitializeSDPlugin()</b> 함수를 정의할 수 있습니다.\
이 기능을 사용하여 리소스를 확보하고 네트워크 연결을 닫는 등의 작업을 할 수 있습니다.

```
## Plugin entry point. Called by Designer when loading a plugin.

def initializeSDPlugin(): 

 print("Hello!") 

 

## If this function is present in your plugin,

## it will be called by Designer when unloading the plugin.

def uninitializeSDPlugin(): 

 print("Bye!")
```
