---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/caustics.html"
breadcrumb-title: ''
description: '[빛 무늬] 노드를 사용하여 수중 및 굴절 조명 효과를 만들기 위한 빛 무늬 패턴을 생성합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Caustics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 빛 무늬
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 5%

---


# 빛 무늬

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](caustics.resources/caustics-01.png){width="128px"}

<b>내부:</b> 텍스처 생성기 > 잡음

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

높이 맵 및 조명 방향을 기반으로 투영된 빛 무늬 효과를 생성합니다.회색 음영과 색상 버전 모두에서 나타나며, 차이는 미세하지만 색상 버전은 색상 분산 효과를 추가합니다. 조명은 단일 지점에서 캐스팅되며 환경 맵은 사용되지 않습니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>출력 색상 공간</b> <i>원시, sRGB</i> | 출력 색상 공간을 설정합니다. |
| <b>광자 격자 크기</b> <i>자동, 512, 1024, 2048, 4096</i> | 격자 크기를 조정하여 품질을 설정하지만 기본값은 일치하는 입력으로 설정됩니다. 계산 속도를 높이는 데 사용할 수 있습니다. |
| <b>표면 Height 비율</b> <i>0.0 - 1.0</i> | Height 해석 방법을 결정하는 승수입니다. |
| <b>표면 Height 위치</b> <i>0.0 - 1.0</i> | 굴절된 서피스에서 투영까지의 거리를 설정합니다. |
| <b>표면 IOR</b> <i>1.0 - 2.0</i> | 굴절률을 설정합니다. 색상 버전에서는 이 옵션이 더 많은 색상 분산을 추가합니다. |
| <b>광자 크기</b> <i>1.0 - 50.0</i> | 광자 크기는 효과의 선명도에 영향을 줍니다. |
| <b>분산</b> <i>0.0 - 0.01(색상 버전만)</i> | 색상 분산에만 영향을 줍니다. IOR가 낮으면 표시되지 않습니다. |
| <b>떨림</b> <i>0.0 - 1.0</i> | 캐스트 광자 입자에 불규칙한 지터링을 추가합니다. |
| <b>조명 위치</b> | 광원 위치를 이동합니다. 또한 2D 보기에서 기즈모를 통해 이루어졌습니다. |
| <b>배경색</b> <i>(색상 값)(색상 버전만)</i> | 배경색을 변경합니다. 회색 음영 버전에서 검은색으로 제한됩니다. |
| <b>비정사각형 확장</b> <i>거짓/참</i> | 제곱이 아닌 비율로 스쿼시와 스트레치를 보정합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="caustics.resources/caustics-02.png" />
        </td>
    </tr>
</table>
