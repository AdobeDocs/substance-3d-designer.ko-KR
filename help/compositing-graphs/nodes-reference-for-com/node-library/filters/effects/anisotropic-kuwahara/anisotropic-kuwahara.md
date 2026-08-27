---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/anisotropic-kuwahara.html"
breadcrumb-title: ''
description: '[비등방성 구와하라 색상] 필터를 사용해서 직접 보정을 사용하여 스타일화된 회화적인 색상 효과를 만듭니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Anisotropic Kuwahara Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 비등방성 구와하라 색상
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '841'
ht-degree: 0%

---


# 비등방성 구와하라 색상

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![비등방성 구와하라 색상 아이콘](https://helpx.adobe.com/content/dam/substance-3d-designer/substance-graphs/nodes/filters/effects/anisotropic-kuwahara/AnisotropicKuwaharaColor.png "비등방성 구와하라 색상 아이콘"){width="200px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이미지의 세부 사항에 맞는 비등방성 방향 흐림 효과를 적용합니다. 결과는 *흐름*&#x200B;이 포함된 모양 방향으로 나타나는 이미지입니다.

이 조절 가능한 흐림 효과는 흐름을 결정하기 위해 *방향 맵*&#x200B;을 계산하거나 수신하므로 더 평평하고 명확하게 정의된 영역으로 선명하게 만들 수 있습니다.

</td>
</tr>
</table>

유동은 흐림 효과가 적용되는 방향을 회전시킴으로써 분해될 수도 있다. 마찬가지로, 사용자 정의 방향 맵을 사용하여 이미지에서 계산된 항목을 오버라이드할 수 있습니다.

이 필터는 회화적인 효과를 낼 수 있으며, 스타일화에 유용합니다.

<b>비등방성</b>

플로우 강도는 아래 이미지에서 확인할 수 있는 것처럼 [비등방성](#parameters) 매개 변수에 의해 주로 제어됩니다.

왼쪽: 비등방성 0.0 / 오른쪽: 비등방성 1.0

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![비등방성 0이 적용된 쿠와하라 필터가 있는 과일 그릇.](https://helpx.adobe.com/content/dam/substance-3d-designer/substance-graphs/nodes/filters/effects/anisotropic-kuwahara/anisotropic_kuwahara_color_example_3_before.jpg){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![비등방성 0이 적용된 쿠와하라 필터가 있는 과일 그릇.](https://helpx.adobe.com/content/dam/substance-3d-designer/substance-graphs/nodes/filters/effects/anisotropic-kuwahara/anisotropic_kuwahara_color_example_3_after.jpg){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### 출력 커넥터

</td>
<td style="border: 0;" valign="top">

### 매개변수

</td>
</tr>
</table>

## 입력 커넥터

|  |  |
| --- | --- |
| <b>입력</b> 기본 *색상* | 처리해야 하는 색상 이미지입니다. |
| <b>비등방성 각도 맵</b> *회색 음영* | 계산된 방향에 적용된 추가 회전을 설명하는 회색 음영 이미지입니다. 여기서 회색 음영 값은 회전 수입니다.   Kuwahara 필터에서 사용하는 커널의 회전에 영향을 미치므로 &#39;비등방성&#39; 매개 변수를 0으로 설정하면 맵이 계속 영향을 받습니다. |
| <b>경사 맵</b> *회색 음영* | &#39;경사 맵 입력 승수&#39; 매개 변수 값에 따라 방향 맵이 일치하는 경사를 나타내는 맵입니다. |
| <b>반경 맵(선택 사항)</b> *회색 음영* | 연결되면 흐림 효과 &#39;반경&#39;이 입력 이미지에 곱해집니다. |
| <b>방향 맵</b> *색상* | 비등방성 필터 커널이 사용하는 방향을 설명하는 맵이다.   Kuwahara 필터에서 사용하는 커널의 회전에 영향을 미치므로 &#39;비등방성&#39; 매개 변수를 0으로 설정하면 맵이 계속 영향을 받습니다.   참고: 이 입력은 &#39;입력 방향 맵 사용&#39; 매개 변수가 &#39;True&#39;로 설정된 경우에만 사용됩니다. |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *색상* | 노드가 입력 이미지에 적용한 비등방성 흐림 효과의 결과입니다. |
| <b>방향 맵</b> *색상* | 입력 이미지에서 계산된 방향 맵으로, 이방성 흐림 효과를 구동하는데 사용됩니다.   &#39;입력 방향 맵 사용&#39; 매개 변수를 &#39;True&#39;로 설정하면 &#39;방향 맵&#39; 입력에 제공된 이미지를 그대로 사용하여 출력합니다. |

## 매개변수

|  |  |
| --- | --- |
| <b>반경</b> *부동* | 흐림 반경. 여기서 값이 높을수록 더 강한 흐림 효과가 발생합니다.   최대값은 32입니다. |
| <b>Smoothness</b> *부동* | 계산된 방향으로의 색상 혼합 양을 조정합니다.   이 값이 0이면 색상은 대부분 해당 방향으로 이동하고 혼합은 거의 발생하지 않습니다. |
| <b>선명도</b> *부동* | 흐린 영역의 대비를 증가시켜 영역이 더 평평하고 선명하게 보이도록 합니다. |
| <b>비등방성</b> *부동* | 흐림 효과의 방향 맵 기여도를 조정합니다.   방향 맵이 Kuwahara 필터 커널에서 사용되므로 이 매개 변수 값이 0인 경우에도 방향 맵과 모든 해당 한정자(매개 변수 및 입력 맵 모두)에 영향을 미칩니다. |
| <b>입력 방향 맵 사용</b> *부울* | &#39;True&#39;인 경우 입력 이미지에서 방향 맵이 계산되지 않고 &#39;방향 맵&#39; 입력에 연결된 이미지를 사용하여 비등방성 흐림 효과를 대신 실행합니다. |
| <b>텐서 Smoothness</b> *Float* *&#39;입력 방향 맵 사용&#39;이 &#39;False&#39;로 설정된 경우 사용 가능* | 이미지에서 계산되어 방향 맵에 저장된 방향에 적용되는 흐림 효과의 강도를 조정합니다.   이 값을 높이면 이미지의 세부 묘사가 고주파인 경우 더 매끄러운 결과가 나옵니다. |
| <b>비등방성 각도</b> *Float* *&#39;입력 방향 맵 사용&#39;이 &#39;False&#39;로 설정된 경우 사용 가능* | 회전 수로 방향 맵에 회전을 추가합니다.   이 추가 회전은 &#39;비등방성 각도 맵&#39; 입력으로 지정된 것과 함께 *누적*&#x200B;입니다. |
| <b>비등방성 각도 맵 멀티플라이어</b> *Float* *&#39;입력 방향 맵 사용&#39;이 &#39;False&#39;로 설정된 경우 사용 가능* | &#39;비등방성 각도 맵&#39; 입력의 값 강도를 조정합니다. 이 값은 방향 맵에 적용된 회전 위에 회전수로 추가됩니다.   이 추가 회전은 &#39;비등방성 각도&#39; 매개 변수에 지정된 것과 함께 *누적*&#x200B;입니다. |
| <b>경사 맵 입력 승수</b> *Float* *&#39;입력 방향 맵 사용&#39;이 &#39;False&#39;로 설정된 경우 사용 가능* | &#39;경사 맵&#39; 입력에서 제공하는 경사에 방향 맵이 맞춰지는 강도를 조정합니다. |
| <b>알파 무시</b> *부울* | &#39;True&#39;인 경우 이미지의 알파 채널은 필터의 영향을 받지 않습니다.   &#39;False&#39;이면 알파 채널에도 필터가 적용됩니다. |

## 예

<table>
  <tr>
    <td>
      <img src="https://helpx.adobe.com/libs/settings/wcm/designs/default/resources/0.gif" alt="anisotropic_kuwahara_color_example_1_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="https://helpx.adobe.com/libs/settings/wcm/designs/default/resources/0.gif" alt="anisotropic_kuwahara_color_example_1_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="https://helpx.adobe.com/libs/settings/wcm/designs/default/resources/0.gif" alt="anisotropic_kuwahara_color_example_2_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="https://helpx.adobe.com/libs/settings/wcm/designs/default/resources/0.gif" alt="anisotropic_kuwahara_color_example_2_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="https://helpx.adobe.com/libs/settings/wcm/designs/default/resources/0.gif" alt="anisotropic_kuwahara_color_example_4_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="https://helpx.adobe.com/libs/settings/wcm/designs/default/resources/0.gif" alt="anisotropic_kuwahara_color_example_4_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>
