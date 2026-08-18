---
title: 원통 2 포인트
description: Designer > Substance 합성 그래프 > Substance 합성 그래프의 노드 참조 > 노드 라이브러리 > SDF 함수 > 프리미티브 > 원통 2점
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---


# 원통 2 포인트

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![원통 2점 아이콘](./3d-sdf-cylinder-2-points.png "원통 2점")

<b>내부:</b> SDF 함수 > 기본

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

시작 및 끝 디스크의 위치에 따라 정의되는 조정 가능한 반지름의 원통에 대한 SDF 함수.

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
| <b>시작</b> *Float3* | 실린더의 시작 디스크 위치입니다.<br><br><i>기본값: (0, 0, 0)</i> |
| <b>종료</b> *Float3* | 실린더의 끝 디스크 위치입니다.<br><br><i>기본값: (0, 0, 1)</i> |
| <b>반경</b> *부동* | 원통의 반경입니다.<br><br><i>기본값: 0.25</i> |
| <b>P</b> *Float3* | 변형된 세계 공간 위치. <b>오프셋 P</b> 및 <b>회전 P</b> 노드를 사용하여 추가 변형을 적용하려면 이 입력을 사용합니다.<br><br><i>기본값: 변환되지 않은 월드 공간 위치.</i> |
