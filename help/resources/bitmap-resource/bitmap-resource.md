---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/resources/bitmap-resource.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 텍스처 기반의 재질 제작을 위해 비트맵 리소스를 가져오고 만들고 사용하는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Resources > Bitmap resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 비트맵 리소스
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 2%

---


# 비트맵 리소스

비트맵 리소스는 Substance 패키지의 리소스입니다. [atomic bitmap 노드와 다릅니다. atomic Bitmap 노드](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)은(는) [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md) 내에 있는 해당 비트맵의 특정 표현입니다.

비트맵은 Substance 3D Designer에서 가장 일반적인 그래프가 아닌 리소스 중 일부이며 일반적으로 다음 범주 중 하나에 사용됩니다.

* [Designer에서 내부적으로 구워졌거나](../../bakers/bakers.md) 외부에서 다른 응용 프로그램에서 구워낸 베이킹된 맵.
* 패턴, 그런지 맵 또는 데칼과 같은 보조 텍스처입니다.
* [비트맵 노드](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)를 사용하여 내부적으로 만들거나 외부 앱과 함께 만드는 혼합을 위한 간단한 회색 음영 마스크입니다.

## 비트맵 스토리지

일반적으로 비트맵은 Designer에서 다루는 가장 큰 리소스입니다. 그렇기 때문에 Designer에서 두 개의 기본 파일 유형으로 이러한 파일을 처리하는 방법을 이해하면 좋습니다.

### Substance 3D 파일(SBS)

비트맵이 SBS에 저장되는 방법은 [연결할지 또는 가져오는지에 따라 다릅니다. 먼저 개념을 알고 있어야 합니다.](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) 가져온 비트맵은 [비트맵 페인팅 도구](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)를 사용하여 편집할 수 있습니다.

SVG(벡터 그래픽) 리소스와 달리 비트맵은 새 리소스로 만들어지거나 가져오는 경우에도 항상 외부에 저장됩니다. 새 Substance 패키지의 경우 .SBS 파일이 디스크에 저장될 때까지 메모리에 저장됩니다. 디스크에 저장되면 비트맵은 SBS 파일 옆의 */resources* 폴더에 저장됩니다.

### Substance 3D 에셋(SBSAR)

[SBSAR 파일](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)에는 비트맵이 포함되어 있어 최종 SBSAR 파일 크기에 많은 영향을 줍니다. 이 페이지에서 파일 크기에 미치는 영향에 대해 자세히 알아볼 수 있습니다. SBSAR 파일이 게시되면 그래프의 출력을 계산하는 데 사용되는 비트맵만 포함됩니다. 사용하지 않은 모든 비트맵은 최적화되어 파일 크기에 영향을 주지 않고 최종 SBSAR 패키지에서 제외됩니다.

## 파일 유형, 색상 모드 및 해상도

Substance 3D Designer에서는 비트맵의 데이터를 손쉽게 편집하고 다시 정렬할 수 있지만, 다음 사항에 유의하는 것이 좋습니다.

* 해상도를 2의 강력으로 설정하십시오. 즉, <b>256, 512, 1024, 2048,</b> 등과 같은 표준 실시간 텍스처 크기를 따르십시오. Designer은 이 범위를 벗어나는 텍스처의 크기를 가장 가까운 일치 해상도로 다시 조정합니다. 정사각형 비율일 필요는 없습니다.
* 지원되는 파일 유형은 다양하지만 용도에 가장 적합한 파일 유형을 선택하십시오. PNG 또는 TGA와 같은 <b>손실 없는 압축 또는 압축되지 않은 파일 유형</b>은(는) JPG 또는 DDS보다 더 좋은 품질을 제공합니다.
* 색상, 회색 음영 또는 알파 채널이 필요한지 여부에 따라 <b>색상 모드를 올바르게 설정</b>해야 합니다.

## 비트맵 속성

패키지의 비트맵 리소스에는 사용자 정의할 수 있는 여러 가지 속성이 있습니다. 대부분의 특성은 큰 목적이 없으며 라이브러리 필터에 사용되지만 파일 크기에 영향을 주는 소수 특성이 있습니다.

| 특성 이름 | 용도 |
| --- | --- |
| 식별자 | 패키지에서 비트맵 리소스를 참조하는 데 사용되어야 합니다. |
| 파일 경로 | 리소스가 참조하는 비트맵의 디스크 경로입니다. |
| 설명 | 이 리소스에 대한 [탐색기](../../interface/the-explorer-window/the-explorer-window.md) 및 [라이브러리](../../interface/the-library/the-library.md) 도구 설명에 표시된 설명입니다. |
| 카테고리 | [라이브러리](../../interface/the-library/the-library.md)에서 [리소스 정렬 및 큐레이션](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)에 사용됩니다. |
| 레이블 | [라이브러리](../../interface/the-library/the-library.md)에서 [리소스 정렬 및 큐레이션](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)에 사용됩니다. |
| 작성자 | [라이브러리](../../interface/the-library/the-library.md)에서 [리소스 정렬 및 큐레이션](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)에 사용됩니다. |
| 작성자 URL | [라이브러리](../../interface/the-library/the-library.md)에서 [리소스 정렬 및 큐레이션](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)에 사용됩니다. |
| 태그 | [라이브러리](../../interface/the-library/the-library.md)에서 [리소스 정렬 및 큐레이션](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)에 사용됩니다. |
| 사용자 데이터 | 비트맵에는 사용되지 않는 선택적 추가 데이터입니다. |
| 라이브러리에 표시 | [라이브러리 보기](../../interface/the-library/the-library.md)에서 비트맵을 숨길지 여부를 결정합니다. |
| 비트맵 형식 | Raw 또는 Jpeg는 SBSAR 파일 크기에 큰 영향을 줍니다. 자세한 내용은 [파일 크기 축소 지침](../../best-practices/filesize-reduction-gui/filesize-reduction-guidelines.md)을 참조하세요. |
| 비트맵 압축 품질 | Jpeg 압축에만 영향을 주고 품질/파일 크기 균형을 결정합니다. |

## 파일 크기 축소

[게시된 Substance 3D 에셋(SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)에 포함된 비트맵의 파일 크기 최소화와 관련된 권장 사항은 [모범 사례](../../best-practices/best-practices.md) 섹션의 [파일 크기 축소 지침](../../best-practices/filesize-reduction-gui/filesize-reduction-guidelines.md) 페이지를 참조하십시오.
