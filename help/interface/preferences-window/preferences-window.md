---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/preferences-window.html"
breadcrumb-title: ''
description: Substance 3D Designer의 환경 설정 창에 액세스하여 애플리케이션 설정 및 비헤이비어를 사용자 정의합니다.
helpx_creative_field: ""
helpx_description: Designer > Interface > Preferences
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 환경 설정
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1973'
ht-degree: 1%

---


# 환경 설정 창

![환경 설정 창](preferences-window.resources/image2021-6-22-20-56-1.png "환경 설정 창")

이 페이지에는 <b>환경 설정</b> 창과 모든 설정이 표시됩니다.

기본 설정 창은 응용 프로그램의 기본 상단 표시줄에 있는 <b>편집</b> 메뉴를 통해 찾을 수 있습니다. 이 대화 상자에서는 여러 가지 설정을 조정할 수 있습니다. 다양한 비헤이비어 및 기능 영역을 다루는 탭으로 구성됩니다.\
애플리케이션의 작동 원리와 워크플로우에 맞게 조정할 수 있는 방법을 더 잘 살펴보려면 이러한 설정을 모두 검토하는 것이 좋습니다.

>[!NOTE]
>
> 이러한 환경 설정을 저장하는 방법 및 이러한 환경 설정을 프로덕션 환경에 통합하는 방법에 대한 자세한 내용은 설명서의 [사용자 환경 설정 - 설정 자동화](../../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md) 페이지를 참조하십시오.

## 일반

### 최근 문서

|  |                                                                                                                                         |
| --- |-----------------------------------------------------------------------------------------------------------------------------------------|
| <b>최근 문서 목록에는 </b>이(가) 포함되어 있습니다.  *기본값: 10* | 그러면 [기본 메뉴](../the-main-toolbar/the-main-toolbar.md)에서 <b>파일</b> 항목의 <b>최근 패키지</b> 항목에 나열할 문서 수를 선택할 수 있습니다. |

### 내역

|  |  |
| --- | --- |
| **작업 내역 스택 크기** *기본값: 200* | 이는 [기본 메뉴](../the-main-toolbar/the-main-toolbar.md)의 <b>편집 > 실행 취소</b> 항목에서 주어진 시간에 사용 가능한 실행 취소 작업 수를 나타냅니다.  **주의:** 실행 취소 작업이 많을수록 응용 프로그램에 더 많은 메모리가 필요합니다. |

### 언어

|  |  |
| --- | --- |
| **응용 프로그램 언어 선택** *기본값: 시스템* | 이 설정은 응용 프로그램 인터페이스에 사용되는 언어를 정의합니다. &#39;*시스템*&#39; 옵션은 시스템 언어 설정에서 언어를 자동으로 검색합니다. 사용 가능한 언어는 [시스템 요구 사항](../../getting-started/system-requirements/system-requirements.md)에 나열되어 있습니다.  **참고:** 이 설정을 변경하면 응용 프로그램을 다시 시작한 후에만 적용됩니다. |

### 보기

|  |  |
| --- | --- |
| <b>확대 보기 반전</b>  *기본값: 선택 취소됨* | 선택하면 확대/축소 컨트롤이 [2D 보기](../../interface/2d-view/2d-view.md), [3D 보기](../../interface/3d-view/3d-view.md) 및 [그래프](../../interface/the-graph-view/the-graph-view.md)에서 반전됩니다. |

### 경로

|  |  |
| --- | --- |
| <b>경로 저장/내보내기</b>  *기본값: 마지막 경로* | 제안된 저장/내보내기 경로가 마지막으로 선택한 경로인지 [SBS 패키지](../../getting-started/overview/overview.md)의 경로인지 확인합니다. 마지막으로 선택한 경로는 세션 전체에 저장됩니다. |
| <b>임시 폴더</b>  *기본값: 시스템 OS에 따른 경로* | 그래프의 이미지 데이터가 할당된 메모리 풀(<b>메모리 > 이미지 캐시</b> 아래 참조)을 초과하면 오버플로된 데이터가 디스크에 기록됩니다. 이 설정을 사용하면 오버플로된 이미지 캐시 데이터가 기록되는 위치를 정의할 수 있습니다.   이 위치는 마지막 수동 저장 이후 최신 수정 사항이 있는 현재 열려 있는 SBS 패키지의 복사본을 저장하는 데에도 사용됩니다. |

### 메모리

#### 이미지 캐시

응용 프로그램은 현재 그래프에서 렌더링된 각 노드에 대해 *전체 해상도, 압축되지 않은 이미지*&#x200B;를 캐시에 유지합니다.\
인스턴스 노드는 참조하는 그래프의 모든 노드에 대해 이러한 이미지를 생성하고 [출력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)이 계산되면 삭제합니다. 출력만 해당 시점에 메모리에 저장됩니다.

시스템 메모리의 축소판 및 이미지에 할당된 최대 캐시 크기를 설정하고 현재 사용량을 확인할 수 있습니다. 캐시 데이터가 할당된 풀을 오버플로하면 초과 데이터가 <b>임시 폴더</b>에 기록됩니다(<b>경로 > 임시 폴더</b> 위 참조).

|  |  |
| --- | --- |
| <b>메모리 예산</b>  *기본값: 자동* | 이 할당은 전체 시스템 메모리 풀의 약 75%에 자동으로 계산됩니다. 이 값을 수동으로 설정하려면 &#39;*사용자 지정*&#39; 옵션을 선택하고 인접한 입력 필드에 값을 설정합니다. |

디스크에 쓰는 것은 시스템 메모리에 쓰는 것보다 *크기가 느린*&#x200B;입니다. 따라서 넘치는 데이터를 임시 폴더에 기록해야 하므로 그래프 렌더링 시간이 *기하급수적으로 증가*&#x200B;합니다.\
이러한 문제가 발생하지 않도록 하려면 설명서의 [성능 최적화 지침](../../best-practices/performance-optimization/performance-optimization-guidelines.md) 섹션에서 그래프의 메모리 사용량을 줄이는 방법을 살펴보는 것이 좋습니다.

#### 작업 스케줄러

축소판 또는 [2D 보기](../../interface/2d-view/2d-view.md)에 대한 이미지 변환과 같은 특정 작업 중에 효율성을 위해 별도의 작업이 만들어지고 시스템 처리 코어 전체에 배포됩니다. 각 작업은 작업을 수행하기 위해 데이터를 시스템 메모리에 기록합니다.\
이 설정을 사용하면 *모든 동시 작업*&#x200B;에 대해 할당된 메모리 풀을 정의할 수 있습니다. 이 풀을 완전히 사용하면 현재 작업이 완료될 때까지 새 작업이 대기됩니다.

|  |  |
| --- | --- |
| <b>메모리 예산</b>  *기본값: 자동* | 이 할당은 전체 시스템 메모리 풀의 약 10%에 자동으로 계산됩니다. 이 값을 수동으로 설정하려면 &#39;*사용자 지정*&#39; 옵션을 선택하고 인접한 입력 필드에 값을 설정합니다. |

### 사용자 인터페이스

|  |  |
| --- | --- |
| **높은 DPI 사용 안 함** *기본값: 선택 취소됨* | <b>높은 DPI</b> 모드에서는 시스템의 디스플레이 및 크기 조정 설정에 따라 텍스트 및 사용자 인터페이스 요소의 크기가 *독립적으로* 일관되게 유지됩니다.   이 설정을 사용하지 않도록 설정(예: 확인란 *채움*)하면 인터페이스 크기를 조정할 수 있습니다. 이로 인해 일부 디스플레이에서 텍스트가 더 커지고 가독성이 높아지지만 다른 레이아웃 문제와 함께 텍스트 크기가 불일치할 수도 있습니다.  **주의:** Designer은 OS *에서*&#x200B;의 특정 규모의 사용자 인터페이스 요소를 획득합니다. 따라서 사용자 인터페이스의 비율 조정은 OS의 디스플레이 설정에서 수행해야 합니다. Designer에서 디스플레이 설정이 올바르게 적용되도록 하려면 OS 사용자 세션의 *로그아웃*&#x200B;을 하고 이 설정을 변경한 후 다시 로그인하십시오.  **참고:** 이 설정을 변경하면 응용 프로그램을 다시 시작한 후에만 적용됩니다. |

### 자동 백업

자동 저장 기능은 기본적으로 포함되며, 이 기능은 설정된 시간에 열려 있는 [SBS 패키지](https://docs.substance3d.com/display/DRAFTDESIGNER/.Overview+vDraftVersion)의 현재 상태 복사본을 만듭니다. 자동 저장은 SBS 패키지 위치의 <b>.autosave</b> 폴더에 저장됩니다.

|  |  |
| --- | --- |
| <b>매 #분마다 자동 백업</b>  *기본값: 5* | 각 자동 저장 사이의 기간입니다. |
| <b>최신 버전 수</b>  *기본값: 6* | 지정된 시간에 보관할 최대 자동 저장 수입니다. |

최대 버전 수에 도달하면 최신 백업에서 가장 오래된 백업이 삭제됩니다.\
자동 저장은 원래 SBS 패키지 위치로 이동한 후&#x200B;*연 후*&#x200B;해야 합니다. 현재 위치에서 *열지 않아야* 합니다.

### SBSAR 파일 게시 및 보내기

|  |  |
| --- | --- |
| <b>.sbsar에 게시하거나 다른 응용 프로그램으로 보낼 때 항상 .sbs 파일 저장</b>  *기본값: True* | [게시](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)하거나 다른 응용 프로그램으로 보낼 때 SBS 패키지의 자동 저장을 제어합니다. |

### 쿠커

|  |                                                                                                                                                                                                                                                                                                 |
| --- |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>조리 크기 제한</b>  *기본값: 8192픽셀* | 모든 Substance [그래프](../../compositing-graphs/substance-compositing-graphs.md)에서 모든 노드에 허용되는 최대 픽셀 해상도를 정의합니다. 그래프 출력은 항상 2제곱의 제곱 이미지이므로 여기에서 설정된 값은 최대 폭과 Height을 픽셀 단위로 정의합니다. |

### 엔진

|  |  |
| --- | --- |
| <b>GPU 캐시 제한</b>  *기본값: 2048MB* | 이 설정을 사용하면 렌더링 단계를 캐시하기 위해 예약해야 하는 메모리 양을 정의할 수 있습니다. 일반적으로 Substance 엔진은 Substance 그래프에서 각 노드의 출력을 캐싱합니다. |

>[!NOTE]
>
> 설명서의 [성능 최적화 지침](../../best-practices/performance-optimization/performance-optimization-guidelines.md) 섹션에서 그래프의 메모리 점유율을 줄이기 위한 제안 사항을 살펴보는 것이 좋습니다.

## 프로젝트

[프로젝트 설정](../../interface/preferences-window/project-settings/project-settings.md) 페이지를 참조하십시오.

## 그래프

### 일반

|  |  |
| --- | --- |
| <b>Tab 키가 노드 메뉴를 표시합니다</b>  *기본값: 선택됨* | 선택하면 &#39;Tab&#39; 키가 <b>노드 메뉴</b>를 열고 &#39;Space&#39; 키의 기능을 복제합니다. |
| <b>커넥터를 클릭하여 노드를 만들 수 있도록 설정</b>  *기본값: 선택됨* | 선택한 경우 커넥터를 클릭하면 커서를 드래그하고 그래프 빈 공간에 만든 링크를 놓아 <b>노드 메뉴</b>를 표시합니다.   클릭한 커넥터의 유형에 따라 메뉴도 *필터링*&#x200B;됩니다. 즉, 클릭한 커넥터와 호환되는 노드만 표시됩니다. |
| <b>그래프를 열 때 3D 보기에서 출력 보기</b>  *기본값: 선택됨* | 선택하면 모든 그래프 출력이 해당 그래프를 열 때 [3D 보기](../../interface/3d-view/3d-view.md)에 자동으로 적용됩니다.   또한 스트림의 일부인 모든 노드를 [출력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 노드로 렌더링하는 효과가 있습니다. |

### Substance 합성 그래프

|  |  |
| --- | --- |
| <b>그래프를 열 때 모든 노드 축소판 자동 계산</b>  *기본값: 선택됨* | 선택하면 그래프를 로드할 때 모든 노드 축소판을 자동으로 렌더링합니다. |
| <b>그래프를 열 때 2D 보기에서 출력 보기</b>  *기본값: 선택됨* | 선택하면 [2D 보기](../../interface/2d-view/2d-view.md)에서 첫 번째 그래프 출력이 자동으로 표시됩니다. 또한 스트림의 일부인 모든 노드를 해당 [출력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 노드로 렌더링하는 효과가 있습니다. |
| <b>새로 만든 합성 노드를 자동으로 표시</b>  *기본값: 선택됨* | 선택하면 [2D 보기](../../interface/2d-view/2d-view.md)가 자동으로 업데이트되어 새로 만든 노드의 출력을 표시합니다. |
| <b>색상/회색조 변환 노드 자동 삽입</b>  *기본값: 선택 취소됨* | 선택하면 *특정 노드를 배치*&#x200B;하여 적절한 변환을 수행하여 색상/회색 음영 연결 유형의 불일치를 자동으로 해결합니다.   *회색 음영* 출력(회색 커넥터)이 *색상* 입력(노란색 커넥터)에 연결되면 [그레이디언트 맵](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md) 노드가 두 커넥터 사이에 자동으로 배치됩니다.   *색상* 출력(노란색 커넥터)이 *회색 음영* 입력(회색 커넥터)에 연결되면 [회색 음영 전환](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/grayscale-conversion/grayscale-conversion.md) 노드가 두 커넥터 사이에 자동으로 배치됩니다. |
| <b>컨텍스트에서 그래프 편집 사용</b>  *기본값: 선택 취소됨* | 기본적으로 노드를 마우스 오른쪽 단추로 클릭하여 [인스턴스 노드](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)에서 참조하는 그래프를 열고 <b>참조 열기</b>를 선택하면 해당 그래프가 *격리된 상태로* 로드되고 편집됩니다.   이 옵션을 선택하면 현재 그래프에서 인스턴스 *에 전달된 정보를 사용하여 인스턴스*&#x200B;에서 참조하는 그래프를 편집할 수 있습니다. 이렇게 하려면 인스턴스 노드를 마우스 오른쪽 단추로 클릭하고 <b>컨텍스트에서 참조 열기</b>를 선택하거나 Ctrl+E 키 입력을 사용합니다.   즉, 인스턴스 그래프는 인스턴스 그래프의 컨텍스트에서 편집할 수 있습니다. 이 기능은 작업 중인 그래프에서 편집 내용을 확인하는 데 매우 유용합니다. 아래의 예를 참조하십시오.  **참고:** 컨텍스트 편집을 사용할 때 [그래프 속성](../../compositing-graphs/graph-parameters/graph-parameters.md)에서 <b>미리 보기</b> 및 <b>사전 설정</b> 탭이 *비활성화*&#x200B;됩니다. |

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![직접 편집 사용 안 함](preferences-window.resources/substance3ddesigner_incontext_no.gif "직접 편집 사용 안 함")

*참조 열기*

</td>
<td style="border: 0;" valign="top">

![직접 편집 사용](preferences-window.resources/substance3ddesigner_incontext_yes.gif "직접 편집 사용")

*컨텍스트에서 참조 열기*

</td>
</tr>
</table>

## 3D 보기

### 기타

|  |  |
| --- | --- |
| <b>기본적으로 숨겨진 환경</b>  *기본값: 선택됨* | [환경](../../interface/3d-view/3d-view.md) 기본 표시 여부 설정을 결정합니다. 숨겨지면 3D 보기의 배경이 *단색*&#x200B;으로 바뀝니다. |
| <b>뷰포트 크기 조절</b>  *기본값: 자동* | 시스템에서 디스플레이 비율을 사용할 때 3D 뷰의 렌더링 해상도 비율을 제어합니다.<ul data-preserve-html="true"> <li data-preserve-html="true"><i>자동</i>: 렌더링 해상도는 <i>크기 조정</i> 디스플레이 해상도를 기반으로 합니다.</li> <li data-preserve-html="true"><i>없음</i>: 렌더링 해상도는 <i>네이티브</i> 디스플레이 해상도를 기반으로 합니다.</li> </ul> |

### OpenGL

|  |  |
| --- | --- |
| <b>샘플 수</b>  *기본값: 64* | 3D 뷰 셰이더의 샘플 테이블 크기에 영향을 줍니다. 값이 높을수록 성능이 저하되는 대신 이미지 품질이 향상됩니다.  **참고:** 셰이더 샘플 테이블은 시스템의 GPU 및 OS의 영향을 받기도 합니다. |

## 베이커

|  |  |
| --- | --- |
| <b>GPU 광선 추적</b>  *기본값: 선택됨* | 선택하면 [호환 베이커](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing)에 대해 GPU에서 광선 추적이 수행됩니다.   다음 GPU 광선 추적 백엔드가 NVIDIA GPU 아키텍처에 따라 기본값이 됩니다.<ul data-preserve-html="true"> <li data-preserve-html="true"><i>DXR</i>: 튜링 이상</li> <li data-preserve-html="true"><i>옵션</i>: Pascal 및 Maxwell</li> </ul>  **참고:** GPU 기반 베이커에 대한 자세한 내용은 [Substance 베이커](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/home) 설명서의 [GPU 광선 추적](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing) 섹션에서 확인할 수 있습니다.  **팁:** 응용 프로그램을 시작할 때 다음 *명령줄 인수*&#x200B;를 사용하여 다른 GPU 광선 추적 백엔드를 *강제*&#x200B;할 수 있습니다. <ul data-preserve-html="true"> <li data-preserve-html="true"><code>—force-optix</code> : Nvidia 튜링 또는 이후 GPU에서 Optix 강제 사용</li> <li data-preserve-html="true"><code>—force-dxr</code> : Nvidia Pascal GPU의 DXR 강제 사용</li> </ul> |

## 라이브러리

|  |  |
| --- | --- |
| <b>축소판 다시 작성</b> | 이 옵션을 선택하면 모든 [라이브러리](../../interface/the-library/the-library.md) 축소판의 재계산이 트리거되어 이전 축소판을 자동으로 대체합니다. |

## 단축키

그래프에서 노드를 만들기 위한 사용자 정의 키보드 단축키를 할당할 수 있습니다.

모든 그래프 유형의 노드에 대해 단축키를 할당할 수 있습니다. [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md), [Substance 함수 그래프](../../function-graphs/function-graphs.md) 및 [FX-맵 그래프](../../function-graphs/fxmaps/fxmaps.md).

모든 노드에는 단축키(사용자 정의 라이브러리 노드 포함)를 할당할 수 있습니다. 동일한 단축키를 다른 그래프 유형에 할당할 수 있습니다. 기본적으로 할당된 단축키가 없습니다. 원하는 대로 언제든지 단축키를 사용자 정의할 수 있습니다.

다른 노드 바로 가기 또는 기본 제공 프로그램 바로 가기와 충돌하는 경우 항목이 강조 표시되고 경고가 표시됩니다. 충돌이 해결될 때까지 바로 가기에는 *효과가 없습니다*.

>[!IMPORTANT]
>
> Python 플러그인이 재정의한 단축키
> 
> Python 플러그인이 노드에 할당된 키보드 단축키를 정의하면 플러그인이 해당 단축키를 재정의합니다. 즉, 키는 노드를 만드는 대신 플러그인 작업을 트리거합니다.
> 
> [노드 정렬 도구](../../interface/the-graph-view/node-alignment-tools/node-alignment-tools.md)에서 사용하는 H, S 및 V 키에 이미 해당됩니다.
