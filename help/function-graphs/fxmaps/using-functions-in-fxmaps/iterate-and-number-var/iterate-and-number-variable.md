---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-variable.html"
breadcrumb-title: ''
description: FXMaps에서 반복 변수 및 숫자 변수를 사용하여 반복 패턴 및 절차 변형을 만드는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Iterate and number variable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 반복 및 숫자 변수
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# 반복 및 $number 변수

![](../../../../assets/iterate-1.jpg)

Iterate 노드는 Iterations 값에 지정된 시간 동안 오른쪽 출력에 연결된 노드를 렌더링합니다.

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../assets/1-iteration.png"/></div> | 1회 반복: 가우시안 패턴이 한 번 렌더링됨 |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="../../../../assets/10-iterations.png"/></div> | 10회 반복: 동일한 위치에서 가우시안 패턴이 10회 렌더링됩니다. |

반복 노드를 사용할 때 $number 변수를 사용하여 현재 반복 값을 가져올 수 있습니다. $number는 부동 소수점 값이며 0부터 시작합니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../assets/position-function.jpg){width="300px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../assets/10-iterations-position-function.png){width="300px"}

</td>
</tr>
</table>

패턴 오프셋 매개변수로 설정된 이 함수는 각 패턴마다 하나씩 10번 실행됩니다.

첫 번째 패턴은 $number 값이 0이고 (0, 0) 좌표에서 렌더링됩니다. 두 번째 패턴은 $number 값이 1이 되고 (0.1, 0) 좌표(1 x 0.1 = 0.1)에서 다음 패턴으로 렌더링됩니다.

다운로드 샘플: [iterate\_node.sbs](https://helpx.adobe.com/content/dam/help/en/substance-3d/documentation/sddoc/files/102400023/102367299/1/1423458106000/iterate-node.sbs)
