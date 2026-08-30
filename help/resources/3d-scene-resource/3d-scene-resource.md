---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/resources/3d-scene-resource.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 재질 미리 보기 및 테스트를 위해 3D 장면 리소스를 가져오고 사용하는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Resources > 3D scene resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 장면 리소스
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 1%

---


# 3D 장면 리소스

이 페이지에서는 지원되는 파일 형식 및 사용 방법을 포함하여 Substance 3D Designer의 **3D 장면** 리소스 유형에 대해 설명합니다.

## 개요

3D 장면 리소스는 다양한 워크플로에서 사용할 수 있습니다.

* [베이킹 메시 맵](../../bakers/bakers.md)
* [3D 보기](../../interface/3d-view/3d-view.md)의 [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)에서 *텍스처*&#x200B;를 미리 봅니다.

다음과 같은 3D 장면 파일 형식이 지원됩니다.

* [USD](https://graphics.pixar.com/usd/release/index.html)&#x200B;(\*.usd)
* [USDA](https://graphics.pixar.com/usd/release/index.html) (\*.usda)
* [USDZ](https://graphics.pixar.com/usd/release/index.html)&#x200B;(\*.usdz)
* [Autodesk FBX](https://www.autodesk.com/products/fbx/overview)&#x200B;(\*.fbx)
* [Wavefront OBJ](https://www.fileformat.info/format/wavefrontobj/egff.htm) (\*.obj)
* [Autodesk 3D Studio 메시](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2022/ENU/3DSMax-Data-Exchange/files/GUID-A16ECF7F-70E5-4F9F-8EAD-35F5CFB485A2-htm.html)&#x200B;(\*.3ds)
* [Collada](https://www.khronos.org/collada/)&#x200B;(\*.dae)
* [Autodesk AutoCAD 드로잉](https://knowledge.autodesk.com/support/autocad/learn-explore/caas/CloudHelp/cloudhelp/2019/ENU/AutoCAD-Core/files/GUID-D4242737-58BB-47A5-9B0E-1E3DE7E7D647-htm.html) (\*.dxf)

## 메시 저장소

3D 장면은 *만*&#x200B;연결할 수 있습니다. 즉, 디스크의 해당 위치에 있으며 응용 프로그램에서 참조됩니다.

3D 장면 리소스가 있는 패키지가 [Substance 3D](https://www.adobe.com/kr/products/substance3d/3d-augmented-reality.html) 에셋(SBSAR)으로 게시되면 메쉬가 *임베드되지 않음*&#x200B;이지만 삭제됩니다.

## 베이킹 메시 맵

3D 장면을 패키지에 연결하는 것은 해당 장면 지오메트리 중 [메시 맵을 분리하는](../../bakers/bakers.md) 유일한 방법입니다. 다음 단계를 수행하여 시작할 수 있습니다.

* 패키지에서 *RMB*&#x200B;을 클릭하고 상황에 맞는 메뉴에서 <b>링크 > 3D 메시</b> 옵션을 선택합니다.
* 지원되는 모든 3D 장면 파일 선택
* <b>Udim mesh로 연결</b> 대화 상자 프롬프트가 나타나면 UV 타일을 구우지 않으려면 *아니요*&#x200B;를 클릭합니다
* 리소스를 [탐색기](../../interface/the-explorer-window/the-explorer-window.md)에 로드한 상태에서 *RMB*&#x200B;을(를) 클릭하고 상황에 맞는 메뉴에서 <b>모델 정보 굽기</b> 옵션을 선택합니다
* 메시 맵 베이크를 설정하고 실행할 수 있는 [베이크 모델 정보](../../bakers/bakers.md) 대화 상자가 나타납니다

![메시 맵 굽기](3d-scene-resource.resources/bake-model-information.gif "메시 맵 굽기"){width="512px"}

## UDIM/UV-tile 사용

메시 리소스가 연결되어 응용 프로그램에서 0-1 범위를 벗어난 UV를 가졌다고 감지하면 이 메시를 UDIM 메시(UV 타일이라고도 함)로 처리해야 하는지 묻는 메시지가 표시됩니다. 나중에 변경할 수 있는 설정이며 UV-Tiles를 사용하고 있는지 확실하지 않은 경우 <b>아니요</b>로 응답해야 합니다.

UV-Tile 비헤이비어가 활성화되면 베이킹이 다르게 작동하고 감지된 각 UV-Tile에 대해 텍스처를 베이킹합니다.

## 리소스/장면 및 상태

애플리케이션은 3D 뷰에 표시되는 항목을 두 개의 개별 파일로 분리합니다. 실제 3D 모델 또는 메시는 탐색기에 표시되는 리소스입니다. 조명, 카메라 및 기타 설정의 설정을 &quot;<b>상태</b>&quot;이라고 합니다. 상태는 외부 .sbsscn 파일에 저장할 수 있으며 나중에 다시 로드할 수 있습니다. .sbsscn 파일은 리소스가 아니며 [3D 보기의 장면 메뉴](../../interface/3d-view/3d-view.md)를 통해서만 로드할 수 있는 추가 구성 파일입니다.
