---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise.html"
breadcrumb-title: ''
description: 3D Perlin 노이즈 노드를 사용하여 3D 공간에 부드러운 Perlin 노이즈 패턴을 생성하여 자연스러워 보이는 볼륨 텍스처를 만듭니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Perlin Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Perlin 노이즈
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---


# 3D Perlin 노이즈

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-perlin-noise.resources/3d-perlin-noise-01.png){width="200px"}

<b>내부:</b> 텍스처 생성기 > 잡음

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

<b>3D Perlin Noise</b> 노드는 <b>위치 맵</b> 입력을 기반으로 3D 공간에서 Perlin 노이즈를 생성합니다.

이 베이킹된 맵은 실제 노드 대신 [큐브 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md)을(를) 입력으로 사용하여 테스트할 수 있습니다(아래 그림 참조).

</td>
</tr>
</table>

>[!WARNING]
>
> 이 노이즈는 <i>GPU 엔진</i>(예: <b>Direct3D</b> 또는 <b>OpenGL</b>)에만 사용됩니다. <b>도구 > 엔진 전환...</b>(으)로 이동하거나 <b>F9</b> 키를 눌러 원하는 엔진을 선택합니다.

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>반전</b> <i>부울</i> | 출력 이미지를 반전합니다. |
| <b>크기 조절</b> <i>부동</i> | 3D Perlin 노이즈의 크기를 제어합니다. |
| <b>크기</b> <i>Float3</i> | <b>X</b>, <b>Y</b> 및 <b>Z</b> 축의 3D Perlin 노이즈 크기를 제어합니다. 균일하지 않은 값을 사용하면 <i>스트레치 또는 스쿼싱</i> 효과가 발생합니다. |
| <b>오프셋</b> <i>Float3</i> | <b>X</b>, <b>Y</b> 및 <b>Z</b> 축에서 3D Perlin 노이즈의 <i>위치</i>에 오프셋을 적용합니다. |
| <b>왜곡 강도</b> <i>부동</i> | 3D 펄린 노이즈에 적용된 <i>뒤틀기 효과</i>의 강도를 제어합니다. |
| <b>왜곡 배율 배율</b> <i>부동</i> | <b>왜곡 강도</b>로 제어되는 뒤틀기 효과에 사용되는 <i>변형 패턴</i>의 비율을 제어합니다. |
| <b>기준선</b> <i>부동</i> | 3D Perlin 노이즈 값 분포의 기준선 <i>광도</i> 값에 <i>오프셋</i>을 적용합니다. |
| <b>대비</b> <i>부동</i> | 3D Perlin 노이즈의 대비를 조정합니다. |
| <b>절대</b> <i>부울</i> | 3D Perlin 노이즈에 절대값을 사용합니다. 이렇게 하면 <i>0.5</i> 아래의 값에 대한 값 분포가 효과적으로 <i>반전</i>됩니다. |
| <b>타일링 사용</b> <i>부울</i> | 3D Perlin 노이즈를 조정하여 결과 패턴이 X, Y 및 Z축에서 <i>반복</i>되도록 합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise.resources/3d-perlin-noise-02.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise.resources/3d-perlin-noise-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise.resources/3d-perlin-noise-04.jpg" />
        </td>
    </tr>
</table>
