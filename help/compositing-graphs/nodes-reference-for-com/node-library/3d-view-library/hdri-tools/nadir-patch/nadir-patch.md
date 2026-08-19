---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/nadir-patch.html"
breadcrumb-title: ''
description: Nadir Patch 노드를 사용하여 HDRI 파노라마의 아래쪽 영역을 패치하여 환경 맵의 아래쪽 아티팩트를 수정합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Nadir Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nadir Patch
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 1%

---


# Nadir Patch

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-nadir-patch.png){width="200px"}

## Nadir Patch

**내부:** *3D 보기/HDRI 도구*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

이 노드는 구형으로 매핑된 이미지의 중앙 그라운드 포인트(nadir)를 패치하는 기능을 제공한다. 이 효과는 보기 흉한 바닥 또는 눈에 보이는 카메라 또는 삼각대를 숨기거나 &quot;복제&quot;하는 데 사용할 수 있습니다. [복제 패치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)처럼 작동하지만 구형으로 매핑된 이미지의 조정도 사용할 수 있습니다. 사용자는 이미지의 다른 곳에서 점, 즉 복제하여 바닥에 블렌딩하는 점을 선택합니다. 단일 HDRI 외에 다른 외부 입력은 처리할 필요가 없지만 외부 마스크를 패치 효과에 대한 알파로 사용할 수 있습니다.

[Nadir Extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/nadir-extract/nadir-extract.md)을(를) 사용하여 효과를 빠르게 확인하고 유효성을 검사할 수 있습니다.

## 입력

* **입력**: *색상 입력*
* **마스크 입력**: *회색 음영 입력*\
  패치를 마스킹하는 데 사용되는 선택적 마스크 슬롯입니다. 알파처럼 작동합니다.

## 매개변수

* **사용**: *False/True*\
  패치 효과를 활성화하거나 비활성화합니다.
* **프레임 도우미 표시**: *False/True*\
  디버그를 위해 보조 줄을 표시하거나 숨깁니다.
* **프레임 Thickness**: *0.0 - 1.0*\
  보조 줄의 Thickness.
* **패치 크기**: *0.0 - 1.0*\
  패치의 전역적이고 균일한 비율입니다. 소스와 타겟 모두에 영향을 줍니다.
* **패치 크기**: *0.0 - 1.0*\
  패치의 크기가 일정하지 않습니다.
* **패치 회전**: *0.0 - 1.0*\
  패치의 회전입니다. 소스와 대상에 영향을 줍니다.
* **패치 Alpha**: *부드러운 사각형, 가우시안, 마스크 입력*\
  패치와 배경을 혼합하는 데 사용할 알파를 설정합니다.
* **패치 경도**: *0.0 - 1.0*\
  알파의 경도/대비를 설정합니다.
* **원본 회전 오프셋**: *0.0 - 1.0*\
  패치 소스에 대해서만 회전합니다.
* **위치 좌표**
  * **원본 위치**:\
    소스의 위치입니다. 2D 보기에 핸들이 있습니다.
  * **패치 위치**:\
    대상의 위치입니다. 2D 보기에 핸들이 있습니다.

## 예제 이미지

![](../../../../../../assets/nadir-patch-ex.gif)

</td>
</tr>
</table>
