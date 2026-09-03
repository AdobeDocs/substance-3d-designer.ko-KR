---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan-non-uniform.html"
breadcrumb-title: ''
description: '[히스토그램 스캔 비균일] 노드를 사용하여 고급 색상 교정을 위한 비균일 히스토그램 스캔을 수행합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan Non-Uniform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 막대 그래프 스캔 불균일
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 3%

---


# 막대 그래프 스캔 불균일

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-scan-non-uniform.resources/histogram-scan-non-uniform-01.png){width="128px"}

<b>내부:</b> 필터 > 조정

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

[막대 그래프 스캔](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)의 고급 버전으로서, 전체 이미지에 균일하게 적용되는 것이 아니라 픽셀 단위로 효과를 구동하는 추가 컨트롤 및 입력이 포함되어 있습니다. 마스크에서 훨씬 더 복잡한 대비와 전환을 수행하는 데 사용할 수 있습니다.

일반 [막대 그래프 스캔](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)보다 훨씬 더 복잡하므로, [비균일] 버전을 사용하기 전에 이 기능을 숙지하고 있는지 확인하세요.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>입력</b> <i>회색 음영 입력</i> | 수정할 원본 결과입니다. |
| <b>위치 맵</b> <i>회색 음영 입력</i> | 위치 매개 변수를 구동하기 위한 입력 슬롯입니다. &quot;위치 입력 사용&quot;이 True로 설정된 경우 활성화됩니다. 유효 값 범위는 작으며 대비 맵과 설정에 따라 다릅니다. |
| <b>대비 맵</b> <i>회색 음영 입력</i> | 대비 매개 변수를 구동하기 위한 입력 슬롯입니다. &quot;대비 입력 사용&quot;이 True로 설정된 경우 활성화됩니다. 유효 값 범위가 작습니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>위치 입력 사용</b> <i>거짓/참</i> | 위치 맵 입력 슬롯 사용 전환. |
| <b>위치</b> <i>0.0 - 1.0</i> | 맵 결과를 제어하거나 수정하여 위치 설정을 제어합니다. |
| <b>대비 입력 사용</b> <i>거짓/참</i> | 대비 맵 입력 슬롯 사용을 전환합니다. |
| <b>대비</b> <i>0.0 - 1.0</i> | 맵 결과를 제어하거나 수정하여 대비 설정을 제어합니다. |
