---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random.html"
breadcrumb-title: ''
description: 유기적인 텍스처 효과를 위해 프로시저 변형을 사용하여 무작위 타일 패턴을 만들 때 [타일 무작위] 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 타일 무작위
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 7%

---


# 타일 무작위

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tile-random.resources/tile-random-01.png){width="128px"}

<b>내부:</b> 생성기 > 패턴

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

[무작위 타일]은 타일 모양에 [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)보다 좀 더 많은 혼란이 있는 절차적 타일 패턴을 생성합니다. 이것은 어떤 타일을 더 작은 타일로 무작위로 쪼개서 이것을 한다. 많은 개념이 유사하기 때문에 타일 무작위와 씨름하기 전에 먼저 Tile Generator에서 방법을 찾는 것이 좋습니다.

목표가 구체적이고 덜 조직화된 패턴인 경우 [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) 대신 타일 임의성이 사용됩니다. 하지만 제한 사항이 있으므로 다른 고급 요구 사항을 위해 [Sampler 바둑판식 배열](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)을 사용해 보세요.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>패턴 입력</b> <i>회색 음영 입력(색상 입력)</i> | &quot;Pattern&quot; 매개 변수를 &quot;Image Input&quot;으로 설정한 경우 사용되는 사용자 정의 패턴 이미지입니다. |
| <b>배경 입력</b> <i>회색 음영 입력(색상 입력)</i> |  |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>X 양</b> <i>1 - 64</i> | 패턴의 X-반복의 양입니다. |
| <b>Y 양</b> <i>1 - 64</i> | 패턴의 Y-반복의 양입니다. |
| <b>비정사각형 확장</b> <i>거짓/참</i> | 사각형이 아닌 비율로 squash 및 squash를 보정할 수 있습니다. |
| <b>패턴</b> |  |
| <b>패턴</b> <i>패턴 입력, 정사각형, 디스크, 포물면, 벨, 가우스, 가시, 피라미드, 벽돌, 그라데이션, 파도, 하프 벨, 고정된 벨, 초승달, 캡슐, 원뿔</i> | 사용할 패턴 모양을 선택합니다. |
| <b>이미지 입력 필터링(엔진 > v4)</b> <i>쌍선형 + 밉맵, 쌍선형, 최근접</i> |  |
| <b>패턴별</b> <i>0.0 - 1.0</i> | 선택한 패턴의 모양을 변경할 수 있습니다. 효과는 선택한 패턴에 따라 달라집니다. |
| <b>패턴별 무작위</b> <i>0.0 - 1.0</i> | 임의화 효과는 선택한 패턴에 따라 달라집니다. |
| <b>회전</b> <i>0, 90, 180, 270, 임의의 가로, 임의의 세로</i> | 임의화를 선택적으로 사용하여 90도 단계의 회전을 설정합니다. |
| <b>회전 무작위</b> <i>0.0 - 1.0</i> | 임의의 자유 회전을 추가합니다. |
| <b>무작위 대칭</b> <i>0.0 - 1.0</i> | 선택한 대칭 무작위 모드 로 특정 패턴을 무작위로 미러링합니다. 이 값이 높을수록 더 많은 패턴이 미러링됩니다. |
| <b>대칭 무작위 모드</b> <i>가로 + 세로, 가로, 세로</i> | 대칭 난수가 0보다 큰 경우 미러링 동작을 결정합니다. |
| <b>분할</b> |  |
| <b>모드</b> <i>없음, 자동, 자동 수평, 자동 수직, 임의 h+v</i> | 타일을 분할하는 방법에 대한 규칙을 설정합니다. |
| <b>임계값</b> <i>0.0 - 1.0</i> | 타일 분할 시점에 대한 크기 임계값 |
| <b>승수</b> <i>0 - 10</i> | 분할 승수입니다. 이 값이 높을수록 분할이 많습니다. |
| <b>크기</b> |  |
| <b>무작위 X</b> <i>0.0 - 1.0</i> | X축 위의 균일하지 않은 비율을 임의화합니다. |
| <b>임의 Y</b> <i>0.0 - 1.0</i> | Y축에 대해 균일하지 않은 비율을 임의화합니다. |
| <b>중간</b> |  |
| <b>모드</b> <i>가장 작은 벽돌 기준, 가장 큰 벽돌 기준</i> | 크기를 기준으로 하는 벽돌 크기를 설정합니다. |
| <b>금액</b> <i>0.0 - 1.0</i> | 벽돌 사이의 간격을 설정합니다. |
| <b>모양</b> |  |
| <b>크기 조절</b> <i>0.0 - 1.0</i> | 모든 타일의 크기를 전체적으로 조절합니다. |
| <b>무작위 크기 조정</b> <i>0.0 - 1.0</i> | 타일 단위로 무작위 크기 조절을 수행합니다. |
| <b>회전</b> <i>0.0 - 1.0</i> | 모든 타일에 대한 전역 회전입니다. |
| <b>회전 무작위</b> <i>0.0 - 1.0</i> | 타일을 기준으로 임의로 회전합니다. |
| <b>회전 제약 조건</b> <i>거짓/참</i> | 회전된 타일이 겹치지 않도록 크기를 제한합니다. |
| <b>위치</b> |  |
| <b>오프셋</b> <i>0.0 - 1.0</i> | X축 위에서만 슬라이드를 포함하여 타일을 전체적으로 이동하거나 변환합니다 |
| <b>임의 오프셋</b> <i>0.0 - 1.0</i> | 타일당 오프셋(X축 위의 슬라이드만 임의화) |
| <b>무작위</b> <i>0.0 - 1.0</i> | 위치를 임의화하고 타일을 X축과 Y축 모두에서 이동합니다. |
| <b>임의 제약 조건</b> <i>거짓/참</i> | 타일이 닿도록 크기를 제한하지만 겹치지 않습니다. [무작위 위치] 효과의 톤을 크게 낮춥니다. |
| <b>색상</b> |  |
| <b>색상</b> <i>(회색 음영 값) / (색상 값)</i> | 모든 타일에 단색을 설정합니다. |
| <b>색상 무작위</b> <i>0.0 - 1.0</i> | 타일을 기준으로 색상을 임의화합니다. |
| <b>색상 매개 변수화</b> <i>없음, 영역, 크기 x, 크기 y</i> | 이러한 설정 중 하나에 따라 색상 변형이 달라집니다. |
| <b>색상 매개 변수화 강도</b> <i>0.0 - 1.0</i> | 위의 매개 변수화 효과에 대한 승수입니다. |
| <b>색상 매개 변수화 효과(색상에만 해당)</b> <i>RGB+Alpha, RGB 전용, Alpha 전용</i> | 색상 전용 매개 변수화 효과를 결정합니다. |
| <b>배경색</b> <i>(회색 음영 값) / (색상 값)</i> | 단색 배경색을 설정합니다. |
| <b>혼합 모드</b> <i>추가/하위, 최대/추가/하위, Alpha 혼합(색상)</i> | 타일을 배경에 혼합하는 모드를 설정합니다. |
| <b>마스크</b> |  |
| <b>무작위</b> <i>0.0 - 1.0</i> | 타일에 마스크를 임의로 시작합니다. 이 값이 높을수록 타일이 더 많이 사라집니다. |
| <b>반전</b> <i>거짓/참</i> | 마스크 결과를 반전합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="tile-random.resources/tile-random-02.png" />
        </td>
    </tr>
</table>
