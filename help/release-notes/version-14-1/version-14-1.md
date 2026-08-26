---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-14-1.html"
breadcrumb-title: ''
description: 노드 배열 도구와 새로운 스플라인 및 패스 노드에 대해 알아보려면 Substance 3D Designer 버전 14.1의 릴리스 정보를 검토하십시오.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 14.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 버전 14.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 1%

---


# 버전 14.1

이 업데이트에서는 Substance 3D Designer을 일상적으로 사용할 수 있도록 그래프 레이아웃을 빠르게 개선하는 노드 배열 툴, 매개 변수 세트를 다른 노드에 적용하는 복사/붙여넣기 툴, 그래프를 디버깅하는 동안 특정 픽셀을 추적하는 2D 보기의 픽셀 핀 등 새로운 기능을 소개합니다. 또한 주로 스플라인 및 패스 노드 세트를 완성하기 위해 새 내용을 추가합니다.

*출시일: 2025년 1월 14일*

![스플라인에 스플라인 산란](../../assets/fond.png)

## 스플라인 및 패스 업데이트

스플라인과 패스 노드는 버전 13.0에 도입되었으며 여러분의 피드백 덕분에 초기 개선 사항을 적용했습니다. 먼저 부모 스플라인을 따라 스플라인을 분포하는 [스플라인에 산란 스플라인](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-splines-splines/scatter-splines-on-splines.md) 노드를 추가하여 일반 산란 노드와 유사한 옵션을 제공합니다. 또한 [패스에 마스크 적용](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 노드가 향상되어 패스에서 첫 번째 정점의 위치를 더 많이 제어할 수 있습니다. 또한 [스플라인 브리지 목록](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md) 노드에 임의성을 적용할 수 있습니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![스플라인 애니메이션의 산란 스플라인 1](../../assets/spline1.gif){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![스플라인의 산란 스플라인 2](../../assets/spline2.gif){zoomable="yes"}

</td>
</tr>
</table>

## 노드 정렬 도구

깔끔하고 읽기 쉬운 그래프를 유지하는 데 열중하면 [노드 정렬 도구](../../interface/the-graph-view/node-alignment-tools/node-alignment-tools.md)가 만들어졌으며 완전히 개선되었습니다! 이제 노드를 수평 또는 수직으로 균일하게 배치할 수 있으며 노드를 정렬하면 노드를 깔끔하게 쌓아 겹치는 부분을 방지할 수 있습니다. Cherry on top: 두 기능 모두 노드의 실제 크기를 고려합니다!

![노드 정렬](../../assets/alignment.gif){zoomable="yes"}

## 파라미터 복사/붙여넣기

이제 [한 노드의 매개 변수를 복사하여 다른 노드에 붙여넣을 수 있습니다](../../compositing-graphs/manage-parameters/manage-parameters.md). 따라서 대상 노드의 일치하는 모든 매개 변수는 원본 노드의 값으로 업데이트됩니다. 예를 들어, 색상 노드의 매개 변수를 회색 음영 버전으로 또는 그 반대로 이동하려는 경우 매우 유용합니다. (예: 타일 Sampler 노드)

## 2D 보기에서 픽셀에 핀 고정

2D 보기의 새로운 [색상 Sampler 도구](../../interface/2d-view/color-sampler/color-sampler.md)를 사용하면 선택한 픽셀에 핀을 놓아 해당 픽셀의 값을 추적할 수 있습니다. 이 기능은 그래프에서 여러 노드에 걸쳐 동일한 픽셀의 정보를 항상 보고 있는지 확인하는 데 매우 유용합니다. 정보 패널을 열어 도구에 액세스하고 사용해 보십시오!

![색상 샘플러: 도구 사용](../../assets/color-sampler-demo.gif "색상 샘플러: 도구 사용"){width="640px" zoomable="yes"}

## 검색 개선 사항

[노드 찾기 도구](../../interface/the-graph-view/node-finder/node-finder.md)가 약간 개선되었습니다.

* 이제 더 자세한 검색을 위해 재귀 모드를 활성화할 수 있습니다.
* 정확한 용어를 검색하려는 경우 퍼지 모드를 비활성화할 수 있습니다.
* Node Finder 툴을 활성화하면 검색 필드에 포커스가 자동으로 설정됩니다.
* 도구 모음의 레이아웃이 공간을 절약하도록 다시 고려되었습니다.

![검색 도구 모음](../../assets/search-53.png){width="640px"}

## 비디오

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[![스플라인의 비디오 산란 스플라인](../../assets/video_spline.png)](https://www.youtube.com/watch?v=aUUWV1dYQdI)

</td>
<td style="border: 0;" valign="top">

[![비디오 사용자 경험 기능](../../assets/video_ux.png)](https://www.youtube.com/watch?v=LwexybAEjaI)

</td>
</tr>
</table>

## 릴리스 정보

### 14.1.0

*(2025년 1월 14일 릴리스)*

### 추가됨

* [2D 보기] 정보 패널에 고정된 픽셀 디스플레이 추가
* [API] 그래프 뷰 장면에 노드 Box 크기를 표시합니다.
* [Content] &#39;재질 Height 혼합&#39;: &#39;Height 마스크&#39; 출력 추가
* [Content] &#39;Path Vertex Processor&#39;: &#39;정점별 함수&#39; 매개 변수에 &#39;함수 편집&#39; 단추 사용
* [콘텐츠] 자동 레벨: 사용하지 않는 매개 변수를 정리하고, 레이블 및 도구 설명을 조정합니다.
* [내용] 패스 v2에 마스크
* [내용] 새로운 최소 분산 노드 평균(MLV)
* [Content] 새로운 중간 필터 노드
* [콘텐츠] 색상 양화: &#39;가장 가까운&#39; 필터링 옵션 추가
* [Content] 스플라인 브리지 목록: 임의의 스플라인 오프셋 매개 변수 추가
* [Content] 자유 곡선 도구: 새 스플라인(2차) 노드
* [내용] Triangle Grid: 삼각 측량 방법을 변경하고 루프를 사용합니다.
* [Content] 스플라인 노드의 새 산란 스플라인
* [Cooker] &#39;Pixel ratio&#39; 기본 매개 변수를 &#39;$pixelratio&#39; 정적 변수로 노출합니다.
* [CrashReport] 새 충돌 보고서 창 통합
* [엔진] 혼합 엔진의 Vulkan/Metal 버전을 추가합니다.
* [그래프] 질감 모드: 단일 링크를 선택한 경우 사용 없이 입력 가능한 연결을 허용합니다.
* [그래프] 재질 링크: 연결이 모호하지 않은 경우 표준 연결을 허용합니다.
* [그래프] 노드 정렬 도구: 가로/세로 분포, 왼쪽/오른쪽/위쪽/아래쪽 정렬을 추가하고 누적 노드를 지원합니다.
* [라이브러리] 컨텍스트 메뉴에서 텍스트 색상 수정
* [매개 변수] 노드에서 다른 노드로 매개 변수를 복사합니다.
* [속성] &quot;모두 재설정&quot;: 확인 팝업 창을 제거합니다
* [리소스] &quot;비트맵 연결&quot; 대화 상자에서 형식을 &quot;모든 형식&quot;으로 설정합니다.
* [검색] 재귀 모드를 활성화/비활성화하는 방법을 추가합니다.
* [검색] 퍼지 검색을 활성화/비활성화하는 방법을 추가합니다.
* [검색] 키보드 단축키를 사용하여 Node Finder를 활성화할 때 항상 검색어 필드에 포커스를 표시하고 설정합니다.
* [Search] 필터 옵션 다시 작업
* [단축키] &#39;V&#39;, &#39;H&#39; 및 &#39;S&#39; 키 할당 허용
* [ThirdParty] Qt 6.5.7로 업그레이드
* [UX] 모달 대화 상자를 최소화할 수 없어야 합니다.
* [UX] 경고 대화 상자에서 가로 스크롤 제거

### 수정 사항

* [내용] 경사: 일반 포맷은 전역 환경 설정의 영향을 받지 않습니다.
* [내용] 색상-마스크 노드가 알파를 무시하지 않음
* [내용] 방향 거리: 입력에 수직 이미지 비율이 있는 경우 잘못된 결과입니다
* [Content] Flood Fill 매퍼: 변수가 없다는 경고가 발생했습니다.
* [내용] 히스토그램 계산: 결과는 필요한 것의 16배입니다.
* [내용] RT 빛 무늬 도구가 정사각형이 아닌 해상도에서 작동하지 않습니다.
* [Content] 스플라인 브리지 목록: 시작/끝 오프셋을 사용할 때 잘못된 결과가 발생합니다.
* [Content] 스플라인 선택: 출력 스플라인 양은 입력 스플라인 양보다 클 수 있습니다.
* [Content] 스플라인 뒤틀기를 수행하면 SSE 엔진이 있는 검정 결과가 생성됩니다.
* [내용] Triangle Grid: 패턴이 제대로 타일링되지 않습니다
* [내용] Triangle Grid: 특정 경우에 타일링이 손상됨
* [Data] 특정 경우에 그래프 입력 식별자를 변경할 때 충돌이 발생합니다
* [함수 그래프] 긴 값이 &#39;Float&#39; 노드에서 겹쳐서 나타납니다.
* [Fx-Map] 사분면 노드 속성을 표시할 때 충돌이 발생합니다.
* [그래프] [UDIM] UDIM 목록에 스크롤 막대가 있으면 1..1 1..2 항목이 생성됩니다.
* [그래프]&#x200B;[단축키] 단축키를 사용하여 생성된 노드는 노드 복제 후 기존 링크에 배치되지 않습니다.
* [Properties] 값이 유효하지 않은 경우 잘못된 매개 변수 표시가 나타납니다.
* [Publish] 패키지를 게시할 때 상호 종속성 때문에 무한 루프가 발생합니다.
* [Publish] 종속성이 언로드된 패키지에서 &#39;Publish&#39; 작업을 사용할 때 자동 오류 발생
* [UI] &#39;상위 크기&#39; 위젯이 확장되면 올바르게 표시되지 않으며 인터페이스를 차단할 수 있습니다(macOS만 해당)
* [UI] 경우에 따라 주 창이 다른 애플리케이션 뒤에 표시됩니다(Windows만 해당)
