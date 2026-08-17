---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/arc-pavement.html"
breadcrumb-title: ''
description: 호 포장 노드를 사용하여 곡선 도로와 패스 텍스처를 만들기 위한 호 모양의 포장 패턴을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Arc Pavement
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 아크 포장
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# 아크 포장

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/arcpavement-ex.png)

## 아크 포장

**인:** *텍스처 생성기**/패턴*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

파리 호 포장 패턴을 생성합니다. 이 효과는 표준 [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) 또는 [타일 Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)으로는 수행할 수 없으므로 이 전용 노드입니다.

## 매개변수

* **비율**: *1 - 8*&#x200B;전체 비율/타일링을 설정합니다.
* **패턴 양**: *1 -* 32\
  모든 원호에 사용되는 벽돌의 양을 설정합니다.
* **패턴 양 무작위**: *0.0 - 1.0*\
  모든 호로 벽돌의 양을 임의화합니다. 벽돌에 다양한 스케일을 부여하는 추가 효과가 있습니다.
* **패턴 최소 양**: *1 - 10*\
  호를 임의화할 때 벽돌의 최소 양을 제어합니다.
* **호 양**: *0 - 20*\
  세로로 쌓이는 호의 양을 설정합니다. 벽돌 Height을 변경합니다.
* **패턴**: *입력 이미지, 정사각형, 디스크, 포물선, 벨, 가우스, 가시, 피라미드, 벽돌, 그레이디언트, 파도, 하프 벨, 융기된 벨, 초승달, 캡슐, 원뿔*\
  사용할 패턴 모양을 선택합니다.
* **입력 이미지 필터링**: *쌍선형 + 밉맵, 쌍선형, 최근접*
* **패턴 크기 조절**: *0.0 - 1.0*&#x200B;각 타일에 대한 크기를 설정합니다.
* **패턴 너비**: *0.0 - 1.0*\
  각 타일의 너비를 설정합니다.
* **패턴 Height**: *0.0 - 1.0*\
  각 타일의 Height을 설정합니다.
* **패턴 너비 무작위**: *0.0 - 1.0*\
  타일 폭을 임의화합니다.
* **패턴 Height 무작위**: *0.0 - 1.0*\
  타일 Height을 임의화합니다.
* **전역 패턴 너비 임의**: *0.0 - 1.0*&#x200B;타일 폭 사이에 더 큰 간격을 만들지 않고 임의로 지정합니다.
* **패턴 Height 감소**: *0.0 - 1.0*&#x200B;모든 호의 끝에서 타일 Height의 비산을 제어합니다.
* **색상 무작위**: *0.0 - 1.0*\
  타일 색상을 임의화합니다.
* **비정사각형 확장**: *False/True*\
  제곱이 아닌 비율로 스쿼시와 스트레치를 보정할 수 있습니다.

## 예제 이미지

![](../../../../../../assets/arcpavement-ex.png)

</td>
</tr>
</table>
