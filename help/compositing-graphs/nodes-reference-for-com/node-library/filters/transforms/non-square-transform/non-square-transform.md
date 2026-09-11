---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-square-transform.html"
breadcrumb-title: ''
description: 비 사각형 노드를 사용하고 독립적인 Y 비율을 갖는 비 사각형 텍스처에 변환을 적용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Square Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 비-사각형
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 4%

---


# 비-사각형

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](non-square-transform.resources/safe-transform.png)

![](non-square-transform.resources/safe-transform-grayscale.png)

<b>필터</b>:

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

[변환 2D&lbrace;1의 사각형이 아닌 안전한 버전. &#x200B;](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)정사각형이 아닌 비율을 자동으로 감지하여 정사각형이 아닌 캔버스에 이미지를 입력할 수 있습니다.

몇 가지 설정을 올바르게 설정해야 하므로 이 노드를 최대한 활용하려면 [그래프 매개 변수](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)를 완전히 이해해야 합니다.

* **그래프** 크기는 정사각형이 아니어야 합니다. 그렇지 않으면 이 노드가 필요하지 않습니다.
* 비 제곱 **노드**&#x200B;의 출력 크기를 &quot;*부모*&quot;으로 설정합니다.
* 단일 위치에 대한 입력만 원하는 경우 **노드** 타일링 모드를 &quot;*타일링 없음*&quot;으로 설정합니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>타일 모드</b> <i>자동, 수동</i> | 정사각형이 아닌 자동 보상을 활성화하거나 활성화하지 마십시오. |
| <b>타일</b> <i>1 - 16</i> | [타일 모드]가 [수동]으로 설정된 경우에만 액세스할 수 있습니다. 타일링에 적합한 방식으로 배율을 변경할 수 있습니다. |
| <b>오프셋</b> <i>0.0 - 1.0</i> | 결과를 이동하거나 변환합니다. 슬라이더를 두 번 클릭하여 음수 값을 입력합니다. |
| <b>회전</b> <i>0.0 - 1.0</i> | 입력 이미지를 회전합니다. |
| <b>안전한 회전(정사각형만 해당)</b> <i>거짓/참</i> | 안전한 값에 스냅하여 픽셀의 선명도를 유지합니다. |
| <b>배경색</b> <i>(색상 값)</i> | 이미지를 채울 배경색입니다. 기본 매개 변수의 [타일링 모드가 &quot;*타일링 없음*&quot;](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)&quot;으로 설정된 경우에만 표시됩니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="non-square-transform.resources/nonsquare-ex.png" />
        </td>
    </tr>
</table>
