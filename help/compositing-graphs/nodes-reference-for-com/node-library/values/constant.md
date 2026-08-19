---
helpx_url: ""
breadcrumb-title: ''
description: Substance 3D Designer의 상수 노드에 액세스하여 Substance 그래프에서 상수 값을 정의합니다.
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 상수
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2cb8395834eb64124ebadb2cd051aead9babfa69
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---


# 상수

상수 노드는 Substance 그래프 내에서 사용할 정적 값을 만드는 방법입니다.

라이브러리의 **값 > 상수** 섹션에서 이러한 노드를 찾을 수 있습니다.\
여기에는 모두 값을 생성하는 간단한 [값 프로세서](../../atomic-nodes/value-processor/value-processor.md) 노드가 포함됩니다.

+++ 라이브러리의 상수 노드

![constants-library.png](constant.resources/constants-library.png)

+++

<p style="text-align: center;"><img src="./constant.resources/constants-float-01.png" alt="상수 부동 노드" /></p>

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

Integer2의 일반적인 사용 사례 중 하나는 [Tile Generator](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) 노드에서처럼 X 및 Y 격자 크기를 설정하도록 설정하는 것입니다.

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

</td>
</tr>
</table>

## 부동

상수 부동 소수점 값은 소수점 기호 이후의 값을 지원하며 1보다 작은 단계로 조정할 수 있습니다. (기본값: 0.01)

[부동 소수점 수는 정수](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md)로 변환할 수 있지만 반올림하거나 가장 가까운 정수로 내려갑니다. 데이터 및 정확도가 손실됩니다.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![부동 형식 아이콘](../../../../assets/fn-constant-float.png "부동 형식 아이콘")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>부동</b>

플로트는 단일 컴포넌트를 가지며 정밀도가 필요한 모든 단일 값에 매우 일반적으로 사용됩니다.

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

Float2 노드는 (X, Y) 성분을 갖는 2-성분 벡터를 생성한다.

Float2는 일반적으로 [샘플링 좌표](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md), [오프셋 변환](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/transforms.md) 및 일반적인 2D 벡터 조작에 사용됩니다.

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

Float3 노드는 3성분 (X, Y, Z) 벡터를 생성한다.

Float3는 [3D SDF 노드](../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions)와 같이 3D 개체와 [3D 배율 좌표](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md)를 사용하여 작업할 때, 그리고 Alpha 없이 RGB 색상을 저장하는 간단한 방법으로 주로 사용됩니다.

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

Float4는 4성분 (X, Y, Z, W) 벡터를 생성한다.

Float4는 [균일 색상 노드](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md)에서와 같이 XYZW 값이 RGBA에 매핑되는 색상 정보를 저장하고 설정하는 기본 방법입니다.

</td>
</tr>
</table>

## 비수치

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![부울 유형 아이콘](../../../../assets/fn-constant-boolean.png "부울 유형 아이콘")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>부울</b>

Boolean은 두 가지 상태만 알고 있는 가장 단순한 데이터 형식입니다. <code>true</code> 또는 <code>false</code>.

이 유형은 토글 매개 변수 및 [If/Else](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/control-nodes/control-nodes.md) 조건으로 작업할 때 매우 일반적입니다.<br>부울은 [스위치 노드](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md)를 사용하여 함수 또는 그래프의 흐름을 제어하는 간단하고 효율적인 방법입니다.

</td>
</tr>
</table>
