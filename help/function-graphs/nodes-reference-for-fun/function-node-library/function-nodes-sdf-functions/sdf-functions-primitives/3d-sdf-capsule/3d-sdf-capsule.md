---
title: 캡슐
description: Designer > Substance 합성 그래프 > Substance 합성 그래프의 노드 참조 > 노드 라이브러리 > SDF 함수 > 프리미티브 > 캡슐
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 2%

---


# 캡슐

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![캡슐 아이콘](./3d-sdf-capsule.png "캡슐")

<b>내부:</b> SDF 함수 > 기본

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

길이 및 반경 조절이 가능한 캡슐 SDF 함수.<br>캡슐은 두 개의 구를 연결한 결과입니다.

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
| <b>시작</b> *Float3* | 시작 구의 위치입니다.<br><br><i>기본값: (0, 0, 0)</i> |
| <b>종료</b> *Float3* | 끝 구의 위치입니다.<br><br><i>기본값: (0, 0, 1)</i> |
| <b>반경</b> *부동* | 시작 구와 끝 구의 반경입니다.<br><br><i>기본값: 0.25</i> |
| <b>팁에서 시작/종료</b> *부울* | <b>시작</b> 및 <b>끝</b> 위치가 구의 끝부분에 있어야 하는지 여부를 제어합니다.<br>즉, 캡슐의 Height에 구의 반경이 포함되어야 하는지 여부를 제어합니다.<br><br><i>기본값: 거짓</i> |
| <b>가운데 위치</b> *Float3* | 캡슐의 피벗의 세계 공간 위치입니다.<br><br><i>기본값: (0, 0, 0)</i> |
| <b>P</b> *Float3* | 변형된 세계 공간 위치. <b>오프셋 P</b> 및 <b>회전 P</b> 노드를 사용하여 추가 변형을 적용하려면 이 입력을 사용합니다.<br><br><i>기본값: 변환되지 않은 월드 공간 위치.</i> |
