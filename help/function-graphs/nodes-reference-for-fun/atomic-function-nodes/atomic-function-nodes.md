---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes.html"
breadcrumb-title: ''
description: 사용자 정의 함수 구축을 위한 Substance 함수 그래프에서 가장 작은 노드 단위인 원자 함수 노드에 대해 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Atomic function nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 원자 함수 노드
user-guide-description: ''
user-guide-title: ''
source-git-commit: 953b99bc5f48c431e7ace47a23b0b451cceaa0db
workflow-type: tm+mt
source-wordcount: '1108'
ht-degree: 16%

---


# 원자 함수 노드

Substance 그래프의 [원자 노드](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)과 마찬가지로, Substance 함수 그래프의 원자 노드는 해당 그래프 유형의 가장 작은 노드 단위입니다.

이 범주는 목적에 따라 여러 범주로 분류할 수 있습니다.

| 카테고리 | 노드 | 입력 유형 | 출력 유형 | 설명 |
|:---------------------------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------|:------------------|:---------------------------------------------------------------------------------------------------|
| [상수](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) | 부동 | - | 부동 | 상수 부동 값(예: 0.1)을 정의합니다. |
|                                                                                                                                        | 실수2 | - | 실수2 | 2개의 부동 값으로 상수 벡터를 정의합니다(예: (0.1, 0.2). |
|                                                                                                                                        | 실수3 | - | 실수3 | 부동 값이 3인 상수 벡터(예: 0.1, 0.2, 0.3)를 정의합니다. |
|                                                                                                                                        | 실수4 | - | 실수4 | 4개의 부동 값으로 상수 벡터를 정의합니다(예: 0.1, 0.2, 0.3, 0.4). |
|                                                                                                                                        | 정수 | - | 정수 | 상수 정수 값(예: 1)을 정의합니다. |
|                                                                                                                                        | 정수2 | - | 정수2 | 2개의 정수 값(예: (1, 2)의 상수 벡터를 정의합니다. |
|                                                                                                                                        | 정수3 | - | 정수3 | 3개의 정수 값(예: (1, 2, 3)의 상수 벡터를 정의합니다. |
|                                                                                                                                        | 정수4 | - | 정수4 | 4개의 정수 값(예: (1, 2, 3, 4)의 상수 벡터를 정의합니다. |
|                                                                                                                                        | 부울 | - | 부울 | 상수 부울 값(예: True 또는 False)을 정의합니다. |
|                                                                                                                                        | 문자열 | - | 문자열 | 상수 문자열 값을 정의합니다(예: &quot;Substance&quot;). |
| [벡터](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md) | 벡터 부동 소수점2 | Float1 | 부동 2 | 2개의 좌표가 있는 벡터에 2개의 부동 값을 캐스팅합니다. |
|                                                                                                                                        | 벡터 Float3 | Float1 / Float2 | 부동 3 | 3개 좌표의 벡터에 2개의 부동 값을 캐스팅합니다. |
|                                                                                                                                        | 벡터 부동 소수점4 | Float1 / 2 / 3 | 플로트 | 4개 좌표의 벡터에 2개의 부동 값을 캐스팅합니다. |
|                                                                                                                                        | 스위즐 부동 소수점1 | 벡터 부동 | Float1 | 벡터에서 부동 좌표 추출 |
|                                                                                                                                        | 스위즐 부동 소수점2 | 벡터 부동 | 실수2 | 벡터에서 2개의 부동 좌표를 추출합니다. |
|                                                                                                                                        | 스위즐 부동 소수점3 | 벡터 부동 | 실수3 | 벡터에서 3개의 부동 좌표를 추출합니다. |
|                                                                                                                                        | 스위즐 부동 소수점4 | 벡터 부동 | 실수4 | 벡터에서 4개의 부동 좌표를 추출합니다. |
|                                                                                                                                        | 벡터 정수2 | 정수2 | 벡터 정수2 | 좌표가 2인 벡터에 2개의 정수 값을 캐스팅합니다. |
|                                                                                                                                        | 벡터 정수3 | 정수3 | 정수3 | 좌표가 3인 벡터에 2개의 정수 값을 캐스팅합니다. |
|                                                                                                                                        | 벡터 정수4 | 정수4 | 정수4 | 4개 좌표의 벡터에 2개의 정수 값을 캐스팅합니다. |
|                                                                                                                                        | 스위즐 정수1 | 벡터 정수 | Integer1 | 벡터에서 정수 좌표 추출 |
|                                                                                                                                        | 스위즐 정수2 | 벡터 정수 | 정수2 | 벡터에서 2개의 정수 좌표를 추출합니다. |
|                                                                                                                                        | 스위즐 정수3 | 벡터 정수 | 정수3 | 벡터에서 3개의 정수 좌표를 추출합니다. |
|                                                                                                                                        | 스위즐 정수4 | 벡터 정수 | 정수4 | 벡터에서 4개의 정수 좌표를 추출합니다. |
| [변수](../../../function-graphs/variables/variables.md) | 설정 | any | 입력 유형 | 변수 설정 |
|                                                                                                                                        | Integer1 가져오기 | - | Integer1 | 함수 또는 그래프 정수 값 입력 가져오기 |
|                                                                                                                                        | 정수2 얻기 | - | 정수2 | 함수 또는 그래프 Integer2 값 입력 가져오기 |
|                                                                                                                                        | 정수3 얻기 | - | 정수3 | 함수 또는 그래프 Integer3 값 입력 가져오기 |
|                                                                                                                                        | 정수4 얻기 | - | 정수4 | 함수 또는 그래프 Integer4 값 입력 가져오기 |
|                                                                                                                                        | Float1 가져오기 | - | Float1 | 함수 또는 그래프의 부동 값 입력 가져오기 |
|                                                                                                                                        | 부동 소수점2 얻기 | - | 실수2 | 함수 또는 그래프 Float2 값 입력 가져오기 |
|                                                                                                                                        | 부동 소수점3 얻기 | - | 실수3 | 함수 또는 그래프 Float3 값 입력 가져오기 |
|                                                                                                                                        | 부동 소수점4 얻기 | - | 실수4 | 함수 또는 그래프 Float4 값 입력 가져오기 |
|                                                                                                                                        | 부울 얻기 | - | 부울 | 함수 또는 그래프 부울 값 입력 가져오기 |
| 샘플러 | 샘플 회색 | 벡터 부동 소수점2 | 실수4 | 지정된 UV 좌표(float2)에서 입력 이미지의 회색 음영 값을 반환합니다 |
|                                                                                                                                        | 샘플 색상 | 벡터 부동 소수점2 | 실수4 | 지정된 UV 좌표(float2)에서 입력 이미지의 색상 값을 반환합니다 |
| 캐스팅 | 부동 소수점으로 | Integer1 | Float1 | Float에서 정수를 변환합니다. |
|                                                                                                                                        | 부동 소수점2로 | 정수2 | 실수2 | Float2에서 Integer2를 변환합니다. |
|                                                                                                                                        | 부동 소수점3으로 | 정수3 | 실수3 | Float3에서 Integer3를 변환합니다. |
|                                                                                                                                        | 부동 소수점4로 | 정수4 | 실수4 | Float4에서 Integer4를 변환합니다 |
|                                                                                                                                        | 정수로 | Float1 | Integer1 | Float를 정수로 변환합니다. |
|                                                                                                                                        | 정수2로 | 실수2 | 정수2 | Float2를 Integer2로 변환합니다. |
|                                                                                                                                        | 정수3으로 | 실수3 | 정수3 | Float3를 Integer3로 변환합니다. |
|                                                                                                                                        | 정수4로 | 실수4 | 정수4 | Integer4에서 Float4를 변환합니다. |
| [연산자](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/operator-nodes/operator-nodes.md) | 추가 | 벡터 부동 / 정수 | a &amp; b 유형 | 동일한 유형의 두 값(a + b)을 추가합니다. |
|                                                                                                                                        | 뺄셈 | 벡터 부동 / 정수 | a &amp; b 유형 | 동일한 유형의 두 값(a - b)을 뺍니다 |
|                                                                                                                                        | 곱셈 | 벡터 부동 / 정수 | a &amp; b 유형 | 동일한 유형의 두 값(a \* b)을 곱합니다. |
|                                                                                                                                        | 스칼라 곱셈 | 벡터 부동 | 문자 유형 | 값에 부동 값을 곱합니다. \* 스칼라 |
|                                                                                                                                        | 나눗셈 | Float1 / Integer1 | a &amp; b 유형 | 동일한 유형의 두 값 a/b를 나눕니다. |
|                                                                                                                                        | 부정 | Float1 / Integer1 | 문자 유형 | 부정 값을 반환합니다. -a |
|                                                                                                                                        | 모듈로 | Float1 / Integer1 | 문자 유형 | modulo 값을 구합니다. mod(a, diger) |
|                                                                                                                                        | 도트 곱 | 벡터 부동 | a &amp; b 유형 | dot(a, b)와 같이 동일한 유형의 2개 값의 내적을 반환합니다. |
| [논리](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) | And | 부울 | 부울 | 2개의 부울 항목이 true이면 true를 반환합니다. 항목이 false이면 false를 반환합니다. |
|                                                                                                                                        | Or | 부울 | 부울 | 부울 항목 중 1개가 true이면 true를 반환합니다. 둘 다 false이면 false를 반환합니다. |
|                                                                                                                                        | 아님 | 부울 | 부울 | 항목의 부정 부울을 반환합니다. !a |
| [비교](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/comparison-nodes/comparison-nodes.md) | Equal | Float1 / Integer1 | 부울 | a = b인 경우 true를 반환합니다. |
|                                                                                                                                        | 같지 않음 | Float1 / Integer1 | 부울 | != b인 경우 true를 반환합니다. |
|                                                                                                                                        | 보다 큼 | Float1 / Integer1 | 부울 | a > b인 경우 true를 반환합니다. |
|                                                                                                                                        | 크거나 같음 | Float1 / Integer1 | 부울 | a >= b이면 true를 반환합니다. |
|                                                                                                                                        | 보다 작음 | Float1 / Integer1 | 부울 | &lt; b인 경우 true를 반환합니다. |
|                                                                                                                                        | 작거나 같음 | Float1 / Integer1 | 부울 | a &lt;= b이면 true를 반환합니다. |
| 함수 | 절대치 | Float1 / Integer1 | Float1 | a의 절대값을 구합니다. abs(a) |
|                                                                                                                                        | 내림 | Float1 / Integer1 | Float1 | -floor(a)보다 작거나 같은 가장 큰 값을 반환합니다. |
|                                                                                                                                        | 상한 | Float1 / Integer1 | Float1 | 다음보다 크거나 같은 가장 작은 값을 구합니다. ceil(a) |
|                                                                                                                                        | 코사인 | Float1 / Integer1 | Float1 | a의 코사인 값을 구합니다. cos(a) |
|                                                                                                                                        | 사인 | Float1 / Integer1 | Float1 | a의 사인 값을 반환합니다. sin(a) |
|                                                                                                                                        | 탄젠트 | Float1 / Integer1 | Float1 | tan(a)의 탄젠트 값을 반환합니다. |
|                                                                                                                                        | 아크 접선 2 | 벡터 부동 소수점2 | Float1 | vector2 항목의 arc tan 2 값을 반환합니다. arctan2(xa, ya) |
|                                                                                                                                        | 데카르트식 | Float1 | 실수2 | 2극좌표를 카트 좌표(rho, theta)로 변환합니다. |
|                                                                                                                                        | 제곱근 | Float1 / Integer1 | Float1 | 의 제곱근 값을 반환합니다. |
|                                                                                                                                        | 로그 값 | Float1 / Integer1 | Float1 | 로그 값 a: log(a)를 반환합니다. |
|                                                                                                                                        | 지수 | Float1 / Integer1 | Float1 | 지수 값 a를 구합니다. exp(a) |
|                                                                                                                                        | 펑 2 | Float1 / Integer1 | Float1 | a의 2제곱값을 구합니다. |
|                                                                                                                                        | 선형 보간 | Float1 / Integer1 | Float1 | 부동 값에 따라 두 값 사이의 선형 보간을 반환합니다. (1-x)a + x \* b |
|                                                                                                                                        | 최소 | Float1 / Integer1 | a &amp; b 유형 | a와 b 사이의 최소값을 반환합니다. |
|                                                                                                                                        | 최대 | Float1 / Integer1 | a &amp; b 유형 | a에서 b 사이의 최대값을 반환합니다. |
| 임의 |                       | Float1 | Float1 | 0에서 a 사이의 부동 값을 생성합니다. |
| [제어](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/control-nodes/control-nodes.md) | 시퀀스 | any | 입력 유형 | 두 값 중에서 먼저 계산할 값을 선택할 수 있습니다. |
|                                                                                                                                        | If...Else | 부울 / a &amp; b | a &amp; b 유형 | If의 조건이 true이면 true를 반환합니다. false이면 false를 반환합니다. |
