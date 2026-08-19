---
title: 큐브
description: Designer > Substance 합성 그래프 > Substance 합성 그래프의 노드 참조 > 노드 라이브러리 > SDF 함수 > 프리미티브 > 큐브
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# 큐브

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![큐브 아이콘](./3d-sdf-cube.png "큐브")

<b>내부:</b> SDF 함수 > 기본

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

조정 가능한 XYZ 크기 및 모서리의 라운딩이 가능한 육면체 SDF 함수.

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
| <b>크기</b> *Float3* | X, Y 및 Z의 큐브 크기입니다.<br><br><i>기본값: (1, 1, 1)</i> |
| <b>반올림</b> *부동* | 육면체의 가장자리에 적용된 둥근 호의 반경입니다.<br><br><i>참고:</i> 둥근 반경이 교차하는 곳에 단단한 가장자리가 나타날 수 있습니다.<br><br><i>기본값: 0</i> |
| <b>피벗 위치(로컬)</b> *Float3* | 큐브의 로컬 피벗의 세계 공간 위치입니다. 여기서 (0, 0, 0)은 피벗을 큐브의 중심에 배치합니다.<br><br><i>기본값: (0, 0, -0.5)</i> |
| <b>가운데 위치</b> *Float3* | 큐브의 피벗의 세계 공간 위치입니다.<br><br><i>기본값: (0, 0, 0)</i> |
| <b>P</b> *Float3* | 변형된 세계 공간 위치. <b>오프셋 P</b> 및 <b>회전 P</b> 노드를 사용하여 추가 변형을 적용하려면 이 입력을 사용합니다.<br><br><i>기본값: 변환되지 않은 월드 공간 위치.</i> |
