---
title: 결합 모따기
description: Designer > Substance 합성 그래프 > Substance 합성 그래프의 노드 참조 > 노드 라이브러리 > SDF 함수 > 연산자 > 결합 모따기
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# 결합 모따기

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![합치기 모따기 아이콘](./3d-sdf-op-union-chamfer.png "합치기 모따기")

<b>내부:</b> SDF 함수 > 연산자

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

두 SDF 모양의 추가된 볼륨을 반환하며, 교차점 가장자리를 따라 조정 가능한 반경의 추가 볼륨을 반환합니다.

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
| <b>SDF 1</b> *부동* | 첫 번째 SDF 모양입니다. |
| <b>SDF 2</b> *부동* | 두 번째 SDF 모양입니다. |
| <b>반경</b> *부동* | 모양의 교차점 가장자리를 따라 추가된 볼륨의 반경입니다.<br><br><i>기본값: 0</i> |
