---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-sdf.html"
breadcrumb-title: ''
description: 3D 텍스처 SDF 노드를 사용하여 매끄러운 모양과 효과를 만들기 위해 3D 데이터에서 서명된 거리 필드 텍스처를 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture SDF
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 텍스처 PDF
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---


# 3D 텍스처 PDF

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-texture-sdf.resources/3d-texture-sdf-01.png){width="200px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

**3D 텍스처 SDF** 노드는 모양의 *볼륨*&#x200B;의 조각들을 나타내는 **입력**&#x200B;의 *3D 텍스처* 마스크에서 모양의 *부호 있는 거리 필드*&#x200B;를 생성합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>마스크 입력</b> <i>회색 음영</i> | 모양의 <i>볼륨</i>의 조각을 나타내는 <i>3D 텍스처</i> 마스크입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>임계값</b> <i>부동</i> | 모양 볼륨이 <i>페이딩 그레이디언트</i>로 기술되면 모양의 <i>표면</i>이 <i>검색</i>되는 그레이디언트 값을 설정합니다. |
| <b>출력</b> <i>정수</i> | 출력해야 하는 거리 필드 유형:<br>- <i>거리 필드</i>: 모양의 <i>바깥쪽</i> 거리를 설명하는 거리 필드를 출력합니다.<br>- <i>부호 거리 필드</i>: 모양의 <i>바깥쪽</i>(양수) 및 <i>안쪽</i>(음수) 거리를 설명하는 거리 필드를 출력합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3d-texture-sdf-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3d-texture-sdf-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3d-texture-sdf-04.png" />
        </td>
    </tr>
</table>
