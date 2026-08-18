---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/best-practices/filesize-reduction-guidelines.html"
breadcrumb-title: ''
description: 성능 및 스토리지 요구 사항을 최적화하기 위해 Substance 그래프 파일 크기를 줄이기 위한 지침을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Best Practices > Filesize Reduction Guidelines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 파일 크기 축소 지침
user-guide-description: ''
user-guide-title: ''
source-git-commit: 163ef15c862c56a1b59a4ccd47f4396c825be18f
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 1%

---


# 개요

경우에 따라 [Substance 3D 에셋(SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)의 총 파일 크기가 중요한 요소가 될 수 있습니다. 이 페이지에서는 파일 크기를 줄이려고 할 때 염두에 두어야 할 몇 가지 주요 영역 및 설정을 다룹니다.

파일 크기는 대부분 [포함된 비트맵](../../resources/bitmap-resource/bitmap-resource.md)에 의해 결정됩니다. 연결, 임베드 또는 베이킹되어 [Substance 3D Designer](https://www.adobe.com/kr/products/substance3d-designer.html) 파일(SBS)에 리소스로 추가된 파일입니다. 그래프에 사용되는 비트맵(예: 직접 또는 노드 체인을 통해 출력에 연결됨)만 Substance 3D 에셋에 게시됩니다. Substance 3D 파일에서는 모든 비트맵 리소스가 여전히 파일 외부에 저장되기 때문에 비트맵이 파일 크기에 영향을 주지 않습니다.

>[!IMPORTANT]
>
> 모든 [비트맵](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) 노드의 [출력 크기](../../compositing-graphs/output-size/output-size.md) 속성이 *절대* [상속 메서드](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)(으)로 설정되어 있는지 확인하십시오. 그렇지 않은 경우 참조된 [비트맵 리소스](../../resources/bitmap-resource/bitmap-resource.md)가 게시된 Substance 3D 에셋 파일의 기본 256\*256 해상도로 저장되므로 하나 이상의 출력의*&#x200B;품질에 영향을 줍니다*.

## 파일 크기 계수

[SBSAR](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html)의 총 파일 크기에 영향을 주는 몇 가지 다른 요소가 있습니다. 아래에 간단한 설명과 함께 나열됩니다.

+++해결 방법
분명히 큰 효과가 있다. Substance 파일이 큰 해상도에서 작동하도록 할 수도 있다는 점을 염두에 두고 가능한 가장 작은 해상도를 사용합니다. 표준 해상도 마스크 요령을 사용하여 더 작은 비트맵이 더 커 보이게 할 수 있습니다.

*찾음: 외부 소프트웨어 또는 Designer에서 비트맵 가져오기/다시 내보내기.*

+++

+++파일 색상 모드
내보내기 전에 이미지 편집기에서 설정하면 Raw 비트맵 형식을 사용할 때 색상 모드가 파일 크기에도 영향을 줍니다. 회색 음영 전용 비트맵은 RGB(A) 이미지보다 작습니다.

*찾음: 외부 소프트웨어 또는 [출력 노드](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)를 올바르게 설정하는 동안 Designer에서 비트맵 가져오기/다시 내보내기.*

+++

+++파일 포맷
이미지의 파일 형식은 차이를 만들지만 경우에 따라 무시해도 됩니다. Photoshop과 같은 프로그램을 사용하면 JPG 압축을 조금 더 제어할 수 있으며 때로는 괜찮은 중간 도로를 제공할 수 있습니다.

*찾음: 외부 소프트웨어 또는 Designer에서 비트맵 가져오기/다시 내보내기.*

+++

+++그래프의 사용량
비트맵 노드를 설정하면 그래프에서 회색 음영 모드 파일을 색상 비트맵으로 사용하여 Designer에서 파일을 압축하는 방식에도 영향을 줍니다. 이러한 설정을 정확하게 해야 합니다!

*다음 위치에서 찾음:[비트맵 노드 속성](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)*

+++

+++패키지의 비트맵 형식
리소스 속성에서 &quot;Raw&quot; 및 &quot;Jpeg&quot; 압축 중에서 선택할 수 있습니다. 이는 최종 결과에 상당한 영향을 미칠 수 있다.

*다음 위치에서 발견: 비트맵 리소스 [속성](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/parameters-ui-129368153.html), [탐색기 창.](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)*

+++

+++패키지의 비트맵 압축 품질
&quot;Jpeg&quot; 비트맵 형식을 사용하는 경우 아래 슬라이더가 품질과 파일 크기에 영향을 줄 수 있습니다. 이 슬라이더는 매우 예측 가능한 동작을 하지 않지만 1은 최고 품질의 JPG 압축에 해당하는 경향이 있고 0.5는 가장 작은 크기를 제공하는 경향이 있습니다.

*다음 위치에서 발견: 비트맵 리소스 [속성](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/parameters-ui-129368153.html), [탐색기 창.](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)*

+++

+++게시 시 압축 모드
SBSAR에 게시할 때 압축을 위해 &quot;자동&quot;, &quot;최고&quot; 및 &quot;없음&quot; 중에서 선택할 수 있으며, &quot;원시&quot; 비트맵 형식을 사용하는 경우 상당한 차이를 만들 수 있습니다. 또한 내보내기 속도에 많은 영향을 미칩니다. 일반적으로 품질 향상을 제공하지 않으므로 &quot;없음&quot;을 사용하지 않는 것이 좋습니다.

*SBSAR 패키지에 대한 최종 게시 설정에 있습니다.*

+++

## 파일 크기 비교

아래 표는 모든 설정이 서로 미치는 영향을 보여줍니다. 사용된 비트맵은 생성된 노이즈의 4096x4096 이미지로, Photoshop에서 24비트 TGA 또는 품질 8의 JPG으로 내보냅니다. 또한 TGA는 회색 음영 및 RGBA 모드로 내보내졌습니다.

그래프는 단일 출력에 연결된 단일 비트맵 노드를 배치합니다. 비트맵 모드는 소스 파일 모드에 따라 설정됩니다.

오른쪽 표가 완전히 결정적인 것은 아니지만 시각적 결과와 파일 크기를 비교할 때 다음과 같은 사항을 알 수 있습니다.

* [Raw 비트맵 + 압축]은 적절한 파일 크기로 최상의 품질을 제공합니다.
* 미리 압축된 소스 파일을 사용하면 대부분의 경우 파일 크기를 줄일 수 있지만 파일 크기는 고품질 비용으로 줄일 수 있습니다.
* 파일 크기가 가장 작지만 JPG 패키지 포맷의 품질이 0.5로 가장 나쁩니다.
* 회색 음영 모델은 파일 크기가 항상 작은 것은 아니지만 유사한 설정에서 색상보다 높은 품질을 갖습니다.

>[!NOTE]
>
> **Jpeg 비트맵 형식**
> 
> [표준] 맵, [벡터 맵] 등과 같이 높은 정확도가 필요한 특수 맵은 표시 가능한 가공물이 많아지므로 Jpeg 압축으로 설정하면 안 됩니다.

| 소스 이미지 | 색상 TGA | 색상 JPG | 회색 음영 TGA | 회색 음영 JPG |
| --- | --- | --- | --- | --- |
| <b>원시 비트맵 형식</b> 압축 모드: *없음* | 48MB | 48MB | 16MB | 16MB |
| <b>원시 비트맵 형식</b> 압축 모드: *최고* | 9.11MB | 3.37MB | 5.06MB | 4.75MB |
| <b>Jpeg 비트맵 형식</b> 압축 품질: *1* | 5.09MB | 1.94MB | 6.30MB | 2.49MB |
| <b>Jpeg 비트맵 형식</b> 압축 품질: *0.5* | 231KB | 230KB | 626KB | 569KB |
| <b>Jpeg 비트맵 형식</b> 압축 품질: *0* | 407KB | 433KB | 990KB | 808KB |
