---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-extrude.html"
breadcrumb-title: ''
description: Substance 3D Designer 텍스처에서 모양 돌출 노드를 사용하여 모양을 돌출시키고 3D 같은 깊이 효과를 만듭니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 모양 돌출
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 5%

---


# 모양 돌출

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-extrude.resources/shape-extrude-01.png){width="128px"}

<b>내부:</b> 텍스처 생성기 > 패턴

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

2d, 이진 &quot;모양&quot; 입력을 3D 회전 높이 맵에 렌더링할 수 있는 고급 노드입니다. 마치 3D 패키지의 돌출과 비슷하게 작동하여 모양을 축을 따라 돌출시켜 볼륨을 만듭니다. 프로필 그레이디언트 마스크와 함께 회전/선반 유형의 바디도 만들 수 있습니다. 하이맵을 위한 복잡한 인공 모양을 만드는 데 매우 유용합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>모양 입력 돌출</b> <i>회색 음영 입력</i> | [돌출 모양]을 [사용자 정의]로 설정한 경우 사용자 고유의(가급적) 이진 모양 마스크를 여기에 연결합니다. |
| <b>프로필 그레이디언트</b> <i>회색 음영 입력</i> | 프로파일 유형이 수직 그레이디언트로 설정되어 있는 경우 를 사용하여 축을 따라 모양의 스케일을 정의할 수 있습니다(회전 바디). |
| <b>프로필 마스크</b> <i>회색 음영 입력</i> | 축을 따라 돌출된 모양을 숨기거나 표시하는 데 사용되는 마스크 슬롯입니다. 축을 따라 모양의 연속성을 깨는 데 사용할 수 있습니다. 이진으로만 해석됨: 회색 음영 put 값은 0 또는 1로 반올림됩니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>돌출 Height</b> <i>0.0 - 1.0</i> | 중앙에서 위쪽으로 모양을 돌출시키는 양입니다. |
| <b>돌출 깊이</b> <i>0.0 - 1.0</i> | 중앙에서 다운로드해서 모양을 돌출시키는 양입니다. |
| <b>모양 돌출</b> <i>큐브, 원통, 사용자 지정 입력</i> | 기본 제공 모양을 사용하거나 외부에서 사용자 정의 모양을 입력합니다. |
| <b>돌출 모양 크기</b> <i>0.0 - 1.0</i> | 기본 제공 육면체 및 원통과 함께 사용되며 기본 모양 크기를 결정하며 균일하지 않게 크기를 조절할 수 있습니다. |
| <b>크기 조절</b> <i>0.0 - 1.0</i> | 효과의 전체 배율을 설정합니다. 기본 제공 도형을 사용하면 균일한 기본 도형 배율이며 Height 또는 깊이에 영향을 주지 않습니다.<br><br>사용자 지정 입력을 사용하면 전체 최종 결과의 배율을 균일한 방식으로 조절할 수 있습니다. |
| <b>프로필 유형</b> <i>직선, 수직 그레이디언트, 마스크</i> | 효과의 동작 및 선택적 추가 입력 맵 사용을 결정하는 기본 컨트롤입니다.<br><br>직선은 표준 돌출 동작이며 [수직 그레이디언트]를 사용하면 전체 축을 따라 사용자 정의 비율 값을 사용할 수 있고 [마스크]를 사용하면 축을 따라 마스크를 통해 섹션을 숨길 수 있습니다. |
| <b>경사 Height</b> <i>0.0 - 1.0</i> | 경사가 돌출 축을 따라 도달하는 거리를 설정합니다. |
| <b>경사 강도</b> <i>0.0 - 1.0</i> | 경사가 원래 모양에서 얼마나 되돌아가는지 설정합니다. |
| <b>경사 곡선</b> <i>-1.0 - 1.0</i> | 경사 효과의 볼록 또는 오목 곡선을 설정합니다. 값을 0으로 지정하면 커브가 없고 직선이 됩니다. |
| <b>경사 미러링</b> <i>거짓/참</i> | 모양 아래뿐만 아니라 위쪽에도 경사를 적용하려면 토글합니다. |
| <b>멀티플라이어 다운스케일</b> <i>0 - 2</i> | 손쉬운 다운스케일링 컨트롤 내장. 앤티 앨리어스를 빠르게 추가하는 데 사용할 수 있으며, 노드 해상도도 높여야 합니다. |
| <b>위치</b> | 3D 공간에서 결과를 회전하기 위한 기본 컨트롤입니다. 2D 보기에서 인터랙티브 Gizmo와 상호 작용. |
| <b>출력 범위</b> <i>[0, 1], [-1, 1]</i> | 출력 최소 및 최대 값을 설정합니다. [범위]를 [-1,1]로 설정하면 음수 값이 검정으로 표시됩니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-extrude.resources/shape-extrude-02.png" />
        </td>
    </tr>
</table>
