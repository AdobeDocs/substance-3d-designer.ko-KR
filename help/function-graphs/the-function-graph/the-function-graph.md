---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/function-graphs/the-function-graph.html"
breadcrumb-title: ''
description: Designer에서 사용자 정의 함수 및 재사용 가능한 노드 네트워크를 만들기 위한 Substance 함수 그래프에 대해 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Substance function graphs > The Substance function graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance 함수 그래프
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---


# Substance 그래프와의 유사점

언뜻 보기에 Substance 함수 그래프는 Substance 그래프와 정말 비슷하고 작업 과정도 거의 비슷하다.

![Substance 함수 그래프](../../assets/image2015-12-18-11-29-28.png "Substance 함수 그래프")

## 탐색은 유사합니다.

Substance 함수 그래프에서는 Substance 그래프와 같은 방법으로 노드를 만들고 구성할 수 있습니다.

다음과 같은 방법으로 노드에 액세스할 수 있습니다.

* 라이브러리에서
* 스페이스바 또는 Tab 키를 눌러
* 마우스 오른쪽 단추를 클릭하고 노드 추가 메뉴를 사용합니다.

### 작업 과정은 유사합니다.

Substance 그래프와 마찬가지로 일련의 노드를 연쇄적으로 연결하여 함수를 만듭니다. 각 노드는 이전 노드에서 생성한 결과를 사용합니다.

출력은 파라미터의 값 또는 픽셀 프로세서 노드의 출력을 정의할 것이다.

## Substance 그래프와의 차이

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 노드

Substance 함수 그래프에서 사용 가능한 노드는 Substance 그래프에서 나타나는 노드와 완전히 다르다.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Substance 함수 그래프 노드 목록](../../assets/image2015-12-18-13-46-55.png "Substance 함수 그래프 노드 목록")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 출력

Substance 그래프와는 반대로 함수는 오직 하나의 출력만을 가질 수 있다.

또한 최종 결과를 연결할 특정 출력 노드가 없다는 점도 유의해야 합니다. 대신 원하는 결과를 생성하는 노드, 즉 출력으로 직접 플래그를 지정할 수 있습니다.

</td>
<td style="border: 0;" valign="top">

![Substance 함수 그래프의 출력 노드](../../assets/image2015-12-18-13-49-43.png "Substance 함수 그래프의 출력 노드")

</td>
</tr>
</table>

#### 출력 노드를 정의하는 방법

출력을 정의하려면 원하는 출력을 생성하는 노드를 마우스 오른쪽 단추로 클릭하고 *출력 노드로 설정:*&#x200B;을 클릭하십시오.

![출력 노드 정의](../../assets/setoutputnode.gif "출력 노드 정의")

>[!WARNING]
>
> <b>생성된 결과 형식을 다시 확인하십시오</b>
> 
> *출력 노드로 설정*&#x200B;이 회색으로 표시되면 노드에서 생성된 값이 매개 변수 또는 픽셀 프로세서에서 예상한 값과 다르다는 의미입니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Substance 그래프의 경우 다른 그래프에서 만든 함수를 가져올 수 있습니다. 마우스 오른쪽 버튼으로 클릭하여 참조 그래프를 열고 &quot;참조 열기&quot;를 선택할 수 있습니다.

</td>
<td style="border: 0;" valign="top">

![참조된 Substance 함수 그래프 열기](../../assets/image2017-6-27-10-44-55.png "참조된 Substance 함수 그래프 열기")

</td>
</tr>
</table>

여러 함수가 포함된 sbs가 있는 경우 sbs를 Substance 함수 그래프로 바로 끌어 놓고 표시 목록에서 가져올 함수를 선택할 수 있습니다.

![패키지에서 Substance 함수 그래프 삭제](../../assets/sbsdrag.gif "패키지에서 Substance 함수 그래프 삭제")
