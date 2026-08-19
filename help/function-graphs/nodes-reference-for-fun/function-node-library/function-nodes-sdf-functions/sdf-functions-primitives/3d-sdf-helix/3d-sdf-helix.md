---
title: 헬릭스(약)
description: Designer > Substance 합성 그래프 > Substance 합성 그래프의 노드 참조 > 노드 라이브러리 > SDF 함수 > 프리미티브 > 헬릭스(근사치)
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# 헬릭스(약)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![헬릭스(약) 아이콘](./3d-sdf-helix.png "헬릭스(약)")

<b>내부:</b> SDF 함수 > 기본

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

헬릭스의 근사치를 위한 SDF 함수로, 축을 중심으로 상향 곡선을 따라 곡선을 따라 원을 쓸어 만든 모양입니다.<br><br><i>참고:</i>이 SDF 함수는 근사치이므로 렌더링 시 아티팩트가 나타날 수 있습니다.

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
| <b>주 반경</b> *부동* | 축에서 굴곡 곡선의 거리입니다.<br><br><i>기본값: 0.4</i> |
| <b>보조 반경</b> *부동* | 곡선을 따라 스윕되어 헬릭스의 표면을 형성하는 원의 반지름입니다.<br><br><i>기본값: 0.1</i> |
| <b>Height</b> *부동* | 헬릭스의 Z-up Height.<br><br><i>기본값: 0.5</i> |
| <b>권선</b> *부동* | 0.5.<br>Height 내에서 헬릭이 얼마나 많이 회전하는지에 대한 단계로 커브가 축을 중심으로 완전히 감기는 횟수입니다.<br><br><i>기본값: 4</i> |
| <b>가운데 위치</b> *Float3* | 헬릭선 피벗의 세계 공간 위치입니다.<br><br><i>기본값: (0, 0, 0)</i> |
| <b>P</b> *Float3* | 변형된 세계 공간 위치. <b>오프셋 P</b> 및 <b>회전 P</b> 노드를 사용하여 추가 변형을 적용하려면 이 입력을 사용합니다.<br><br><i>기본값: 변환되지 않은 월드 공간 위치.</i> |
