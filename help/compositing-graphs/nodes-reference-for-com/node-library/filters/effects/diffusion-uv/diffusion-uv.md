---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-uv.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 1%

---


# 확산 UV

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-icon.png){width="200px"}

**내부:** *필터/효과*

**중간**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 설명

제공된 **마스크** 이미지 입력에 따라 **소스** 이미지 입력의 UV 좌표에 확산 프로세스를 적용하고 **소스**&#x200B;의 값 사이의 좌표를 보간합니다.

마스크와 일치하는 픽셀의 UV만 확산되고, 다른 픽셀은 결과에 참여하지 않습니다.

타일링은 특별한 방식으로 처리됩니다. 타일링이 *사용*&#x200B;인 경우(기본적으로 이러한 경우) 인접 좌표는 0/1 제한에서 평균을 낼 수 있습니다.

예를 들어 U 좌표 값이 한 픽셀에서는 0.1이고 다른 픽셀에서는 0.8이면 *좌표 타일링*&#x200B;이 가정되므로 평균값은 0.45가 아니라 0.95가 됩니다. 이는 실제 픽셀 위치와는 별개입니다. 좌표 값은 이미지 전체에서 동일한 방식으로 처리됩니다.

이 필터를 *텍스처 변형*&#x200B;에 사용할 때 원치 않는 결과가 발생할 수 있습니다. 이 경우 마스크가 &#39;곡선/점 제어&#39;를 *텍스처 길이의 절반 이하*&#x200B;로 정의하는지 확인하십시오.

</td>
</tr>
</table>

## 매개변수

* **반복**: *0.0 - 64.0*&#x200B;수행할 확산 반복 수입니다(높을수록 좋지만 느림). 유용한 값은 [8, 48] 범위에 있습니다.\
  만약 여러분이 수학적 정확성을 찾고 있지 않다면, 낮은 값들이 괜찮거나 더 낫다는 것을 알아두세요.

## 입력

* **원본** *색상*\
  확산될 UV입니다. 이 필터에서는 타일링이 특별한 방식으로 처리됩니다(*설명* 참조).
* **마스크** *회색 음영*&#x200B;확산 마스크: 흰색 픽셀은 *소스*&#x200B;에서 샘플링되고 검은색 픽셀로 확산됩니다. 이미지는 흑백이어야 합니다. 마스크에 그레이디언트가 포함되어 있으면 차단 값은 0.5입니다.

## 예제 이미지

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01a-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01a-after.jpg){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01b-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01b-after.jpg){width="256px"}

</td>
</tr>
</table>
