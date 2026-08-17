---
title: P 회전
description: Designer > Substance 합성 그래프 > Substance 합성 그래프의 노드 참조 > 노드 라이브러리 > SDF 함수 > 변형 > 회전
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# P 회전

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![P 회전 아이콘](./3d-sdf-transform-rotate-p.png "P 회전")

<b>내부:</b> SDF 함수 > 변형

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

조정할 수 있는 각도로 축을 중심으로 세계 공간을 회전합니다.<br>변환된 월드 위치는 대부분의 SDF 함수의 <b>P</b> 입력에 연결하여 변환된 이 월드 공간에서 정의할 수 있습니다.<br><br>수행된 회전을 시각화하려면 <b>3D 뷰어</b>의 <b>변형 피벗</b> 도우미를 사용하세요.<br><br><i>팁:</i> P 변환은 연결할 수 있지만 결과는 작업 순서에 따라 달라집니다.

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
| <b>각도</b> *부동* | 세계 공간이 회전하는 각도입니다.<br><br>각도는 <b>3D 뷰어</b>의 <b>변형 피벗</b> 도우미에 있는 원으로 시각화됩니다. 회전 각도를 회전의 일부로 명확하게 보려면 <b>축</b> 화살표가 이 원의 중심으로 표시되도록 카메라를 정렬합니다. |
| <b>축</b> *Float3* | 월드 공간이 회전하는 축을 정의하는 정규화된 벡터입니다.<br>예: (0, 1, 0)은 피벗점의 Y축을 중심으로 세계 공간을 회전합니다.<br><br>축은 <b>3D 뷰어</b>의 <b>변형 피벗</b> 도우미에 있는 화살표로 시각화됩니다. 화살표의 색상은 이 벡터의 XYZ 구성 요소에 매핑됩니다.<br><br><i>기본값: (0, 1, 0)</i> |
| <b>피벗 위치</b> *Float3* | 회전의 원점을 정의하는 피벗의 세계 공간 위치입니다.<br><br>기준점은 <b>3D 뷰어</b>의 <b>피벗 변환</b> 도우미에 있는 화살표의 시작에 의해 시각화됩니다. |
| <b>P</b> *Float3* | 변형된 세계 공간 위치. <b>오프셋 P</b> 및 <b>회전 P</b> 노드를 사용하여 추가 변형을 적용하려면 이 입력을 사용합니다.<br><br><i>기본값: 변환되지 않은 월드 공간 위치.</i> |
