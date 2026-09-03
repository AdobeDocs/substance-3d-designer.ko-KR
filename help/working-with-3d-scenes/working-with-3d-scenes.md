---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/working-with-3d-scenes.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 3D 장면을 가져와 편집하고 사용하여 재질을 미리 보고 테스트하는 방법을 살펴보세요.
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 장면 작업
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 0%

---


# 3D 장면 작업

![3D 장면 작업](working-with-3d-scenes.resources/working-with-3d-scenes-01.png "3D 장면 작업"){zoomable="yes"}

Designer을 사용하면 컨텍스트에서 재질 작업을 위해 [3D 장면](../glossary/glossary.md)을 로드할 수 있습니다. 각 형식에 대해 지원되는 기능 목록을 포함하여 3D 장면에 대해 지원되는 파일 형식 목록을 여기에서 확인할 수 있습니다. <b>&lt;링크 필요></b>

컨텍스트에서 작업하려면 장면의 [재질](../glossary/glossary.md) 중 하나를 [재정의](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)하여 Designer에서 작성된 재질로 바꾸는 작업이 포함됩니다.\
Designer에서 사용할 수 있는 Substance 그래프 템플릿을 사용하거나 3D 장면의 재질에서 [값 및 텍스처 추출](../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md)을 시작점으로 사용하여 처음부터 시작할 수 있습니다.

3D 장면 사용을 완료하면 다른 응용 프로그램에서 인제스트할 새 파일로 [내보내기](../working-with-3d-scenes/exporting-scenes/exporting-scenes.md)할 수 있습니다.

USD 형식으로 내보낼 때 이 워크플로우는 완전히 <b>비파괴</b>할 수 있습니다. 즉, 편집 및 추가 내용만 내보냅니다.

먼저 작업할 3D 장면을 로드하고 세션 간에 Designer의 상태를 유지할 수 있어야 합니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 3D 장면의 내용

</td>
<td style="border: 0;" valign="top">

### 장면 불러오기

</td>
<td style="border: 0;" valign="top">

### 장면 상태 파일

</td>
</tr>
</table>

## 3D 장면의 내용

3D 장면을 로드할 때 Designer에서 자체 장면을 만들어 호스팅했습니다.

장면의 다음 콘텐츠와 상호 작용할 수 있습니다.

* <b>재질:</b> 장면에 사용된 모든 재질은 Designer에서 만든 사본으로 [재정의](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)할 수 있습니다. Substance 그래프의 원시 값 또는 텍스처를 사용하여 해당 사본의 [재질 속성](../interface/3d-view/material-properties/material-properties.md)을 편집할 수 있습니다.
* <b>메시:</b> 지오메트리는 뷰포트에서 직접 선택하거나 [장면 브라우저](../interface/3d-view/scene-browser/scene-browser.md)에서 선택하여 재질 동작에 액세스할 수 있습니다([재정의](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md), [재설정](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md), [Substance 그래프로 추출](../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md))
* <b>조명:</b> 장면의 모든 조명은 [장면 브라우저](../interface/3d-view/scene-browser/scene-browser.md)에서 비활성화할 수 있습니다.
* <b>카메라:</b> 장면에서 감지된 모든 카메라는 Designer에서 추가한 카메라에 사전 설정으로 추가됩니다.

![3D 장면의 콘텐츠](working-with-3d-scenes.resources/working-with-3d-scenes-02.png "3D 장면의 콘텐츠"){zoomable="yes"}

Designer은 3D 장면에 USD 설명을 사용합니다. 해당 레이아웃은 장면 브라우저에서 탐색할 수 있으며, 각 [USD prim](https://openusd.org/release/glossary.html#usdglossary-prim) 유형에는 자체 아이콘(지오메트리, 재질, 셰이더, 카메라, 변환 등)이 있습니다.

[장면 브라우저](../interface/3d-view/scene-browser/scene-browser.md)를 사용하여 장면의 콘텐츠를 선택, 활성화 및 비활성화할 수 있습니다. 따라서 사용자 정의 3D 장면을 사용하여 작업할 때는 계속 표시되는 것이 좋습니다.

## 장면 불러오기

3D 뷰에는 3D 장면을 로드하는 몇 가지 경로가 있습니다.

1. [패키지](../glossary/glossary.md)에서 [3D 장면 리소스](../resources/3d-scene-resource/3d-scene-resource.md)를 두 번 클릭하거나 3D 보기로 드래그합니다.
1. [라이브러리](../interface/the-library/the-library.md)의 3D 장면 항목을 3D 보기로 드래그합니다([라이브러리에 자신의 콘텐츠를 추가한 경우](../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)).
1. 시스템의 파일 브라우저에서 3D 장면 파일을 3D 보기로 드래그합니다
1. 3D 장면 상태 파일(SBSSCN)과 참조된 메시 불러오기

장면 상태가 3D 장면 리소스와 장면 상태 파일에 기록되어 패키지에 저장되므로 메서드 1과 4만 사용하면 마지막으로 작업했을 때와 정확히 장면을 다시 로드할 수 있습니다. 방법 2와 방법 3은 장면을 다른 것과 같이 로드합니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![3D 장면 로드 - 3D 장면 리소스](working-with-3d-scenes.resources/working-with-3d-scenes-03.gif "3D 장면 로드 - 3D 장면 리소스"){zoomable="yes"}

3D 장면 리소스 로드

</td>
<td style="border: 0;" valign="top">

![라이브러리에서 3D 장면 불러오기](working-with-3d-scenes.resources/working-with-3d-scenes-04.gif "라이브러리에서 3D 장면 불러오기"){zoomable="yes"}

라이브러리에서 3D 장면 불러오기

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![3D 장면 불러오기 - 3D 장면 파일에서 불러오기](working-with-3d-scenes.resources/working-with-3d-scenes-05.gif "3D 장면 불러오기 - 3D 장면 파일에서 불러오기"){zoomable="yes"}

3D 장면 파일 불러오기

</td>
<td style="border: 0;" valign="top">

![3D 장면 불러오기 - 장면 상태 파일에서](working-with-3d-scenes.resources/working-with-3d-scenes-06.gif "3D 장면 불러오기 - 장면 상태 파일에서"){zoomable="yes"}

장면 상태 파일 로드

</td>
</tr>
</table>

>[!NOTE]
>
> 3D 보기에서 장면 탐색 및 시각화는 [3D 보기 설명서](../interface/3d-view/3d-view.md)에서 다룹니다.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Designer에서는 장면에 있을 수 있는 환경 외에도 항상 자체 환경(USD의 DomeLight)과 카메라를 만듭니다.

Designer에서 만든 모든 항목은 장면 브라우저에서 <b>굵은 레이블</b>과 함께 나열됩니다.

>[!NOTE]
>
> 로드된 장면에 하나 이상의 환경(DomeLight)이 있는 경우 Designer에서 만든 환경은 *기본적으로 사용하지 않도록 설정*&#x200B;되므로 장면의 환경 조명을 방해하지 않습니다.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![장면 브라우저 - Designer에서 만든 요소](working-with-3d-scenes.resources/working-with-3d-scenes-07.png "장면 브라우저 - Designer에서 만든 요소"){zoomable="yes"}

</td>
</tr>
</table>

## 장면 상태 파일

3D 보기에서 재질, 카메라, 조명 등을 설정한 후 해당 상태를 나중에 로드하여 해당 상태를 복원할 수 있는 장면 상태 파일(.sbsscn)에 저장할 수 있습니다. 예를 들어 서로 다른 유형의 재질이나 특정 조명 환경을 미리 볼 수 있도록 몇 가지 장면을 설정할 수 있습니다.

![장면 상태 파일 불러오기](working-with-3d-scenes.resources/working-with-3d-scenes-08.gif "장면 상태 파일 불러오기"){zoomable="yes"}

저장된 장면 상태는 3D 보기의 기본 상태로 사용될 수도 있으므로, 새 3D 보기가 생성될 때마다 해당 상태가 사용됩니다. 이 기능은 타일링 값이 2이고 특정 환경 맵이 있는 구 2-타일 메시에서 기본적으로 재질을 미리 보려는 경우에 유용합니다.

장면 상태 파일과 관련된 작업은 3D 보기의 [장면] 메뉴에 있으며 [여기](../interface/3d-view/3d-view.md)에 문서화되어 있습니다.

장면 상태 파일은 XML 형식을 사용하며 [프로젝트 설정](../interface/preferences-window/project-settings/project-settings.md)에 정의된 경우 [별칭](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)을 사용합니다.

>[!NOTE]
>
> 렌더러는 장면 상태 파일에 저장되지 않습니다.
