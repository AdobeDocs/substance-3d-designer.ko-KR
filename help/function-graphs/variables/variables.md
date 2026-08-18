---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/variables.html"
breadcrumb-title: ''
description: Substance 3D Designer 함수 그래프에서 변수를 사용하여 값을 효율적으로 저장하고 다시 사용하는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 변수
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# 변수

>[!NOTE]
>
> 변수 노드를 만들고 사용하는 방법에 대한 자세한 내용은 *[변수 노드 섹션](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)*&#x200B;을 참조하세요.

## 정의

프로그래밍에 대한 지식이 거의 없다면 변수의 개념에 익숙할 수 있다.

그렇지 않은 경우 다음과 같은 간단한 정의를 사용합니다.

>[!NOTE]
>
> 변수는 값이 포함된 특정 이름의 &quot;컨테이너&quot;일 뿐입니다.
> 
> 변수에 포함된 값을 이름으로 호출하여 사용할 수 있습니다.

## 변수 유형

Substance 3D Designer에는 Numerics와 Booleans라는 두 가지 변수 패밀리가 있습니다.

## 숫자 변수

숫자 변수는 기본적으로 숫자입니다. 그러나 우리는 두 종류의 숫자 사이에 명확한 구별을 한다:

* 정수 : 0 | 1 | -1 | 203568 등
* 부동: 0.23 | 1.0 | -0.3546 | 등..

>[!WARNING]
>
> Designer은 정수와 부동 소수점 사이를 명확하게 구분합니다. 기본적으로 이러한 정수 및 부동 소수점 사이를 함께 사용할 수는 없습니다.
> 
> *To Integer* 또는 To Float 노드를 사용하여 형식 변환을 수행할 수 있습니다.

### 동일한 변수의 여러 숫자 값

필요에 따라 동일한 변수 내에 최대 4개의 숫자 값을 누적할 수 있습니다.

다시 한 번 모든 값은 동일한 유형에서 가져와야 합니다.

이렇게 하려면 다음 모든 숫자 값 중에서 선택할 수 있습니다.

![](../../assets/image2015-12-18-14-10-36.png)

## 부울

부울은 순수 이진 값이므로 값은 *True* 또는 *False*&#x200B;만 될 수 있습니다(0 또는 1이라고도 함).
