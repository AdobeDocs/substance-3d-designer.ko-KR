---
title: 록
description: Designer > Substance 합성 그래프 > Substance 합성 그래프의 노드 참조 > 노드 라이브러리 > SDF 함수 > 프리미티브 > 바위
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---


# 록

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![바위 아이콘](./3d-sdf-rock.png "바위")

<b>내부:</b> SDF 함수 > 기본

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

SDF 함수를 사용하여 빌드된 파라메트릭 및 임의화 가능한 바위 모양의 SDF 함수.

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
| <b>최대. 패싯</b> *정수* | 암석의 최대 면 수(최대 32개).<br><br><i>기본값: 8</i> |
| <b>Smoothness</b> *부동* | 바위의 가장자리에 적용된 둥근 호의 반경입니다.<br><br><i>기본값: 0</i> |
| <b>임의성</b> *부동* | 면의 방향과 중심까지의 거리를 불안정하게 합니다.<br>결과적으로 값이 클수록 바위가 작아집니다.<br><br><i>기본값: 0</i> |
| <b>시드</b> *부동* | <b>임의성</b> 매개 변수의 초기값입니다.<br><br><i>기본값: 0</i> |
| <b>크기 조절</b> *부동* | 바위 모양의 전체 비율입니다.<br><b>임의성</b> 후 및 <b>Smoothness</b> 전에 적용되었습니다.<br><br><i>기본값: 0.5</i> |
| <b>가운데 위치</b> *Float3* | 암석의 피벗의 세계 공간 위치입니다.<br><br><i>기본값: (0, 0, 0.5)</i> |
| <b>P</b> *Float3* | 변형된 세계 공간 위치. <b>오프셋 P</b> 및 <b>회전 P</b> 노드를 사용하여 추가 변형을 적용하려면 이 입력을 사용합니다.<br><i>기본값: 변환되지 않은 월드 공간 위치.</i> |
