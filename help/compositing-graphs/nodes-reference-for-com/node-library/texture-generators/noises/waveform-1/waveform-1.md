---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/waveform-1.html"
breadcrumb-title: ''
description: 파형 1 노드를 사용하면 유기 텍스처 및 프로시저 변형을 만들기 위한 파형 패턴을 생성할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Waveform 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 파형 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 1%

---


# 파형 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![파형 1 - 아이콘](waveform-1.resources/waveform_01_v2.png "파형 1 - 아이콘"){width="200px"}

<b>내부:</b> 텍스처 생성기 > 노이즈

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

파형과 유사한 모양으로 스택된 사용자 선택 패턴의 가로 배열입니다.

</td>
</tr>
</table>

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>출력</b> <i>회색 음영</i> | 회색 음영 비트맵으로 생성된 노이즈 |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>샘플</b> <i>정수</i> | 파형을 그리기 위해 X축을 따라 배치되는 패턴의 양입니다. 값이 낮을수록 더 단조로운 모양이 됩니다. |
| <b>함수</b> <i>정수</i> | 파형을 그리는 데 사용되는 함수입니다.   이는 각 샘플에 있는 패턴의 세로 크기를 제어합니다.<ul data-preserve-html="true"> <li data-preserve-html="true"><i>값 노이즈:</i> 값의 임의 분포</li> <li data-preserve-html="true"><i>코사인:</i> 값이 코사인 함수의 진행률을 따릅니다.</li> <li data-preserve-html="true"><i>사용자 지정 함수:</i> 사용자가 작성한 함수를 사용하여 값을 실행하십시오</li> </ul> |
| <b>사용자 지정 함수</b> <i>부동</i>   *&#39;함수&#39;가 &#39;사용자 지정 함수&#39;로 설정된 경우 사용 가능* | 각 샘플에 배치된 패턴의 세로 크기를 계산합니다.   사용 가능한 변수:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>pos</b>(<i>부동</i>) X축의 패턴 위치입니다. 이는 패턴을 선택하는 데 사용될 수 있다.</li> </ul> |
| <b>거칠음</b> <i>부동</i> | 좀 더 거칠고 고르게 분포된 청정하고 매끄러운 파형 사이에 보간합니다.    이는 깨끗한 신호 대 백색 잡음으로 생각할 수 있다. |
| <b>크기 조절</b> <i>정수</i> | 이미지에 표시되는 파형의 가로 범위입니다. |
| <b>최소 진폭</b> <i>부동</i> | 파형의 최소값(또는 Thickness)입니다. |
| <b>최대 진폭</b> <i>부동</i> | 파형의 최대값(또는 Thickness)입니다. |
| <b>노이즈</b> <i>부동</i> | 파형의 세로 범위에서 임의로 제거하는 파형에 노이즈를 적용합니다. |
| <b>위치</b> <i>정수</i> | 이미지의 파형 위치:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>가운데:</i> 원점은 이미지의 세로 중앙에 있습니다</li> <li data-preserve-html="true"><i>아래쪽:</i> 원점은 이미지의 아래쪽입니다</li> </ul> |
| <b>패턴</b> <i>정수</i> | 파형의 각 샘플에 배치된 패턴입니다. |
| <b>패턴 변형</b> <i>부동</i> | 일부 패턴에 사용할 수 있는 추가 조정입니다. |
| <b>장애</b> <i>부동</i> | 파형 값을 변위합니다.    이 효과를 사용하여 애니메이션을 적용할 수 있습니다. |
| <b>장애 속도</b> <i>부동</i> | <b>Disorder</b> 매개 변수에 의해 적용된 변위의 거리를 조정합니다.    파형에 애니메이션을 적용할 때 변위 속도를 제어하는 데 사용할 수 있습니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![파형 1 - 예 1](waveform-1.resources/waveform_01_v2_speed0.1_aniso0.gif "파형 1 - 예 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
