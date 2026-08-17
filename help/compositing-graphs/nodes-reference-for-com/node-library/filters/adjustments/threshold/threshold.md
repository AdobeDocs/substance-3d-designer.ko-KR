---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/threshold.html"
breadcrumb-title: ''
description: '[한계값] 노드를 사용하여 회색 음영 텍스처를 마스크 만들기의 한계값에 따라 흑백으로 변환합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Threshold
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 임계값
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---


# 임계값

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/threshold-2.png){width="200px"}

## 임계값

**내부:** *필터/조정*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

**임계값** 값과 상대적으로 입력 픽셀 값에 대해 **모드** 매개 변수에 설정된 *비교 조건*&#x200B;이 충족되면 흰색을 반환합니다.\
[막대 그래프 스캔](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)과(와) 유사하지만 대비가 항상 최대 수준입니다. 히스토그램 스캔과 유사한 결과를 얻을 수 있는 보다 정확하고 빠른 방법입니다.

### 매개변수

* **임계값**: *0.0 - 1.0*\
  입력 픽셀 값과 비교할 광도 값입니다.
* **모드**:\
  입력 픽셀 값을 **임계값** 값과 비교하는 기준:
  * *높음*
  * *크거나 같음*
  * *아래쪽*
  * *아래쪽 또는 위쪽*

## 예제 이미지

</td>
</tr>
</table>
