---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-scatter.html"
breadcrumb-title: ''
description: Atlas Scatter 노드를 사용하여 스캔한 자료에서 타일 패턴을 만들기 위해 아틀라스에 걸쳐 텍스처를 산란 합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Scatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas Scatter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 7%

---


# Atlas Scatter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](atlas-scatter.resources/atlas-scatter-01.png){width="200px"}

<b>내부:</b> 재질 필터 > 스캔 처리

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

Atlas에서 요소를 추출하고 배경에서 산란을 만듭니다. 아틀라스 입력은 완전한 재질을 가지며, 단일 텍스처 시트에 배열되고 패키징된 개별 요소로 구성된다. 이 산란은 [모양 튄](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md)과(와) 유사하게 내부 [Atlas Splitter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/atlas-splitter/atlas-splitter.md) 프로세스를 사용하여 노드를 분할하고 노드를 분할합니다. Atlas Scatter이 작동하려면 최소한 불투명도 맵 입력 과 Atlas에 대한 Height 맵 입력 이 필요합니다.

</td>
</tr>
</table>

>[!NOTE]
>
> Atlas Scatter 노드에서 사용할 수 있는 수백 개의 [아틀라스](https://source.substance3d.com/allassets?assetType=substanceAtlas)를 [Substance Source](https://source.substance3d.com/)에서 사용할 수 있습니다.

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>아틀라스 입력 해상도</b> <i>해상도, 1~12</i> | 성능 대 품질 비율이 양호하도록 전체 입력 아틀라스의 해상도를 수동으로 설정합니다. |
| <b>X 양</b> <i>1 - 64</i> | 패턴의 X 반복 정도. |
| <b>Y 양</b> <i>1 - 64</i> | 패턴의 Y 반복의 양입니다. |
| <b>패턴</b> |  |
| <b>패턴 범위</b> <i>0 - 10</i> | 흩어질 패턴의 범위를 정의합니다. 0으로 설정하면 모든 패턴이 사용됩니다. |
| <b>패턴 분포 모드</b> <i>임의, 패턴 색인, 선 색인, 열 색인</i> | Atlas 요소가 사용되는 순서를 정의합니다. |
| <b>패턴 분포 맵 승수</b> <i>0.0 - 1.0</i> | 입력 이미지 회색 음영 값에 맞는 모양 패턴을 선택합니다. |
| <b>패턴 회전</b> <i>0, 90, 180, 270</i> | 선택한 각도만큼 각 아틀라스 요소에 고정 회전을 적용합니다. |
| <b>패턴 회전 무작위</b> <i>0.0 - 1.0</i> | 아틀라스 요소의 설정된 부분에 임의의 회전을 적용합니다. |
| <b>아틀라스 모양 감지 정밀도</b> <i>단순하거나 작은 모양, 복잡하거나 큰 모양, 실패 모드 없음</i> | 모양을 감지할 정밀도를 설정합니다. 정확도가 높을수록 성능에 미치는 영향이 커집니다. |
| <b>아틀라스 불투명도 축소(더 빠른 감지)</b> <i>-4 - 0</i> | 모양 감지에 사용되는 입력 아틀라스 불투명도 맵의 다운스케일 비율을 제어할 수 있습니다. 해상도가 낮을수록 성능이 향상되고 정확도가 떨어집니다. |
| <b>다음보다 작은 모양 무시</b> <i>0.0 - 1.0</i> | 모양을 감지해야 하는 최소 크기를 전체 이미지의 비율로 표시합니다. |
| <b>크기</b> |  |
| <b>크기 조절</b> <i>0.0 - 5.0</i> | 흩어진 모양의 상대적 비율을 설정합니다. |
| <b>무작위 크기 조정</b> <i>0.0 - 1.0</i> | 각 분산 모양에 무작위 크기 조절을 적용하기 위한 승수를 정의합니다. |
| <b>겹치지 않게 크기 조정</b> <i>0.0 - 1.0</i> | 겹치지 않도록 모양 비율을 줄입니다. |
| <b>맵 배율 조정</b> <i>0.0 - 1.0</i> | 입력 이미지 회색 음영 값의 함수에서 모양 비율을 곱합니다. |
| <b>크기</b> <i>0.0 - 1.0</i> | 길이(X) 및 폭(Y)을 기준으로 흩어진 모양의 상대 비율을 설정합니다. |
| <b>배경색 경사의 크기 비율</b> <i>0.0 - 1.0</i> | 배경 Height 경사 기능의 모양 크기 비율을 수정합니다. |
| <b>종횡비 유지</b> <i>0.0 - 1.0</i> | 격자 셀 비율(예: X 양 및 Y 양 값의 비율)을 사용하는 대신 흩어져 있는 모양의 원래 비율을 유지해야 하는 양을 결정합니다. |
| <b>위치</b> |  |
| <b>위치 무작위</b> <i>0.0 - 2.0</i> | 각 모양을 격자 시작점에서 임의의 방향으로 이동하는 승수입니다. |
| <b>무작위 분포</b> <i>가우스, 균일</i> | 임의의 위치에 대해 가우시안 분포에서 균일 분포로 전환합니다. 가우스 분포는 균일 분포에 비해 더 유기적인 결과를 생성할 것이다. |
| <b>벡터 맵 멀티플라이어</b> <i>0.0 - 1.0</i> | 맵의 빨강(X) 및 녹색(Y) 채널에서 지정한 벡터 방향으로 모양을 이동하기 위한 벡터 맵 입력의 영향을 제어합니다. |
| <b>오프셋 가로</b> <i>-2.0 - 2.0</i> | X축을 따라 위치 오프셋을 나타내는 승수입니다. |
| <b>오프셋 세로</b> <i>-2.0 - 2.0</i> | Y축을 따라 위치 오프셋을 나타내는 승수입니다. |
| <b>범위를 벗어남 옵션</b> <i>모양 크기 조정, 위치 제한</i> | 스플래터의 기술적 특성으로 인해 모양은 원래 위치에서 2셀 크기 이상 멀리 그릴 수 없습니다. 모양이 너무 커지거나 너무 멀리 이동하는 경우에는 다음 두 가지 옵션이 있습니다. - [모양 비율]은 경계에 닿았을 때 모양 크기를 줄입니다. - [위치 제한]은 모양을 원래 위치로 되돌립니다 |
| <b>회전</b> |  |
| <b>회전</b> <i>0.0 - 1.0</i> | 모든 모양의 로컬 회전을 제어할 수 있습니다. |
| <b>회전 무작위</b> <i>0.0 - 1.0</i> | 모양당 적용되는 임의 회전 양에 대한 승수입니다. |
| <b>배경에서 회전 경사</b> <i>0.0 - 1.0</i> | 배경 Height 경사 기능의 모양 회전을 수정합니다. 일반적으로 &quot;Bg 경사 크기 비율&quot; 매개 변수와 함께 사용됩니다. |
| <b>회전 맵 승수</b> <i>0.0 - 1.0</i> | 입력 이미지 회색 음영 값의 함수에서 모양 회전을 곱합니다. |
| <b>벡터 맵 멀티플라이어</b> <i>0.0 - 1.0</i> | 벡터 이미지 입력의 함수에서 모양 회전을 설정합니다. |
| <b>Height</b> |  |
| <b>Height 크기 자동 조정</b> <i>거짓/참</i> | 모양 Height이 배경 Height에 비례하여 유지되도록 패턴 크기 조절 기능에 따라 Height을 자동으로 조정합니다. |
| <b>혼합 모드</b> <i>Height 혼합, Alpha 테스트</i> | 모양 겹침 문제를 해결하는 방법을 설정합니다. |
| <b>Height 오프셋</b> <i>-1.0 - 1.0</i> | 모양 Height에 전역 오프셋을 적용합니다. |
| <b>Height 오프셋 무작위</b> <i>0.0 - 1.0</i> | 모양마다 적용된 무작위 Height 오프셋의 승수 |
| <b>Height 오프셋 맵 배율기</b> <i>0.0 - 1.0</i> | 입력 이미지 회색 음영 값의 함수에서 모양 Height 오프셋을 곱합니다. |
| <b>Height 크기</b> <i>0.0 - 1.0</i> | 흩어져 있는 모양의 전체 Height 비율을 제어할 수 있습니다 |
| <b>Height 비율 무작위</b> <i>0.0 - 1.0</i> | 모양마다 적용되는 무작위 Height 비율에 대한 승수입니다. |
| <b>Height 비율 맵 승수</b> <i>0.0 - 1.0</i> | 입력 이미지 회색 음영 값에 따라 모양 Height 비율을 곱합니다. |
| <b>배경 일치</b> <i>0.0 - 1.0</i> | 0에서는 모양 Height이 그대로 유지되고, 1에서는 모양 Height이 기본 Height 배경에 의해 변형됩니다. |
| <b>일치된 배경 매끄럽게</b> <i>0.0 - 2.0</i> | 모양이 배경에 맞춰질 때 모양의 Height 변형에 적용되는 매끄러움 정도를 제어할 수 있습니다. |
| <b>배경 경사에서 기울이기</b> <i>0.0 - 1.0</i> | 로컬 배경 Height 경사의 기능에서 모양 Height을 변형합니다. 배경 경사에 해당하는 선형 그레이디언트가 모양 Height에 추가됩니다. |
| <b>배경 경사 Smoothness</b> <i>0.0 - 2.0</i> | 해당 경사에 따라 모양이 기울어질 때 배경 경사에 적용되는 매끄러움 정도를 제어합니다. |
| <b>검정 픽셀 오려내기</b> <i>거짓/참</i> | 패턴 입력의 검정색 값을 무시합니다. |
| <b>패턴 기준 병합</b> <i>거짓/참</i> | 시작 Height 모양과 일치하도록 모양 아래에 배경 Height을 병합할 수 있습니다. |
| <b>마스킹</b> |  |
| <b>무작위 마스크</b> <i>0.0 - 1.0</i> | 모양의 양을 임의로 마스크하며 전체 양의 비율로 표시됩니다. |
| <b>마스크 무작위 맵 승수</b> <i>0.0 - 1.0</i> | 회색 음영 이미지 입력에 따라 무작위 모양 마스킹을 설정합니다. |
| <b>배경에서 마스크 경사</b> <i>-1.0 - 1.0</i> | 해당 위치의 배경 경사에 따라 모양의 마스크를 제어합니다. |
| <b>색상</b> |  |
| <b>색상 조정</b> <i>-1.0 - 1.0</i> | 흩어져 있는 요소의 색상을 전체적으로 조정할 수 있습니다. |
| <b>색상 무작위</b> <i>0.0 - 1.0</i> | 모양당 임의의 양만큼 색상 값을 이동하기 위한 승수입니다. |
| <b>배경색</b> <i>0.0 - 1.0</i> | 모양 색상을 해당 위치의 배경 색상으로 이동합니다. |
| <b>표준</b> |  |
| <b>배경 경사에서 기울이기</b> <i>0.0 - 1.0</i> | 배경 법선에 따라 모양을 법선으로 기울입니다. |
| <b>보통 무작위</b> <i>0.0 - 1.0</i> | 모양당 임의의 양만큼 모양을 표준으로 기울이기 위한 승수입니다. |
| <b>표준 형식</b> <i>DirectX, OpenGL</i> | 다른 표준 맵 포맷 간 전환(녹색 채널을 반전함) |
| <b>거칠음</b> |  |
| <b>거칠음 조정</b> <i>-1.0 - 1.0</i> | 전체 모양 거칠기를 상쇄할 수 있습니다. |
| <b>배경에서 거칠음</b> <i>0.0 - 1.0</i> | 해당 위치에서 모양 거칠기를 배경 거칠기로 이동합니다. |
| <b>거칠음 무작위</b> <i>0.0 - 1.0</i> | 모양당 임의의 양만큼 거칠기를 상쇄하기 위한 승수입니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="atlas-scatter.resources/atlas-scatter-02.png" />
        </td>
    </tr>
</table>
