---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/function-graphs/what-is-a-function.html"
breadcrumb-title: ''
description: Substance 3D Designer에 포함된 기능을 알아보고 이를 사용하여 재사용 가능한 노드 네트워크를 만드는 방법을 살펴보세요.
helpx_creative_field: ""
helpx_description: "Designer > Function graphs > What is a function "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: '기능이란 무엇입니까? '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# 기능이란 무엇입니까?

Substance 3D Designer의 함수를 사용하면 프로그래밍 언어에서 찾을 수 있는 논리를 사용하여 결과를 생성할 수 있습니다.

하지만 Designer의 함수는 코드 줄을 사용하는 대신 동일한 노드 방식을 유지합니다. 언뜻 보기에 함수 그래프는 정규 그래프와 정말 비슷해 보인다.

![](what-is-a-function.resources/image2015-12-17-18-19-37.png)

함수는 다음 두 가지 경우에 나타날 수 있습니다.

* 매개변수 결과 제어
* 픽셀 프로세서를 편집하는 경우

## 매개 변수의 결과 제어

Substance 3D Designer에서 모든 매개 변수는 함수로 제어할 수 있습니다.

![](what-is-a-function.resources/image2015-12-17-21-3-46.png)

따라서 고유한 결과를 얻기 위해 그래프의 부분 사이에 규칙과 종속성을 상상할 수 있습니다.

예를 들어 혼합 노드의 불투명도가 뒤틀기 노드 강도의 절반이 되도록 결정할 수 있습니다.

![](what-is-a-function.resources/warpblend.gif)

실제로 사용자는 이미 기능을 인식하지 못한 채 다음 기능을 만들었을 수 있습니다.

매개변수를 표시한 경우 자동으로 함수 및 변수를 생성했습니다. 함수에는 새로 생성된 변수의 값을 포착하는 get float 노드가 포함되어 있습니다.

![](what-is-a-function.resources/expose.gif)
