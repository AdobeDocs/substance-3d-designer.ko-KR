---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/sampler-nodes.html"
breadcrumb-title: ''
description: Substance 3D Designer 함수 그래프의 샘플러 노드에 액세스하여 텍스처를 샘플링하고 색상 값을 추출합니다.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Samplers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 샘플러
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 1%

---


# Sampler 노드

![Sampler 노드](sampler-nodes.resources/image2016-1-12-14-45-43.png "Sampler 노드")

이러한 노드는 제공된 2D 좌표에서 입력 이미지의 값을 샘플링합니다.

<b>회색 샘플링</b>은(는) 회색 음영 이미지에서 <b>위치</b> 입력의 광도 값을 샘플링하여 <b>부동</b> 값으로 출력합니다.

<b>샘플 색상</b>은 색상 이미지에서 <b>위치 </b>에서 RGBA 값을 샘플링하여 <b>Float4</b> 값으로 출력합니다. 여기서 R,G,B 및 A 구성 요소는 각각 X, Y, Z 및 W 구성 요소에 매핑됩니다.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

좌표는 입력의 왼쪽 위 모퉁이에서 시작하며 가로 및 세로로 0에서 1 사이의 범위입니다.

이 범위를 벗어나는 위치는 선택한 <b>주소 지정 모드</b>에 따라 처리됩니다(아래 참조).

</td>
<td width="33.33%" style="border: 0;" valign="top">

![픽셀 좌표](sampler-nodes.resources/samplercoords.png "픽셀 좌표")

</td>
</tr>
</table>

>[!NOTE]
>
> <b>위치</b> 입력은 이미지의 X 및 Y 좌표가 각각 값의 X 및 Y 구성 요소에 매핑되는 Float2 값이어야 합니다

## 매개변수

+++입력 이미지
샘플링에 사용할 노드 입력을 선택할 수 있습니다.

목록은 현재 연결된 입력에 동적으로 조정됩니다. 즉, 노드 입력을 연결할 때 항목이 추가됩니다.

입력의 번호 매기기가 0에서 시작되어 노드의 첫 번째 입력에 연결된 이미지가 *입력 이미지 0*&#x200B;으로 나열됩니다.

+++

+++필터링 모드
해상도 차이로 인해 샘플 이미지의 픽셀이 출력 이미지에 정확하게 매핑되지 않는 경우 보간을 처리하는 방법을 정의할 수 있습니다.

<b>가장 가까운</b>\
픽셀이 일치하는 좌표에서 대상 *있는 그대로*&#x200B;에 매핑됩니다. 타겟이 더 낮은 해상도이면 픽셀은 완전히 무시될 수 있다. 대상의 해상도가 더 높은 경우 해당 범위를 포함하는 모든 픽셀에 매핑됩니다. 출력은 *더 선명하게*&#x200B;이며 약간 *앨리어스*&#x200B;로 표시됩니다.

<b>쌍선형 필터링</b>\
필터링 프로세스가 소스 이미지에 적용되어 해당 픽셀이 대상 해상도에 매핑되어 픽셀 간의 전환을 *매끄럽게* 합니다. 출력은 *더 매끄럽게*&#x200B;이며 약간 *흐리게* 표시됩니다.

+++

+++주소 지정 모드
[0;1] 범위를 벗어나는 위치 값을 처리하는 방법을 제어합니다.

<b>반복</b>\
값이 증가함에 따라 [0;1] 범위 위에 루프가 있습니다.\
예: 3.4는 0.4이고, -1.7은 0.3입니다.

<b>가장자리로</b>\
0, 1&rbrack; 범위\
예: .3.4는 1이고, -1.7은 0입니다.

+++
