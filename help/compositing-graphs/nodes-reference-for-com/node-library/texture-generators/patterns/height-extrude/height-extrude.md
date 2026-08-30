---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/height-extrude.html"
breadcrumb-title: ''
description: 텍스처에서 3D 깊이 효과를 만들기 위해 높이 맵을 기반으로 모양을 돌출시키려면 높이 돌출 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Height Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 높이 돌출
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 3%

---


# 높이 돌출

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-extrude.resources/height-extrude.png){width="200px"}

<b>내부:</b> 텍스처 생성기 > 패턴

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

높이 돌출은 입력 높이 맵에서 3D Z 깊이를 렌더링합니다. [모양 돌출](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) 및 [큐브 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md)와 마찬가지로 이 도구를 사용하면 2D 보기에서 카메라를 회전할 수 있습니다. 평면 높이 맵에서 3D 회전 모양을 만드는 제네레이터 역할을 하는 것이 주요 목표입니다. 그런 다음 이러한 모양을 [모양 튀김](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md)과 함께 사용할 수 있습니다.

[모양 돌출](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md)의 주된 차이점은 입력 맵이 이진 &quot;알파&quot; 형식의 맵이 아니라 전체 범위의 회색 음영 맵이어야 한다는 것입니다. 즉, 돌출 Height(유기적이고 복잡한 모양)은 더 잘 제어할 수 있지만 경사 프로파일(단단한 표면, 단순한 모양)은 제어할 수 없습니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>카메라 각도</b> | 반회전으로 카메라의 오일러 각도 수평 회전 및 배율은 입력에 직접 적용됩니다. |
| <b>카메라 비율</b> <i>0.001 - 3.0</i> | 출력에 적용된 전체 비율입니다. |
| <b>Height 크기</b> <i>0.0 - 2.0</i> | 입력 Height 값에 전역 계수를 적용합니다. |
| <b>세로 오프셋</b> <i>-1.0 - 1.0</i> | 최종 출력을 위 또는 아래로 이동합니다. |
| <b>지표</b> <i>끄기/켜기</i> | Ground가 꺼져 있으면 지면과 같은 평면이 아니라 입력이 0인 검정 배경이 표시됩니다. |
| <b>표준 형식</b> <i>DirectX/OpenGL</i> | <b>표준 형식</b> 매개 변수는 노멀 맵의 y 좌표를 반전합니다. |
| <b>표준 강도</b> <i>0.0 - 256.0</i> | <b>표준</b> 노드의 <b>강도</b> 매개 변수와 동일합니다. 회전하는 동안 충돌이 없는 표준이 되도록 이를 256으로 설정하십시오. |
