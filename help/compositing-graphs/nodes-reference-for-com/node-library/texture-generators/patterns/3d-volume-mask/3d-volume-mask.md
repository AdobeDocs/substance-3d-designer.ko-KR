---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-volume-mask.html"
breadcrumb-title: ''
description: 3D 볼륨 마스크 노드를 사용하여 고급 재질 효과를 위해 3D 위치를 기반으로 볼륨 마스크를 만듭니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Volume Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 볼륨 마스크
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---


# 3D 볼륨 마스크

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-volume-mask.resources/3d-volume-mask-01.png){width="256px"}

<b>내부:</b> 생성기 > 패턴

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

**3D 볼륨 마스크** 노드는 **위치** 입력 맵을 기반으로 *기본 모양*&#x200B;의 표현을 생성합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>위치</b> <i>색상</i> | 프리미티브의 *3D 공간 좌표*&#x200B;를 설명하는 맵이 로 표시됩니다.<br><br>X/Y/Z **좌표가 각각** R/G/B **채널에 매핑됩니다.** |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>모양</b> <i>정수</i> | 표시되어야 하는 기본 모양:<br><br>- *큐브*<br>- *실린더*<br>- *구* |
| <b>크기 조절</b> <i>부동</i> | 모든 축에 *균일하게*&#x200B;을(를) 적용한 프리미티브 *전역* 비율을 정의합니다. |
| <b>크기</b> <i>Float3</i> | 각 축에 있는 모양의 크기를 정의합니다. |
| <b>위치 입력</b> <i>정수</i> | **위치** 입력을 통해 *공간을 나타내는* 방법:<br><br>- *UV 위치*: *UV 맵*&#x200B;을 사용하십시오. X/Y(U/V) 좌표는 각각 R/G 채널에 맵핑된다. Z축은 *직교 정방향* 벡터로 가정합니다.<br>- *세계 공간 위치*: *위치 맵*&#x200B;을 사용하여 3D 공간의 기본 위치를 매핑합니다. X/Y/Z 좌표는 각각 R/G/B 채널에 맵핑된다. |
| <b>UV 위치</b> <i>Float2</i> | UV 공간에서 기본 위치의 위치&#x200B;<br><br>*참고*: 이 매개 변수는 **위치 입력** 매개 변수가 *UV 위치*(으)로 설정된 경우에만 사용할 수 있습니다. |
| <b>위치</b> <i>Float3</i> | 월드 공간에서 기본 위치 <br><br>*참고*: 이 매개 변수는 **위치 입력** 매개 변수가 *세계 공간 위치*(으)로 설정된 경우에만 사용할 수 있습니다. |
| <b>회전</b> <i>Float3</i> | 월드 공간에서 모양의 회전을 정의합니다. |
| <b>페더 폭</b> <i>부동</i> | 프리미티브 표면의 안쪽으로 *페이딩 그레이디언트*&#x200B;의 폭을 조정합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3d-volume-mask-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3d-volume-mask-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3d-volume-mask-04.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3d-volume-mask-05.jpg" />
        </td>
    </tr>
</table>
