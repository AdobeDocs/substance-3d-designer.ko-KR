---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/constant-nodes.html"
breadcrumb-title: ''
description: Substance 3D Designer 함수 그래프에서 상수 노드에 액세스하여 상수 값과 매개변수를 정의합니다.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Constant
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 상수
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 0%

---


# 상수

상수 노드는 Substance 함수 그래프 내에서 사용할 정적 값을 만드는 방법입니다. [변수](../../../../function-graphs/variables/variables.md)와 달리 외부에서 수정할 수 없습니다.

또한 이 페이지에서는 각 데이터 유형 및 일반적인 사용 사례에 대한 몇 가지 추가 정보를 제공합니다.

## 정수

상수 정수는 정수를 생성하며 1의 단계를 가진다.

[Float,](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md)(으)로 변환할 수 있습니다. 이 변환은 추가, 빼기 및 단순 비교보다 복잡한 작업을 수행할 때 권장됩니다.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![정수 형식 아이콘](../../../../assets/fn-constant-integer.png "정수 형식 아이콘")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>정수</b>

정수는 단일 구성 요소를 가집니다. 다음과 같이 선택할 수 있는 색인으로 유용합니다.

* 사용자에게 드롭다운 메뉴로 표시되는 옵션 선택([이 페이지](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)의 &#39;드롭다운 목록&#39; 참조)
* [다중 스위치](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md) 노드의 입력을 선택하는 중입니다.<b></b>

>[!IMPORTANT]
>
> 매개 변수 함수의 <b>음수 정수</b>는 *지원되지 않습니다*. 해결 방법은 &#39;기술 문제&#39; 섹션의 [이 페이지](../../../../technical-issues/parameters-not-working/parameters-not-working-as-expected.md)를 참조하십시오.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Integer2 형식 아이콘](../../../../assets/fn-constant-integer2.png "Integer2 형식 아이콘")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>정수2</b>

Integer2 노드는 (X, Y) 개의 구성 요소를 가진 정적 2-구성 요소 정수 벡터를 생성한다.

Integer2는 일반적으로 사용되지 않지만 예를 들어 [Tile Generator](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)에서 X 및 Y 2D 타일링을 설정하는 데 사용됩니다.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Integer3 형식 아이콘](../../../../assets/fn-constant-integer3.png "Integer3 형식 아이콘")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>정수3</b>

Integer3 노드는 (X, Y, Z) 성분을 갖는 정적 3-성분 정수 벡터를 생성한다.

정수 3은 흔히 사용되지 않으며 많이 발생할 가능성이 낮습니다.<b>\
</b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Integer4 형식 아이콘](../../../../assets/fn-constant-integer4.png "Integer4 형식 아이콘")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>정수4</b>

Integer4 노드는 (X, Y, Z, W) 성분을 갖는 정적 4-성분 정수 벡터를 생성한다.

정수 4는 일반적이지 않으며 많이 발생할 가능성이 낮습니다.<b>\
</b>

</td>
</tr>
</table>

## 부동

상수 부동 소수점 자리는 전체 숫자가 아닌 분수를 생성합니다. 즉, 소수점 기호 뒤에 항상 값을 가지며 1보다 작은 단계만큼 증가 또는 감소할 수 있습니다(기본값 0.01).

[부동 소수점 수는 정수](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md)로 변환할 수 있지만 반올림하거나 가장 가까운 정수로 내려갑니다. 데이터 및 정확도가 손실됩니다.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![부동 형식 아이콘](../../../../assets/fn-constant-float.png "부동 형식 아이콘")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>부동</b>

플로트는 단일 구성 요소를 가지며, (1)은 간결성을 위해 이름에서 생략된다. Float는 매우 일반적이며 슬라이더 또는 각도 형태의 정밀한 제어가 필요한 모든 값에 사용됩니다. 거의 모든 노드의 매개 변수에서 찾을 수 있습니다. 또한 회색 음영 값의 기본 데이터 형식입니다.<b></b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Float2 형식 아이콘](../../../../assets/fn-constant-float2.png "Float2 형식 아이콘")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float2</b>

Float2 노드는 정적 2 구성 요소 Float 벡터를 생성합니다. 구성 요소의 이름은 X, Y입니다. Float2는 매우 일반적이며 [샘플링 좌표](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) 및 [변환 오프셋](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/transforms.md)에 사용됩니다.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Float3 형식 아이콘](../../../../assets/fn-constant-float3.png "Float3 형식 아이콘")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float3</b>

Float3 노드는 정적 3 구성 요소 Float 벡터를 생성합니다. 구성 요소의 이름은 X,Y,Z입니다. Float3는 흔하지 않으며, 주로 [3D 배율 좌표](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md)를 나타내는 데 사용되며, Alpha 데이터 없이 색상을 더 간단하게 저장하는 데 사용됩니다.<b>\
</b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Float4 형식 아이콘](../../../../assets/fn-constant-float4.png "Float4 형식 아이콘")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float4</b>

Float4는 정적 4 구성 요소 Float 벡터를 생성합니다.구성 요소의 이름은 X,Y,Z,W입니다. Float4는 [색상 정보를 저장하고 설정하는 기본 방법이므로 매우 일반적입니다. 여기서 XYZW 데이터는 RGBA 값을 나타냅니다.](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md)<b>\
</b>

</td>
</tr>
</table>

## 기타

Substance 함수 그래프에는 부울과 문자열이라는 두 개의 추가 데이터 유형이 있습니다. 문자열은 Designer 버전 6에서 [텍스트](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) 노드와 함께 도입되었습니다.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![부울 유형 아이콘](../../../../assets/fn-constant-boolean.png "부울 유형 아이콘")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>부울</b>

부울은 True 또는 False, 1 또는 0의 두 가지 상태만 알고 있는 가장 간단한 데이터 형식입니다. 흰색으로 표시됩니다. [Casting](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md) 없이 또는 [논리 노드](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md)를 사용하여 부울과 정수를 교환할 수 없습니다. 부울은 매우 일반적이며 함수 또는 그래프의 흐름을 제어하는 탁월한 방법입니다. 일반적으로 [스위치 노드](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md)<b></b>에 사용됩니다.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![문자열 유형 아이콘](../../../../assets/fn-constant-string.png "문자열 유형 아이콘")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>문자열</b>

문자열 노드는 정적 문자열(텍스트의 일부)을 생성합니다. 이 데이터 형식은 함수에서 사용할 수 있는 가장 이국적인 데이터 형식이며 일반적으로 다른 함수 노드와 함께 사용할 수 없습니다. 주된 목표는 [텍스트 노드](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)의 최종 출력으로 작동하는 것입니다.

</td>
</tr>
</table>
