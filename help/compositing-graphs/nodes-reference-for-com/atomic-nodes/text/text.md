---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/text.html"
breadcrumb-title: ''
description: 텍스트 기반 패턴을 만들기 위해 텍스트 노드를 사용하여 사용자 정의 가능한 글꼴과 스타일로 텍스트 텍스처를 생성할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Text
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 텍스트
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---


# 텍스트

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomic node: Text](text.resources/comp_text_1.png "Atomic node: Text"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

텍스트 노드는 사용자가 만든 텍스트를 그래프에 배치하는 방법을 제공합니다. 사용자는 글꼴, 정렬 및 회전과 같은 설정을 선택하여 텍스트 배치를 사용자 정의할 수도 있습니다.

텍스트 노드는 매우 강력하며 텍스트를 쉽게 배치할 수 있는 유일한 방법입니다. 배치는 항상 제한된 정사각형 캔버스에서 이루어지며 글꼴은 시스템에서 정의된 외부 목록에 의해 구동되므로 다소 사용하기 어려울 수 있습니다.

</td>
</tr>
</table>

Truetype(.ttf) 및 특정 Opentype 글꼴만 지원됩니다. 목록에서 누락된 글꼴이 있는 경우, 그 때문일 수 있습니다. <b>글꼴을 매개 변수로 표시할 수 없습니다.</b>

텍스트를 사용하는 그래프가 sbsar에 게시되면 글꼴이 모든 시스템 및 응용 프로그램에서 작동하도록 비트맵 및 기타 리소스와 마찬가지로 패키지에 포함됩니다.

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

## 출력 커넥터

</td>
<td style="border: 0;" valign="top">

### 예

</td>
</tr>
</table>

## 매개변수

|  |  |
| --- | --- |
| <b>색상 모드</b> *부울* | 회색 음영과 색상 출력 이미지 사이를 전환합니다. |
| <b>텍스트</b> *문자열* | 텍스트 설명을 결정합니다. |
| <b>글꼴</b> *문자열* | 텍스트를 렌더링하는 데 사용되는 글꼴 리소스입니다. |
| <b>글꼴 크기</b> *부동* | 텍스트의 글꼴 크기(포인트 단위)입니다. |
| <b>맞춤</b> *정수* | 텍스트 정렬을 왼쪽, 가운데(기본값) 또는 오른쪽으로 설정합니다. |
| <b>변환</b> *Float4* | 렌더링된 텍스트에 적용된 2x2 변형 행렬입니다. |
| <b>위치</b> *Float2* | 출력 이미지에서 텍스트의 위치입니다. |
| <b>배경</b> *Float/Float4* | 출력 이미지의 배경색입니다. |
| <b>글꼴 색상</b> *Float/Float4* | 텍스트의 색상입니다. |

## 입력 커넥터

|  |  |
| --- | --- |
| <b>배경</b> 기본 *회색 음영/색상* | 출력 이미지의 배경색입니다. |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *회색 음영/색상* |  |

## 예

*곧 출시 예정*
