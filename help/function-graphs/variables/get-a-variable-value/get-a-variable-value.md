---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/function-graphs/variables/get-a-variable-value.html"
breadcrumb-title: ''
description: 변수 가져오기 노드를 사용하여 Substance 3D Designer 함수 그래프에서 변수 값을 검색하는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Get a variable value
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 변수 값 가져오기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---


# 변수 값 가져오기

함수에 변수를 사용하려면 변수를 &quot;호출&quot;해야 합니다. 즉, 변수의 값을 함수로 가져와야 합니다.

이렇게 하려면 *Get* 노드를 사용해야 합니다.

![](get-a-variable-value.resources/get-a-variable-value-01.png)

Get 노드에는 다양한 종류가 있습니다. 가져올 값의 유형에 따라 적절한 노드를 선택하십시오.

![](get-a-variable-value.resources/get-a-variable-value-02.png)

## Get 노드에 변수 할당

기본적으로 get 노드에는 경고 부호가 표시됩니다. 이는 아직 어떤 변수에도 연결되어 있지 않음을 의미합니다.

변수를 연결하려면 매개 변수로 이동하여 &quot;Variables/Get \*\*\*&quot; 목록에서 변수를 하나 선택합니다(\*\*\*는 Get 노드가 호출할 수 있는 값 유형으로 바뀝니다).

변수 이름이 노드에 표시됩니다.

![](get-a-variable-value.resources/get-a-variable-value-03.gif)

Get 노드 유형과 동일한 유형의 변수만 목록에 나타납니다.

>[!WARNING]
>
> *Set* 노드로 생성된 변수는 *Get* 노드 목록에 나타나지 않습니다.
> 
> 그러나 목록에 이름을 수동으로 기록하면 변수를 가져올 수 있습니다.
> 
> 다음과 같은 경우 Set 노드로 생성된 변수를 호출할 수 있습니다.
> 
> * Get 및 Set 노드는 동일한 노드의 매개변수를 제어하는 함수 그래프에 있습니다
> * *Get* 노드 그래프에서 제어하는 매개 변수가 매개 변수 스택에서 *Set* 노드 그래프의 매개 변수 아래에 있거나 동일합니다.
