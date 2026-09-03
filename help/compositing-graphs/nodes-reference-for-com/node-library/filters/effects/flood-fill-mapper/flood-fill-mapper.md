---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-mapper.html"
breadcrumb-title: ''
description: Flood Fill 매퍼 노드를 사용하여 텍스처 처리에 플러드 필 알고리즘을 사용하여 연결된 영역 간에 값을 매핑합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill 매퍼
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 6%

---


# Flood Fill 매퍼

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-mapper.resources/flood-fill-mapper-01.png)![](flood-fill-mapper.resources/flood-fill-mapper-02.png)

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

Flood Fill 매퍼를 사용하면 기존 패턴 또는 텍스처를 [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)의 모든 단일 셀로 다시 매핑할 수 있습니다. 단색이나 값을 생성하지 않지만 사용자 고유의 입력 맵을 사용할 수 있다는 점에서 [무작위 회색 음영](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md) 또는 [그레이디언트](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md)와 같은 다른 Flood Fill 변환과는 다릅니다. [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)과 [타일 Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) 또는 [모양 매퍼](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-mapper/shape-mapper.md)를 조합한 것으로 볼 수 있습니다. 유사한 컨트롤과 인터페이스를 몇 가지 제공합니다.

색상 버전에는 노멀 맵 작업을 위한 추가 컨트롤이 있으며, 여기서 [접선 공간 노맵 회전을 보정](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-vector-rotation/normal-vector-rotation.md)할 수 있습니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>Flood Fill 상자</b> <i>색상 입력</i> | 표준 Flood Fill 입력(필수) |
| <b>패턴 입력 1-8</b> <i>회색 음영/색상 입력</i> | 사용자 정의 패턴 이미지 입력입니다. |
| <b>패턴 분포 맵</b> <i>회색 음영 입력</i> | ID 맵 - 어느 패턴이 어느 셀로 가는지를 결정합니다. 색인에 Flood Fill 등 다른 Flood Fill 맵에서 가져올 수 있습니다. |
| <b>지도 크기 조절</b> <i>회색 음영 입력</i> | 맵을 사용하여 셀당 배율 결정 |
| <b>회전 맵</b> <i>회색 음영 입력</i> | 맵으로 셀당 회전을 결정합니다. |
| <b>광도 오프셋 맵</b> <i>회색 음영 입력</i> | 셀당 광도 설정을 위한 매핑 |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>타일링 모드</b> <i>타일링 없음, H+V</i> | 타일링 사용 여부를 설정합니다. [크기] 또는 [비율]이 1 미만으로 설정된 경우에만 표시됩니다. |
| <b>패턴</b> |  |
| <b>패턴 입력 번호</b> <i>1 - 8</i> | 사용할 사용자 정의 패턴 입력 양을 설정합니다. |
| <b>패턴 분포 모드</b> <i>무작위, 모양 크기, 분포 맵 입력</i> | 셀에 표시되는 패턴을 결정하는 방법을 설정합니다. |
| <b>패턴 분포 지터링</b> <i>0.0 - 1.0</i> | [임의화]를 통해 모든 것을 변경하지 않고 패턴 분포에서 약간의 변경이나 오프셋을 허용합니다. |
| <b>크기</b> |  |
| <b>크기 모드</b> <i>텍스처 기준, 모양 기준점 기준, 가장 큰 모양 기준, 가장 작은 모양 기준, 모양 상자 맞추기</i> | 각 셀의 패턴 크기를 결정하는 방법을 설정합니다. |
| <b>크기</b> <i>0.0 - 1.0</i> | 패턴의 균일하지 않은 배율 조정을 허용합니다. |
| <b>크기 조절</b> <i>0.0 - 1.0</i> | 효과의 전체(균일) 배율을 설정합니다. |
| <b>지도 배율기</b> <i>0.0 - 1.0</i> | 선택 사항인 [비율 맵]의 영향을 설정합니다. |
| <b>무작위 크기 조정</b> <i>-1.0 - 1.0</i> | 패턴 크기 내에서 임의 변형 정도를 설정합니다. |
| <b>회전</b> |  |
| <b>회전</b> <i>0.0 - 1.0</i> | 모든 셀에 대해 전체적으로 균일한 회전을 설정합니다. |
| <b>회전 맵 배율기</b> <i>0.0 - 1.0</i> | 옵션 회전 맵의 영향을 설정합니다. |
| <b>회전 무작위</b> <i>0.0 - 1.0</i> | 모든 셀에 대해 임의 회전 양을 설정합니다. |
| <b>회전 자동 크기 조정</b> <i>거짓/참</i> | 패턴을 회전할 때 셀 내부에 맞게 패턴의 크기를 조정할지 여부를 설정합니다. |
| <b>위치</b> |  |
| <b>위치 오프셋</b> <i>0.0 - 1.0</i> | 모든 셀에 대해 전역 위치 오프셋을 설정합니다. |
| <b>위치 오프셋 정렬</b> <i>텍스처, 패턴</i> | 오프셋 0점을 패턴 셀이나 텍스처에 정렬하도록 설정합니다. |
| <b>위치 오프셋 무작위</b> <i>0.0 - 1.0</i> | 셀별 위치 오프셋 임의화의 양을 설정합니다. |
| <b>색상(회색 음영 버전만)</b> |  |
| <b>광도 범위</b> <i>0.0 - 1.0</i> | 텍스처의 전체 대비를 설정합니다. 여기서 0은 중간 회색이 됩니다. |
| <b>광도 범위 무작위</b> <i>0.0 - 1.0</i> | [광도 범위]에 대한 임의화의 양을 설정합니다. |
| <b>광도 오프셋</b> <i>-1.0 - 1.0</i> | 명도 컨트롤 역할을 하는 광도의 오프셋을 설정합니다. |
| <b>광도 오프셋 무작위</b> <i>0.0 - 1.0</i> | [광도 오프셋]에 대한 임의화의 양을 설정합니다. |
| <b>광도 오프셋 맵 배율기</b> <i>0.0 - 1.0</i> | 선택적 광도 오프셋 맵의 영향을 설정합니다. |
| <b>배경색</b> <i>(회색 음영 값)</i> | 텍스처가 혼합되는 배경색을 설정합니다. |
| <b>색상(색상 버전만)</b> |  |
| <b>노멀 맵</b> <i>거짓/참</i> | 패턴 입력을 노멀 맵으로 해석하도록 설정합니다. 수직 탄젠트 공간 회전을 보정하고 수정합니다. |
| <b>표준 형식</b> <i>DirectX, OpenGL</i> | 다른 표준 맵 포맷 간을 전환합니다(녹색 채널을 반전합니다). Is 노멀 맵이 True인 경우에만 활성화됩니다. |
| <b>HSL 조정</b> <i>-1.0 - 1.0</i> | HSL을 전역적으로 조정합니다. |
| <b>HSL 무작위</b> <i>-1.0 - 1.0</i> | 셀당 HSL 임의화를 설정합니다. |
| <b>Alpha 조정</b> <i>-1.0 - 1.0</i> | 전체 Alpha 조정을 설정하여 Alpha 대비를 줄입니다. |
| <b>무작위 Alpha</b> <i>-1.0 - 1.0</i> | 셀당 Alpha 조정 임의화를 설정합니다. |
| <b>배경색</b> <i>(색상 값)</i> | 텍스처가 혼합되는 배경색을 설정합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-mapper.resources/flood-fill-mapper-03.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="flood-fill-mapper.resources/flood-fill-mapper-04.jpg" />
        </td>
    </tr>
</table>
