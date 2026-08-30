---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/bitmap.html"
breadcrumb-title: ''
description: 비트맵 노드를 사용하여 비트맵 이미지를 가져와 Substance 합성 그래프의 텍스처로 사용할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Bitmap
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 비트맵
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 1%

---


# 비트맵

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomic node: 비트맵](bitmap.resources/comp_bitmap.png "Atomic node: 비트맵"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

[비트맵 리소스](../../../../resources/bitmap-resource/bitmap-resource.md)를 그래프에 로드합니다.

이 노드는 [비트맵](../../../../glossary/glossary.md)을 그래프로 가져오거나 [비트맵 페인팅 도구](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)와 함께 사용할 새 비트맵을 만드는 데 사용됩니다.

이 노드를 만드는 몇 가지 방법이 있으며, 이 방법은 모두 [리소스 연결과 가져오기의 차이점](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)을 이해해야 합니다.

</td>
</tr>
</table>

노드를 처음부터 만들거나 지원되는 형식의 [비트맵](../../../../glossary/glossary.md)을 그래프 보기로 놓아 만들 수 있습니다.

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
> 생성하거나 가져온 8비트 비트맵은 [2D 보기](../../../../interface/2d-view/2d-view.md) 도크에서 [비트맵 페인팅 도구](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)를 사용하여 페인팅할 수 있습니다.

>[!IMPORTANT]
>
> 이 노드는 외부 리소스에 종속되므로 해당 노드를 사용할 때 유의해야 할 몇 가지 사항이 있습니다.
> 
> * 비트맵 노드는 색상이나 회색 음영을 반환할 수 있지만 리소스가 회색 음영 비트맵인 경우에도 기본적으로 색상이 사용됩니다. 이는 그래프 성능과 복잡성에 영향을 줄 수 있으므로 필요한 경우 항상 &#39;회색 음영&#39; [색상 모드](#parameters)로 전환해야 합니다.
> * 비트맵 노드를 삭제해도 [패키지](../../../../glossary/glossary.md)에서 [비트맵 리소스](../../../../resources/bitmap-resource/bitmap-resource.md)은(는) 삭제되지 않으며 [탐색기](../../../../interface/the-explorer-window/the-explorer-window.md)에서 수동으로 삭제해야 합니다.
> * 반면에 탐색기에서 [비트맵 리소스](../../../../resources/bitmap-resource/bitmap-resource.md)을 삭제할 때는 주의해야 합니다. 이 리소스는 캐시에 유지되므로 해당 세션의 그래프에서 계속 작동하지만 다음에 [패키지](../../../../glossary/glossary.md)를 로드할 때 리소스가 누락된 것으로 표시됩니다.
> * Substance 그래프가 [조리](../../../../glossary/glossary.md)되면 비트맵 해상도는 원래 크기를 기반으로 하지 않고 그래프 내의 해상도로 고정됩니다. 비트맵 노드의 &#39;Output size&#39; [기본 매개 변수](../../../../glossary/glossary.md)이(가) &#39;Absolute&#39; [상속 메서드](../../../../glossary/glossary.md)을(를) 사용하고, 노드 뒤에 &#39;Relative to parent&#39;로 설정된 [Transform 2D](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) 노드(즉, 호스트 그래프의 해상도)를 사용하는 것이 좋습니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 매개변수

</td>
<td style="border: 0;" valign="top">

### 비트맵 페인팅 도구

</td>
<td style="border: 0;" valign="top">

### 출력 커넥터

</td>
<td style="border: 0;" valign="top">

### 예

</td>
</tr>
</table>

## 매개변수

|  |  |
| --- | --- |
| <b>색상 모드</b> *부울* | 노드의 출력 유형을 결정하며 컬러 또는 회색 음영으로 돌아갑니다. |
| <b>패키지 리소스 경로</b> *문자열* | 노드에서 참조하는 [비트맵 리소스](../../../../resources/bitmap-resource/bitmap-resource.md)의 경로입니다.   수동으로 입력하지 않고 탐색기에서 리소스를 복사하여 매개 변수 텍스트 필드에 붙여넣거나, [탐색기](../../../../interface/the-explorer-window/the-explorer-window.md)에서 직접 그래프의 비트맵 노드로 비트맵 리소스를 끌어서 놓는 것이 좋습니다. |
| <b>메서드 크기 조정</b> *정수* | 비트맵을 확대 또는 축소할 때 사용할 리샘플링 방법은 다음과 같습니다.<ul data-preserve-html="true"> <li data-preserve-html="true"><i>매끄러운 스트레치:</i> [쌍선형 필터링](../../../../glossary/glossary.md)을 적용하여 스트레치된 이미지의 소스 픽셀을 보간합니다.</li> <li data-preserve-html="true"><i>가장 가까운 스트레치:</i> 이미지를 늘이고 가장 가까운 소스 픽셀의 색상을 그대로 사용합니다.</li> </ul> |

## 비트맵 페인팅 도구

Designer에서 비트맵을 편집할 수 있습니다. [이 섹션](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)의 편집 도구에 대해 자세히 알아보세요.

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *회색 음영/색상* |  |

## 예

*곧 출시 예정*
