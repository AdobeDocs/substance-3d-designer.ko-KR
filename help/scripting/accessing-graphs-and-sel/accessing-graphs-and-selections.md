---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/scripting/accessing-graphs-and-selections.html"
breadcrumb-title: ''
description: Substance 3D Designer Python 스크립트의 그래프와 노드 선택에 액세스하고 조작하는 방법에 대해 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Accessing graphs and selections
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 그래프 및 선택 영역 액세스
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# 그래프 및 선택 영역 액세스

<b>SDApplication</b> 클래스에는 *현재 활성* 그래프와 그 안의 *현재 선택*&#x200B;에 액세스할 수 있는 유용한 메서드가 포함되어 있습니다.

```
import sd 

 

## Get the application and UI manager object.

ctx = sd.getContext() 

app = ctx.getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

 

## Get the current graph.

g = uiMgr.getCurrentGraph() 

print("The current graph is %s" % g) 

 

## Get the currently selected nodes.

selection = uiMgr.getCurrentGraphSelectedNodes() 

for node in selection: 

 print("Node %s" % node)
```


<b>graphViewID</b>을(를) 사용하여 *특정* 그래프 보기에 표시된 그래프에 액세스할 수 있습니다.

이 방법은 사용자 정의 그래프 보기 도구 모음을 만들 때 유용합니다. 자세한 내용은 [사용자 인터페이스 요소 만들기](../../scripting/creating-user-interface/creating-user-interface-elements.md) 장의 <b>그래프 보기에서 도구 모음 만들기</b> 샘플을 참조하십시오.
