---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-flow-mapper.html"
breadcrumb-title: ''
description: 스플라인 흐름 매퍼 노드를 사용하여 유기 효과를 위한 스플라인 경로를 따라 흐르는 텍스처 패턴을 만듭니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Flow Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스플라인 플로우 매퍼
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---


# 스플라인 플로우 매퍼

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](spline-flow-mapper.resources/spline-flow-mapper-01.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

입력 스플라인을 따라 플로우 벡터 데이터가 그려지는 플로우 맵을 그립니다.

그러면 스플라인을 사용하여 흐름의 방향, 궤적, 강도 및 Thickness을 제어할 수 있을 뿐만 아니라 그린 데이터를 중간색 배경으로 페이드하는 데 사용되는 그레이디언트 경사를 제어할 수 있습니다.

</td>
</tr>
</table>

>[!IMPORTANT]
>
> 그 결과는 매우 낮은 Thickness 값을 사용할 때 스플라인의 엔벌로프 외부에 원하지 않는 아티팩트를 포함할 수 있다. 이것은 알려진 문제입니다.

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>스플라인 코드</b> <i>색상</i> | 색상 이미지의 RGBA 채널로 인코딩된 입력 스플라인의 좌표:<br><b>R</b> - X 위치<br><b>G</b> - Y 위치<br><b>B</b> - Height<br><b>A</b> - 압축된 데이터:<br>- 기호: 스플라인이 닫힘(음수) 또는 열림(양수);<br>- 절대값: Thickness + 1. |
| <b>스플라인 데이터</b> <i>색상</i> | 색상 이미지의 RGBA 채널에 인코딩된 입력 스플라인의 추가 데이터입니다.<br><b>R</b> - 탄젠트 X<br><b>G</b> - 탄젠트 Y<br><b>B</b> - 미사용<br><b>A</b> - 미사용 |
| <b>스플라인 양</b> <i>정수</i> | 입력 스플라인의 수입니다. |
| <b>감쇠 프로파일 곡선</b> <i>회색 음영</i> | <span id="_Hlk135812146"></span>첫 번째 픽셀 행 값을 사용하여 곡선을 설명하는 이미지입니다. 감쇠 프로파일 매개변수가 입력 프로파일 커브로 설정된 경우 이 입력은 스플라인을 따라 그려진 흐름 벡터 데이터의 감쇠를 위한 그레이디언트 경사를 제어하는 데 사용됩니다.<br>곡선을 만드는 데 [곡선](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) 노드를 사용할 수 있습니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>출력</b> <i>색상</i> | 색상 이미지로 인코딩되는 출력 흐름 맵입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>세그먼트 양</b> <i>정수</i> | 스플라인은 벡터 플로우 데이터가 통과하기 전에 세그먼트로 단순화됩니다. 선분의 양이 많을수록 커브를 따라 플로우 매핑이 더 매끄러워집니다. |
| <b>모드</b> <i>정수</i> | 벡터 플로우 데이터를 그릴 스플라인을 선택하는 방법:<br><br>- <i>스플라인 목록 그리기</i>: 입력 목록에 있는 모든 스플라인이 사용됩니다.<br>- <i>단일 스플라인 그리기</i>: 지정된 인덱스가 있는 스플라인만 사용됩니다.<br>- <i>스플라인 범위 그리기</i>: 지정된 범위에 인덱스가 포함된 스플라인만 사용됩니다. |
| <b>스플라인 색인 그리기</b> <i>정수</i>(&#39;모드&#39;가 &#39;단일 스플라인 그리기&#39;로 설정된 경우 사용 가능) | 벡터 흐름 데이터를 그릴 스플라인의 인덱스입니다. |
| <b>스플라인 범위 그리기</b> <i>Integer2</i>(&#39;모드&#39;가 &#39;스플라인 범위 그리기&#39;로 설정된 경우 사용 가능) | 벡터 흐름 데이터를 그릴 스플라인의 인덱스 범위입니다. |
| <b>Thickness 모드</b> <i>정수</i> | 그려진 벡터 플로우 데이터의 Thickness을 설정하는 방법<br><br>- <i>수동</i>: 임의의 값으로 Thickness을 명시적으로 설정합니다.<br>- <i>스플라인에서 설정</i>: 스플라인의 Thickness을 사용합니다. |
| <b>Thickness</b> <i>부동</i>(&#39;Thickness 모드&#39;가 &#39;수동&#39;으로 설정된 경우 사용 가능) | 스플라인을 따라 그려지는 벡터 흐름 데이터의 Thickness에 대한 임의 값입니다. |
| <b>Thickness 승수</b> <i>부동</i>(&#39;Thickness 모드&#39;가 &#39;스플라인부터&#39;로 설정된 경우 사용 가능) | 스플라인을 따라 그려지는 벡터 흐름 데이터의 Thickness에 대한 전역 승수입니다. 이 Thickness이 스플라인의 해당 데이터에 의해 제어됩니다. |
| <b>방향</b> <i>정수</i> | 스플라인을 기준으로 한 벡터 흐름의 방향입니다.<br><br>- <i>탄젠트</i>: 스플라인의 탄젠트 벡터를 사용합니다.<br>- <i>수직</i>: 스플라인의 수직 벡터를 사용합니다.<br>- <i>수직 대칭됨</i>: 스플라인의 수직 벡터의 대칭된 버전을 사용합니다. |
| <b>방향 뒤집기</b> <i>부울</i> | 스플라인의 방향을 반전합니다. 이는 플로우 벡터의 방향에도 영향을 줍니다. |
| <b>감쇠 프로필</b> <i>정수</i> | 스플라인을 따라 그려진 흐름 벡터 데이터의 감쇠를 그리는 데 사용되는 그레이디언트 경사:<br><br>- <i>선형</i>: 선형 그레이디언트 경사 사용;<br>- <i>가우시안</i>: 가우시안 그레이디언트 경사 사용<br>- <i>입력 프로파일 곡선</i>: 감쇠 프로파일 곡선 입력에 제공된 곡선을 그레이디언트 경사로 사용합니다. |
| <b>감쇠 시작</b> <i>부울</i> | <span id="_Hlk135769398"></span>스플라인 시작 부분에 반원을 추가합니다. 반원은 스플라인과 동일한 감쇠를 사용합니다. |
| <b>감쇠 종료</b> <i>부울</i> | 스플라인 끝에 반원을 추가합니다. 반원은 스플라인과 동일한 감쇠를 사용합니다. |
| <b>스플라인 Height 감쇠</b> <i>부동</i> | 스플라인을 따라 그려지는 흐름 벡터 데이터의 강도는 스플라인의 Height에 곱해집니다. 여기서 Height이 0에 가까워지면 그려진 데이터는 배경의 중간 색상(0.5, 0.5, 0)으로 희미해집니다. |
| <b>정사각형이 아닌 수정</b> <i>부울</i> | 점의 위치와 Thickness을 조정하여 정사각형이 아닌 해상도에서 스플라인 모양을 유지합니다. 이는 또한 균일한 분포에도 영향을 미친다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-flow-mapper.resources/spline-flow-mapper-02.jpg" alt="SplineFlowMapper-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="spline-flow-mapper.resources/spline-flow-mapper-03.jpg" alt="SplineFlowMapper-Variant1-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![노드 예 2](spline-flow-mapper.resources/spline-flow-mapper-04.gif "노드 예 2")

</td>
</tr>
</table>
