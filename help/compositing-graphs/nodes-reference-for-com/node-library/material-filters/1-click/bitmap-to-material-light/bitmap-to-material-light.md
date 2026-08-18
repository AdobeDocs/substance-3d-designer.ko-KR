---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/1-click/bitmap-to-material-light.html"
breadcrumb-title: ''
description: '[비트맵 대 재질 조명] 노드를 사용하면 비트맵 이미지를 빠른 작업 과정에 최적화된 조명이 있는 재질로 빠르게 변환할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > 1-Click > Bitmap to Material Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 비트맵에서 재질 조명으로
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---


# 비트맵에서 재질 조명으로

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/b2m-light.png)

## 비트맵에서 재질 조명으로

**내부:** *재질 필터/1-클릭*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

이 노드는 단일 확산/기본 색상 입력을 전체 재질로 변환합니다. 별도로 구입할 수 있는 [Allegorihmic의 완전한 Bitmap2Material의 간단한 &quot;가벼운&quot; 버전으로서,](https://www.allegorithmic.com/products/bitmap2material) 정식 버전의 맛을 약간 제공합니다. 더 단순한 경우에 잘 작동할 수 있습니다.

PBR이 교정되는 완벽한 재질을 만들지는 않지만 이미지가 하나만 있고 전체 재질을 원하신다면 작업을 시작하는 데 빠르고 좋은 방법입니다.

## 매개변수

* **채널**
  * 이 그룹에서 재질 채널을 켜거나 끕니다. 예를 들어 [금속]/[거칠음] 대신 [Specular/광택] 맵을 사용하는 경우
* **전역**
  * **깊이 균형**: *-1.0 - 1.0* Heightmap에 대한 편향/이동을 설정합니다.
* **확산**
  * **선명 효과**: *0.0 - 1.0*&#x200B;확산 결과에 선명 효과를 추가합니다.
  * **색조**: *0.0 - 1.0*&#x200B;색조는 사용자가 선택한 색조 이동으로 확산됩니다.
  * **채도**: *0.0 - 1.0*&#x200B;확산 결과의 채도를 수정합니다.
  * **밝기**: *0.0 - 1.0*&#x200B;확산 결과 밝기를 조정합니다.
  * **대비**: *-1.0 - 1.0*\
    결과의 대비를 조정합니다.
* **부조**\
  부조 그룹은 [표준] 및 [Height] 출력을 모두 제어합니다.
  * **출력 표준 형식**: *DirectX, OpenGL*&#x200B;표준 형식 간 전환(녹색으로 뒤집기).
  * **생성된 부조 반전**: *False/True* Height 해석을 반전합니다.
  * **표준 강도**: *0.0 - 20.0*&#x200B;생성된 표준 맵의 강도를 설정합니다.
  * **부조 이퀄라이저**: *0.0 - 1.0*&#x200B;다른 세부 비율에 대한 변환 잔액을 설정합니다.
  * **핀치 강도**: *0.0 - 1.0*&#x200B;표준 전환을 더 선명하게 합니다. 표준으로 변환하기 전에 선명하게 하기 필터를 효과적으로 추가하여 가장자리를 더욱 뚜렷하게 만듭니다.
  * **표준 선명 효과**: *0.0 - 1.0*&#x200B;변환 후 표준 선명 효과를 적용한 후 세부 사항을 표시합니다.
  * **일반 부드럽게**: *0.0 - 1.0*&#x200B;변환 후 표준 맵을 부드럽게 하고 세부 사항을 숨깁니다.
* **Specular**
  * **Specular 확산 영향**: *0.0 - 1.0* Specular에 대한 확산 영향을 설정합니다. 광택 및 거칠기 출력에도 영향을 줍니다.
  * **Specular 채도**: *0.0 - 1.0* Specular 출력의 채도를 변경합니다.
  * **Specular 선명하게**: *0.0 - 1.0* Specular 출력을 선명하게 합니다.
  * **Specular level 입력**: *0.0 - 1.0* Specular 해석에 대한 입력 수준을 설정합니다.
  * **Specular level 아웃**: *0.0 - 1.0* Specular의 출력 수준을 수정합니다.
  * **금속 Specular 영향**: *0.0 - 1.0* Specular 맵에 대한 선택적 금속 입력의 영향을 결정합니다.
* **광택**
  * **광도 수준**: *0.0 - 1.0*&#x200B;광도 해석에 대한 입력 수준을 설정합니다.
  * **광도 레벨 초과**: *0.0 - 1.0*&#x200B;광도 출력 레벨을 수정합니다.
  * **금속 광택 영향**: *0.0 - 1.0*&#x200B;선택적 금속 입력이 광택 지도에 미치는 영향을 결정합니다.
* **거칠음**
  * **거칠기 레벨**: *0.0 - 1.0*&#x200B;거칠기 해석에 대한 입력 레벨을 설정합니다.
  * **거칠기 레벨 아웃**: *0.0 - 1.0*&#x200B;거칠기 출력 레벨을 수정합니다.
  * **금속 거칠기 영향**: *0.0 - 1.0*&#x200B;광택 지도에 대한 선택적 금속 입력의 영향을 결정합니다.
* **주변 오클루전**
  * **확산에 주변 오클루전**: *0.0 - 1.0*&#x200B;생성된 AO를 확산 출력에 혼합합니다.
  * **주변 오클루전 스프레드**: *0.0 - 1.0* AO 스프레드를 얼마나 많이 생성할지 설정합니다.
  * **주변 오클루전 조명 거리**: *0.0 - 1.0* AO &quot;깊이&quot; 해석을 설정합니다. 스프레드가 큰 경우에는 영향이 적습니다.
  * **주변 오클루전 조명 각도**: *0.0 - 1.0*&#x200B;모조 조명 AO 주조 각도를 설정합니다. 반대 각도로 설정된 경우, 확산 영역에 이미 존재하는 모든 방향 AO를 보상하는 데 사용할 수 있습니다.
  * **주변 오클루전 수준**: *0.0 - 1.0* AO 출력 수준을 수정합니다.

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
