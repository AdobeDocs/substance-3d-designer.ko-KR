---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/mdl-library.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 재질 정의 언어 라이브러리에 액세스하여 사용자 정의 재질을 만듭니다.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > MDL library
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MDL 라이브러리
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# MDL 라이브러리

이 페이지에는 Substance 3D Designer에 포함된 [MDL 그래프](../../mdl-graphs/mdl-graphs.md) 및 재질과 관련된 콘텐츠 라이브러리가 표시됩니다. 또한 [라이브러리](../../interface/the-library/the-library.md)에서 사용자 지정 콘텐츠를 설치하고 관리하는 방법에 대해서도 설명합니다.

## 라이브러리에서 MDL 콘텐츠

MDL 그래프에서 사용할 수 있는 노드는 [라이브러리](../../interface/the-library/the-library.md)의 <b>mdl</b> 섹션에서 사용할 수 있습니다. 노드들은 그들이 정의되는 MDL 모듈에 따라 필터들로 배열된다.\
모듈이 하위 폴더에 저장되면 이 계층은 라이브러리에서 *미러링*&#x200B;되어 *범주*(으)로 표시됩니다.

이 섹션에는 다음 소스의 컨텐츠가 포함됩니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 기본 제공 콘텐츠

Designer에는 MDL 그래프를 작성하기 위한 기본 구성 요소뿐만 아니라 사용할 준비가 된 전체 재질 정의가 포함된 MDL 모듈이 포함됩니다.

이 콘텐츠는 설치 디렉터리 `./resources/view3d/iray/` 아래의 이 위치에 저장됩니다.

### 사용자 정의 콘텐츠

기본 제공 콘텐츠 외에도 라이브러리에 *보유 중인* MDL 모듈을 추가할 수 있습니다.

실제로 [프로젝트 설정](../../interface/preferences-window/project-settings/project-settings.md)의 <b>MDL</b> 섹션에 나열된 디렉터리에서 찾은 모든 MDL 모듈이 프로젝트 파일 전체에서 이 섹션 *누적*&#x200B;에 추가됩니다.

### NVIDIA vMaterials

NVIDIA의 [vMaterials](https://developer.nvidia.com/vmaterials) 라이브러리가 설치되어 있는 경우 *자체 범주*&#x200B;의 라이브러리에 *자동으로 추가*&#x200B;됩니다.

</td>
<td style="border: 0;" valign="top">

![라이브러리의 MDL 리소스](../../assets/mdl-library.png "라이브러리의 MDL 리소스")

라이브러리, vMaterials 라이브러리, 사용자 정의 콘텐츠의 *&quot;mdl&quot; 섹션이 프레임됨*

</td>
</tr>
</table>

## 3D 보기에서 MDL 콘텐츠

라이브러리에서 사용 가능한 모든 MDL 모듈은 Ray 렌더러를 사용할 때 [3D 보기](../../interface/3d-view/3d-view.md)에서 사용할 수 있습니다.

<b>재질</b> 메뉴를 열고 *장면 재질 하위 메뉴*&#x200B;를 열어 사용 가능한 MDL 모듈을 찾아봅니다. 목록에는 다음이 포함됩니다.

* 기본 제공 콘텐츠
* 사용자 정의 콘텐츠
* NVIDIA [vMaterials](https://developer.nvidia.com/vmaterials)
* [MDL 그래프](../../mdl-graphs/mdl-graphs.md)를 로드했습니다.

![3D 보기에서 MDL 재질](../../assets/mdl-apply-in-3dview-material-list.png "3D 보기에서 MDL 재질")

*3D 보기의 MDL 재질*
