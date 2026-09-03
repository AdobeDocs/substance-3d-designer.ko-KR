---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/svg.html"
breadcrumb-title: ''
description: SVG 노드를 사용하여 SVG 벡터 그래픽을 확장 가능한 그래픽 요소를 만들기 위한 텍스처로 가져오고 렌더링합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > SVG
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SVG
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 1%

---


# SVG

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomic node: SVG](svg.resources/svg-01.png "Atomic node: SVG"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

[SVG 이미지](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)를 비트맵으로 렌더링합니다. 즉, 벡터 모양을 픽셀로 매핑합니다.

이 노드를 만드는 몇 가지 방법이 있으며, 이 방법은 모두 [리소스를 연결하는 것과 가져오는 것의 차이](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)를 이해해야 합니다.

</td>
</tr>
</table>

노드를 처음부터 새로 만들거나 SVG 파일을 그래프 보기로 놓아 만들 수 있습니다.

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
> 생성되었거나 가져온 SVG 이미지는 [2D 보기](../../../../interface/2d-view/2d-view.md) 도크에서 [벡터 편집 도구](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md)를 사용하여 편집할 수 있습니다.

>[!IMPORTANT]
>
> 이 노드는 외부 리소스에 종속되므로 해당 노드를 사용할 때 유의해야 할 몇 가지 사항이 있습니다.
> 
> * SVG 노드는 색상이나 회색 음영을 반환할 수 있지만 리소스가 회색 음영 벡터인 경우에도 기본적으로 색상으로 설정됩니다. 이는 그래프 성능과 복잡성에 영향을 줄 수 있으므로 필요한 경우 항상 &#39;회색 음영&#39; [색상 모드](#parameters)로 전환해야 합니다.
> * SVG 노드를 삭제해도 [패키지](../../../../glossary/glossary.md)에서 [SVG 리소스](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)가 삭제되지 않습니다. [탐색기](../../../../interface/the-explorer-window/the-explorer-window.md)에서 수동으로 삭제해야 합니다.
> * SVG 모양은 모양/다각형으로 [테셀레이션](../../../../glossary/glossary.md)한 다음 Substance 그래프에 비트맵으로 사용하기 위해 *래스터화*&#x200B;합니다. 이러한 작업에 사용되는 기술은 윤곽선과 같은 여러 벡터 속성을 지원하지 않습니다. [여기](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)에서 이러한 제한 사항에 대해 자세히 알아보세요.

>[!WARNING]
>
> SVG 모양은 모양/다각형으로 [테셀레이션](../../../../glossary/glossary.md)한 다음 Substance 그래프에 비트맵으로 사용하기 위해 *래스터화*&#x200B;합니다.
> 
> 이러한 작업에 사용되는 기술은 윤곽선과 같은 여러 벡터 속성을 지원하지 않습니다.
> 
> [여기](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)에서 이러한 제한 사항에 대해 자세히 알아보세요.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 예

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## 매개변수

|  |  |
| --- | --- |
| <b>색상 모드</b> *부울* | 노드의 출력 유형을 결정하며 컬러 또는 회색 음영으로 돌아갑니다. |
| <b>배경색</b> *색상/회색 음영* | 벡터 모양으로 가려지지 않은 영역에서 사용할 출력 이미지의 배경색을 설정합니다.   *해당 입력이 연결되면 &#39;[배경](#inputs)&#39; 입력에 의해 재정의됩니다.* |
| <b>패키지 리소스 경로</b> *문자열* | 노드에서 참조하고 있는 [SVG 리소스](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)에 대한 경로입니다.   수동으로 입력하지 않고 탐색기에서 리소스를 복사하여 매개 변수 텍스트 필드에 붙여넣거나, [탐색기](../../../../interface/the-explorer-window/the-explorer-window.md)에서 직접 그래프의 SVG 노드로 비트맵 리소스를 끌어서 놓는 것이 좋습니다. |

## 벡터 편집 도구

벡터 모양은 Designer에서 편집할 수 있습니다. [이 섹션](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md)의 편집 도구에 대해 자세히 알아보세요.

## 입력 커넥터

|  |  |
| --- | --- |
| <b>배경</b> 기본 *회색 음영/색상* | 벡터 모양으로 가려지지 않은 영역에서 사용할 출력 이미지의 배경색을 설정합니다.   *연결할 때 &#39;[배경색](#parameters)&#39; 매개 변수를 재정의합니다.* |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *회색 음영/색상* |  |

## 예

*곧 출시 예정*
