---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/season-filter.html"
breadcrumb-title: ''
description: '[시즌 필터] 노드를 사용하여 봄, 여름, 가을, 겨울 변형을 만드는 재질에 계절별 효과를 적용합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Season Filter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 계절 필터
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 11%

---


# 계절 필터

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](season-filter.resources/default-icon.png){width="128px"}

<b>내부:</b> 재질 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이 노드는 애니메이션 수위, 눈, 얼음 및/또는 이끼와 같은 효과를 추가합니다.

이 필터는 PBR 교정이 불가능한 이전 버전이라는 점을 명심하십시오. 일부 경우에는 여전히 유용할 수 있지만 대부분 레거시/호환성의 이유로 보관됩니다. [Snow 표지](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) 및 [수위](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md)에서 최신 PBR 수정 버전을 확인할 수 있습니다.

노드는 적절한 재료 투입의 집합을 요구하는데, 주로 세밀한 Heightmap 또는 Normalmap과 함께한다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>마스크</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. &quot;마스크&quot; 매개 변수로 전환할 수 있습니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>채널</b> | 예를 들어 [금속]/[거칠음] 대신 [Specular/광택] 맵을 사용하는 경우 이 그룹에서 재질 채널을 켜거나 끌 수 있습니다. |
| <b>고급</b> |  |
| <b>표준 형식</b> <i>DirectX, OpenGL</i> | 서로 다른 표준 맵 포맷 사이를 전환합니다(녹색 채널을 반전합니다). |
| <b>마스크</b> <i>거짓/참</i> | 마스크 맵 사용을 설정하거나 해제합니다. |
| <b>조명 강도</b> <i>0.0 - 1.0</i> | (위조된) 조명의 강도입니다. |
| <b>조명 각도</b> <i>0.0 - 1.0</i> | (가짜) 빛의 입사각 |
| <b>효과</b> |  |
| <b>Height 또는 표준으로 효과</b> <i>Height, 표준</i> | 효과를 구동하는 입력 맵을 선택합니다. |
| <b>수위</b> <i>0.0 - 1.0</i> | Height/일반 정보에 따라 수위를 높이거나 낮춥니다. |
| <b>물 세부 정보</b> <i>0.0 - 1.0</i> | 물에 세부 사항의 양을 설정합니다. |
| <b>굴절</b> <i>0.0 - 1.0</i> | 효과에서 거짓 굴절의 양을 설정합니다. |
| <b>반사</b> <i>0.0 - 1.0</i> | 효과에서 거짓 반사의 양을 설정합니다. |
| <b>반사 거리</b> <i>0.0 - 1.0</i> | 반사 비주얼을 제어합니다. |
| <b>반사 각도</b> <i>0.0 - 1.0</i> | 반사 비주얼을 제어합니다. |
| <b>흐름 방향</b> <i>0.0 - 1.0</i> | 애니메이션 흐름을 제어합니다(시각화하려면 Substance Player 사용). |
| <b>얼음</b> <i>0.0 - 1.0</i> | 물이 얼마나 얼었는지 설정합니다. |
| <b>얼음 세부 정보</b> <i>0.0 - 1.0</i> | 얼음의 세부 사항 양을 설정합니다. |
| <b>Snow</b> <i>0.0 - 1.0</i> | 적설량을 설정합니다. |
| <b>이끼</b> <i>0.0 - 1.0</i> | 이끼 커버리지 양을 설정합니다. |
| <b>이끼 비율</b> <i>1 - 4</i> | 생성된 이끼 텍스처의 비율을 설정합니다. |
| <b>이끼색</b> <i>(색상 값)</i> | 이끼의 색상을 설정합니다. |
| <b>수채화 효과</b> <i>(색상 값)</i> | 알파/불투명도를 비롯한 물의 색상을 설정합니다. |
| <b>혼합</b> |  |
| <b>확산 강도</b> <i>0.0 - 1.0</i> | 확산 영역의 혼합 강도입니다. |
| <b>기본 색상 강도</b> <i>0.0 - 1.0</i> | 기본 색상의 혼합 강도입니다. |
| <b>표준 강도</b> <i>0.0 - 1.0</i> | 표준의 혼합 강도입니다. |
| <b>Specular 강도</b> <i>0.0 - 1.0</i> | Specular의 혼합 강도입니다. |
| <b>광택도 강도</b> <i>0.0 - 1.0</i> | 광택의 혼합 강도입니다. |
| <b>거칠음 강도</b> <i>0.0 - 1.0</i> | 거칠기의 혼합 강도입니다. |
| <b>앰비언트 오클루전 강도</b> <i>0.0 - 1.0</i> | 주변 오클루전의 혼합 강도입니다. |
| <b>Height 강도</b> <i>0.0 - 1.0</i> | Height의 혼합 강도입니다. |
