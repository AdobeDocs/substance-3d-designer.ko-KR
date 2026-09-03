---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-3.html"
breadcrumb-title: ''
description: 셀 3 노드를 사용하여 유기적 및 생물학적 텍스처 효과를 만들기 위한 중간 세포 패턴을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 셀 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---


# 셀 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![셀 3 - 아이콘](cells-3.resources/cells-3-01.png "셀 3 - 아이콘"){width="200px"}

<b>내부:</b> 텍스처 생성기 > 노이즈

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

<b>셀</b> 벽으로 둘러싸인 노이즈의 변형.

원반이 교차하면 고르지 않은 부드러움의 얇은 벽을 가진 셀이 생성된다.

참고 항목: [셀 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md), [셀 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md), [셀 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

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
| <b>크기 조절</b> <i>정수</i> | 노이즈 타일을 생성하는 데 사용되는 격자의 하위 분할입니다.    값이 높을수록 더 많은 타일이 그려지고 노이즈가 더 많아집니다. |
| <b>경도</b> <i>부동</i> | 값이 높을수록 벽이 더 선명해지고 선명해집니다. |
| <b>반전</b> <i>부울</i> | 이미지 출력의 회색 음영 값을 반전합니다. |
| <b>장애</b> <i>부동</i> | 소음의 성분을 제거합니다.    이 효과를 사용하면 노이즈에 애니메이션을 적용할 수 있습니다. |
| <b>장애 속도</b> <i>부동</i> | <b>Disorder</b> 매개 변수에 의해 적용된 변위의 거리를 조정합니다.    이 효과는 노이즈에 애니메이션을 적용할 때 변위 속도를 제어하는 데 사용할 수 있습니다. |
| <b>장애 비등방성</b> <i>부동</i> | <b>Disorder</b> 매개 변수에 의해 적용된 변위의 방향 범위를 제어합니다. 값이 높을수록 방향이 더 좁고 정의됩니다.    방향은 <b>장애 비등방성 각도</b> 매개 변수에 의해 제어됩니다. |
| <b>장애 비등방성 각도</b> <i>부동</i> | &#39;Disorder 비등방성&#39; 매개 변수가 0이 아닌 경우 <b>Disorder</b> 매개 변수에 의해 적용된 변위의 방향을 제어합니다. |
| <b>패턴 크기</b> <i>Float2</i> | 셀에 있는 분산 디스크의 크기에 대한 승수입니다. 여기서 1.0은 셀의 전체 범위입니다. |
| <b>패턴 크기 조절</b> <i>부동</i> | <b>패턴 크기</b>에 대한 승수입니다. 여기서 1.0은 전체 크기입니다. |
| <b>각도</b> <i>부동</i> | 디스크의 방향을 설정할 때 사용된 각도로, 회전 수로, 수평 오른쪽부터 시작하여 설정합니다. |
| <b>각도 무작위</b> <i>부동</i> | <b>각도</b> 값에 적용되는 최대 무작위 변형 양(회전 수)입니다. |
| <b>타일 오프셋</b> <i>Float2</i> | 노이즈를 렌더링하는 데 사용되는 무한 평면 부분의 위치를 제어합니다. |
| <b>정사각형이 아닌 확장</b> <i>부울</i> | 정사각형이 아닌 이미지에서 생성된 타일 사각형을 유지하고 노이즈 생성을 이미지 경계까지 확장합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![셀 3 - 예 1](cells-3.resources/cells-3-02.png "셀 3 - 예 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![셀 3 - 예 2](cells-3.resources/cells-3-03.gif "셀 3 - 예 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![셀 3 - 예 3](cells-3.resources/cells-3-04.gif "셀 3 - 예 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![셀 3 - 예 4](cells-3.resources/cells-3-05.gif "셀 3 - 예 4"){zoomable="yes"}

</td>
</tr>
</table>
