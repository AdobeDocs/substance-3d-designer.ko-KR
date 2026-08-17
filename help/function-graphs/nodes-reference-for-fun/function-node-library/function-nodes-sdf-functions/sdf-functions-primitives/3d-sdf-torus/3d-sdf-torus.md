---
title: 토러스
description: Designer > Substance 합성 그래프 > Substance 합성 그래프에 대한 노드 참조 > 노드 라이브러리 > SDF 함수 > 프리미티브 > 토러스
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---


# 토러스

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![토러스 아이콘](./3d-sdf-torus.png "토러스")

<b>내부:</b> SDF 함수 > 기본

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

원환의 SDF 함수는 큰 원을 따라 작은 원을 쓸어 만든 모양이다.<i>두 원 모두 반경을 조정할 수 있습니다.

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
| <b>반경 주</b> *부동* | 보조 원반이 회전하면서 원환의 표면을 형성하는 원의 반지름입니다.<br><br><i>기본값: 0.5</i> |
| <b>반경 부</b> *부동* | 원환의 표면을 형성하기 위해 주 원을 따라 스윕되는 원의 반경입니다.<br><br><i>기본값: 0.2</i> |
| <b>가운데 위치</b> *Float3* | 원환의 피벗의 세계 공간 위치입니다.<br><br><i>기본값: (0, 0, 0)</i> |
| <b>P</b> *Float3* | 변형된 세계 공간 위치. <b>오프셋 P</b> 및 <b>회전 P</b> 노드를 사용하여 추가 변형을 적용하려면 이 입력을 사용합니다.<br><br><i>기본값: 변환되지 않은 월드 공간 위치.</i> |
