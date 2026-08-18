---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/scratches-generator.html"
breadcrumb-title: ''
description: Scratches 생성기 노드를 사용하여 재료의 마모와 손상을 추가하기 위한 절차적 스크래치 패턴을 만듭니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Scratches Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Scratches 생성기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---


# Scratches 생성기

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/scratches-generator.png)

## Scratches 생성기(표준)

**인:** *텍스처 생성기**/패턴*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

이렇게 하면 방향, 스프레드 및 왜곡 등을 설정할 수 있는 등 다양한 사용자 지정 옵션이 있는 임의의 스크래치가 배치됩니다.

이 스크래치 깊이를 기반으로 하여 Normalmap을 생성하는 특수 버전의 Scratches 생성기 인 Scratches 생성기 표준이 있습니다. 대부분의 옵션은 정확히 동일하지만 [표준] 설정에 명확하게 표시된 몇 가지 추가 매개 변수가 있습니다(아래 참조).

## 매개변수

* **스플라인 번호**: *1 - 512*&#x200B;배치할 스크래치(스플라인) 양.
* **스플라인당 최대 선분**: *2 - 256*&#x200B;스크래치 길이 이상의 선분/하위 분할의 양. 그러면 곡선과 왜곡이 더 매끄러워집니다. 이 효과는 왜곡 값이 높을수록 더 두드러집니다.
* **스플라인 회전**: *0.0 - 1.0*&#x200B;방향을 조정하기 위해 모든 스플라인의 균일한 회전.
* **스플라인 회전 무작위**: *0.0 - 1.0*&#x200B;각도의 변화, 모든 스플라인을 무작위로 회전합니다.
* **스플라인 배율**: *0.0 - 1.0*&#x200B;모든 스플라인의 비율을 균일하게 조정합니다.
* **스플라인 배율 무작위**: *0.0 - 1.0*&#x200B;각 스플라인의 비율을 개별적으로 무작위로 조정합니다.
* **스플라인 왜곡**: *0.0 - 1.0*&#x200B;모든 스플라인의 균일한 왜곡 레벨.
* **스플라인 왜곡 무작위**: *0.0 - 1.0*&#x200B;각 스플라인의 왜곡 레벨을 개별적으로 임의화합니다.
* **스플라인 왜곡 빈도**: *0.0 - 1.0*&#x200B;왜곡 빈도를 설정하고 왜곡 세부 정보 비율을 제어합니다.
* **스플라인 폭**: *0.0 - 2.0*&#x200B;모든 스플라인의 폭을 균일하게 설정합니다.
* **스플라인 폭 무작위**: *0.0 - 1.0*&#x200B;각 스플라인의 스플라인 폭을 개별적으로 임의화합니다.
* **스플라인 위치 무작위**: *0.0 - 1.0*&#x200B;각 스플라인의 위치를 개별적으로 임의화합니다. 이 값이 낮을수록 스플라인이 캔버스의 중앙에 더 많이 모입니다. 스크래치 스팟을 만드는 데 사용할 수 있습니다.
* **px에서 스플라인 폭 설정**: *False/True*&#x200B;스플라인 폭 설정에 사용되는 단위를 결정합니다.
* **광도 무작위(회색 음영 버전만)**: *0.0 - 1.0*&#x200B;각 스플라인의 광도를 개별적으로 임의화합니다.
* **표준 강도(표준 버전만)**: *0.0 - 1.0*&#x200B;모든 스플라인에 대한 표준 효과의 강도를 전체적으로 설정합니다.
* **&#x200B;표준 강도 임의 **(표준 버전만)****: *0.0 - 1.0*각 스플라인의 표준 강도를 개별적으로 임의화합니다.
* **&#x200B;일반 형식 **(일반 버전만)****: *DirectX, OpenGL*\
  서로 다른 표준 맵 포맷 사이를 전환합니다(녹색 채널을 반전합니다).
* **페이드 모드**: *없음, 시작, 종료, 시작 + 종료*&#x200B;스플라인이 페이드되는지 여부 및 방향을 설정합니다.
* **페이드 길이**: *0.0 - 1.0*&#x200B;위에서 활성화된 경우 페이드 효과의 길이를 설정합니다.
* **비정사각형 확장**: *False/True*\
  제곱이 아닌 비율로 스쿼시와 스트레치를 보정할 수 있습니다.

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/scratches-ex1.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/scratches-ex2.png" width="256px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
