---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/input.html"
breadcrumb-title: ''
description: 입력 노드를 사용하여 사용자가 표시하고 조정할 수 있는 Substance 그래프에 대한 입력 매개변수를 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Input
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 입력
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---


# 입력

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Atomic node: 입력 색상](input.resources/comp_inputcolor_1.png "Atomic node: 입력 색상"){width="200px"}

</td>
<td style="border: 0;" valign="top">

![원자 노드: 입력 회색 음영](input.resources/comp_inputgrayscale_1.png "원자 노드: 입력 회색 음영"){width="200px"}

</td>
<td style="border: 0;" valign="top">

![Atomic node: 입력 값](input.resources/comp_inputnumeric_1.png "Atomic node: 입력 값"){width="200px"}

</td>
</tr>
</table>

입력 노드는 그래프에 동적 슬롯을 만드는 특수한 유형의 노드로서, 그래프를 다른 컨텍스트에서 사용하면 모든 입력을 연결할 수 있습니다.

[출력 노드](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)와 달리 색상, 회색 음영 또는 값 입력을 명시적으로 배치해야 합니다. 자신에게 연결된 것에 따라 유형이 변하는 자신만의 &#39;불가지론적&#39; 입력을 만들 수 없다.

입력 노드는 [출력 노드](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)만큼 중요하지 않습니다. 입력이 필요 없는 완벽한 기능의 고급 그래프를 사용할 수 있습니다. 입력은 그래프 또는 노드 인스턴스의 결과를 외부 입력(예: Substance 3D Painter에 대한 [인스턴스](../../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)또는 [필터](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/effects/filter)를 만들 때)을 기반으로 하려는 경우에만 사용됩니다.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 파라미터

</td>
<td style="border: 0;" valign="top">

### 속성

</td>
<td style="border: 0;" valign="top">

### 상속

</td>
<td style="border: 0;" valign="top">

### 통합 속성

</td>
</tr>
</table>

## 매개변수

기본적으로 아무 것도 연결되어 있지 않으면 [입력 색상] 또는 [회색 음영]이 검정을 반환합니다. 다른 기본값을 설정하거나 기존 [비트맵 리소스](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)를 [탐색기](../../../../interface/the-explorer-window/the-explorer-window.md)에서 그래프의 입력 노드로 드래그하여 이 데이터를 슬롯에서 미리 볼 수 있습니다. 이 옵션은 색상 및 회색 음영 입력에만 사용할 수 있습니다. 다른 컨텍스트에서 사용할 경우 기본값은 지속적이며 미리 보기 비트맵은 다른 컨텍스트에서는 모두 삭제됩니다.

다른 그래프의 출력에서 이 그래프를 확인하려면 위의 방법을 위해 해당 그래프를 비트맵으로 내보내거나 &quot;직접&quot; 편집을 사용해야 합니다.

|  |  |
| --- | --- |
| <b>패키지 리소스 경로</b> *문자열* | 미리 보기를 위한 사용자 정의 비트맵 리소스를 가리킵니다. |
| <b>기본값</b> *색상/회색 음영/값* | 이 슬롯에 아무것도 연결되어 있지 않은 경우 검정색 이외의 다른 값을 기본 입력으로 사용할 수 있습니다. |

## 특성

|  |  |
| --- | --- |
| <b>식별자</b> *문자열* | 유일한 필수 고유 속성입니다. 공백을 포함할 수 없습니다.   이 레이블은 설정된 레이블이 없는 경우 입력에 레이블을 지정하고 다른 출력을 구분하는 데 사용됩니다. &quot;input\_1&quot;에 그대로 두지 마십시오. |
| <b>설명</b> *문자열* | Designer 라이브러리 및 Painter 선반에 사용되는 선택적 설명입니다. |
| <b>레이블</b> *문자열* | Designer 및 Painter UI에서 멋진 레이블 지정에 사용되는 UI 레이블 공백을 포함할 수 있습니다.   밑줄 대신 스페이스바를 사용하여 식별자와 유사한 이름으로 설정하는 것이 좋습니다. |
| <b>사용자 데이터</b> *문자열* | 특정 필터링 작업에 사용할 수 있는 선택적 사용자 데이터(기본적으로 와일드카드 사용자 정의 데이터 필드)입니다. |
| <b>그룹</b> *문자열* | Designer의 [링크 만들기 모드](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)에 대한 입력을 함께 그룹화하는 데 사용되는 그룹 특성입니다.   동일한(대/소문자 구분) 그룹 속성을 가진 입력은 컴팩트 재질 모드에서 단일 연결로 표시됩니다. |

## 상속

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

여러 입력이 있는 경우 이러한 입력에서 그래프가 [기본 매개 변수를 상속](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)하는 방법에 주의해야 합니다.\
기본 매개 변수에는 특히 <b>출력 크기</b>, <b>출력 형식</b> 및 <b>타일링 모드</b>가 포함됩니다.

</td>
<td width="33.33%" style="border: 0;" valign="top">

[![Substance 그래프의 기본 입력](input.resources/node-primary-input.png)](https://helpx.adobe.com/Primary%20input%20in%20Substance%20graph)

</td>
</tr>
</table>

입력을 [기본 입력](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)(으)로 정의할 수 있습니다. 그러면 이 입력은 상속 메서드가 *부모에 대해*(으)로 설정된 모든 입력의 특성을 구동합니다. 입력 노드에서 기본적으로 설정된 *상속 메서드*&#x200B;입니다.

노드에서 *RMB*&#x200B;을 클릭하고 컨텍스트 메뉴에서 <b>기본 입력으로 설정</b> 옵션을 선택하여 입력 노드를 그래프의 기본 입력으로 설정할 수 있습니다.\
노드의 기본 입력은 커넥터에서 *작은 어두운 점*&#x200B;으로 표시됩니다(이 섹션 옆의 예에서 빨간색으로 동그라미 표시됨).

또는 *입력 기준* 상속 메서드에 대한 모든 입력 집합은 기본 입력의 *관계*&#x200B;에 관계 없이 연결된 노드의 특성을 상속합니다.

마지막으로 상속 메서드를 *절대*(으)로 설정하여 지정된 특성의 값을 재정의할 수 있습니다.

>[!TIP]
>
> 상속에 대해 자세히 알아보려면 이 설명서의 [Substance 그래프의 상속](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) 페이지로 이동하십시오.

>[!IMPORTANT]
>
> 입력 노드에 대한 *입력 기준* 상속 메서드는 [Substance 3D 에셋(SBSAR)](https://helpx.adobe.com/substance-3d-assets.html)에서 *지원되지 않음*&#x200B;입니다. 패키지를 게시하기 전에 모든 입력 노드의 상속 메서드를 *부모에 대한 상대*(으)로 설정하십시오.

## 통합 특성

입력은 3D 보기로 직접 전송되지 않지만 해당 사용 특성은 [Substance 3D Painter](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/home)에서 특정 맵으로 슬롯을 자동으로 채우는 데 사용됩니다(대부분 [필터](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/effects/filter)와 함께 사용됨).

또한 올바른 입력 및 출력 슬롯과 일치하도록 [링크 만들기 모드](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)에서도 사용 특성이 사용됩니다.

<b>사용</b>

|  |  |
| --- | --- |
| <b>구성 요소</b> *문자열* | 이 옵션은 결과 입력에 실제로 있는 채널을 결정합니다.   이는 통합 및 그래프에서 더 이상 사용되지 않는 레거시 설정입니다. |
| <b>사용</b> *문자열* | 이 입력의 유형 또는 용도를 정의합니다. 다른 노드가 이 입력에 연결하는 방법을 나타냅니다. |
| <b>색상 공간</b> *문자열* | 이 입력을 해석해야 하는 색상 공간을 설정합니다. |
