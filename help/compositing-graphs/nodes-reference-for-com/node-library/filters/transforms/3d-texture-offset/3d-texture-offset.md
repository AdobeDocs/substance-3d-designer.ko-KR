---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/3d-texture-offset.html"
breadcrumb-title: ''
description: 시차 효과 및 표면 변형을 만들기 위해 3D 공간에서 텍스처를 오프셋하려면 3D 텍스처 오프셋 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > 3D Texture Offset
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 텍스처 오프셋
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# 3D 텍스처 오프셋

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](3d-texture-offset.resources/3d-texture-offset-01.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](3d-texture-offset.resources/3d-texture-offset-02.png){width="200px"}

</td>
</tr>
</table>

<b>내부:</b> 필터 > 변환

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

**3D 텍스처 오프셋** 노드는 **입력**&#x200B;에 연결된 *3D 텍스처*&#x200B;에 의해 설명된 개체에 **X**, **Y** 및 **Z** 축의 *오프셋 변환*&#x200B;을 적용합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>입력</b> <i>회색 음영/색상</i> | 3D 개체를 설명하는 <i>3D 텍스처</i>입니다.<br>개체는 일반적으로 <i>단위 큐브</i>에 설명되어 있습니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>오프셋</b> <i>Float3</i> | <b>입력</b>에 연결된 <i>3D 텍스처</i>에 의해 설명된 개체에 적용된 <i>세계 공간</i>의 오프셋 양입니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-offset.resources/3d-texture-offset-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-offset.resources/3d-texture-offset-04.png" />
        </td>
    </tr>
</table>
