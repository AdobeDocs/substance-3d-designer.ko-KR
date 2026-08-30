---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-12-1.html"
breadcrumb-title: ''
description: Substance 3D Designer 버전 12.1의 릴리스 노트를 검토하여 새로운 기능, 개선 사항 및 버그 수정에 대해 알아보십시오.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 12.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 버전 12.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1381'
ht-degree: 0%

---


# 버전 12.1

**Substance 3D Designer 12.1**&#x200B;은(는) Substance 자료 그래프, USD 파일 형식 지원을 위한 많은 새로운 노드를 제공하고 Stager와의 상호 운용성을 추가합니다.

출시일: *2022년 4월 26일*

## 주요 기능

### Substance 재질 그래프의 새로운 내용

![](version-12-1.resources/yellow-intense-reduce.png)

이 버전에는 많은 노드가 추가되어 몇 가지 새로운 패턴, 새로운 잡음, 새로운 필터 등을 찾을 수 있습니다...

아래의 링크된 노드 페이지를 살펴보고 이러한 강력한 새 노드가 제공하는 광범위한 출력의 예를 살펴보십시오.

* **새 패턴**

  * 무작위 크기 및 비율의 인접한 타일을 생성하기 위해 새로운 <b>타일 무작위 2</b> 노드를 추가했습니다. 이는 기울어짐, 둥근 모서리 및 베일링이 있는 완전히 불규칙한 격자를 빠르게 만드는 데 매우 유용합니다.

    ![](version-12-1.resources/tilerandom2-demo2.gif){width="640px"}
  * 삼각형으로 구성된 격자를 생성하기 위한 새로운 <b>Triangle Grid</b> 패턴입니다. 우리는 아래의 재질에 이를 사용하여 쉽고 완벽하게 가죽 그레인을 모사할 것입니다. 이 생성기는 3D 공간에서 정점들의 표면을 나타내며, 다양한 다각형 스타일들을 생성하는데 사용될 수 있다.

    ![](version-12-1.resources/trianglegrid-demo.png){width="640px"}
* **새 노이즈**

  * 더 다양한 기능을 제공하기 위해 <b>15개의 새 그런지 지도</b> 세트(콘크리트, 노출, 더러운 물방울 등) 이(가) 라이브러리에 추가되었습니다.

    ![](version-12-1.resources/grungemaps.png){width="640px"}
  * 보로노이(2D 및 3D), 보로노이 프랙탈(2D 및 3D), 3D 리지 프랙탈 및 현재 3D 펄린 노이즈 업데이트(타일링 및 절대 옵션 추가)와 같은 <b>새로운 2D 및 3D 노이즈</b>도 많이 찾습니다.\
    이러한 노이즈는 모두 3D 공간에서 매핑되며 다양한 스타일을 제공하여 다양성을 높이고 컨트롤을 제공하므로 바다와 아래의 SF 패널 자료와 같이 자료에 맞는 완벽한 맵을 만드는 데 많은 선택을 할 수 있습니다.

    ![](version-12-1.resources/fractal-voronoi-sea.gif){width="640px"}

    ![](version-12-1.resources/fractal-voronoi-scifi-panel.gif){width="640px"}
  * 3D 모델 조각의 아틀라스인 3D 텍스처를 만들고 렌더링하기 위한 <b>3D 텍스처 노드</b>(위치, SDF, 오프셋) 및 <b>3D 렌더링 노드 </b>(표면 또는 볼륨)의 컬렉션입니다.

    ![](version-12-1.resources/image2022-4-22-11-46-17.png){width="640px"}

* **새 필터**

  * <b>자동 자르기</b> 노드를 사용하면 크기를 조정하지 않고 이미지의 *중앙*&#x200B;에 모양을 배치하거나 공간에 맞게 크기를 조정할 수 있습니다. 예를 들어 흩어져 있을 때 일정한 위치와 크기를 유지하면서 모양을 자유롭게 변경할 수 있습니다.

    ![](version-12-1.resources/autocrop-demo-01-resized.gif){width="640px"}
  * <b> Extend Shape</b> 노드를 사용하면 사용자 지정 방향과 거리 위에 모양의 섹션을 늘릴 수 있습니다.

    ![](version-12-1.resources/extendshape.gif){width="640px"}
  * <b>균일 없는 회전</b> 노드를 사용하면 지정된 맵에 따라 입력을 회전할 수 있습니다.

    ![](version-12-1.resources/nonuniformrotation-demo-02-resized.gif){width="640px"}
* **또한...**

  * 비선형 방식으로 값을 제어하는 데 매우 유용한 이징 함수(함수 그래프).
  * 그리고 마지막으로 이 버전에서는 새로운 <b>Summded Area Table</b> 유틸리티 필터뿐만 아니라 <b>Quantize</b> 노드의 더 정확한 새 버전도 제공합니다.

### 상호 운용성 향상

* **USD 지원**&#x200B;외에

  및

  파일 형식, 이제 USD 파일을 가져오고 내보낼 수 있습니다(

  ,

  ,

  )를 사용하여 Substance 모델 그래프의 리소스로 사용하고 굽거나 3D 보기에서 Substance 자료를 표시할 수 있습니다. 이 형식을 사용하여 Substance 모델 그래프나 3D 뷰의 내용을 내보낼 수도 있습니다.
* <b>Stager로 보내기\
  </b>Sampler 및 Painter에서 이미 가능했으므로 이제 클릭 한 번으로 Substance 자료를 Stager로 보낼 수 있습니다. 이 기능 덕분에 더 이상 SBSAR로 게시하고 개별 파일을 로드할 필요가 없습니다(새로운 재질 관리자를 사용하는 Stager 버전 1.2.0 필요).

  ![](version-12-1.resources/sendtostagershort.gif)

### 기타

* 패브릭에서 작업하는 경우 이제 재료가 드레이프된 모양에서 렌더링되는 방식을 더 잘 볼 수 있도록 3D 보기에 전용 메쉬를 표시할 수 있습니다. 3D 보기 패널에서 <b>장면</b> 메뉴를 열고 <b>천</b> 옵션을 선택하여 이 모델을 표시합니다.

  ![](version-12-1.resources/fabric-rendering.png){width="640px"}

* 또한 Substance 모델 그래프에 대한 새로운 장면 관리 노드를 몇 개 추가했습니다. 이러한 노드를 사용하면 장면 계층 구조를 구성하기 위해 장면 요소의 이름을 바꾸거나, 부모로 다시 설정하거나, 융합하거나, 확장할 수 있습니다. 또한 장면의 하나 이상의 요소의 피벗을 설정할 수 있는 새로운 노드도 있습니다.

* Designer에서 프로젝트 작업을 하는 동안 프로젝트에 문제가 있다는 경고 및 오류 메시지가 표시될 수 있습니다. 이 버전에서는 탐색기의 모든 오류와 경고를 표시하기 위해 <b>오류 관리 시스템을 개선</b>합니다. 모든 항목이 한 곳에 나열되므로 프로젝트에 문제가 있는지 확인하는 것이 더 쉽습니다.

  ![](version-12-1.resources/warning-overview-explorer.png){width="640px"}

## 릴리스 정보

### 12.1.0

*(2022년 4월 19일 릴리스)*

<b>추가됨:</b>

* [기본] 질감 그래프의 새로운 내용
* [기본] Stager로 재질 보내기
* [기본] USD 파일 지원
* [기본] UI에서 오류 보고 개선
* [기본] 모델 그래프에 대한 장면 관리 노드
* [내용] 3D Perlin 노이즈에 더 많은 옵션을 추가합니다(타일링, 절대...).
* [Content] 새로운 3D Ridged 노이즈 프랙탈 노드
* [Content] 새로운 3D 텍스처 오프셋 노드
* [Content] 새로운 3D 텍스처 위치 노드
* [Content] 새로운 3D 텍스처 렌더링 표면 노드
* [Content] 새로운 3D 텍스처 렌더링 볼륨 노드
* [Content] 새로운 3D 텍스처 부호 거리 필드 노드
* [콘텐츠] 새로운 자동 자르기 노드
* [내용] 새로운 속도 조절 기능
* [Content] 새 Extend Shape 노드
* [내용] 새 그런지 맵
* [Content] 균일하지 않은 새로운 회전 노드
* [Content] 새로운 합산 영역 테이블 필터
* [콘텐츠] 새로운 타일 랜덤 2 생성기
* [Content] 새로운 Triangle Grid 패턴 생성기
* [내용] 새로운 버전의 회색 음영 노드 수치화
* [내용] 새로운 보로노이 및 보로노이 프랙탈 노이즈 (2D/3D)
* [Content] 임계값: &#39;Lower&#39; 및 &#39;Lower and equal&#39; 비교 모드 추가
* [Content][3D 보기] 배송된 리소스에 패브릭을 표시하기 위한 메시 핏을 추가합니다
* [Substance 모델] 새 그룹 인스턴스 확장 노드
* [Substance 모델] 새 Fuse 노드
* [Substance 모델] 새 노드 이름 바꾸기
* [Substance 모델] 새 부모 노드
* [Substance 모델] 새 피벗 설정 노드
* [Substance 모델] SDK 1.6.0으로 업데이트
* [서드파티] Qt(및 QtForPython)를 5.15.8로 업그레이드
* [ThirdParty] Python을 3.9.9로 업그레이드
* [ThirdParty] OpenSSL을 1.1.1m으로 업그레이드
* [UI] 잘못 클릭하면 노드 메뉴 동작이 개선됨
* [UI] 고정된 경우에도 동일한 탭에서 하위 그래프 열기
* [UI] 탐색기 패널의 제목 표시줄에서 [고정] 버튼 제거
* [UI] 여러 버전에서 시작 화면에 &quot;다시 표시하지 않음&quot; 옵션 저장
* [3D 보기] &quot;Axis&quot; 도우미가 활성화된 경우 뷰포트에 그리드 장치를 표시합니다.
* [자동화] Designer에서 sbsbaker 명령줄 도구 제공
* [색상 관리] Adobe ACE용 새로운 GPU 백엔드 구현
* [밥솥] 타임스탬프 없이 패키지를 요리할 수 있는 옵션을 추가합니다.
* [그래프] FxMap 그래프에 배지를 추가합니다
* [라이브러리] 이징 함수에 대한 새 필터 추가
* [Player] USD 지원
* [Properties] 비트맵 노드의 &quot;PKG Resource Path&quot; 매개 변수에 리소스가 없는 경우 경고 오류를 추가합니다
* [Substance 엔진] 8.4.1로 업그레이드
* [Yebis] 다음 버전에서 Yebis 포스트 효과가 제거됨을 사용자에게 경고합니다.
* [설명서] 새 [경고 및 오류] 페이지
* [문서] Substance 그래프의 상속을 설명하는 새 페이지
* [설명서] &#39;Iray&#39; 섹션 업데이트
* [설명서] &#39;MDL 그래프&#39; 섹션 업데이트

<b>고정:</b>

* [UI] 새 그래프 창에서 템플릿 도구 설명의 클리핑 문제
* [UI] macOS에서 다크 모드를 사용할 때 노드에서 흰색 텍스트를 읽기 어렵습니다.
* [UI] 일부 대화 상자의 레이아웃 문제
* [UI] 탐색기에서 Substance 함수 그래프를 만드는 동안 경고 메시지가 잘려서 표시됩니다.
* [UX] 새 열 때마다 색상 피커가 아래로 이동합니다.
* [UX] 그레이디언트 편집기 창이 생성될 때마다 위로 이동합니다
* [UX] 로드된 패키지에 대해 그래프 속성이 자동으로 표시되지 않습니다.
* [콘텐츠] Flood Fill 매퍼: 특정 경우 입력 선택이 잘못되었습니다.
* [Content] Flood Fill: 부울 매개 변수 버튼의 텍스트 도련
* [Content] 다중 각도와 일반 노드의 첫 번째 샘플 광각 매개 변수에 대한 범위가 잘못되었습니다.
* [Substance 모델] 노드의 속성이 레이블 대신 식별자를 표시합니다.
* [Substance 모델][3D 보기] 프로젝트를 다시 열 때 문제 새로 고침
* [Substance 모델][3Dview] 와이어프레임 미리보기 사용 시 새로 고침 문제
* [매개 변수] 특정 경우 연속으로 빠르게 그래프 입력을 삭제할 때 충돌이 발생합니다
* [Parameters] 참조 설명을 편집하는 동안 인스턴스 매개 변수를 재설정할 때 충돌이 발생합니다
* [비트맵] 그래프에 드롭된 비트맵 파일에 대해 UDIM 감지가 트리거되지 않습니다.
* [Graph] 패키지를 로드한 후 디스크에서 리소스를 수정할 때 비트맵/SVG 노드가 무효화되지 않습니다.
* [GraphRender] Substance 그래프 평가가 취소될 때 메모리 누수
* [Localization] &quot;이 리소스에 대한 모든 맵을 다시 굽기&quot; 문자열이 지역화되지 않은 상태로 나타납니다
* [MDL] 입력이 연결되지 않은 점 노드에 연결된 경우 노출된 매개변수가 0으로 초기화되었습니다.
* [환경 설정] 커서가 빈 공간에 있는 경우에도 도구 설명이 표시됩니다
* [속성] 색상 공간 값 변경을 실행 취소하면 특정 경우 대신 기본값이 설정됩니다
* [Text] 누락된 글꼴 리소스로 글꼴 전환을 실행 취소할 수 없습니다.
