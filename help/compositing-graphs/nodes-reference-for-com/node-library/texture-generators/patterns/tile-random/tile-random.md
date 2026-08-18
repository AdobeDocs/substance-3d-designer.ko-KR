---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random.html"
breadcrumb-title: ''
description: 유기적인 텍스처 효과에 대해 절차적 변형을 사용하여 무작위 타일 패턴을 만들려면 [타일 무작위] 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 타일 무작위
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---


# 타일 무작위

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tile-random.png){width="128px"}

## 타일 무작위(색상)

**내부:** *생성기/패턴*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

[무작위 타일]은 타일 모양에 [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)보다 좀 더 많은 혼란이 있는 절차적 타일 패턴을 생성합니다. 이것은 어떤 타일을 더 작은 타일로 무작위로 쪼개서 이것을 한다. 많은 개념이 유사하기 때문에 타일 무작위와 씨름하기 전에 먼저 Tile Generator에서 방법을 찾는 것이 좋습니다.

목표가 구체적이고 덜 조직화된 패턴인 경우 [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) 대신 타일 임의성이 사용됩니다. 하지만 제한 사항이 있으므로 다른 고급 요구 사항을 위해 [Sampler 바둑판식 배열](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)을 사용해 보세요.

## 매개변수

### 입력

* **패턴 입력**: *회색 음영 입력(색상 입력)*\
  &quot;Pattern&quot; 매개 변수를 &quot;Image Input&quot;으로 설정한 경우 사용되는 사용자 정의 패턴 이미지입니다.
* **배경 입력**: *회색 음영 입력(색상 입력)*

### 매개변수

* **X 양**: *1 - 64*\
  패턴의 X-반복의 양입니다.
* **Y 양**: *1 - 64*\
  패턴의 Y-반복의 양입니다.
* **비정사각형 확장**: *False/True*\
  제곱이 아닌 비율로 스쿼시와 스트레치를 보정할 수 있습니다.
* **패턴**
  * **패턴**: *패턴 입력, 정사각형, 디스크, 포물면, 벨, 가우스, 가시, 피라미드, 벽돌, 그라데이션, 파도, 하프 벨, 융기된 벨, 초승달, 캡슐, 원뿔*\
    사용할 패턴 모양을 선택합니다.
  * **이미지 입력 필터링(엔진 > v4)**: *쌍선형 + 밉맵, 쌍선형, 최근접*
  * **패턴별**: *0.0 - 1.0*\
    선택한 패턴의 모양을 변경할 수 있습니다. 효과는 선택한 패턴에 따라 달라집니다.
  * **패턴별 무작위**: *0.0 - 1.0*&#x200B;임의화 효과는 선택한 패턴에 따라 달라집니다.
  * **회전**: *0, 90, 180, 270, 임의 수평, 임의 수직*&#x200B;임의 임의화를 사용하여 90도 단계로 회전을 설정합니다.
  * **회전 임의**: *0.0 - 1.0*&#x200B;임의의 자유 회전을 추가합니다.
  * **대칭 무작위**: **0.0 - 1.0** 선택한 대칭 무작위 모드로 특정 패턴을 무작위로 미러링합니다. 이 값이 높을수록 더 많은 패턴이 미러링됩니다.
  * **대칭 무작위 모드**: *수평 + 수직, 수평, 수직*&#x200B;대칭 무작위가 0보다 높을 때 미러링 동작을 결정합니다.
* **분할**
  * **모드**: *없음, 자동, 자동 수평, 자동 수직, 임의 h+v*&#x200B;타일 분할 방법에 대한 규칙을 설정합니다.
  * **임계값**: *0.0 - 1.0*&#x200B;타일 분할 시점에 대한 크기 임계값
  * **승수**: *0 - 10*&#x200B;분할 승수. 이 값이 높을수록 분할이 많습니다.
* **크기**
  * **무작위 X**: *0.0 - 1.0* X축을 기준으로 균일하지 않은 비율을 임의화합니다.
  * **무작위 Y**: *0.0 - 1.0* Y축에 대해 균일하지 않은 비율을 임의화합니다.
* **중간**
  * **모드**: *가장 작은 벽돌에 대한 상대, 가장 큰 벽돌에 대한 상대*&#x200B;벽돌 크기의 상대적을 설정합니다.
  * **양**: *0.0 - 1.0*&#x200B;벽돌 사이의 간격을 설정합니다.
* **모양**
  * **크기 조절**: *0.0 - 1.0*&#x200B;모든 타일의 크기를 전체적으로 조절합니다.
  * **무작위 크기 조정**: *0.0 - 1.0*&#x200B;타일별 무작위 크기 조정
  * **회전**: 모든 타일에 대해 *0.0 - 1.0*&#x200B;전역 회전.
  * **회전 무작위**: *0.0 - 1.0*&#x200B;타일당 기준으로 무작위로 회전합니다.
  * **회전 제약 조건**: *False/True*&#x200B;회전된 타일이 겹치지 않도록 크기를 제한합니다.
* **위치**
  * **오프셋**: *0.0 - 1.0*\
    X축 위에서만 슬라이드를 포함하여 타일을 전체적으로 이동하거나 변환합니다
  * **오프셋 무작위**: *0.0 - 1.0* X축 위의 슬라이드만 오프셋된 타일을 임의화합니다.
  * **무작위**: *0.0 - 1.0*&#x200B;위치를 임의화하고 타일을 X축과 Y축 둘 다 이동합니다.
  * **임의 제약 조건**: *False/True*&#x200B;타일이 닿도록 크기를 제한하지만 겹치지 않습니다. [무작위 위치] 효과의 톤을 크게 낮춥니다.
* **색상**
  * **색상**: *(회색 음영 값) / (색상 값)*모든 타일에 대한 단색을 설정합니다.
  * **색상 무작위**: *0.0 - 1.0*&#x200B;타일별로 색상을 임의화합니다.
  * **색상 매개 변수화**: *없음, 영역, 크기 x, 크기 y*&#x200B;색상 변형이 이 설정 중 하나에 종속되도록 합니다.
  * **색상 매개 변수화 강도**: 위의 매개 변수화 효과에 대한 *0.0 - 1.0*&#x200B;승수.
  * **색상 매개 변수화 효과(색상만 해당):** **RGB+Alpha, RGB 전용, Alpha 전용** 색상 전용 매개 변수화 효과를 결정합니다.
  * **배경색**: *(회색 음영 값) / (색상 값)*단색 배경색을 설정합니다.
  * **혼합 모드**: *추가/하위, 최대 /*&#x200B;추가/하위, Alpha 혼합(색상)**타일의 혼합 모드를 배경에 설정합니다.
* **마스크**
  * **무작위**: *0.0 - 1.0*&#x200B;타일에 무작위로 마스킹 작업을 시작합니다. 이 값이 높을수록 타일이 더 많이 사라집니다.
  * **반전**: *False/True*\
    마스크 결과를 반전합니다.

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/tile-random-1.png" width="256px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
