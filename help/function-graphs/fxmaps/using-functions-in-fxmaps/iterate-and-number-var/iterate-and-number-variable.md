---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-variable.html"
breadcrumb-title: ''
description: FXMaps에서 반복 및 번호 변수를 사용하여 반복 패턴 및 프로시저 변형을 만드는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Iterate and number variable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 반복 및 숫자 변수
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# 반복 및 `$number` 변수

![](iterate-and-number-variable.resources/iterate-and-number-variable-01.jpg)

반복 노드는 반복 값에 지정된 시간 동안 오른쪽 출력에 연결된 노드를 렌더링합니다.

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="iterate-and-number-variable.resources/iterate-and-number-variable-02.png"/></div> | 1반복: 가우시안 패턴이 한 번 렌더링됨 |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="iterate-and-number-variable.resources/iterate-and-number-variable-03.png"/></div> | 10개 반복: 동일한 위치에서 가우시안 패턴이 10번 렌더링됩니다. |

반복 노드를 사용할 때는 `$number` 변수를 사용하여 현재 반복 값을 가져올 수 있습니다. `$number`은(는) 부동 소수점 값이며 0에서 시작합니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](iterate-and-number-variable.resources/iterate-and-number-variable-04.jpg){width="300px"}

</td>
<td style="border: 0;" valign="top">

![](iterate-and-number-variable.resources/iterate-and-number-variable-05.png){width="300px"}

</td>
</tr>
</table>

패턴 오프셋 매개변수로 설정된 이 함수는 각 패턴마다 하나씩 10번 실행됩니다.

첫 번째 패턴의 `$number` 값은 0이고 (0, 0) 좌표에서 렌더링됩니다. 두 번째 패턴의 `$number` 값은 1이고 다음 패턴에 대해 (0.1, 0) 좌표(1 x 0.1 = 0.1) 등으로 렌더링됩니다.
