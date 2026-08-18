---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/best-practices/performance-optimization-guidelines.html"
breadcrumb-title: ''
description: 그래프 성능을 개선하고 처리 시간을 줄이기 위해 Substance 3D Designer에서 사용할 수 있는 성능 최적화 지침을 살펴보세요.
helpx_creative_field: ""
helpx_description: Designer > Best Practices > Performance optimization guidelines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 성능 최적화 지침
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1051'
ht-degree: 0%

---


# 성능 최적화 지침

## Substance 그래프

[Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)가 복잡할수록 이를 렌더링하는 데 필요한 처리 능력이 향상됩니다. <b>복잡성과 렌더링 속도 사이의 균형을 맞추기</b>해야 합니다.\
이는 게임과 같은 실시간 그래픽 애플리케이션에서 사용할 경우 *특히*&#x200B;중요합니다.

일반적으로 사용자 지정 매개 변수를 노출하는 노드는 런타임에 수정할 수 있습니다. <b>가능한 한 그래프 끝에 가깝게 배치해야 합니다</b>.

각 노드의 출력이 가능하면 항상 캐시되기 때문입니다. 따라서 그래프가 더 위로 변경될수록 노출된 매개 변수 중 하나가 수정될 때마다 더 많은 출력을 처리해야 합니다. 노출된 노드가 그래프의 끝에 가까우면 노드와 출력 노드 사이에 있는 몇 개의 노드만 다시 계산해야 합니다.

예를 들어 그래프의 시작 부분에서 균일한 색상을 변경하면 다음 노드가 모두 다시 계산됩니다. 출력 바로 앞에 있는 HSL 노드를 조정하면 이 노드만 다시 계산되어 그래프의 성능이 크게 향상됩니다.

다음 지침에 유의하십시오.

### 일반 성능 관련 설정

+++GPU 엔진이 CPU 엔진보다 훨씬 빠름
지원되지 않는 (통합) 그래픽 카드가 없는 경우 GPU Substance 엔진(핫키 F9로 변경)을 사용합니다.

+++

+++그래프의 부모 해상도 전환 속도가 느립니다
그래프, 캐시 및 모든 축소판을 다시 계산합니다. [내보내기 대화 상자의 <b>일괄 처리 </b>탭](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)을 사용하면 8192 해상도로 내보낼 때와 같이 광범위하고 불필요한 재계산을 방지할 수 있으므로 더 좋습니다.

+++

+++심각한 경우에는 메모리 캐시를 늘려야 합니다
응용 프로그램 [은(는) 이미지 캐시에 사용할 수 있는 RAM 용량을 제한](../../interface/preferences-window/preferences-window.md)하지만 주의해서 이 용량을 재정의하고 늘릴 수 있습니다.

+++

### 그래프 최적화

+++일반적으로 노드 해상도 및 상속에 주의하세요!
값이 높으면 성능에 심각한 영향을 주므로 해당 재질이 어떻게 사용될 것인지, 그리고 이와 관련된 데이터 크기를 줄일 수 있는지 여부를 고려하십시오.

[Substance 해상도(출력 크기)](../../compositing-graphs/output-size/output-size.md) 및 [노드 그래프의 상속](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)에 대해 자세히 알아보십시오.

+++

+++색상이 필요하지 않은 경우 회색 음영 사용
색상 작업은 회색 음영 작업보다 4배 더 오래 걸립니다. 또한 색상과 회색 음영 간의 문자 변환을 최소화합니다.

+++

+++16비트가 필요하지 않은 경우 8비트 사용
Substance 엔진 CPU 버전(SSE2) *은(는) 실제로 16비트 색상 또는 8비트 회색 음영을 지원하지 않습니다*. GPU 엔진은 8/16비트 및 회색조/색상의 4가지 조합을 모두 지원합니다. *현재 Unity 및 Unreal 엔진 플러그인에서는 CPU 엔진만 사용됩니다*.

+++

+++가능한 한 노드 출력 크기를 최소화합니다.
경우에 따라 일부 노드를 축소해도 최종 결과에는 영향을 주지 않지만 성능에는 영향을 줍니다. 예를 들어 문서와 같은 출력 크기로 설정된 균일한 색상 노드를 사용하는 것은 의미가 없습니다. [균일한 색상]은 [절대] [16px x 16px]로 설정되고 그 다음 노드는 [마스터 기준]으로 설정해야 합니다. 일반적으로 이 비법은 펄린 노이즈와 같은 저주파수 이미지에 적합합니다.

+++

+++16*16픽셀보다 작은 이미지는 사용하지 마십시오.
이렇게 하면 렌더링 성능이 느려집니다.

+++

+++혼합 노드를 사용할 때 필요하지 않으면 Alpha 혼합을 비활성화합니다


+++

+++흐림 효과 및 뒤틀기 는 프로세서 집약도가 가장 높은 노드입니다


+++

+++일부 노이즈 발생기는 그려지는 패턴의 양에 영향을 받습니다
예를 들어 [Tile Generator](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) 노드가 더 많은 패턴을 처리하는 속도가 느려집니다.

+++

+++일부 노이즈는 비율 계수의 영향을 받습니다
이 요인은 사실 더 많은 패턴을 그릴 것이다. 영향을 받는 노드에는 노이즈, 셀 패턴 등이 있습니다. 흰색 노이즈 패턴이 필요한 경우 비율 값이 매우 높은 노이즈를 사용하지 말고 [흰색 노이즈](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise/white-noise.md) 또는 [흰색 노이즈 빠른](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise-fast/white-noise-fast.md) 노드를 대신 사용하십시오.

+++

+++반대로 매우 빠른 소음 발생기도 있습니다
여기에는 [빠른 흰색 노이즈](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise-fast/white-noise-fast.md), [프랙탈 합산 기반](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-base/fractal-sum-base.md) 및 [비등방성 노이즈](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/anisotropic-noise/anisotropic-noise.md)가 포함됩니다.

+++

+++경우에 따라 대용량 이미지 샘플링 기능으로 주의하십시오.
함수는 [픽셀 프로세서](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)를 제외하고 CPU 엔진에서 실행됩니다. [값 프로세서](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) 또는 [FXmaps](../../function-graphs/fxmaps/fxmaps.md)에서 과도한 이미지 샘플링($pos 좌표 변경)을 많이 하는 경우 VRAM과 CPU RAM 간에 많은 변경이 발생하여 성능이 지연됩니다.

+++

### 모바일 사용에 대한 최적화

+++뒤틀기 및 FX-Maps는 사용하지 않는 것이 좋습니다
성능에는 많은 비용이 듭니다.

+++

+++흐림 효과 노드 사용 안 함
대신 다운스케일 변형을 사용합니다.

+++

+++회색 음영에서 가능한 한 많이 작업하기
그래프 끝의 색상 모드로 전환합니다.

+++

+++출력 간에 가능한 한 노드 공유


+++

### 포함 비트맵에 대한 크기 최적화

[비트맵](../../resources/bitmap-resource/bitmap-resource.md)의 [출력 크기](../../compositing-graphs/output-size/output-size.md)는 기본적으로 [&#39;절대&#39;](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)(으)로 설정되어 있습니다. 즉, 비트맵이 노드 체인을 통해 출력에 연결되면 최종 출력이 포함된 비트맵의 크기가 됩니다.\
비트맵 뒤에 삽입한 노드의 출력 크기는 입력 &#39;](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)에 대해 [&#39;(으)로 설정됩니다. 즉, 비트맵 크기도 노드에 고유하고 노드 체인에서 출력으로 이 크기를 전달합니다. 이 문제를 해결하려면 비트맵의 출력 크기를 [&#39;부모 항목&#39;](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)으로 설정하도록 비트맵의 다음 노드를 설정해야 합니다.

그래프가 동적 해상도로 설정된 경우 포함된 비트맵의 출력 크기를 부모를 기준으로 변경할 수 있습니다.\
이렇게 하면 마스터 그래프를 기반으로 비트맵 크기가 변경되므로 그래프가 비트맵에서 필요한 해상도보다 더 높은 해상도를 처리할 수 없게 됩니다.

>[!WARNING]
>
> [비트맵](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) 노드를 &quot;부모에 상대적으로&quot;로 설정하고 그래프를 Substance 3D 에셋(SBSAR)에 [게시](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html)하면 원본 크기 대신 **256x256**&#x200B;의 해상도로 비트맵이 저장됩니다. 대신 비트맵 노드의 [상속 메서드](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)&#39; [출력 크기](../../compositing-graphs/output-size/output-size.md)&#39;을(를) &#39;절대&#39;로 유지하고 비트맵 노드 바로 뒤에 &#39;부모 대비&#39;로 설정된 [변환 2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) 노드를 사용하는 것이 좋습니다.

![포함된 비트맵 최적화 1](../../assets/input-1.jpg "포함된 비트맵 최적화 1")

![포함된 비트맵 최적화 2](../../assets/relativetoparent.jpg "포함된 비트맵 최적화 2")

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

또한 SBSAR(Substance 3D 에셋) [게시](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html)의 크기를 최소화하려면 비트맵 리소스의 형식을 Jpeg로 설정하는 것이 좋습니다.

</td>
<td style="border: 0;" valign="top">

![포함된 비트맵 최적화 3](../../assets/format.jpg "포함된 비트맵 최적화 3")

</td>
</tr>
</table>
