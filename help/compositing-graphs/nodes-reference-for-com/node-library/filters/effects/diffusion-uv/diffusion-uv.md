---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-uv.html"
breadcrumb-title: ''
description: '[확산] UV 노드를 사용하여 UV 공간에 확산 효과를 적용하여 매끄러운 색상 전환과 혼합을 만들 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion UV
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 확산 UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 2%

---


# 확산 UV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](diffusion-uv.resources/diffusion-uv-01.png){width="200px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

제공된 **마스크** 이미지 입력에 따라 **소스** 이미지 입력의 UV 좌표에 확산 프로세스를 적용하고 **소스**&#x200B;의 값 사이의 좌표를 보간합니다.

마스크와 일치하는 픽셀의 UV만 확산되고, 다른 픽셀은 결과에 참여하지 않습니다.

타일링은 특별한 방식으로 처리됩니다. 타일링이 *사용*&#x200B;인 경우(기본적으로 이러한 경우) 인접 좌표는 0/1 제한에서 평균을 낼 수 있습니다.

예를 들어 U 좌표 값이 한 픽셀에서는 0.1이고 다른 픽셀에서는 0.8이면 *좌표 타일링*&#x200B;이 가정되므로 평균값은 0.45가 아니라 0.95가 됩니다. 이는 실제 픽셀 위치와는 별개입니다. 좌표 값은 이미지 전체에서 동일한 방식으로 처리됩니다.

이 필터를 *텍스처 변형*&#x200B;에 사용할 때 원치 않는 결과가 발생할 수 있습니다. 이 경우 마스크가 &#39;곡선/점 제어&#39;를 *텍스처 길이의 절반 이하*&#x200B;로 정의하는지 확인하십시오.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>원본</b> <i>색상</i> | 확산될 UV입니다. 이 필터에서는 타일링이 특별한 방식으로 처리됩니다(<i>설명</i> 참조). |
| <b>마스크</b> <i>회색 음영</i> | 확산 마스크: 흰색 픽셀은 <i>소스</i>에서 샘플링되고 검은색 픽셀에서 확산됩니다. 이미지는 흑백이어야 합니다. 마스크에 그레이디언트가 포함되어 있으면 차단 값은 0.5입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>반복</b> <i>0.0 - 64.0</i> | 수행할 확산 반복 수입니다(높을수록 좋지만 느림). 유용한 값은 [8, 48] 범위에 있습니다.<br>수학적 정확성을 찾고 있지 않은 경우 낮은 값이 적합하거나 더 좋습니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-03.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-04.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-05.jpg" />
        </td>
    </tr>
</table>
