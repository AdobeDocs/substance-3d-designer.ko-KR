---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/scripting/logging.html"
breadcrumb-title: ''
description: Substance 3D Designer Python 플러그인에 로그인하여 디버깅 및 모니터링하는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Logging
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 로깅
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 4%

---


# 로깅

로깅에는 표준 Python 로깅 모듈을 사용하는 것이 좋습니다.

<b>sd</b> 모듈에는 로깅을 Designer 콘솔로 리디렉션하는 도우미 클래스가 포함되어 있습니다.

## Designer 콘솔 패널에 로깅

```
import logging 

import sd 

 

 

## Create a logger.

logger = logging.getLogger("MyLogger") 

 

 

## Add a handler to redirect logging to Designer's console panel.

ctx = sd.getContext() 

logger.addHandler(ctx.createRuntimeLogHandler()) 

 

 

## Do not propagate log messages to Python's root logger.

logger.propagate = False 

 

 

## Set the default log level if needed.

logger.setLevel(logging.DEBUG) 

 

 

## Use the logger

logger.info("Info message") 

logger.warning("Warning message") 

logger.error("Error message")
```
