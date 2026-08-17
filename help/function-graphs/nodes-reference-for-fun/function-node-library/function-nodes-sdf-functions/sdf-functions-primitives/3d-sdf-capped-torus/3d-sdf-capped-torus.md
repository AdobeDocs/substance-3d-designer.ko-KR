---
title: 뚜껑이있는원환체
description: Designer > Substance 합성 그래프 > Substance 합성 그래프의 노드 참조 > 노드 라이브러리 > SDF 함수 > 프리미티브 > 닫힌 원환
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# 뚜껑이있는원환체

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![닫힌 원환체 아이콘](./3d-sdf-capped-torus.png "닫힌 원환체")

<b>내부:</b> SDF 함수 > 기본

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

주 원을 따라 보조 원의 스윕을 비스듬히 제한할 수 있는 닫힌 원환에 대한 SDF 함수.<br>두 원 모두 반경을 조정할 수 있습니다.

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
| <b>주 반경</b> *부동* | 보조 원이 휘저어 원환체의 표면을 형성하는 주 원의 반지름입니다.<br><br><i>기본값: 0.5</i> |
| <b>보조 반경</b> *부동* | 주 원을 따라 스윕되어 원환체의 표면을 형성하는 보조 원의 반지름입니다.<br><br><i>기본값: 0.2</i> |
| <b>각도</b> *부동* | 중심 각도는 보조 원이 스윕되지 않는 주 원의 트리밍 호를 차례로 정의합니다.<br><br><i>기본값: 0.75</i> |
| <b>각도 오프셋</b> *부동* | 주 반경을 따라 마이너 원이 스윕되지 않는 트리밍 호의 오프셋입니다.<br><br><i>기본값: 0</i> |
| <b>대칭</b> *부울* | 트리밍 호를 한 방향으로 그려야 할지 두 방향으로 그려야 할지를 제어합니다.<br><br><i>기본값: True</i> |
| <b>가운데 위치</b> *Float3* | 닫힌 원환의 피벗의 세계 공간 위치입니다.<br><br><i>기본값: (0, 0, 0.5)</i> |
| <b>P</b> *Float3* | 변형된 세계 공간 위치. <b>오프셋 P</b> 및 <b>회전 P</b> 노드를 사용하여 추가 변형을 적용하려면 이 입력을 사용합니다.<br><br><i>기본값: 변환되지 않은 월드 공간 위치.</i> |
