---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render.html"
breadcrumb-title: ''
description: PBR 렌더링 노드를 사용하여 실제 조명으로 실제 기반 재질을 렌더링하여 재질 모양을 미리 볼 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR 렌더링
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 6%

---


# PBR 렌더링

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-render.resources/pbr-render.png){width="250px"}

<b>내부:</b> 재질 필터 > PBR 유틸리티

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이미지 기반 조명(IBL)을 사용하여 구, 평면 또는 원통에 PBR 재질을 렌더링합니다. 이것은 노드 내의 렌더링 엔진으로, 썸네일, 미리 보기 또는 2D 에셋을 생성하는 데 매우 유용할 수 있습니다. 3D 보기처럼 렌더링되는 것이 아니라 그래프에서 실제 텍스처가 생성되는 것입니다.

이 노드에는 적어도 전체 PBR 자료가 꽂혀 있어야 합니다. [PBR 렌더링 생성 모드]를 사용하여 재질을 링크에 연결하는 것이 좋습니다. 또한 조명을 계산하려면 렌더링에 구형에서 래핑하지 않은 HDRI 환경이 필요합니다. 테스트용 재질은 PBR 재질에서 찾을 수 있으며, 환경 맵은 라이브러리의 [3D 보기에서 찾을 수 있습니다.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/3d-view-library.md)

</td>
</tr>
</table>

>[!WARNING]
>
> **CPU(SSE2) 엔진**
> 
> PBR 렌더링 노드가 매우 무거우며 SSE2 CPU 엔진에서 제대로 작동하지 않습니다. 노드가 매우 좋지 않으면 F9 키를 눌러 다른 엔진으로 전환합니다.

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>재료 채널 입력</b> | 여러 재질 입력을 사용하여 지오메트리 위에 재질을 렌더링합니다. <br><br>- 기본 색상<br>- 표준<br>- 방출<br>- 거칠기<br>- 금속성<br>- Specular level<br>- Height<br>- 앰비언트 오클루전<br>- 불투명 마스크<br>- 비등방성 레벨<br>- 비등방성 각도<br>- 반투명도<br>- 분산 거리 비율 |
| <b>렌즈 Dirt 맵</b> <i>회색 음영 입력</i> | 렌즈 플레어 시 나타나는 렌즈에서의 Dirt에 대한 사용자 정의 맵 |
| <b>렌즈 조리개 맵</b> <i>회색 음영 입력</i> | 초점이 맞지 않는 보케 모양을 재정의하는 데 사용할 수 있습니다. 대비가 많을수록 더 잘 보입니다. 텍스처 안의 원만 샘플링되므로 모든 모양이 원 안에 맞아야 한다는 점을 명심하십시오. |
| <b>배경 입력</b> <i>색상 입력</i> | <b>배경 모드</b> 매개 변수를 <i>배경 입력</i>(으)로 설정한 경우 사용자 지정 맵이 배경으로 사용됩니다. |
| <b>환경 맵</b> <i>색상 입력</i> | 조명을 계산하는 데 사용되는 환경 맵입니다. 구형으로 매핑되고 HDR에 있어야 합니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>아름다움</b> | 최종 렌더링 |
| <b>원시 조도</b> | 최종 렌더링<br><br><i>Alpha:</i> 불투명도 맵의 조도 데이터 |
| <b>원시 Specular</b> | 최종 렌더링<br><br><i>Alpha:</i> Specular 그림자 맵의 Specular 데이터 |
| <b>일반 월드 공간</b> | 최종 렌더링<br><br><i>Alpha:</i> 세계 공간 높이 맵의 세계 공간 표준 데이터 |
| <b>일반 접선 공간</b> | 최종 렌더링<br><br><i>Alpha:</i> 접선 공간 높이 맵의 접선 공간 표준 데이터 |
| <b>UV</b> | 최종 렌더링<br><br><i>Alpha:</i> 불투명도 맵의 UV 데이터 |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>모양</b> <i>구, 평면, 원통</i> | 렌더링에 사용할 모양을 설정합니다. 사용자 정의 모양은 사용할 수 없습니다. |
| <b>변위 강도</b> <i>0.0 - 0.5</i> | Height 변위 강도를 설정합니다. |
| <b>환경 회전</b> <i>0.0 - 1.0</i> | 조명 환경을 회전합니다. 카메라를 이동할 때와 비교하여 사전 회전합니다. |
| <b>배경 모드</b> <i>색상, 환경, 주변 환경, 배경 입력</i> | 배경에 표시되는 내용을 설정합니다. 색상은 단색이며, 환경은 선택적 흐림 효과로 연결한 맵입니다. 주변은 환경의 매우 흐린 버전입니다. |
| <b>배경색</b> <i>(색상 값)</i> | 배경 모드가 색상으로 설정된 경우에만 사용할 수 있습니다. |
| <b>환경 배경 흐림 효과</b> <i>0.0 - 1.0</i> | 배경 모드가 환경으로 설정된 경우에만 사용할 수 있습니다. |
| <b>모양</b> |  |
| <b>크기 조절</b> <i>0.0 - 2.0</i> | 구의 배율을 설정합니다. |
| <b>평면 크기</b> <i>0.0 - 1.0</i> | 평면의 배율을 설정합니다. |
| <b>원통 반경</b> <i>0.0 - 1.0</i> | 원통의 반경을 설정합니다. |
| <b>실린더 길이</b> <i>0.0 - 1.0</i> | 원통 길이를 설정합니다. |
| <b>회전</b> <i>0.0 - 1.0</i> | 조명을 회전하지 않고 모양을 회전합니다. |
| <b>회전 방향</b> <i>0.0 - 1.0</i> | 회전 축을 2D로 설정합니다. |
| <b>방향을 중심으로 회전</b> <i>0.0 - 1.0</i> | 회전 축에 모양을 회전합니다. |
| <b>모양 위치</b> <i>-1.0 - 1.0</i> | 모양을 이동합니다. |
| <b>UV 타일링</b> <i>1.0 - 6.0</i> | UV 타일링의 양을 설정합니다. |
| <b>구 UV 비율</b> <i>0.0 - 4.0</i> | 구의 UV 비율을 설정합니다. |
| <b>평면 UV 비율</b> <i>1.0 - 4.0</i> | 평면의 UV 비율을 설정합니다. |
| <b>실린더 UV 비율</b> <i>1.0 - 6.0</i> | [원통]의 UV 비율을 설정합니다. |
| <b>UV 오프셋</b> <i>0.0 - 1.0</i> | UV 오프셋 |
| <b>기울기 UV</b> <i>거짓/참</i> | 구의 UV를 45도 기울입니다. |
| <b>카메라</b> |  |
| <b>노출</b> <i>-4.0 - 4.0</i> | 카메라 노출을 설정합니다. |
| <b>톤 매퍼</b> <i>선형, ACE, 영화 헤더</i> | 최종 이미지에 사용할 톤 매핑 솔루션을 설정합니다. |
| <b>카메라 모드</b> <i>원근감, 직교</i> | 두 투영 모드 간에 카메라를 전환합니다. |
| <b>보기 필드</b> <i>0.01 - 100.0</i> | 카메라 FOV 각도를 설정합니다. |
| <b>거리</b> <i>0.0 - 4.0</i> | 개체 중심으로부터의 카메라 거리를 설정합니다. |
| <b>비네팅 강도</b> <i>0.0 - 1.0</i> | 비네팅 효과의 강도를 설정합니다. |
| <b>비네팅 반경</b> <i>0.0 - 1.0</i> | 비네팅 효과의 반경을 설정합니다. |
| <b>화면 위치</b> | 개체 주위로 카메라를 이동하고 2D 보기에서도 gizmo로 변경할 수 있습니다. |
| <b>필드 깊이</b> |  |
| <b>조리개 반경</b> <i>0.0 - 0.1</i> | 조리개의 반경을 설정합니다. 값이 높을수록 포커스가 맞지 않는 영역이 더 흐려집니다(보케). |
| <b>조리개 블레이드</b> <i>3 - 9</i> | 보케 흐림 효과의 모양을 설정합니다. |
| <b>조리개 링</b> <i>0.0 - 1.0</i> | 보케 모양에 내부 그레이디언트를 추가합니다. |
| <b>조리개 분수</b> <i>0.0 - 2.0</i> | 보크에 색수차를 추가합니다. |
| <b>소용돌이치는 보케</b> <i>0.0 - 1.0</i> | 초점이 맞지 않는 보케 흐림 영역에 소용돌이 또는 회전하는 효과 유형을 추가합니다. |
| <b>초점 모드</b> <i>자동, 지점</i> | 포커스가 미리 결정되거나 사용자 세트인지 설정합니다. 점 초점 을 사용하면 2D 보기 내에서 점을 이동하여 초점 거리를 결정할 수 있습니다. |
| <b>초점</b> | 포커스가 포인트로 설정되어 있으면 해당 포인트를 이동할 수 있습니다. 2D 보기 기즈모가 있습니다. |
| <b>초점 오프셋</b> <i>-0.5 - 0.5</i> | 포커스가 [자동]으로 설정되어 있으면 포커스를 앞뒤로 이동할 수 있습니다. |
| <b>사용자 지정 조리개 맵 사용</b> <i>거짓/참</i> | 위의 조리개 설정을 재정의하고 조리개 맵 입력을 사용하여 보케 모양을 결정합니다. 입력이 필요합니다. |
| <b>Post Effects</b> |  |
| <b>포스트 효과 사용</b> <i>거짓/참</i> | 최종 렌더링에서 <i>모두</i> 후 효과를 전환합니다. |
| <b>개화 강도</b> <i>0.0 - 2.0</i> | 흐림 효과의 강도를 설정합니다. |
| <b>개화 임계값</b> <i>0.0 - 2.0</i> | 꽃이 나타나도록 낮은 임계값을 설정합니다. |
| <b>블룸 크로마 시프트</b> <i>0.0 - 1.0</i> |  |
| <b>렌즈 헤일로 강도</b> <i>0.0 - 1.0</i> | 렌즈 후광 효과의 강도를 설정합니다. |
| <b>렌즈 플레어 강도</b> <i>0.0 - 1.0</i> | 렌즈 플레어의 강도를 설정합니다. 이 효과를 제대로 보려면 환경 배경의 빛이 보이는지 확인하십시오. |
| <b>렌즈 Dirt 강도</b> <i>0.0 - 1.0</i> | [렌즈 플레어]에 렌즈 Dirt 맵의 효과를 설정합니다. |
| <b>렌더링 설정</b> |  |
| <b>확산 품질</b> <i>16개 샘플, 32개 샘플, 64개 샘플, 128개 샘플</i> | 확산 맵의 품질 수준 간을 전환합니다. |
| <b>확산 방출 배율기</b> <i>0.0 - 1.0</i> | 방출 부분이 조도에 기여하는 정도를 제어합니다. |
| <b>확산 그림자 강도</b> <i>0.0 - 1.0</i> | 분산된 그림자의 강도를 제어합니다. |
| <b>Specular 디더링</b> <i>0.0 - 1.0</i> | Specular의 디더링 양을 설정합니다. |
| <b>Specular 섀도 멀티플라이어</b> <i>0.0 - 1.0</i> | Specular 반사에서 어두운 영역의 강도를 제어합니다. |
| <b>불투명도 모드</b> <i>디더링 Alpha 테스트, 단순 Alpha 혼합</i> | 투명도를 적용하는 방법을 제어합니다. <i>단순 Alpha 혼합</i> 모드는 균일한 배경에서 가장 잘 보입니다. |
| <b>앰비언트 오클루전 강도</b> <i>0.0 - 1.0</i> | 주변 오클루전 그림자의 강도를 설정합니다. |
| <b>재질 조정</b> |  |
| <b>표준 다시 계산</b> <i>거짓/참</i> | 표준은 Height 강도에 따라 변위 맵에서 다시 계산됩니다. |
| <b>표준 형식</b> <i>DirectX, OpenGL</i> | 다른 표준 맵 포맷 간 전환(녹색 채널을 반전함) |
| <b>유전체 F0 입력</b> <i>상수 값, Specular level 입력</i> | 드라이브 F0 값을 설정합니다. Specular level 입력 은 입력 맵에 의해 구동됨을 의미합니다. |
| <b>유전체 F0</b> <i>0.0 - 0.08</i> | 유전체 F0 입력에 대해 상수 값 을 선택한 경우 이 슬라이더를 사용하면 전체 값을 설정할 수 있습니다. |
| <b>코트 지우기</b> |  |
| <b>코트 지우기 사용</b> <i>거짓/참</i> | 입력 재질 상단에 간단한 투명 코트 층을 추가로 사용할 수 있습니다. |
| <b>코트 두께 지우기</b> <i>0.0 - 1.0</i> | 클리어코트 레이어의 강도나 강도를 설정합니다. |
| <b>코팅 반사 수준 지우기</b> <i>0.0 - 1.0</i> | 클리어코트 레이어의 거칠기를 설정합니다. |
| <b>기본 레이어에서 일반 상속</b> <i>거짓/참</i> | Clearcoat이 기본 재질의 표준을 무시하거나 사용하는지 여부를 설정합니다. |
| <b>발광</b> |  |
| <b>방출 조명 사용</b> <i>참/거짓</i> | 방출 조명의 확산 기여도를 전환합니다. |
| <b>발광 강도</b> <i>0.0 - 10.0</i> | 방출 맵의 전역 승수를 설정합니다. |
| <b>하위 표면 분산</b> |  |
| <b>하위 표면 분산 사용</b> <i>참/거짓</i> | 최종 렌더링에서 하위 표면 산란을 전환합니다.<br><br><i>참고:</i> 하위 표면 산란을 사용하려면 <b>반투명도</b> 입력 값이 <i>0.0</i>보다 높아야 합니다. |
| <b>분산 거리</b> <i>0.0 - 1.0</i> | 분산 효과의 최대 거리를 조정합니다.<br><br><i>참고:</i> 이 값은 <b>분산 거리 비율</b> 입력 값 <i>색상 채널당</i>에 대해 곱해집니다. |
| <b>빨간색 Shift</b> <i>0.0 - 1.0</i> | 분산에서 빨강 이동 효과의 강도를 조정합니다. |
| <b>레일리</b> <i>0.0 - 1.0</i> | 분산에서 레일리 효과의 강도를 조정합니다. |

## 예

모든 이미지는 [Substance 3D 에셋](https://substance3d.adobe.com/assets) 라이브러리의 재질을 사용하여 Designer의 2D 뷰포트 내부에서 직접 생성되었습니다.

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/pbr-render-v2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-thermal-insulation-panel.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-ominous-obsidian.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-forest-gravel-1.jpg" />
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-chesterfield-1.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-carbon-fiber.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/plane-inclined-lumber-tiles.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/cylinder-medieval-leaded-glass-window.jpg" />
        </td>
    </tr>
</table>
