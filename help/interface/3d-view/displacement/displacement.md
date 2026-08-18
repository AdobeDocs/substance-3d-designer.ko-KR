---
helpx_url: ""
breadcrumb-title: ''
description: 변위 팝업을 사용하여 3D 장면의 메시에 적용된 변위 및 테셀레이션을 빠르게 조정할 수 있습니다.
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 보기 - 변위 팝업
user-guide-description: ''
user-guide-title: ''
source-git-commit: c7b3b375144c8b58a8e7a7a408895a23e9bd1143
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 2%

---


# 변위 팝업

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="vertical-align: top; border: 0">
        <td style="border: 0">
            <p>3D 보기 도구 모음에서 사용할 수 있는 변위 팝업은 메시의 변위 및 테셀레이션에 대한 직접 컨트롤을 제공합니다.</p>
            <p>세 가지 매개 변수가 있습니다.<ul>
                <li>높이 비율</li>
                <li>높이 수준</li>
                <li>테셀레이션</li></ul>
        </td>
        <td style="width: 60%; margin-left: 32px; border: 0">
            <img src="./displacement.resources/3d-view-displacement-popup-mograph.gif" alt="3D 보기의 변위 팝업" />
        </td>
    </tr>
</table>

## 높이 비율

메시 정점의 수직을 따른 변위의 최대 거리(장면 단위)입니다.<br>
Height 맵에서 값 1.0으로 이동한 거리입니다.

Substance 그래프가 자료에 연결되어 있고 해당 그래프는 다음과 같은 [출력 노드](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)를 포함할 때
<code>heightScale</code> 그러면 팝업에서 Height 크기 조정 매개 변수가 해당 재질에 대해 *사용 안 함*이 됩니다.
현재 그래프로 구동되고 있으므로

>[!TIP]
> 
>[정상 세계 단위에 대한 Height](../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/height-normal-world-units/height-to-normal-world-units.md) 노드를 사용하고 &#39;Height 깊이&#39; 매개 변수가 &#39;Height 비율&#39; 값과 일치합니다.
>변위 사용 시 음영이 올바른지 확인합니다.

## 높이 수준

변위 Height의 *중간점*(으)로 사용되는 Height 맵의 회색 음영 값입니다.
즉, 0.0 승격으로 사용되는 임계값입니다.

이 임계값 미만의 값은 정점을 뒤로 변위시키고 임계값 이상의 값은 변위합니다.
정점이 앞으로 이동됩니다.

## 테셀레이션

쪽맞춤은 개별 메시 면을 세분화하여 해당 선분에 정점을 추가한 다음 연결하는 작업을 포함합니다
모든 정점은 중앙의 새 정점에 도달하므로 한 면이 **6**&#x200B;이 됩니다.

매개 변수는 얼굴을 재귀적으로 세분해야 하는 횟수를 정의합니다.

테셀레이션 매개 변수의 *범위*&#x200B;는 현재 사용 중인 *렌더러*에 따라 다릅니다. 적용할 수 있습니다.
메시 또는 재질마다 다릅니다.

### 메쉬당

[래스터라이저](../3d-renderers/3d-renderers.md#rasterizer) 또는 [GPU 패스트레이서](../3d-renderers/3d-renderers.md#gpu-pathtracer) 렌더러를 사용하는 경우 장면의 각 메시 개체에는 *분리된 개체가 있습니다*
세분 값입니다.

하위 분할은 상황에 따라 다릅니다. *불균일한 Height 값*을 가진 서체만 표시되도록 최적화되었습니다.
*비플랫 Height 맵*&#x200B;은 매개 변수 값에 관계 없이 세분화됩니다.

### 재질당

[OpenGL](../3d-renderers/3d-renderers.md#opengl) 렌더러를 사용하는 경우 장면의 각 재질에는 *Separate* 하위 분할 값이 있습니다.
이 재질은 *해당 재질을 사용하는 모든 면*&#x200B;에 적용됩니다.

세분 구분은 컨텍스트가 아닙니다. 서피스는 현재 시간에 관계없이 지정된 횟수만큼 세분 구분됩니다
Height 값 또는 텍스처.

## 쪽맞춤 시각화

메시의 **와이어프레임**&#x200B;을 확인하여 쪽맞춤의 결과를 시각화할 수 있습니다.<br>
각 렌더러의 와이어프레임 표시 단계는 다음과 같습니다.

### 래스터라이저/GPU 패스트레이서

사용: <img src="../3d-view.resources/3d-view-scene-toolbar-render-settings.png" width="22" /> **렌더러 설정**
 그런 다음 속성 도크에서 **렌더링 설정 > 진단 모드**(으)로 이동하고 **와이어프레임을 선택합니다
 (월드 공간)** 옵션.

### OpenGL

사용: <img src="../3d-view.resources/3d-view-scene-toolbar-wireframe.png" width="22" /> **와이어프레임**
 버튼을 클릭합니다.
