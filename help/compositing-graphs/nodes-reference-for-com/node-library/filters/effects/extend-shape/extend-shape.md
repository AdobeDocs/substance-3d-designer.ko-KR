---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/extend-shape.html"
breadcrumb-title: ''
description: Extend Shape 노드를 사용하여 모양을 경계 너머로 확장하여 확장된 마스크 및 패턴 효과를 만듭니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Extend Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extend Shape
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---


# Extend Shape

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshapegrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshapecolor.png){width="200px"}

</td>
</tr>
</table>

**인:** 필터*/효과*

**단순**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 설명

**Extend Shape** 노드는 **입력**&#x200B;의 *섹션*&#x200B;을(를) 설정된 방향과 거리 위로 확장합니다.

**Show helper** 매개 변수를 사용하면 확장된 섹션 및 확장 방향을 시각화할 수 있습니다.

</td>
</tr>
</table>

## 매개변수

* **모드** *정수*&#x200B;확장을 적용하는 데 사용되는 *매개 변수*&#x200B;를 정의합니다.
  * *양방향*: **확장 위치** 및 **확장 각도**&#x200B;에 지정된 **입력**&#x200B;의 섹션이 *반대 방향*&#x200B;으로 **확장 거리**&#x200B;에 걸쳐 확장되었습니다.
  * *단방향*: **확장 위치** 및 **확장 각도**&#x200B;로 지정된 **입력**&#x200B;의 섹션이 *단일 방향*&#x200B;으로 **확장 거리**&#x200B;에 걸쳐 확장됩니다.
  * *시작/끝 위치*: *벡터* 확장명은 **시작 위치** 및 **끝 위치**&#x200B;로 정의됩니다. **시작 위치**&#x200B;에 있는 **입력**&#x200B;의 *수직* 섹션이 **종료 위치**&#x200B;까지 이 벡터&#x200B;*에 대해*&#x200B;확장됩니다.
* **확장 거리** *부동&#x200B;***확장 위치** 및 **확장 각도**&#x200B;에 의해 지정된 구간보다 긴 거리를 늘려야 합니다. 거리는 이미지 범위의 *비율*&#x200B;로 표시됩니다.
* **확장 위치** *부동*&#x200B;확장 가능한 섹션 이미지의 위치입니다. 값은 *가운데에서 오프셋*(으)로 표시됩니다.
* **확장 각도** *부동*&#x200B;시작점을 고려하여 확장되어야 하는 섹션의 각도는 *수직 섹션*&#x200B;입니다.
* **시작 위치** *Float2*&#x200B;확장 벡터&#x200B;*의 시작 위치입니다.*
* **종료 위치** *Float2**확장 벡터*&#x200B;의 종료 위치입니다.
* **시작 광도 오프셋** *부동*&#x200B;확장 섹션의 *이전* 이미지 영역에 광도 오프셋을 적용합니다. 이 광도 오프셋은 *섹션을 따라 보간됨*&#x200B;을 섹션 다음에 오는 이미지 영역의 광도로 보간합니다.\
  *참고*: 이 매개 변수는 노드의 **회색 음영** 버전에서만 사용할 수 있습니다.
* **광도 오프셋 종료** *부동*&#x200B;확장 섹션을 *다음* 이미지 영역에 광도 오프셋을 적용합니다. 이 광도 오프셋은 *섹션을 따라 보간됨*&#x200B;을 섹션 앞에 있는 이미지 영역의 광도로 보간합니다.\
  *참고*: 이 매개 변수는 노드의 **회색 음영** 버전에서만 사용할 수 있습니다.
* **룸. 오프셋은 검정 픽셀을 무시합니다** *부울&#x200B;**True*(으)로 설정된 경우 *6&rbrace;**&#x200B;광도 오프셋 시작&#x200B;**및&#x200B;**&#x200B;광도 오프셋 종료**에 지정된 광도 오프셋은*&#x200B;검정이 아닌&#x200B;*픽셀, 즉 0보다 큰 픽셀에만 적용됩니다.*\
  *참고*: 이 매개 변수는 노드의 **회색 음영** 버전에서만 사용할 수 있습니다.
* **필터링 모드** *정수*&#x200B;픽셀 간에 *보간*&#x200B;할 때 샘플링된 결과를 처리하는 방법을 정의합니다.
  * *가장 가까운*: 정확히 *같은* 값을 샘플링합니다(더 빠름).
  * *쌍선형*: *더 매끄럽게* 모양을 위해 결과에 쌍선형 필터를 적용합니다.
* **도우미 표시** *부울*&#x200B;확장의 *방향*&#x200B;을 보여주는 화살표를 사용하여 *확장된 섹션*&#x200B;을 오버레이로 시각화합니다.

## 예제 이미지

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-node.png){width="360px"}

</td>
</tr>
</table>
