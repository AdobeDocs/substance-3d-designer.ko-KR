---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-mapper.html"
breadcrumb-title: ''
description: 모양 매퍼 노드를 사용하여 사용자 정의 가능한 변형 및 위치를 사용하여 모양을 텍스처에 매핑할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 모양 매퍼
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---


# 모양 매퍼

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![모양 매퍼 - 아이콘](shape-mapper.resources/shape_mapper.png "모양 매퍼 - 아이콘"){width="200px"}

<b>내부:</b> 텍스처 생성기 > 패턴

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

원 또는 다각형을 따라 입력 이미지를 투영합니다.

이 투영은 이미지가 모양의 윤곽선을 따라 변형되어 간격 없이 지정된 횟수만큼 정확하게 맞도록 합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>입력</b> <i>회색 음영</i> | 모양을 따라 배치해야 하는 패턴입니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>출력</b> <i>회색 음영</i> | 모양을 따라 패턴을 회색 음영 비트맵으로 투영한 결과 |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>모양</b> <i>정수</i> | 패턴을 배치할 모양 유형을 설정합니다.<ul data-preserve-html="true"> <li data-preserve-html="true">원</li> <li data-preserve-html="true">다각형</li> </ul> |
| <b>패턴 양</b> <i>정수</i> | 선택한 모양을 따라 배치된 패턴의 양입니다. |
| <b>패턴 양이 포함된 링크 세그먼트</b> <i>부울</i>   *&#39;모양&#39;이 &#39;다각형&#39;으로 설정된 경우 사용 가능* | <b>패턴 양</b>을 <b>세그먼트</b> 수로 사용합니다.   이렇게 하면 패턴이 모퉁이를 감싸는 것을 방지하여 곧고 일관된 모습을 유지할 수 있습니다. |
| <b>세그먼트</b> <i>정수</i>   *모양&#39;이 &#39;다각형&#39;으로 설정되고 &#39;패턴 양이 있는 링크 세그먼트&#39;가 &#39;거짓&#39;으로 설정된 경우 사용 가능* | 패턴이 배치된 다각형의 선분 양입니다.   선분은 *균일한 크기*&#x200B;이고 모든 정점은 *중심에서 등거리*&#x200B;이므로 선분의 양을 늘리면 다각형이 원 쪽으로 수렴합니다. |
| <b>반경</b> <i>부동</i> | 모양의 반지름에 대한 승수입니다. 여기서 1.0은 이미지의 가장 짧은 쪽 길이의 절반입니다. |
| <b>너비</b> <i>부동</i> | 도형을 따르는 패턴의 너비에 대한 승수입니다. 여기서 1.0은 이미지의 가장 짧은 변의 절반입니다. |
| <b>회전</b> <i>부동</i> | 모양에 적용된 회전의 양(수평 오른쪽으로부터 시계 방향으로 돌아가는 회전의 수)입니다. |
| <b>한 번에 하나씩 뒤집기</b> <i>부울</i> | 모양을 세로로 하나씩 뒤집습니다. |
| <b>필터링 모드</b> <i>정수</i> | 모양을 따라 배치된 패턴에 적용되는 필터링 방법:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>가장 가까운 픽셀:</i> 가장 가까운 투영 픽셀의 값을 그대로 적용하여 보다 선명하면서도 앨리어싱된 모양을 만듭니다.</li> <li data-preserve-html="true"><i>쌍선형:</i> 더 매끄럽지만 흐린 모양을 위해 인접 픽셀과 프로젝션된 픽셀을 보간하는 쌍선형 필터를 적용합니다.</li> </ul> |
| <b>정사각형이 아닌 확장</b> <i>부울</i> | 정사각형이 아닌 이미지에서 생성된 모양을 정사각형으로 유지하고 이미지 생성을 이미지의 경계까지 확장합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
