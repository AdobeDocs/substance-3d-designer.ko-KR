---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/shape-light.html"
breadcrumb-title: ''
description: 모양 조명 노드를 사용하여 독특한 조명 효과를 주기 위해 HDRI 환경에 사용자 정의 모양의 광원을 추가합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Shape Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 도형 조명
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---


# 도형 조명

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-shape.png){width="200px"}

## 도형 조명

**내부:** *3D 보기/HDRI 도구*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

구형으로 투영된 직사각형 모양을 생성합니다. 모양 변형은 변형 기즈모 로 구동됩니다.

## 입력

* **배경 이미지 입력**: *색상 입력*&#x200B;생성된 빛을 구성할 선택적 배경입니다.
* **모양 이미지 입력**: *색상 입력*&#x200B;구면 빛에 매핑할 선택적 이미지. [모양 색상 모드]가 [이미지 입력]으로 설정된 경우에만 사용됩니다.

## 매개변수

* **모양 매트릭스**
  * **행렬**: *(변환 행렬)*\
    결과에 대한 변형 컨트롤입니다. 캔버스와 직접 상호 작용하여 결과를 수정할 수 있습니다.
  * **오프셋**: *-2.0 - 2.0*\
    결과를 이동하거나 변환합니다. 캔버스와 직접 상호 작용하여 결과를 수정할 수 있습니다.
* **모양**: *사각형, 디스크*\
  배치할 모양을 선택합니다.
* **모양 색상 모드**: *RGB, 온도(켈빈), 이미지 입력*\
  모양 색상을 설정하는 데 사용할 방법을 선택합니다. 이미지 입력(Image Input)은 두 번째 입력 슬롯을 사용할 수 있게 합니다.
* **색상**: *(색상 값)*\
  [모양 색상 모드]가 [RGB]로 설정된 경우에만 가능합니다. 모양의 색상을 선택합니다.
* **모양 온도**: *800.0 - 20000.0*\
  [모양 색상 모드]가 [온도]로 설정된 경우에만 가능합니다. 모양 색상의 켈빈 값을 설정합니다.
* **모양 이미지 입력 감마**: *sRGB, 선형*\
  [모양 색상 모드]가 [이미지 입력]으로 설정된 경우에만 가능합니다. 모양 이미지 입력을 해석하는 방법을 결정합니다.
* **모양 노출(EV)**: *0.0 - 10.0*\
  생성된 모양에 대한 노출 값 설정, 배경 이미지 노출 값과 이상적인 일치.
* **모양 경도**: *0.0 - 1.0*\
  모양 가장자리의 경도를 설정합니다.
* **핫스팟 노출(EV)**: *0.0 - 10.0*\
  중앙 핫스폿의 노출을 설정합니다. 참고: RGB 모드에서는 이 버튼이 잘 보이지 않습니다.
* **핫스팟 크기**: *0.0 - 1.0*\
  중앙 핫스폿의 크기입니다.
* **핫스팟 밝기 감소**: *0.0 - 1.0*\
  중앙 핫스폿의 밝기 감소.
* **핫스팟 위치**: *0.0 - 1.0*\
  중앙 핫스폿의 X 및 Y 위치
* **배경 입력 사용**: *False/True*\
  선택적 배경 이미지 사용을 전환합니다. 합성 이미지에서 배경 상단에 조명이 생성되었습니다.
* **배경색**: *(색상 값)*\
  [배경 입력]을 사용하지 않는 경우에는 여기에서 단색 배경 값을 설정합니다.
* **배경 감마**: *sRGB, 선형*&#x200B;배경 입력을 사용하는 경우 배경 입력을 해석하는 방법을 설정하십시오.

## 예제 이미지

![](../../../../../../assets/shape-light-ex.gif)

</td>
</tr>
</table>
