---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/extend-shape.html"
breadcrumb-title: ''
description: Extend Shape 노드를 사용하여 모양을 경계 너머로 확장하여 확장된 마스크 및 패턴 효과를 만듭니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Extend Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extend Shape
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---


# Extend Shape

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](extend-shape.resources/extendshapegrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](extend-shape.resources/extendshapecolor.png){width="200px"}

</td>
</tr>
</table>

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

<b>Extend Shape</b> 노드는 <b>입력</b>의 <i>섹션</i>을(를) 설정된 방향과 거리 위로 확장합니다.

<b>Show helper</b> 매개 변수를 사용하면 확장된 섹션 및 확장 방향을 시각화할 수 있습니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>모드</b> <i>정수</i> | <br><br>- <i>양방향</i> 확장을 적용하는 데 사용되는 <i>매개 변수</i>를 정의합니다. <b>확장 위치</b> 및 <b>확장 각도</b>로 지정된 <b>입력</b>의 섹션이 <i>반대 방향</i><br><i>단방향</i>으로 <b>확장 거리</b>에 걸쳐 확장됩니다. <b>확장 위치</b> 및 <b>확장 각도</b>로 지정된 <b>입력</b>의 섹션이 <i>단일 방향</i><br><b>확장 거리</b>에 걸쳐 확장됩니다. <i>시작/종료 위치</i>: 확장 <i>벡터</i>는 <b>시작 위치</b> 및 <b>종료 위치</b>로 정의됩니다. <b>시작 위치</b>에 있는 <b>입력</b>의 <i>수직</i> 섹션이 <b>종료 위치</b>까지 이 벡터</i>에 대해 <i>확장됩니다. |
| <b>확장 거리</b> <i>부동</i> | <b>확장 위치</b> 및 <b>확장 각도</b>로 지정된 구간보다 긴 거리를 늘려야 합니다. 거리는 이미지 범위의 <i>비율</i>로 표시됩니다. |
| <b>확장 위치</b> <i>부동</i> | 확장해야 하는 섹션 이미지의 위치입니다. 값은 <i>가운데에서 오프셋</i>(으)로 표시됩니다. |
| <b>확장 각도</b> <i>부동</i> | 시작점을 고려하여 연장해야 하는 구간의 각도는 <i>수직 구간</i>입니다. |
| <b>시작 위치</b> <i>Float2</i> | <i>확장 벡터</i>의 시작 위치. |
| <b>끝 위치</b> <i>Float2</i> | <i>확장 벡터</i>의 끝 위치입니다. |
| <b>광도 오프셋 시작</b> <i>부동</i> | 확장된 섹션 <i>앞</i> 이미지 영역에 광도 오프셋을 적용합니다. 이 광도 오프셋은 <i>섹션을 따라 보간됩니다</i>. 섹션 다음 이미지 영역의 광도에 보간됩니다.<br><br><i>참고</i>: 이 매개 변수는 노드의 <b>회색 음영</b> 버전에서만 사용할 수 있습니다. |
| <b>광도 오프셋 종료</b> <i>부동</i> | 확장된 섹션 <i>팔로우</i>하는 이미지 영역에 광도 오프셋을 적용합니다. 이 광도 오프셋은 <i>섹션을 따라 보간됨</i>을 섹션 앞에 있는 이미지 영역의 광도로 보간됩니다.<br><br><i>참고</i>: 이 매개 변수는 노드의 <b>회색 음영</b> 버전에서만 사용할 수 있습니다. |
| <b>룸. 오프셋은 검은색 픽셀을 무시합니다</b> <i>부울</i> | <i>True</i>(으)로 설정된 경우 광도 오프셋은 <i>모두</i>에 지정됩니다. <b>시작 광도 오프셋</b> 및 <b>끝 광도 오프셋</b>은 <i>검은 색이 아닌</i> 픽셀(예: 값이 0보다 큰 픽셀)에만 적용됩니다.<br><br><i>참고</i>: 이 매개 변수는 노드의 <b>회색 음영</b> 버전에서만 사용할 수 있습니다. |
| <b>필터링 모드</b> <i>정수</i> | <i>픽셀 간의 <br><br>-<i>가장 가까운</i>: 정확히 <i>같은</i> 값을 샘플링할 때<br>- <i>쌍선형</i>: <i>더 매끄럽게</i> 보이도록 결과에 쌍선형 필터를 적용할 때 샘플링된 결과를 처리하는 방법을 정의합니다.</i> |
| <b>도우미 표시</b> <i>부울</i> | 확장의 <i>방향</i>을 보여주는 화살표를 사용하여 <i>확장 섹션</i>을 오버레이로 시각화합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extendshape.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extendshape-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extendshape-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extendshape-node.png" />
        </td>
    </tr>
</table>
