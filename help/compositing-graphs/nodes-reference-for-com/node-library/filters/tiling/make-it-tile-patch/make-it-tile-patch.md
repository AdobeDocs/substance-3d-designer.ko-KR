---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-patch.html"
breadcrumb-title: ''
description: Make It Tile Patch 노드를 사용하여 입력 이미지에서 매끄러운 타일링 텍스처를 패치하고 만들 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 타일 패치로 만들기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 8%

---


# 타일 패치로 만들기

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](make-it-tile-patch.resources/make-it-tile-patch.png)

![](make-it-tile-patch.resources/make-it-tile-patch-grayscale.png)

<b>내부:</b> 필터 > 타일링

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이 노드는 그리드 기반 세미 랜덤 타일러입니다. 입력 패치를 적용하고 스탬프를 찍어내 설정에 따라 너무 많은 반복 없이 타일링 이미지로 변환하려고 시도합니다.

텍스처 패치가 작고 대규모 타일링 텍스처를 만들려는 경우에 유용합니다.

이 사진은 주로 가장자리를 수정하는 [Make-It-Tile 사진](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md)과는 다릅니다.

전체 재질을 사용하여 이 작업을 수행하려면 [스마트 자동 타일](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/smart-auto-tile/smart-auto-tile.md)을 참조하세요.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>마스크 크기</b> <i>0.0 - 1.0</i> | 패치를 스탬프할 때 사용되는 둥근 마스크의 크기입니다. |
| <b>마스크 정밀도</b> <i>0.0 - 1.0</i> | 마스크의 밝기 감소/Smoothness 정밀도입니다. |
| <b>마스크 뒤틀기</b> <i>-100.0 - 100.0</i> | 마스크 가장자리에 뒤틀기를 도입합니다. 패치 사이의 매끄럽고 정의되지 않은 전환을 피하는 데 유용합니다. |
| <b>패턴 크기 너비</b> <i>0.0 - 1000.0</i> | 패치의 폭을 불균일하게 변경합니다. |
| <b>패턴 크기 Height</b> <i>0.0 - 1000.0</i> | 패치의 Height을 불규칙하게 변경합니다. |
| <b>장애</b> <i>0.0 - 1.0</i> | 병진 임의성을 도입하고 패치가 약간 이동합니다. |
| <b>크기 변형</b> <i>0.0 - 100.0</i> | 마스크의 크기 변형을 도입합니다. |
| <b>옥타브</b> <i>0 - 6</i> | 전체 크기를 결정하는 기본 컨트롤입니다. |
| <b>회전</b> <i>-360.0 - 360.0</i> | 패치를 사전 회전합니다. |
| <b>회전 변형</b> <i>0.0 - 360.0</i> | 모든 패치 스탬프에 대해 임의 회전을 도입합니다. |
| <b>배경색</b> <i>(색상 값)</i> | 패치가 표시되지 않는 영역의 배경색을 설정합니다. |
| <b>색상 변형</b> <i>0.0 - 1.0(색상 버전만)</i> | 패치당 색상 변형을 소개합니다. |
| <b>광도 변형</b> <i>(회색 음영 버전만)</i> | 패치당 광도 변화를 소개합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="make-it-tile-patch.resources/patch-ex.gif" />
        </td>
    </tr>
</table>
