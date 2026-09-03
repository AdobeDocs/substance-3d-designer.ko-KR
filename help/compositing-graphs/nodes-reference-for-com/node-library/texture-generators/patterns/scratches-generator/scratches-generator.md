---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/scratches-generator.html"
breadcrumb-title: ''
description: Scratches 생성기 노드를 사용하여 재료의 마모와 손상을 추가하기 위한 절차적 스크래치 패턴을 만듭니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Scratches Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Scratches 생성기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 8%

---


# Scratches 생성기

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](scratches-generator.resources/scratches-generator-01.png)

<b>내부:</b> 텍스처 생성기 > 패턴

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이렇게 하면 방향, 스프레드 및 왜곡 등을 설정할 수 있는 등 다양한 사용자 지정 옵션이 있는 임의의 스크래치가 배치됩니다.

이 스크래치 깊이를 기반으로 하여 Normalmap을 생성하는 특수 버전의 Scratches 생성기 인 Scratches 생성기 표준이 있습니다. 대부분의 옵션은 정확히 동일하지만 [표준] 설정에 명확하게 표시된 몇 가지 추가 매개 변수가 있습니다(아래 참조).

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>스플라인 번호</b> <i>1 - 512</i> | 배치할 스크래치(스플라인) 양입니다. |
| <b>스플라인당 최대 선분</b> <i>2 - 256</i> | 스크래치 길이에 대한 세그먼트/하위 분할의 양입니다. 그러면 곡선과 왜곡이 더 매끄러워집니다. 이 효과는 왜곡 값이 높을수록 더 두드러집니다. |
| <b>스플라인 회전</b> <i>0.0 - 1.0</i> | 방향을 정하기 위해 모든 스플라인의 회전을 균일하게 합니다. |
| <b>스플라인 회전 무작위</b> <i>0.0 - 1.0</i> | 각도 변화, 모든 스플라인을 임의로 회전합니다. |
| <b>스플라인 배율</b> <i>0.0 - 1.0</i> | 모든 스플라인의 비율을 균일하게 조정합니다. |
| <b>스플라인 배율 무작위</b> <i>0.0 - 1.0</i> | 각 스플라인의 크기를 개별적으로 임의로 조절합니다. |
| <b>스플라인 왜곡</b> <i>0.0 - 1.0</i> | 모든 스플라인의 왜곡 레벨을 균일하게 합니다. |
| <b>스플라인 왜곡 무작위</b> <i>0.0 - 1.0</i> | 각 스플라인의 왜곡 레벨을 개별적으로 임의화합니다. |
| <b>스플라인 왜곡 빈도</b> <i>0.0 - 1.0</i> | 왜곡 빈도를 설정하고 왜곡 세부 묘사 비율을 제어합니다. |
| <b>스플라인 폭</b> <i>0.0 - 2.0</i> | 모든 스플라인의 폭을 균일하게 설정합니다. |
| <b>스플라인 폭 무작위</b> <i>0.0 - 1.0</i> | 각 스플라인의 스플라인 폭을 개별적으로 임의화합니다. |
| <b>스플라인 위치 무작위</b> <i>0.0 - 1.0</i> | 각 스플라인의 위치를 개별적으로 임의화합니다. 이 값이 낮을수록 스플라인이 캔버스의 중앙에 더 많이 모입니다. 스크래치 스팟을 만드는 데 사용할 수 있습니다. |
| <b>px에서 스플라인 폭 설정</b> <i>거짓/참</i> | 스플라인 폭 설정에 사용할 단위를 결정합니다. |
| <b>광도 무작위(회색 음영 버전만)</b> <i>0.0 - 1.0</i> | 각 스플라인의 광도를 개별적으로 임의화합니다. |
| <b>표준 강도(표준 버전만)</b> <i>0.0 - 1.0</i> | 모든 스플라인의 표준 효과 강도를 전역적으로 설정합니다. |
| <b>표준 강도 무작위(표준 버전만)</b> <i>0.0 - 1.0</i> | 각 스플라인의 표준 강도를 개별적으로 임의화합니다. |
| <b>일반 형식(일반 버전만)</b> <i>DirectX, OpenGL</i> | 서로 다른 표준 맵 포맷 사이를 전환합니다(녹색 채널을 반전합니다). |
| <b>페이드 모드</b> <i>없음, 시작, 종료, 시작 + 종료</i> | 스플라인의 페이드 여부와 페이드 방향을 설정합니다. |
| <b>페이드 길이</b> <i>0.0 - 1.0</i> | 위에 활성화된 경우 페이드 효과의 길이를 설정합니다. |
| <b>비정사각형 확장</b> <i>거짓/참</i> | 제곱이 아닌 비율로 스쿼시와 스트레치를 보정할 수 있습니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="scratches-generator.resources/scratches-generator-02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="scratches-generator.resources/scratches-generator-03.png" />
        </td>
    </tr>
</table>
