---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/1-click/bitmap-to-material-light.html"
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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 11%

---


# 비트맵에서 재질 조명으로

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](bitmap-to-material-light.resources/b2m-light.png)

<b>내부:</b>개 재질 필터 > 한 번 클릭

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이 노드는 단일 확산/기본 색상 입력을 전체 재질로 변환합니다. 별도로 구입할 수 있는 [Allegorihmic의 완전한 Bitmap2Material의 간단한 &quot;가벼운&quot; 버전으로서,](https://www.allegorithmic.com/products/bitmap2material) 정식 버전의 맛을 약간 제공합니다. 더 단순한 경우에 잘 작동할 수 있습니다.

PBR이 교정되는 완벽한 재질을 만들지는 않지만 이미지가 하나만 있고 전체 재질을 원하신다면 작업을 시작하는 데 빠르고 좋은 방법입니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>채널</b> | 이 그룹에서 재질 채널을 켜거나 끕니다. 예를 들어 [금속]/[거칠음] 대신 [Specular/광택] 맵을 사용하는 경우 |
| <b>전역</b> |  |
| <b>깊이 균형</b> <i>-1.0 - 1.0</i> | Heightmap에 대한 편향/이동을 설정합니다. |
| <b>확산</b> |  |
| <b>선명 효과</b> <i>0.0 - 1.0</i> | 확산 결과에 선명하게 하기를 추가합니다. |
| <b>색조</b> <i>0.0 - 1.0</i> | 색조는 사용자가 선택한 색조 이동으로 확산됩니다. |
| <b>채도</b> <i>0.0 - 1.0</i> | 확산 결과의 채도를 수정합니다. |
| <b>밝기</b> <i>0.0 - 1.0</i> | 확산 결과 밝기를 조정합니다. |
| <b>대비</b> <i>-1.0 - 1.0</i> | 결과의 대비를 조정합니다. |
| <b>부조</b> | 부조 그룹은 [표준] 및 [Height] 출력을 모두 제어합니다. |
| <b>출력 표준 형식</b> <i>DirectX, OpenGL</i> | 표준 포맷 간을 전환합니다(녹색으로 뒤집음). |
| <b>생성된 부조 반전</b> <i>거짓/참</i> | Height의 해석을 반전시킵니다. |
| <b>표준 강도</b> <i>0.0 - 20.0</i> | 생성된 Normalmap의 강도를 설정합니다. |
| <b>부조 이퀄라이저</b> <i>0.0 - 1.0</i> | 다양한 상세 스케일에 대한 변환 잔액을 설정합니다. |
| <b>핀치 강도</b> <i>0.0 - 1.0</i> | 표준 전환을 더 선명하게 합니다. 표준으로 변환하기 전에 선명하게 하기 필터를 효과적으로 추가하여 가장자리를 더욱 뚜렷하게 만듭니다. |
| <b>일반 선명 효과</b> <i>0.0 - 1.0</i> | 변환 후 일반 맵을 선명하게 하여 세부 사항을 표시합니다. |
| <b>일반 부드럽게</b> <i>0.0 - 1.0</i> | 변환 후 일반 맵을 부드럽게 하고 세부 정보를 숨깁니다. |
| <b>Specular</b> |  |
| <b>Specular 확산 영향</b> <i>0.0 - 1.0</i> | 확산이 Specular에 미치는 영향을 설정합니다. 광택 및 거칠기 출력에도 영향을 줍니다. |
| <b>Specular 채도</b> <i>0.0 - 1.0</i> | Specular 출력의 채도를 변경합니다. |
| <b>Specular 선명 효과</b> <i>0.0 - 1.0</i> | Specular 출력을 선명하게 합니다. |
| <b>Specular level </b> <i>0.0 - 1.0</i> | Specular 해석에 대한 입력 레벨을 설정합니다. |
| <b>Specular level 아웃</b> <i>0.0 - 1.0</i> | Specular의 출력 레벨을 수정합니다. |
| <b>금속 Specular 영향</b> <i>0.0 - 1.0</i> | Specular 맵에 대한 선택적 금속 입력의 영향을 결정합니다. |
| <b>광택</b> |  |
| <b>광택도 수준 </b> <i>0.0 - 1.0</i> | 광택도 해석에 대한 입력 레벨을 설정합니다. |
| <b>광택도 수준 초과</b> <i>0.0 - 1.0</i> | 광택도 출력 레벨을 수정합니다. |
| <b>금속 광택도 영향</b> <i>0.0 - 1.0</i> | 광택도 맵에 대한 선택적 금속 입력의 영향을 결정합니다. |
| <b>거칠음</b> |  |
| <b>거칠음 수준</b> <i>0.0 - 1.0</i> | 거칠기 해석의 입력 레벨을 설정합니다. |
| <b>거칠기 레벨 아웃</b> <i>0.0 - 1.0</i> | 거칠기 출력 레벨을 수정합니다. |
| <b>금속 거칠기 영향</b> <i>0.0 - 1.0</i> | 광택도 맵에 대한 선택적 금속 입력의 영향을 결정합니다. |
| <b>주변 오클루전</b> |  |
| <b>확산 앰비언트 오클루전</b> <i>0.0 - 1.0</i> | 생성된 AO의 혼합을 확산 출력으로 변환합니다. |
| <b>앰비언트 오클루전 스프레드</b> <i>0.0 - 1.0</i> | AO를 얼마나 많이 생성할지 설정합니다. |
| <b>앰비언트 오클루전 조명 거리</b> <i>0.0 - 1.0</i> | AO &quot;깊이&quot; 해석을 설정합니다. 스프레드가 큰 경우에는 영향이 적습니다. |
| <b>앰비언트 오클루전 조명 각도</b> <i>0.0 - 1.0</i> | 페이크 조명 AO 캐스트 각도를 설정합니다. 반대 각도로 설정된 경우, 확산 영역에 이미 존재하는 모든 방향 AO를 보상하는 데 사용할 수 있습니다. |
| <b>앰비언트 오클루전 수준</b> <i>0.0 - 1.0</i> | AO 출력 레벨을 수정합니다. |
