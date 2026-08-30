---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-sampler.html"
breadcrumb-title: ''
description: Substance 3D Designer 타일 노드를 사용하여 입력 텍스처에서 타일을 샘플링하고 배열하여 Sampler에 타일 패턴을 만듭니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Sampler
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 타일 Sampler
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1060'
ht-degree: 6%

---


# 타일 Sampler

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tile-sampler.resources/tile-sampler.png){width="128px"}

<b>내부:</b> 텍스처 생성기 > 패턴

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

타일 Sampler은 타일 패턴의 궁극적인 생성 노드입니다. [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)의 발전된 복잡한 버전입니다. 2017 2.1년을 기준으로 하면 타일 Sampler과 [생성기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)의 차이가 훨씬 줄어듭니다. 주요 차이점은 크기 조절, 위치, 회전, 크기, 색상 및 마스크 생성에 사용할 수 있는 7개의 다른 맵 슬롯에서만 있습니다. 효과는 개별적으로 혼합할 수 있습니다.

타일 Sampler은 외부 입력 맵으로 제어되는 특정 매개 변수에 대한 추가 제어와 함께 인공 절차 패턴을 만드는 데 유용합니다.

타일 Sampler으로 넘어가기 전에 [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)에 익숙한지 확인하세요. 대부분의 경우 [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)이면 충분하며 타일 Sampler의 복잡성을 추가할 필요가 없습니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>패턴 입력 1-6</b> <i>회색 음영 입력/색상 입력</i> | &quot;Pattern&quot; 매개 변수를 &quot;Image Input&quot;으로 설정할 때 사용되는 사용자 지정 패턴 이미지입니다.<br><br>사용 가능한 입력 양은 <b>패턴 입력 번호</b> 매개 변수에 의해 결정됩니다. |
| <b>맵 입력 크기 조절</b> <i>회색 음영 입력</i> | 타일 비율을 제어하는 회색 음영 맵 |
| <b>변위 맵 입력</b> <i>회색 음영 입력</i> | 타일 변위를 구동하기 위한 회색 음영 맵 |
| <b>회전 맵 입력</b> <i>회색 음영 입력</i> | 타일 회전을 구동하는 회색 음영 맵 |
| <b>벡터 맵 입력</b> <i>색상 입력</i> | 균일하지 않은 비율을 구동하기 위한 색상 벡터 맵. |
| <b>색상 맵 입력</b> <i>회색 음영 입력/색상 입력</i> | 타일당 드라이브 색조에 매핑합니다. |
| <b>마스크 맵 입력</b> <i>회색 음영 입력</i> | 특정 타일을 숨기는 데 사용되는 마스크 슬롯입니다. |
| <b>패턴 분포 맵 입력</b> <i>회색 음영 입력</i> | 여러 사용자 정의 패턴 입력을 구동하는 데 사용되는 마스크 슬롯입니다. |
| <b>배경 입력</b> <i>회색 음영 입력/색상 입력</i> | 선택적 배경 이미지입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>X 양</b> <i>0 - 64</i> | 패턴의 X-반복의 양입니다. |
| <b>Y 양</b> <i>0 - 64</i> | 패턴의 Y-반복의 양입니다. |
| <b>비정사각형 확장</b> <i>거짓/참</i> | 제곱이 아닌 비율로 스쿼시와 스트레치를 보정할 수 있습니다. |
| <b>패턴</b> |  |
| <b>패턴</b> <i>패턴 입력, 정사각형, 디스크, 포물면, 벨, 가우스, 가시, 피라미드, 벽돌, 그라데이션, 파도, 하프 벨, 릿지 벨, 초승달, 캡슐, 원뿔</i> | 사용할 패턴 모양을 선택합니다. |
| <b>패턴 입력 번호</b> <i>1 - 6</i> | 임의로 선택할 수 있는 사용자 정의 패턴의 양입니다. |
| <b>패턴 입력 분포</b> <i>임의, 패턴 번호, 분포 맵</i> | 여러 패턴 입력을 선택하는 방법을 설정합니다. 무작위란 임의의 것이 선택된 것을 의미하고, 패턴 숫자는 그것들이 단지 반복되는 시퀀스 내에 배치됨을 의미한다. 분포 맵은 회색 음영 맵 입력을 사용하여 배치를 제어합니다. |
| <b>패턴 입력 필터링(엔진 > v4)</b> <i>쌍선형 + 밉맵, 쌍선형, 최근접</i> |  |
| <b>패턴별</b> <i>0.0 - 1.0</i> | 선택한 패턴의 모양을 변경할 수 있습니다. 효과는 선택한 패턴에 따라 달라집니다. |
| <b>패턴별 무작위</b> <i>0.0 - 1.0</i> | 임의화 효과는 선택한 패턴에 따라 달라집니다. |
| <b>회전</b> <i>0, 90, 180, 270</i> | 계단식 회전(90도). |
| <b>회전 무작위</b> <i>0.0 - 1.0</i> | 타일 단위로 임의 자유 회전. |
| <b>무작위 대칭</b> <i>0.0 - 1.0</i> | 아래 비헤이비어에 따라 임의로 뒤집거나 미러링할 타일 수를 설정합니다. |
| <b>대칭 무작위 모드</b> <i>가로 + 세로, 가로, 세로</i> | 대칭 미러링 동작을 결정합니다. |
| <b>크기</b> |  |
| <b>크기 모드</b> <i>표준, 비율 유지, 절대, 픽셀</i> | 패턴 크기의 일반 비헤이비어를 설정합니다.<br><br>표준 옵션을 사용하면 패턴 요소의 크기를 정의할 수 있습니다. X와 Y의 양에 영향을 받습니다.<br><br>비율 유지를 사용하면 X와 Y의 양에 따라 영향을 받는 크기를 설정할 수 있습니다. 그러나 둘 사이의 X와 Y 비율은 그대로 유지됩니다.<br><br>절대 크기를 사용하면 X 및 Y 크기의 영향을 받지 않는 절대 크기를 설정할 수 있습니다.<br><br>픽셀 을 사용하면 X 및 Y 양의 영향을 받지 않고 절대 크기를 픽셀 단위로 설정할 수 있습니다. 해상도를 변경하면 요소의 크기에 영향을 줍니다. |
| <b>크기(절대/픽셀)</b> <i>0.0 - 1.0</i> | 타일의 불규칙한 비율을 변경합니다. 정확한 동작은 [크기 모드]에 따라 다릅니다. |
| <b>무작위 크기</b> <i>0.0 - 1.0</i> | 타일당 비율을 임의화합니다. |
| <b>크기 조절</b> <i>0.0 - 10.0</i> | 전체 타일 비율을 설정합니다. |
| <b>무작위 크기 조정</b> <i>0.0 - 1.0</i> | 타일당 비율을 임의화합니다. |
| <b>맵 배율 조정</b> <i>0.0 - 1.0</i> | 비율 맵의 효과에 있는 혼합. |
| <b>벡터 맵 배율 조정</b> <i>0.0 - 1.0</i> | 비율 벡터 맵의 효과에 있는 혼합을 사용하여 균일하지 않은 비율을 조정합니다. |
| <b>매개 변수화 영향 크기 조정</b> <i>X 및 Y, X, Y</i> | 크기 조절 매개 변수화가 영향을 미치는 축을 설정합니다. 비율 맵을 사용하여 요소의 X 또는 Y에만 영향을 줄 수 있습니다. |
| <b>위치</b> |  |
| <b>위치 무작위</b> <i>0.0 - 10.0</i> | 두 축 위의 타일 위치를 임의화합니다. |
| <b>오프셋</b> <i>0.0 - 1.0</i> | 오프셋 유형에 따라 타일을 이동합니다. |
| <b>오프셋 유형</b> <i>가로 퀸큐스, 세로 퀸큐스, 가로 글로벌, 세로 글로벌</i> | 오프셋이 작동하는 방향을 변경합니다. |
| <b>전역 오프셋</b> <i>0.0 - 1.0</i> | X축 또는 Y축의 모든 타일을 전체적으로 오프셋합니다. |
| <b>변위 맵 강도</b> <i>0.0 - 1.0</i> | [오프셋]에서 변위 맵 강도의 혼합. |
| <b>변위 각도</b> <i>0.0 - 1.0</i> | 변위할 각도를 설정합니다. |
| <b>벡터 맵 변위</b> <i>0.0 - 1.0</i> | 벡터 맵을 사용하여 변위 및 각도를 조정합니다. |
| <b>회전</b> |  |
| <b>회전</b> <i>0.0 - 1.0</i> | 모든 타일을 전역적으로 회전합니다. |
| <b>회전 무작위</b> <i>0.0 - 1.0</i> | 타일당 임의로 회전합니다. |
| <b>회전 맵 승수</b> <i>0.0 - 1.0</i> | 타일 단위 회전에 대한 회전 맵 효과의 혼합. |
| <b>벡터 맵 멀티플라이어</b> <i>0.0 - 1.0</i> | 벡터 맵을 사용하여 타일별 회전을 처리합니다. |
| <b>색상</b> |  |
| <b>마스크 맵 임계값</b> <i>0.0 - 1.0</i> | 타일 숨기기를 시작할 때의 마스크 맵 임계값입니다. |
| <b>마스크 맵 반전</b> <i>거짓/참</i> | 마스크 맵 효과를 반전시킵니다. |
| <b>마스크 맵 샘플링 기법</b> <i>패턴 중심, 패턴 테두리 상자(느림)</i> | 숨기는 포인트는 단일 포인트로 결정할지 아니면 테두리 상자로 결정해야 합니다. 흩어진 픽셀로 인해 이상한 효과가 발생하는 것을 방지합니다. |
| <b>무작위 마스크</b> <i>0.0 - 1.0</i> | 무작위 마스크는 마스크 맵과 병렬로 작동합니다. |
| <b>마스크 반전</b> <i>거짓/참</i> | 무작위 마스킹을 반전합니다. |
| <b>혼합 모드</b> <i>추가/하위, 최대(타일 Sampler)/추가/하위, Alpha 혼합(타일 Sampler 색상)</i> | 타일을 배경과 서로 연결하는 혼합 모드. |
| <b>색상</b> <i>(회색 음영 값) / (색상 값)</i> | 단색 전체 타일 색입니다. |
| <b>색상/광도 무작위</b> <i>0.0 - 1.0</i> | 타일당 색상 임의화. |
| <b>색상 매개 변수화 모드</b> <i>색상 입력, 비율, 선 색인, 행 색인, 패턴 색인(타일 Sampler)/색상 맵, 비율, 선 색인, 행 색인, 패턴 색인, 패턴 중심 위치, 패턴 중심 위치(RG) Bsphere 크기(B)(타일 Sampler 색상)</i> | 색상 임의화의 매개 변수 지정 방법을 설정합니다. |
| <b>색상 매개 변수화 승수</b> <i>0.0 - 1.0</i> | 위 매개 변수화 효과의 혼합. |
| <b>색상 매개 변수화 영향(색상만 해당)</b> <i>RGB+Alpha, RGB 전용, Alpha 전용</i> | 매개 변수화가 색상에 미치는 영향을 설정합니다. |
| <b>전체 불투명도(회색 음영만)</b> <i>0.0 - 1.0</i> | 전체 타일 불투명도를 설정합니다. |
| <b>배경색</b> <i>(회색 음영 값) / (색상 값)</i> | 단색 배경색을 설정합니다. |
| <b>역렌더링 순서</b> <i>거짓/참</i> | 렌더링 순서를 반대로 하여 맨 뒤로 이동합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="tile-sampler.resources/tilesampler-ex2.png" /><br><i>예는 입력 맵(패턴 분포, 크기 조절, 회전)에 의해 매개 변수가 제어되는 방법을 보여 줍니다.</i>
        </td>
    </tr>
</table>
