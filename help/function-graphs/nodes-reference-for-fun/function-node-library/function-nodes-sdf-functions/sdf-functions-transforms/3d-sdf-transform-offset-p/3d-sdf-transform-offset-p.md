---
title: 오프셋
description: Designer > Substance 합성 그래프 > Substance 합성 그래프의 노드 참조 > 노드 SDF 함수 > 노드 라이브러리 > 오프셋 P
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---


# 오프셋

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![오프셋 P 아이콘](./3d-sdf-transform-offset-p.png "오프셋 P")

<b>SDF 함수:</b> 변환 >

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

벡터를 따라 월드 공간을 오프셋합니다.<br>출력 변환 위치를 대부분의 SDF 함수의 <b>P</b> 입력에 연결하여 이 월드 공간 팁에서 정의할 수 있습니다.<br><br><i>변환은 연결 상태이지만 작업의 순서에 따라 결과가 달라질 수 있습니다.</i>

</td>
</tr>
</table>

<a name='inputs'></a>

>[!INFO]
> 
> SDF 함수와 관련된 개념 및 작업 과정에 대해 자세히 알아보려면 전용 페이지로 이동하십시오. [SDF 함수 작업](../../working-with-sdf-functions.md)

## 입력

|  |  |
| :--- | :--- |
| <b>오프셋</b> *Float3* | 월드 공간이 X, Y 및 Z 방향으로 오프셋될 거리입니다. |
| <b>P</b> *Float3* | 변형된 세계 공간 위치. <b>오프셋 P</b> 및 <b>회전 P</b> 노드를 사용하여 추가 변형을 적용하려면 이 입력을 사용합니다.<br><br><i>기본값: 변환되지 않은 월드 공간 위치.</i> |
