---
title: 굽히기(부정확함)
description: Designer > Substance 합성 그래프 > Substance 합성 그래프의 노드 참조 > 노드 라이브러리 > SDF 함수 > 변형 > 벤드(부정확하게)
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 1%

---


# 굽히기(부정확함)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![굽히기(부정확한) 아이콘](./3d-sdf-transform-bend.png "굽히기(부정확한)")

<b>내부:</b> SDF 함수 > 변형

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

특정 각도에서 시작점과 끝점 사이의 로컬 Y축을 중심으로 SDF 모양을 굽힙니다.<br><br><i>참고:</i>이 변환 함수는 정확하지 않으므로 렌더링 시 아티팩트가 나타날 수 있습니다.

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
| <b>SDF</b> *부동* | 입력 SDF 셰이프입니다. |
| <b>각도</b> *부동* | 벤드 끝에 적용된 회전 각도(회전 단위) |
| <b>시작</b> *부동* | 벤딩이 시작되는 Z축의 월드 위치입니다. 아래 모든 볼륨이 구부러지지 않았습니다. |
| <b>종료</b> *부동* | 벤딩이 끝나는 Z축의 세계 위치입니다. 상기 모든 부피는 지정된 각도로 균일하게 회전된다. |
| <b>P</b> *Float3* | 변형된 세계 공간 위치. <b>오프셋 P</b> 및 <b>회전 P</b> 노드를 사용하여 추가 변형을 적용하려면 이 입력을 사용합니다.<br><br><i>기본값: 변환되지 않은 월드 공간 위치.</i> |
