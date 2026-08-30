---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/2d-view/color-sampler.html"
breadcrumb-title: ''
description: 2D 보기에서 색상 Sampler 도구를 사용하여 정밀한 색상 일치를 위해 텍스처의 색상을 샘플링합니다.
helpx_creative_field: ""
helpx_description: Designer > Interface > 2D view > Color sampler tool
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 색상 샘플러 도구
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---


# 색상 샘플러 도구

![색상 샘플러 도구](color-sampler.resources/color-sampler-demo.png "색상 샘플러 도구"){zoomable="yes"}

Color Sampler 도구를 사용하면 매개 변수를 조정하거나 노드를 전환할 때 [2D 보기](../../../interface/2d-view/2d-view.md)에서 <b>특정 픽셀의 값을 추적</b>할 수 있습니다.

이렇게 하면 뷰포트에 핀을 배치하고 해당 위치의 픽셀 색상 및 위치를 샘플링합니다.

## 도구 사용

도구에 액세스하고 사용하려면 다음 단계를 따르십시오.

1. 2D 보기 도구 모음에서 ![](color-sampler.resources/color-sampler-information-button.png) <b>정보</b> 단추를 클릭하여 정보 도킹 및 도구 모음을 엽니다
1. 정보 도구 모음에서 ![](color-sampler.resources/color-sampler-tool-icon.png) <b>색상 Sampler 도구</b> 단추를 클릭합니다.
1. 뷰포트에서 샘플링할 특정 픽셀을 클릭하여 ![](color-sampler.resources/color-sampler-pin-icon.png) <b>핀</b>을 배치합니다.
1. 정보 도킹의 전용 섹션에서 샘플 값을 검토합니다.
1. 도구 사용이 완료되면 ![](color-sampler.resources/color-sampler-remove-pin.png) <b>삭제</b> 단추를 클릭하여 뷰포트에서 핀을 제거합니다.\
   RMB를 클릭하고 컨텍스트 메뉴에서 &#39;삭제&#39; 동작을 선택하여 핀을 제거할 수도 있습니다.

다음은 작동 중인 도구의 데모입니다.

![색상 샘플러: 도구 사용](color-sampler.resources/color-sampler-demo.gif "색상 샘플러: 도구 사용"){zoomable="yes"}

*확대하려면 클릭*

+++샘플링된 RGBA 값 복사
핀에 있는 RMB를 클릭하고 상황에 맞는 메뉴에서 &#39;RGBA 값 복사&#39; 동작을 선택하여 샘플 값을 복사할 수 있습니다.

복사한 값은 <b>색상 축소판을 사용하여 매개 변수에 붙여넣기</b>할 수 있습니다.

[정보] 패널의 색상 썸네일을 이러한 매개 변수의 색상 썸네일로 직접 드래그하여 놓을 수도 있습니다.

![색상 샘플러: RGBA 값 복사](color-sampler.resources/color-sampler-demo-copy-rgba-values.gif "색상 샘플러: RGBA 값 복사"){zoomable="yes"}



*확대하려면 클릭*

+++

## 샘플링된 정보

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

정보는 세 가지 유형 및 두 가지 형식으로 그룹화됩니다.

* 이미지의 각 RGBA 채널에 저장된 <b>샘플 값</b>:\
  가변\* / 부동 소수점
* HSV 표현의 <b>샘플 색상</b>:\
  8비트 정수/부동 소수점
* 픽셀 수 및 정규화된 이미지 공간에서 픽셀의 <b>위치</b>:\
  정수/부동 소수점

</td>
<td width="33.33%" style="border: 0;" valign="top">

![샘플 정보](color-sampler.resources/color-sampler-information.png "샘플 정보"){zoomable="yes"}

</td>
</tr>
</table>

값은 이미지에서 사용하는 비트 심도에 따라 달라집니다. Substance 그래프에서 비트 심도는 <b>출력 형식</b>으로 제어됩니다 [기본 매개 변수](../../../compositing-graphs/graph-parameters/graph-parameters.md).

사용 가능한 비트 심도는 다음과 같습니다.

* <b>8비트 정수:</b> 0에서 255까지의 256개 정수 값.
* <b>16비트 정수:</b> 0에서 65,535까지의 65,536개 정수 값.
* <b>HDR 낮은 정밀도(16비트)</b>: 16비트를 사용하여 인코딩된 부동 소수점 값.
* <b>HDR 고정밀(32비트)</b>: 32비트를 사용하여 인코딩된 부동 소수점 값. 이는 Designer에서 사용할 수 있는 가장 높은 정밀도입니다.
