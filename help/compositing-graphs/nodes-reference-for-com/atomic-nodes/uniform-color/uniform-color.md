---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/uniform-color.html"
breadcrumb-title: ''
description: '[균일 색상] 노드를 사용하면 단색 채우기 및 기본 레이어를 만들기 위한 균일 색상 텍스처를 생성할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Uniform color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 균일 색상
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 8%

---


# 균일 색상

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomic node: Uniform color](uniform-color.resources/comp_uniform_1.png "Atomic node: Uniform color"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

플랫 회색 음영 또는 색상 값을 생성합니다.

이 노드는 색상을 추가하거나 특정 값을 만들기 위한 시작점으로 매우 자주 사용되는 간단한 노드입니다.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> 성능 최적화
> 
> 두 조정 모두 노드의 계산 시간과 메모리 공간을 줄여줍니다.
> 
> * 회색 음영 값이 필요한 경우 노드의 [색상 모드](#parameters)를 &#39;회색 음영&#39;으로 전환해야 합니다.
> * 노드의 출력이 플랫 컬러이기 때문에 가능한 가장 낮은 해상도를 사용할 수 있다. &#39;Absolute&#39; [상속 메서드](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) 및 16x16 픽셀의 해상도를 사용하도록 노드의 &#39;[출력 크기](../../../../compositing-graphs/output-size/output-size.md)&#39; 매개 변수를 설정하십시오.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 매개변수

</td>
<td style="border: 0;" valign="top">

### 출력 커넥터

</td>
<td style="border: 0;" valign="top">

### 예

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## 매개변수

|  |  |
| --- | --- |
| <b>색상 모드</b> *부울* | 회색 음영과 색상 출력 이미지 사이를 전환합니다. |
| <b>출력 색상</b> *Float/Float4* | 출력 이미지에 사용할 단색을 선택합니다.   &#39;색상&#39; 색상 모드를 사용하는 경우 불투명도에 Alpha 채널이 사용됩니다. 0은 완전히 투명하고 1은 완전히 불투명합니다. |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *색상/회색 음영* |  |

## 예

*곧 출시 예정*
