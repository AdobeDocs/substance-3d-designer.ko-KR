---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-mapper-grayscale.html"
breadcrumb-title: ''
description: 스플라인 매퍼 회색 음영 노드를 사용하여 사용자 정의 가능한 매개 변수를 사용하여 스플라인 패스를 따라 회색 음영 텍스처를 매핑합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스플라인 매퍼 회색 음영
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 0%

---


# 스플라인 매퍼 회색 음영

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](../../../../../../assets/spline-mapper-grayscale-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

입력 스플라인을 따라 뻗은 기본 모양에 입력 회색 음영 이미지를 매핑합니다.

프리미티브 모양은 평면, 반원통 또는 원통일 수 있습니다. 실린더들은 스플라인을 따라 꼬여져서 그에 따라 맵핑된 이미지를 변형시킬 수 있다.

</td>
</tr>
</table>

노드는 매핑된 이미지를 회색 음영 이미지로서 출력할 뿐만 아니라, Height, UV(즉, 이미지 좌표) 및 매핑된 각 스플라인을 독립적으로 선택하기 위한 ID 마스크와 같은 다른 정보를 출력한다.

>[!IMPORTANT]
>
> 그 결과는 매우 낮은 Thickness 값을 사용할 때 스플라인의 엔벌로프 외부에 원하지 않는 아티팩트를 포함할 수 있다. 이것은 알려진 문제입니다.

>[!NOTE]
>
> [스플라인 매퍼 색상](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-color/spline-mapper-color.md)도 참조하세요.

## 입력 커넥터

<b>스플라인 코드</b> *색상*&#x200B;색상 이미지의 RGBA 채널로 인코딩된 입력 스플라인의 점 좌표:\
<b> R</b> - X 위치\
<b> G</b> - Y 위치\
<b> B</b> - Height\
    <b>A</b> - 압축된 데이터:\
        * Sign: 스플라인이 닫히거나(음수) 열림(양수);\
        * 절대값: Thickness + 1.

<b>스플라인 데이터</b> *색상*&#x200B;색상 이미지의 RGBA 채널로 인코딩된 입력 스플라인의 추가 데이터입니다.\
<b> R</b> - 접선 X\
<b> G</b> - 접선 Y\
<b> B</b> - 미사용\
<b> A</b> - 미사용

<b>스플라인 양</b> *정수*&#x200B;입력 스플라인 수입니다.

<b>색상 맵</b> *회색 음영*&#x200B;입력 스플라인을 따라 매핑해야 하는 입력 회색 음영 이미지입니다.

<b>Height 맵</b> *회색 음영*&#x200B;입력 스플라인을 따라 매핑해야 하는 입력 회색 음영 Height 맵입니다.

<b>Twist Curve</b> *회색 음영*&#x200B;첫 번째 픽셀 행 값을 사용하여 곡선을 설명하는 이미지입니다.\
<b>모양</b> 매개 변수를 *반원통* 또는 *원통*(으)로 설정하면 이 입력을 사용하여 모양 주변의 UV 비틀기를 제어합니다. 이 효과는 <b>비틀기 UV 곡선 승수</b> 매개 변수를 사용하여 제어됩니다.\
커브는 스플라인을 따라 회전하는 양에 대한 프로파일을 제공합니다. 여기서 행의 첫 번째 픽셀은 스플라인이 시작될 때의 회전이고 마지막 픽셀은 끝의 회전입니다. 회색 음영 값은 회전 수를 나타냅니다.\
[곡선](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) 노드를 사용하여 곡선을 만들 수 있습니다.

## 출력 커넥터

<b>색상</b> *회색 음영*&#x200B;입력 색상 이미지를 입력 스플라인에 회색 음영 이미지로 매핑한 결과입니다.

<b>Height</b> *회색 음영*&#x200B;입력 스플라인에 입력 Height 이미지를 회색 음영 이미지로 매핑한 결과입니다.

<b>UV</b> *색상*&#x200B;입력 스플라인에 걸친 매핑의 UV(즉, 좌표)로, 색상 이미지로 인코딩됩니다.

<b>ID</b> *회색 음영*&#x200B;입력 스플라인을 따라 매핑되는 이미지의 마스크입니다. 여기서 흰색 값은 각 모양을 개별적으로 선택할 수 있도록 한 스플라인에서 다음 스플라인까지 1씩 증가합니다.

## 매개변수

<b>세그먼트 양</b> *정수*&#x200B;스플라인은 이미지 좌표가 스플라인을 통과하기 전에 세그먼트로 단순화됩니다.\
선분의 양이 많을수록 커브를 따라 매핑이 더 매끄러워집니다.

<b>UV 자동 크기 조정</b> *부울*&#x200B;스플라인을 따라 매핑할 때 정사각형 이미지를 유지하도록 좌표의 비율을 자동으로 조정합니다.<b></b>

<b>UV 비율</b> *Float2*&#x200B;매핑된 좌표의 비율을 X(가로) 및 Y(세로)로 조정합니다.\
값이 높을수록 바둑판식 이미지가 더 조밀하게 표시됩니다.<b></b>

<b>모드</b> *정수*&#x200B;이미지를 매핑할 스플라인을 선택하는 방법:\
*- 스플라인 목록 그리기*: 입력 목록의 모든 스플라인이 사용됩니다.\
*- 단일 스플라인 그리기*: 지정된 인덱스가 있는 스플라인만 사용됩니다.\
*- 스플라인 범위 그리기*: 색인이 지정된 범위에 포함된 스플라인만 사용됩니다.

<b>스플라인 색인 그리기</b> *정수*(&#39;모드&#39;가 &#39;단일 스플라인 그리기&#39;로 설정된 경우 사용 가능)이미지를 매핑해야 하는 스플라인의 인덱스입니다.

<b>스플라인 범위 그리기</b> *정수2*(&#39;모드&#39;가 &#39;스플라인 범위 그리기&#39;로 설정된 경우 사용 가능)이미지를 매핑해야 하는 스플라인의 인덱스 범위입니다.

<b>시작</b> *부동*&#x200B;매핑할 스플라인 부분의 시작을 오프셋합니다.\
값은 스플라인의 정규화된 길이를 나타냅니다.

<b>종료</b> *부동*&#x200B;매핑할 스플라인 부분의 끝을 오프셋합니다.\
값은 스플라인의 정규화된 길이를 나타냅니다.

<b>Thickness 모드</b> *정수*&#x200B;매핑된 이미지의 Thickness 설정 방법:\
*- 수동*: 임의의 값으로 Thickness을 명시적으로 설정합니다.\
*- 스플라인에서*: 스플라인의 Thickness을 사용합니다.

<b>Thickness</b> *부동*(&#39;Thickness 모드&#39;가 &#39;수동&#39;으로 설정된 경우 사용 가능)스플라인을 따라 매핑된 이미지의 Thickness에 대한 임의의 값입니다.<b></b>

<b>Thickness 승수</b> *Float*(&#39;Thickness 모드&#39;가 &#39;스플라인부터&#39;로 설정된 경우 사용 가능)스플라인을 따라 매핑된 이미지의 Thickness에 대한 전역 승수입니다. 해당 Thickness이 스플라인의 에 의해 제어되는 경우.

<b>모양</b> *정수*&#x200B;스플라인을 따라 이미지 좌표를 매핑하는 데 사용되는 기본 모양:\
*- 평면*: 좌표가 평면 평면에 매핑됩니다.\
*- 반원통*: 좌표가 기본 원의 축이 스플라인 방향을 따르는 반원통에 매핑됩니다.\
*- 원통*: 좌표가 기본 원의 축이 스플라인 방향을 따르는 원통에 매핑됩니다.<b></b>

<b>실린더 Height 멀티플라이어</b> *Float*(&#39;모양&#39;이 &#39;절반 실린더&#39; 또는 &#39;실린더&#39;로 설정된 경우 사용 가능)Height 출력에서 실린더의 Height 기여도 강도에 대한 승수입니다.\
Height 조정은 누적됩니다.

<b>실린더 Height 오프셋</b> *부동*(&#39;모양&#39;이 &#39;절반 실린더&#39; 또는 &#39;실린더&#39;로 설정된 경우 사용 가능) \
원통 또는 반원통 모양 프로파일의 중심을 스플라인 서피스에서 서피스 아래의 한 지름으로 오프셋합니다.

<b>UV 강도 비틀기</b> *Float*(&#39;모양&#39;이 &#39;반원통&#39; 또는 &#39;원통&#39;으로 설정되어 있을 때 사용 가능)원통 주위의 이미지 좌표(회전 수)의 트위스트입니다.\
트위스팅은 스플라인 끝에만 있는 원통을 회전하는 것을 포함합니다. 그런 다음 회전은 스플라인을 따라 보간됩니다.

<b>UV 곡선 승수 비틀기</b> *Float*(&#39;Shape&#39;가 &#39;절반 원통&#39; 또는 &#39;원통&#39;으로 설정되어 있을 때 사용 가능)원통 꼬임에 대한 Twist Curve 입력의 기여도 강도에 대한 승수입니다.\
커브는 스플라인을 따라 회전하는 양에 대한 프로파일을 제공합니다. 여기서 행의 첫 번째 픽셀은 스플라인이 시작될 때의 회전이고 마지막 픽셀은 끝의 회전입니다. 회색 음영 값은 회전 수를 나타냅니다.

<b>UV 곡선 오프셋 비틀기</b> *부동*(&#39;도형&#39;이 &#39;반원통&#39; 또는 &#39;원통&#39;으로 설정되어 있을 때 사용 가능)Twist Curve이 제공한 회전 값에 전역 오프셋을 회전 수 단위로 적용합니다.

<b>스플라인 Height 멀티플라이어</b> *부동*&#x200B;스플라인 Height 입력의 Height 출력 기여도 강도를 조정합니다.\
Height 조정은 누적됩니다.<b></b>

<b>입력 Height 승수</b> *부동* Height 출력에 대한 Height 맵 입력의 기여도 강도를 조정합니다.\
Height 조정은 누적됩니다.

<b>정사각형이 아닌 교정&#x200B;</b>*부울*&#x200B;점의 위치와 Thickness을 조정하여 정사각형이 아닌 해상도에서 스플라인 모양을 유지합니다.\
이는 또한 균일한 분포에도 영향을 미친다.

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineMapperColor-Variant1-Before.jpg" alt="SplineMapperColor-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineMapperGrayscale-Variant1-After.jpg" alt="SplineMapperGrayscale-Variant1-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![노드 예 2](../../../../../../assets/SplineMapperGrayscale-Demo.gif "노드 예 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![노드 예 3](../../../../../../assets/SplineMapperGrayscale-Variant1-After1.jpg "노드 예 3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
