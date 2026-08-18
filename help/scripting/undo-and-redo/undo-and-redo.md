---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/undo-and-redo.html"
breadcrumb-title: ''
description: Substance 3D Designer Python 스크립트에서 사용자 동작을 위한 실행 취소 및 다시 실행 기능을 구현하는 방법에 대해 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Undo and redo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 실행 취소 및 다시 실행
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---


# 실행 취소 및 다시 실행

<b>SDHistoryUtils.UndoGroup</b> 클래스를 사용하면 사용자가 하나의 명령에서 모두 *실행 취소 또는 다시 실행*&#x200B;하기 위해 *그룹 작업*&#x200B;을 수행할 수 있습니다.

이러한 그룹은 사용자가 *이름*&#x200B;을 지정하며, 사용자 인터페이스의 실행 취소/다시 실행 목록에 해당 이름으로 표시됩니다.  따라서 많은 수의 작업을 더 쉽게 관리할 수 있습니다.

```
import sd 

from sd.api.sdhistoryutils import * 

 

## Get the application and package manager objects.

cxt = sd.getContext() 

app = cxt.getSDApplication() 

pkgMgr = app.getPackageMgr() 

 

## Group one or more changes into an undo group.

with SDHistoryUtils.UndoGroup("My Undo Group"): 

## Create two new packages.

    pkgMgr.newUserPackage() 

    pkgMgr.newUserPackage()
```
