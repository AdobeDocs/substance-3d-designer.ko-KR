---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-11-2.html"
breadcrumb-title: ''
description: Substance 3D Designer 버전 11.2의 릴리스 노트를 검토하여 새로운 기능, 개선 사항 및 버그 수정에 대해 알아보십시오.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 11.2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 버전 11.2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '974'
ht-degree: 0%

---


# 버전 11.2

**Substance 3D Designer 11.2**&#x200B;의 이름이 약간 변경되어 이제 Adobe Creative Cloud에 연결되었습니다. Substance 모델 그래프의 첫 번째 릴리스, 보내기 기능, 광선 추적 기반 노드 수 및 일부 UI 변경 사항을 제공합니다.

출시일: *23 2021년 6월*

## 주요 기능

### 새 Substance 모델 그래프

완전히 새로운 그래프 유형인 Substance 모델 그래프를 사용하면 익숙한 노드 인터페이스를 사용하여 프로시저 3D 모델을 만들 수 있습니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](version-11-2.resources/structure-tower-render-b.jpg){width="300px"}

</td>
<td style="border: 0;" valign="top">

![](version-11-2.resources/structure-paper-creatures-render-a.jpg){width="300px"}

</td>
</tr>
</table>

자세한 내용은 새로운 전용 문서 섹션을 살펴보십시오.

첫 번째 릴리스이므로 몇 가지 제한 사항이 예상됩니다.

### 보내기 기능

Substance 3D Designer의 Adobe 버전에는 새로운 보내기 기능이 있어 에셋을 다른 Substance 3D 애플리케이션으로 빠르게 보낼 수 있습니다. 더 이상 SBSAR로 게시하고 개별 파일을 로드할 필요가 없습니다. 보내기 를 사용하면 한 번의 클릭으로 이 문제를 해결할 수 있습니다.

![](version-11-2.resources/sendto-button.gif)

>[!NOTE]
>
> Substance 3D Designer의 Steam 버전에는 보내기 기능이 포함되어 있지 않습니다.

### 새 광선 추적 노드

일부 새 노드가 없으면 Designer 릴리스가 완료되지 않습니다. PBR 렌더링의 경이로운 강점을 바탕으로 만들어진 5개의 새로운 RT 기반 노드가 이번 릴리스에서 새롭게 합류했습니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](version-11-2.resources/image2021-6-18-11-11-11.png){width="300px"}

</td>
<td style="border: 0;" valign="top">

![](version-11-2.resources/image2021-6-18-11-9-0.png){width="300px"}

</td>
</tr>
</table>

RTAO는 이전 HBAO 노드보다 선명하고 정확한 AO를 훨씬 더 잘 수행합니다.

![](version-11-2.resources/rt-caustics-grayscale.png){width="300px"}

[빛 무늬]는 단순한 [펄린 노이즈]와 같은 높이 맵을 기반으로 물리적으로 올바른 광선 추적형 빛 무늬 효과를 생성합니다. 실시간 빛 무늬 효과를 위한 사실적인 애니메이션 플립북 텍스처를 만드는 데 적합합니다.

![](version-11-2.resources/image2021-6-22-16-36-36.png){width="300px"}

[RT 그림자]는 광선 추적형 정확하고 어두운 영역을 몇 가지 간단한 컨트롤로 표현합니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](version-11-2.resources/rt-irr-01.jpg){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](version-11-2.resources/rt-irr-03.jpg){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](version-11-2.resources/rt-irr-02.jpg){width="200px"}

</td>
</tr>
</table>

RT Radiance는 새로운 노드 중 가장 진보된 것입니다. 높이 맵과 환경 맵 및/또는 방출 맵이 있는 재료를 기반으로 광선 추적형 조도를 수행합니다.

![](version-11-2.resources/rt-irrad-pro.jpg){width="600px"}

이는 스타일이 적용된 프로젝트와 같이 사전 제작된 조명을 사용하여 텍스처를 수행할 수도 있고 하이맵에서 반사되는 광선 추적형 광선을 베이킹할 수도 있다는 의미입니다.

![](version-11-2.resources/bent-normal-ex.jpg){width="300px"}

그리고 마지막으로 구부러진 법선 마디가 있습니다. 정규 정규 변환과 비교하여 이 노드는 AO를 사용하여 해당 AO 정보를 사용하기 위해 정규 맵을 수정합니다. 효과를 만들기 위해 메시 베이커가 필요하기 전에 이 노드가 텍스트 공간에서 이를 수행합니다.

### Adobe Standard Material 셰이더

애플리케이션 전체에서 재질과 렌더링을 통합하기 위한 노력에서 3D 뷰의 새로운 기본 셰이더는 Adobe Standard Material 셰이더입니다. 얼핏 보면 이전 PBR 금속 거칠기 셰이더와 다르지 않지만(어쨌든 기반) 더 많은 이국적인 채널을 지원하므로 외부 렌더러 없이 미리 볼 수 있습니다.

### UI 변경 사항

UI는 약간 수정되었지만 가장 눈에 띄는 것은 개선된 파일 > 새 패키지 메뉴로 그래프 유형을 선택할 수 있고 메인 도구 모음의 개선된 버튼 및 업데이트된 버튼입니다. 이는 새 그래프 유형 및 다른 응용 프로그램에 대한 단축키를 제공합니다.

## 튜토리얼

다음은 새로운 기능에 대한 비디오 튜토리얼입니다.

## 릴리스 정보

### 11.2.0

*(2021년 6월 23일 릴리스)*

**추가됨:**

* [브랜딩] Substance Designer이 Adobe Substance 3D Designer으로 변경됨
* [Substance 모델] 절차 3D 모델을 만드는 새로운 Substance 모델 그래프
* [콘텐츠] 새 HDR 환경 맵 추가
* [내용] 새 구부러진 표준 노드
* [Content] 새로운 RT 앰비언트 오클루전 노드
* [Content] 새로운 RT Caustics 노드
* [Content] 새로운 RT Caustics 노드
* [내용] 새로운 RT 방사 조도 노드
* [Content] 새로운 RT 그림자 노드
* [상호 운용성] 에셋을 Painter으로 보내고 Painter을 실행한 다음 라이브러리에 에셋을 추가하거나 업데이트합니다(Adobe Substance 3D 플랜 필요)
* [상호 운용성] 에셋을 Sampler으로 보내고 Sampler을 실행한 다음 라이브러리에 에셋을 추가하거나 업데이트합니다(Adobe Substance 3D 플랜 필요)
* [상호 운용성] Adobe Bridge에서 에셋을 검색할 때 해당 에셋이 있는 위치에서 Bridge가 실행됩니다(Substance 3D Adobe 플랜 필요)
* [ASM] Substance 그래프 및 MDL 그래프에서 새로운 Adobe ASM(Standard Material) 지원
* [ASM] ASM 템플릿 추가
* [ASM] ASM용 OpenGL 셰이더 추가
* [ASM] ASM 셰이더를 기본 셰이더로 설정합니다.
* [일반] 모든 임시 파일을 사용자 설정 임시 디렉토리에 집계합니다
* [일반] 새 &#39;다른 이름으로 사본 저장&#39; 명령
* [일반] 파일 업데이트 메뉴
* [일반] 도움말 메뉴 업데이트
* [Publish] 새 게시 창
* [Publish] SBSAR 파일을 게시하는 동안 SBS 파일을 저장하지 않도록 환경 설정에 옵션을 추가합니다
* [속성] 그래프 속성에 그래프 유형 필드를 추가합니다.
* [속성] 보다 적절한 방식으로 그래프의 속성 순서를 변경합니다
* [브랜딩] 새 정보 창
* [브랜딩] 애플리케이션 스타일 업데이트
* [GLSLFX] 기법에 레이블 추가
* [GLSLFX] GLSLFX 셰이더의 레이블을 설정할 가능성을 추가합니다.
* [메타데이터] 패키지 리소스에 메타데이터 추가
* [메타데이터] 그래프, 입력, 출력 및 리소스에 대한 메타데이터 편집 허용
* [지역화] 독일어, 프랑스어 및 중국어 간체로 된 새로운 번역
* [UX] 마우스 드래그의 경우 3D 보기에서 역방향 확대/축소
* [AXF] 버전 1.8.0으로 업데이트합니다.
* [Logs] 설치된 플러그인을 로그에 추가
* [VFX] ACES 1.2 OpenColorIO 구성 추가
* [Python API] 설정에 지정된 tmp 디렉터리를 쿼리하는 메서드를 추가합니다
* [Python API] isModified 메서드를 SDPackage에 추가하여 패키지 저장 여부를 확인합니다.
* [Python API] SDColorManagementEngine에 일부 색상 변환 메서드 추가
* [Python API] 그래프 객체(주석, 핀, 프레임 등) 삭제
* [Python API] 그래프 인스턴스 노드에 대한 물리적 크기 속성을 표시합니다.
* [Python API] 다른 이름으로 사본 노출
* [Python API] SDPackageMgr.savePackage 메서드 수정
* [Python API] 선택한 그래프 오브젝트 목록 가져오기
* [Python API] 그래프 선택에 사용할 새로운 메서드 이름 소개
* [Python API] 플러그인이 처음 만든 탐색기 패널에 동작을 추가할 수 없음

**고정:**

* [매개 변수] 드롭다운 Integer1 매개 변수에 음수 값을 사용하면 인스턴스에서 일관되지 않은 동작이 발생합니다
* [매개 변수] 각도 위젯에서 값을 늘리는 동안 문제가 발생했습니다.
* [그래프] 2D 또는 3D 보기에서 출력을 표시할 때 타이밍 문제가 발생합니다.
* [국제화] 일부 특정 문자가 파일 식별자에서 공백으로 변경됩니다.
* [Preferences] &#39;User project&#39; 파일 레이블이 일본어에서 다시 변환되지 않습니다.
* [Python API] SDUIMgr.getCurrentGraphSelectedNodes() 메서드를 실행하는 동안 RecursionError 발생
* [Python API] SDApplication.getPath(SDApplicationPath.InstallationDir)가 아무 것도 반환하지 않음
* [Python API] SDSBSARExporter에서 파일 저장 알림을 보내지 않습니다.
