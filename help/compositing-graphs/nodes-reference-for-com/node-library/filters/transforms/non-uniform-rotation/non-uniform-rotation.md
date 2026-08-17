---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-uniform-rotation.html"
breadcrumb-title: ''
description: 나선형 및 소용돌이 효과를 만들기 위한 균일하지 않은 회전 변형을 적용하려면 [균일하지 않은 회전] 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Uniform Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 균일하지 않은 회전
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---


# 균일하지 않은 회전

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotationgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotationcolor.png){width="200px"}

</td>
</tr>
</table>

**내부:** 필터*/변환*

**중간**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 설명

**비균일 회전** 노드는 **회전 맵** 입력을 사용하여 **입력**&#x200B;을 회전합니다.

이미지의 값은 *회전 수*&#x200B;를 나타냅니다. 회전은 **피벗 위치** 값 또는 **피벗 위치 맵** 입력에 의해 지정된 위치를 중심으로 수행됩니다.\
**회전 맵** 입력에서 양수 값을 입력하면 *시계 방향* 회전이 발생합니다.

</td>
</tr>
</table>

## 매개변수

### 입력

* **입력** *회색 음영/색상*\
  회전해야 하는 입력 회색 음영 이미지.
* **회전 맵** *회색 음영*&#x200B;회전량을 제어하는 데 사용되는 맵입니다. *회전 수*. 샘플링된 값은 **회전 각도 승수**&#x200B;에 대해 곱해집니다. 음수 값을 사용하면 *시계 반대 방향* 회전이 발생합니다.
* **회전 피벗 위치 맵** *색상*\
  회전 *피벗*&#x200B;의 위치를 지정하는 데 사용되는 이미지입니다. **X/Y** 위치가 이미지의 **R/G** 채널에 매핑됩니다.

### 매개변수

* **회전 각도 배수** *부동*\
  **회전 맵** 입력의 강도를 조정합니다.
* **회전 각도 오프셋** *부동*\
  지정된 추가 회전 양을 적용합니다.
* **피벗 위치 맵 사용** *부울*\
  *비트맵 입력*&#x200B;을 사용하여 회전 피벗의 위치를 지정하십시오. **X/Y** 위치가 **위치 맵** 입력의 **R/G** 채널에 매핑됩니다.
* **피벗 위치** *부동 소수점2*\
  이미지가 회전하는 피벗의 위치입니다.
* **배경색** *부동/부동 소수점4*\
  타일링이 **H 및 V 타일링**&#x200B;으로 설정되지 않은 경우 이미지 경계의 *외부*&#x200B;에 표시할 배경색입니다.
* **필터링 모드** *정수*\
  픽셀 간에 *보간*&#x200B;할 때 샘플링된 결과를 처리하는 방법을 정의합니다.
  * *가장 가까운*: 정확히 *같은* 값을 샘플링합니다(더 빠름).
  * *쌍선형*: *더 매끄럽게* 모양을 위해 결과에 쌍선형 필터를 적용합니다.

## 예제 이미지

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-demo-02-resized.gif){width="768px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-variant-png.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-node.png){width="256px"}

</td>
</tr>
</table>
