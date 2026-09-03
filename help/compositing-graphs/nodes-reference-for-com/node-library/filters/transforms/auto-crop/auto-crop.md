---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/auto-crop.html"
breadcrumb-title: ''
description: 자동 자르기 노드를 사용하여 텍스처를 자동으로 잘라 빈 테두리를 제거하고 텍스처 크기를 최적화합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Auto Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 자동 자르기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---


# 자동 자르기

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](auto-crop.resources/auto-crop-01.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](auto-crop.resources/auto-crop-02.png){width="200px"}

</td>
</tr>
</table>

<b>필터</b>:

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

**자동 자르기** 노드는 **입력**&#x200B;을 조정하여 해당 콘텐츠가 크기 조정 없이 이미지의 *중앙*&#x200B;에 배치되거나 이미지의 범위&#x200B;*에 맞게*&#x200B;크기 조정됩니다.

이미지의 내용은 **X** 및 **Y**&#x200B;의 *첫 번째 및 마지막 픽셀*&#x200B;에 맞는 상자로 정의되며, 값은 *0*&#x200B;보다 높습니다(예: 검은색이 아님). **색상** 버전에서는 해당 상자를 정의하기 위한 RGB 및 Alpha 채널을 선택할 수 있습니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>모드</b> <i>정수</i> | 적용해야 할 자르기 방법을 설정합니다.<br><br>- <i>자르기 사각형</i>: 이미지가 잘려서 전체 포함할 수 있는 가장 작은 <i>정사각형</i> 이미지의 중심에 있는 모양<br>- <i>자르기 자동</i>: 이미지가 가장 작은 <i>정사각형 또는 정사각형이 아닌 </i> 이미지의 중앙에 있는 모양으로 잘립니다.<br><i>정사각형 또는 정사각형이 아닌 이미지의 중앙에 있는 모양</i>: 이미지가 <i>비율<i>6을 유지하면서 <i>전체 범위&lbrace;14에 맞게 조정됩니다.</i>(폭 대 길이)&lbrace;폭 비율<br> &lbrace;19(이미지 채우기 비율)</i> &lbrace;19(이미지 이미지의 <i>전체 범위</i> 크기로 조정됨</i> |
| <b>알파 사용</b> <i>부울</i> | 자르기를 위해 이미지 콘텐츠의 <i>경계</i>를 결정하려면 <b>입력</b>의 알파 채널을 사용합니다. <i>False</i>(으)로 설정하면 검정 픽셀이 대신 사용됩니다.<br><br><i>참고:</i> 이 매개 변수는 노드의 <b>색상</b> 버전에서만 사용할 수 있습니다. |
| <b>필터링 모드</b> <i>정수</i> | 픽셀 간에 <i>보간</i>할 때 샘플링된 결과를 처리하는 방법을 정의합니다. <br><br>- <i>가장 가까운</i>: 정확히 <i>같은</i> 값을 샘플링합니다(더 빠름)<br>- <i>쌍선형</i>: <i>더 매끄러운</i> 모양을 위해 결과에 쌍선형 필터를 적용합니다<br>- <i>자동</i>: 자르기를 위해 선택한 <b>모드</b>에 따라 위의 두 가지 모드 중 가장 적절한 모드를 사용합니다 |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/auto-crop-03.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/auto-crop-04.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/auto-crop-05.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/auto-crop-06.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/auto-crop-07.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/auto-crop-08.png" />
        </td>
    </tr>
</table>
