---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan.html"
breadcrumb-title: ''
description: '[막대 그래프 스캔] 노드를 사용하여 색상 교정 및 조정을 위한 텍스처 막대 그래프를 스캔하고 분석할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 막대 그래프 스캔
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 1%

---


# 막대 그래프 스캔

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/histogram-scan-1.png){width="128px"}

## 막대 그래프 스캔

**내부:** *필터/조정*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

입력 회색 음영 이미지의 대비와 명도를 다시 매핑하는 직관적인 방법을 제공하는 매우 간단하면서도 유용한 노드입니다. 동적 방식으로 마스크를 &quot;확장&quot; 및 &quot;축소&quot;하는 데 사용할 수 있습니다.

[히스토그램 작업에 대한 Substance 아카데미 비디오를 시청하려면 여기를 클릭하십시오.](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=427s)

## 매개변수

* **위치**: *0.0 - 1.0*&#x200B;밝기 제어와 비슷하게 결과의 중간점을 이동합니다. 그레이디언트 입력에 사용하면 전환점이 확장되고 축소됩니다.\
  중요: 기본값인 0은 최종 결과가 항상 검은색임을 의미하므로 0.5부터 다시 시도하십시오.
* **대비**: *0.0 - 1.0*\
  결과의 대비를 조정합니다. 전환의 경도를 설정하는 데 사용할 수 있습니다.
* **위치 반전**: *False/True*&#x200B;최종 결과를 반전합니다.

## 예제 이미지

![](../../../../../../assets/histogram-scan.gif)

![](../../../../../../assets/histogram-scan2.gif)

![](../../../../../../assets/histogram-scan3.gif)

</td>
</tr>
</table>
