---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/resources/vector-graphics-svg-resource.html"
breadcrumb-title: ''
description: 절차 재질 제작을 위해 Substance 3D Designer에서 SVG 벡터 그래픽을 가져와 리소스로 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Resources > Vector graphics (SVG) resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 벡터 그래픽(SVG) 리소스
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9505c371dff25c5d32a409abf76b95655b499571
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 2%

---


# 벡터 그래픽(SVG) 리소스

Substance 3D Designer은 Scalable Vector 그래픽 형식을 통해 제한된 형식의 Vector 그래픽을 지원합니다. SVG 파일을 다양한 방법으로 리소스로 가져와 그래프의 리소스로 사용할 수 있습니다.

SVG 파일 [은(는) 원자성 SVG 노드를 통해 만들거나 편집할 수 있습니다.](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) 또한 [UV에서 SVG 베이커로](https://experienceleague.adobe.com/ko/docs/substance-3d/bakers/bakers-settings/convert-uv-to-svg)하여 만들 수 있습니다.

>[!NOTE]
>
> Adobe Illustrator(**.ai**) 파일은 현재 지원되지 *않습니다*.

## SVG 스토리지

SVG 스토리지는 링크되어 있는지 또는 가져왔는지에 따라 달라집니다. 가져온 SVG 파일이 SBS 파일에 포함되어 있으므로 [비트맵과 같은 외부 파일이 필요 없음](../../resources/bitmap-resource/bitmap-resource.md)이 요구되며, [벡터 편집 도구](../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md)를 사용하여 편집할 수 있습니다.

## SVG 속성

패키지의 SVG 리소스에는 사용자 정의할 수 있는 여러 가지 속성이 있습니다. 대부분의 특성은 큰 목적이 없고 라이브러리 필터에 사용되지만 렌더링 품질에 영향을 주는 특성이 약합니다.

| 특성 이름 | 용도 |
| --- | --- |
| 식별자 | 패키지의 SVG 리소스를 참조하는 데 사용되므로 고유해야 합니다. |
| 파일 경로 | 리소스에서 참조하는 SVG 파일의 디스크 경로입니다. |
| 설명 | 이 리소스에 대한 [탐색기](../../interface/the-explorer-window/the-explorer-window.md) 및 [라이브러리](../../interface/the-library/the-library.md) 도구 설명에 표시된 설명입니다. |
| 카테고리 | [라이브러리](../../interface/the-library/the-library.md)에서 [리소스 정렬 및 큐레이션](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)에 사용됩니다. |
| 레이블 | [라이브러리](../../interface/the-library/the-library.md)에서 [리소스 정렬 및 큐레이션](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)에 사용됩니다. |
| 작성자 | [라이브러리](../../interface/the-library/the-library.md)에서 [리소스 정렬 및 큐레이션](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)에 사용됩니다. |
| 작성자 URL | [라이브러리](../../interface/the-library/the-library.md)에서 [리소스 정렬 및 큐레이션](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)에 사용됩니다. |
| 태그 | [라이브러리](../../interface/the-library/the-library.md)에서 [리소스 정렬 및 큐레이션](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)에 사용됩니다. |
| 사용자 데이터 | 추가 데이터(선택 사항)이며 벡터 그래픽에는 사용되지 않습니다. |
| 라이브러리에 표시 | [SVG 보기](../../interface/the-library/the-library.md)에서 라이브러리 리소스를 숨길지 여부를 결정합니다. |
| 벡터 그래픽 품질 | 렌더링 품질에 영향을 줍니다. 범위는 선형적이지 않으며 최고 품질은 0.5이다. |

## SVG 작성

제한된 기능 세트만 지원되므로 작성 SVG의 기능이 제한됩니다.

일반적으로 다음과 같습니다.

* 단순한 기본 모양과 패스만 올바르게 그릴 수 있습니다.
* 획이 지원되지만 1픽셀 폭의 획이 생성되고 획 스타일링은 무시됩니다.
* 파선 스타일은 확실히 깨집니다.
* 텍스트를 렌더링할 패스/윤곽선으로 변환해야 합니다.
* [복합 경로](https://helpx.adobe.com/ie/illustrator/desktop/manage-objects/reshape-transform-objects/create-compound-paths.html)는 지원되지 않습니다.
* 그레이디언트와 같은 고급 기능은 지원되지 않습니다.
* CSS 속성의 스타일 요소는 지원되지 않습니다.

## 권장 내보내기 옵션

내보내기 옵션은 각 애플리케이션에 따라 약간 다릅니다.

### Adobe Illustrator

[Illustrator](https://www.adobe.com/kr/products/illustrator.html)에서는 다음 옵션에 유의할 경우 SVG 내보내기를 가장 많이 제어할 수 있습니다.

* <b>다른 이름으로 저장</b>만 사용하고 *다른 이름으로 내보내기* 사용!
* <b>SVG 프로필</b>은(는) 아주 작은 프로필은 기본적으로 올바른 설정으로 설정되지만 크게 중요하지 않습니다.
* 작업하려면 <b>글꼴</b>을 <b>윤곽선으로 변환</b>(으)로 설정해야 합니다.
* <b>CSS 속성</b>은(는) 스타일 요소로 설정하면 *안 됩니다*. 다른 모든 옵션은 작동합니다.
* <b>Illustrator 편집 기능 유지</b>; 선택 해제
* <b>Responsive</b> 선택 해제;
* 선이 제대로 작동하지 않습니다. <b>개체 > 패스 > 윤곽선</b>을 사용하여 선이 표시되도록 합니다.

오른쪽 이미지는 권장되는 내보내기 옵션을 보여 주는 이미지입니다. 전체 크기로 표시하려면 이 옵션을 클릭합니다.

>[!IMPORTANT]
>
> 대지는 생성된 SVG 파일의 결과에 영향을 줄 수 있습니다. 일부 Illustrator 파일 템플릿은 여러 개의 아트보드를 소개합니다.\
> 아트보드를 하나만 제대로 자르고 SVG으로 저장할 때 아트보드 창에서 선택하도록 합니다.

![Illustrator SVG 내보내기 옵션](vector-graphics-svg-resource.resources/svg-export-options-ai.jpg "Illustrator SVG 내보내기 옵션"){width="512px"}

### 잉크스케이프

Inkscape는 기본적으로 SVG으로 저장되지만 파일 형식에 대한 제어력이 떨어집니다. Inkscape 파일은 대부분 응용 프로그램에서 기본적으로 작동하지만 몇 가지 제한 사항이 있습니다.

* Substance 3D Designer에서 획은 너비가 1px만 표시됩니다. <b>패스 > 패스에 획</b>을 사용하여 작업합니다.
* 텍스트가 작동하지 않습니다. <b>패스 > 패스에 개체</b>를 사용하여 텍스트가 작동하도록 합니다.

### Adobe Photoshop

Photoshop에는 매우 제한된 SVG 내보내기 도구(<b>파일 > 내보내기 >내보내기 형식...</b>)이 있습니다. 현재 Substance 3D Designer에 대해 올바른 결과를 생성할 수 없습니다. 모양 및 패스 정보를 가져올 수 있지만 스타일은 항상 요소로 저장되므로 호환되지 않습니다.

이 기능은 간단한 흑백 모양 마스크에 사용할 수 있습니다. 여기서 해결 방법은 [Alpha 분할](../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-split/alpha-split.md)을 사용하여 SVG에서 Alpha을 추출하는 것입니다.

또는 Photoshop에서 내보낸 SVG을 [가져오기](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)할 수 있습니다. 이를 통해 [응용 프로그램 내에서 기본적으로 스타일 정보를 편집할 수 있습니다.](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)
