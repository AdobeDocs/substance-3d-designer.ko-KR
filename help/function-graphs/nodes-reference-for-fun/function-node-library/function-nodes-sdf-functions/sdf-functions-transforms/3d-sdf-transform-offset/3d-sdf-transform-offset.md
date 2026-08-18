---
title: 오프셋
description: Designer > Substance 합성 그래프 > Substance 합성 그래프의 노드 참조 > 노드 라이브러리 > SDF 함수 > 변형 > 오프셋
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---


# 오프셋

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![오프셋 아이콘](./3d-sdf-transform-offset.png "오프셋")

<b>내부:</b> SDF 함수 > 변형

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

벡터를 따라 SDF 모양 오프셋

</td>
</tr>
</table>

<a name='inputs'></a>

|  |  |
| :--- | :--- |
| <b>SDF</b> *부동* | 입력 SDF 셰이프입니다. |
| <b>오프셋</b> *Float3* | SDF 모양이 X, Y, Z 방향으로 오프셋될 거리입니다.<br><br><i>기본값: (0, 0, 0)</i> |
| <b>P</b> *Float3* | 변형된 세계 공간 위치. <b>오프셋 P</b> 및 <b>회전 P</b> 노드를 사용하여 추가 변형을 적용하려면 이 입력을 사용합니다.<br><br><i>기본값: 변환되지 않은 월드 공간 위치.</i> |
