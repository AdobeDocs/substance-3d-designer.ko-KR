---
title: 닫힌 원추 2점
description: Designer > Substance 합성 그래프 > Substance 합성 그래프의 노드 참조 > 노드 라이브러리 > SDF 함수 > 프리미티브 > 원추형 2점
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---


# 닫힌 원추 2점

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![닫힌 원뿔 2점 아이콘](./3d-sdf-capped-cone-2-points.png "닫힌 원뿔 2점")

<b>내부:</b> SDF 함수 > 기본

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

베이스 및 상단 위치에 의해 정의된 원추에 대한 SDF 함수<br>밑면과 윗면에 조정 가능한 반경이 있습니다.

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
| <b>위치 기준</b> *Float3* | 닫힌 원뿔의 기본 위치입니다.<br><br><i>기본값: (0, 0, 0)</i> |
| <b>위쪽 위치</b> *Float3* | 닫힌 원뿔의 위쪽 위치입니다.<br><br><i>기본값: (0, 0, 1)</i> |
| <b>반경 기준</b> *부동* | 닫힌 원뿔의 기준선의 반경입니다.<br><br><i>기본값: 0.5</i> |
| <b>반경 위쪽</b> *부동* | 닫힌 원뿔의 위쪽 반경입니다.<br><br><i>기본값: 0.2</i> |
| <b>P</b> *Float3* | 변형된 세계 공간 위치. <b>오프셋 P</b> 및 <b>회전 P</b> 노드를 사용하여 추가 변형을 적용하려면 이 입력을 사용합니다.<br><br><i>기본값: 변환되지 않은 월드 공간 위치.</i> |
