---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/technical-issues/3d-view-issues.html"
breadcrumb-title: ''
description: 렌더링, 표시 및 성능 문제를 포함한 Substance 3D Designer의 3D 보기 문제를 해결합니다.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > 3D View issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 보기 문제
user-guide-description: ''
user-guide-title: ''
source-git-commit: 21af965a075e8c119d16922f15b867da99c21397
workflow-type: tm+mt
source-wordcount: '1629'
ht-degree: 0%

---


# 3D 보기 문제

이 페이지에는 Substance 3D Designer의 [3D 보기](../../interface/3d-view/3d-view.md)와 관련된 기술적 문제가 나열되어 있으며 각각에 대한 문제 해결 단계를 제공합니다.

## 낮은 성능: 추가 설치형 GPU가 사용되지 않음

**![(오류)](3d-view-issues.resources/error.svg) 문제**

Substance 3D Designer은 시스템의 *추가 설치형* GPU(<b>dGPU</b>)를 사용하지 않으며, 대신 *통합* GPU(<b>iGPU</b>)를 사용합니다. 이렇게 하면 그래프 및/또는 [3D 보기](../../interface/3d-view/3d-view.md)를 렌더링할 때 성능이 저하됩니다.

**![(틱)](3d-view-issues.resources/check.svg) 권장 단계**

스위처블 그래픽이 있는 시스템은 GPU 제조업체에 따라 전용 소프트웨어의 *특정 응용 프로그램*&#x200B;에 사용해야 하는 *dGPU*&#x200B;을(를) 강제 실행할 수 있습니다.

예를 들어 <b>Nvidia dGPU</b>를 사용하는 사용자는 다음을 수행할 수 있습니다.

1. Substance 3D Designer 닫기
2. <b>NVIDIA 제어판</b> 열기
3. <b>3D 설정</b> 섹션의 <b>3D 설정 관리</b> 화면으로 이동
4. <b>프로그램 설정</b> 탭에서 &#39;Substance 3D Designer&#39; 항목을 찾습니다.
5. <b>기본 설정 GPU</b> 콤보 상자에서 <b>고성능 NVIDIA 프로세서</b>를 선택합니다.
6. Substance 3D Designer 시작

>[!WARNING]
>
> 통합 GPU(iGPU)는 *지원되지 않습니다*&#x200B;입니다. [시스템 요구 사항](../../getting-started/system-requirements/system-requirements.md) 페이지에서 자세히 알아볼 수 있습니다.

## 3D 개체가 평평합니다

**![(오류)](3d-view-issues.resources/error.svg) 문제**

한 세션에서 세부 볼륨을 특색있게 지정한 3D 개체는 다음 세션에서 평평하게 되지만 그래프는 변경되지 않았으며 Height 맵은 동일한 데이터를 전달합니다.

**![(틱)](3d-view-issues.resources/check.svg) 권장 단계**

Height 맵에 따른 3D 개체의 변형 효과는 **테셀레이션 변위**&#x200B;이라는 기법을 사용하여 수행된다. 이 기술은 다음 두 단계로 이루어집니다.

1. **테셀레이션**: 개체 도형이 정점으로 *세분화*&#x200B;되어 더 미세한 볼륨 세부 사항을 지원하기 위해 *더 조밀한 도형*&#x200B;이 만들어집니다
2. **변위**: 정점이 *표준 벡터*&#x200B;를 따라 *이동*(즉, 변위)됩니다. 법선 벡터는 다각형이 향하는 방향을 따르고, 크기(즉, 길이)는 1이다

변위 *방향*&#x200B;이(가) 알려져 있습니다. 일반 벡터의 방향입니다.\
정점이 이동하는 변위 *거리*&#x200B;는 다음과 같이 계산됩니다. `Distance = Height scale * Height map`. Height 맵에 *변경되지 않은*&#x200B;이(가) 있으므로 **Height 비율**&#x200B;이 남습니다.

기본 Height 배율 값은 **1.0**&#x200B;이며, 3D 보기에 표시된 메시 및 여기에 적용된 Height 맵에 따라 *표시되지 않는* 변위 효과가 나타날 수 있습니다.

이 값은 다음과 같은 방법으로 수정할 수 있습니다.

| 3D 보기에서 | 그래프 보기에서 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 왼쪽 도구 모음에서 **변위 팝업**&#x200B;을 사용합니다.<br>자세한 내용은 [전용 페이지](../../interface/3d-view/displacement/displacement.md)를 참조하세요. | [출력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 노드를 만들고 해당 속성에서 `heightScale` 사용을 설정합니다.<br>예를 들어 [상수 부동 노드](../../compositing-graphs/nodes-reference-for-com/node-library/values/constant.md#floats)를 사용하여 이 출력에 값을 입력한 다음 3D 보기에서 *그래프를 다시 적용*&#x200B;합니다. |

>[!TIP]
>
> 이 메서드를 사용하면 사용자 정의 Height 비율 값 *그래프당*&#x200B;을 설정할 수 있습니다. 이를 통해 그래프의 특정 재질과 일치하도록 조정할 수 있습니다.

## 3D 보기가 완전히 검정색임

**![(오류)](3d-view-issues.resources/error.svg) 문제**

버전 15.0.0 이상에서 3D 보기의 뷰포트는 평평한 검정색입니다. 일부 텍스트 오버레이(예: 샘플 및 렌더링 시간)가 표시되지만 3D 장면이 표시되지 않습니다.

**![(틱)](3d-view-issues.resources/check.svg) 권장 단계**

버전 15.1 이상

새 3D 렌더러는 버전 15.1에서 업그레이드되었으며 최신 GPU 드라이버가 필요합니다. 시스템의 GPU 드라이버를 최신 버전으로 업데이트하십시오.

다음 위치에서 드라이버를 찾을 수 있습니다. [NVIDIA](https://www.nvidia.com/Download/index.aspx?lang=en-us)  | [AMD](https://www.amd.com/en/support)  | [인텔](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)

버전 15.0 이상

Designer [15.0.0](../../release-notes/version-15-0/version-15-0.md)에서는 최신 기술을 사용하므로 이전 GPU에서 지원하지 않는 새로운 사내 [3D 렌더러](../../interface/3d-view/3d-renderers/3d-renderers.md)를 도입했습니다.

지원되는 GPU에는 Designer의 [시스템 요구 사항](../../getting-started/system-requirements/system-requirements.md)에 따라 NVIDIA RTX 20 시리즈(튜링) 이상이 포함됩니다.

[프로젝트 설정]의 [새 옵션](../../interface/preferences-window/project-settings/project-settings.md)을 사용하여 기본적으로 OpenGL 렌더러를 계속 사용할 수 있습니다.

1. 편집 > 환경 설정 > 프로젝트로 이동합니다.
2. 목록에서 마지막 프로젝트 파일 선택
3. 프로젝트 파일 목록에서 3D 보기 탭을 선택합니다
4. &#39;기본 렌더러&#39; 옵션을 &#39;OpenGL(사용되지 않음)&#39;로 설정합니다.
5. &#39;확인&#39;을 클릭하여 변경 내용을 확인합니다.

이제 모든 새 3D 보기는 기본적으로 OpenGL 렌더러를 사용하며 이를 통해 이전과 같이 계속 작업할 수 있습니다.

>[!NOTE]
>
> 대부분의 AMD 및 Intel GPU에는 동일한 문제 및 문제 해결 단계가 적용되며, 최신 3D 렌더러에서는 현재 *지원되지 않습니다*.

>[!IMPORTANT]
>
> OpenGL 렌더러는 *사용되지 않음*&#x200B;이며 이후에 Designer에서 제거될 수 있습니다. 워크플로의 중단을 방지하고 지속적인 지원을 보장하기 위해 시스템의 GPU를 업그레이드하는 것이 좋습니다.

## &#39;렌더러가 지원되지 않음&#39; 메시지가 표시됩니다.

**![(오류)](3d-view-issues.resources/error.svg) 문제**

버전 15.0.0 이상에서는 새 3D 렌더러(래스터라이저, GPU 패스파래서)를 사용할 때 뷰포트의 오른쪽 하단에 &#39;렌더러 지원 안 됨&#39; 메시지가 표시됩니다. 3D 장면이 표시되지 않습니다.

**![(틱)](3d-view-issues.resources/check.svg) 권장 단계**

Designer [15.0.0](../../release-notes/version-15-0/version-15-0.md)에서는 최신 기술을 사용하므로 이전 GPU에서 지원하지 않는 새로운 사내 [3D 렌더러](../../interface/3d-view/3d-renderers/3d-renderers.md)를 도입했습니다.

지원되는 GPU에는 Designer의 [시스템 요구 사항](../../getting-started/system-requirements/system-requirements.md)에 따라 NVIDIA RTX 20 시리즈(튜링) 이상이 포함됩니다.

기본 설정에서 &#39;기본 렌더러&#39; 옵션이 [프로젝트 설정](../../interface/preferences-window/project-settings/project-settings.md)에서 &#39;기본(미리 정의된 렌더러)&#39;으로 설정되어 있으면 3D 보기가 자동으로 OpenGL 렌더러로 돌아갑니다.

다음 단계에 따라 해당 옵션을 찾아 조정할 수 있습니다.

1. 편집 > 환경 설정 > 프로젝트로 이동합니다.
2. 목록에서 마지막 프로젝트 파일 선택
3. 프로젝트 파일 목록에서 3D 보기 탭을 선택합니다
4. &#39;기본 렌더러&#39; 옵션이 탭 내의 설정에 나열됩니다

>[!NOTE]
>
> 현재 <b>NVIDIA GTX 시리즈</b>의 GPU만 지원되지 않는 것으로 검색됩니다.
> 
> 그러나 대부분의 AMD 및 Intel GPU는 지원되지 않으며 메시지 없이 검정 렌더링을 생성합니다. 해당 GPU에 대한 지침은 위의 &#39;3D 보기가 완전히 검은색임&#39; 항목을 참조하십시오.

>[!IMPORTANT]
>
> OpenGL 렌더러는 *사용되지 않음*&#x200B;이며 이후에 Designer에서 제거될 수 있습니다. 워크플로의 중단을 방지하고 지속적인 지원을 보장하기 위해 시스템의 GPU를 업그레이드하는 것이 좋습니다.

## 3D 개체가 완전히 매끄럽게 보임

**![(오류)](3d-view-issues.resources/error.svg) 문제**

**Height** [출력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)에 보낸 데이터를 작업한 후 개체에 일부 볼륨이 있는 것처럼 보이지만 음영에서 Height 정보를 무시한 것처럼 *완전히 부드럽게 보입니다*.

<table style="margin-left: 0; margin-right: 0;">
<tr style="border: 0;">
<td style="border: 0; width: 60%; vertical-align: top">

**![(틱)](3d-view-issues.resources/check.svg) 권장 단계**

Height 데이터가 **표준** [출력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)에 연결된 *표준으로 변환*&#x200B;되었는지 확인하십시오.

**테셀레이션 변위** 기법을 사용하는 경우(위의 &quot;3D 개체가 평평함&quot; 참조) - 개체가 Height 데이터를 따르도록 *변형*&#x200B;할 수 있지만 *표준*&#x200B;이 Height 데이터를 고려하여 수정될 때까지 표면은 *빛에 다르게 반응하지 않습니다*.

해결 방법은 매우 간단합니다. Height 출력으로 이어지는 스트림의 마지막 노드를 [표준](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) 노드에 연결합니다. 작업 중인 자료에 따라 해당 노드의 **강도** 매개 변수를 조정하고 일반 노드를 **일반** 출력에 연결합니다.

</td>
<td style="border: 0; width: 40%; vertical-align: top">

![](3d-view-issues.resources/3dview-height-without-normals.gif){width="256px"}

</td>
</tr>
</table>

## 렌더링이 흐림/픽셀화됨

**![(오류)](3d-view-issues.resources/error.svg) 문제**

시스템에서 *디스플레이 비율*&#x200B;을 사용하면 렌더링된 이미지가 흐릿하거나 픽셀화되어 보입니다.

<table style="margin-left: 0; margin-right: 0;">
<tr style="border: 0;">
<td style="border: 0; width: 60%; vertical-align: top">

**![(틱)](3d-view-issues.resources/check.svg) 권장 단계**

기본적으로 Designer은 *크기 조절* 디스플레이 해상도를 사용하여 [3D 보기](../../interface/3d-view/3d-view.md)의 렌더링 해상도를 정의합니다. 선명한 렌더링에 *기본* 디스플레이 해상도가 대신 사용되도록 변경할 수 있습니다.

**편집** 메뉴를 열고 **기본 설정...** 옵션을 선택합니다. [환경 설정](../../interface/preferences-window/preferences-window.md) 창에서 **3D 보기** 섹션을 열고 **뷰포트 크기 조절** 매개 변수를 *없음*&#x200B;으로 설정합니다.

</td>
<td style="border: 0; width: 40%; vertical-align: top">

![](3d-view-issues.resources/demo-viewport-scaling-option.png){width="256px"}

</td>
</tr>
</table>

## &#39;테셀레이션 요소&#39; 속성을 찾을 수 없습니다.

**![(오류)](3d-view-issues.resources/error.svg) 문제**

Designer을 버전 15.0.0으로 업그레이드한 후 재질 속성에서 이전의 &#39;테셀레이션 요소&#39; 매개 변수를 찾을 수 없습니다.

**![(틱)](3d-view-issues.resources/check.svg) 권장 단계**

새 렌더러(래스터화 및 GPU 패스트레이서)를 사용할 때 &#39;테셀레이션 요소&#39;가 이러한 렌더러의 속성에서 발견되었습니다. 3D 보기에서 <b>렌더러 > 설정 편집</b>으로 이동합니다. 등록 정보가 등록 정보 도크에 나열됩니다.

>[!NOTE]
>
> 쪽맞춤 범위는 렌더러에 따라 다릅니다.
> 
> * 래스터라이저/GPU 패스트레이서: 전체 장면에 전체적으로 적용되는 고유한 값입니다.
> * OpenGL: 재료당 하나의 값.
> * Iray: 메시당 하나의 값.

## 3D 개체가 이상하게 보임: 해당 음영이 조명에 맞지 않습니다.

**![(오류)](3d-view-issues.resources/error.svg) 문제**

물체의 음영은 법선, 접선, 이항 벡터에 의존한다. 해당 좌표는 `[-1, 1]` 범위를 사용하는 반면 노멀 맵은 대부분의 경우 `[0, 1]` 범위를 사용합니다. 값을 다른 값에 맞추려면 <b>편의와 비율</b>을 적용해야 합니다. `value * scale + bias`.

예를 들어, 소수 자릿수 2와 -1은 x 값을 `[0, 1]`에서 `[-1, 1]`(으)로 조정하므로 `x * 2 - 1`이(가) 됩니다.

Designer은 3D 메시로 지정되지 않는 한 일반 비율 및 편향을 적용하지 않습니다. 해당 정보가 없는 경우 [해당 자료를 재정의](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)할 때 콘솔에 경고가 발생합니다.

```
[SceneGraph]No 'scale' or 'bias' defined on the UsdUVTexture shader '/root/material/<materialName>' (the rendering may be incorrect)
```


**![(틱)](3d-view-issues.resources/check.svg) 권장 단계**

조금 전에 USD 형식으로 내보낸 장면의 경우: 필요한 데이터가 포함된 최신 USD 버전을 사용하여 장면을 다시 내보냅니다. 장면 내보내기에 사용되는 소프트웨어에 따라 달라지는 일반 비율 및 편중과 관련된 속성에 유의하십시오.

[재질 재정의](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)를 수행하면 Designer은 메시를 처리하고 표준, 접선 및 이항식과 관련된 누락된 데이터를 계산합니다. Designer의 기본 비율과 편향이 메시에 필요한 비율과 일치하면 메시 재정의 시 메시가 올바르게 표시됩니다.

## 3D 보기를 시작할 때 충돌 발생

**![(오류)](3d-view-issues.resources/error.svg) 문제**

프로젝트를 만들거나 프로젝트를 로드하거나 3D 보기를 수동으로 시작할 때 3D 보기 시작 시 Designer이 충돌합니다.

**![(틱)](3d-view-issues.resources/check.svg) 권장 단계**

먼저 시스템이 Designer [시스템 요구 사항](../../getting-started/system-requirements/system-requirements.md)을 충족하는지 확인하십시오.

그런 다음 그래픽 드라이버를 업데이트합니다. 다음 링크를 통해 GPU용 최신 드라이버를 찾을 수 있습니다. [NVIDIA](https://www.nvidia.com/Download/index.aspx?lang=en-us)  | [AMD](https://www.amd.com/en/support)  | [인텔](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)

시스템에 통합 GPU(iGPU)와 개별 GPU(dGPU)가 모두 포함된 경우 *둘 다 드라이버를 업데이트*&#x200B;해야 합니다!

그런 다음 3D 그래픽 프로세스에서 데이터를 주입하거나 오버레이할 수 있는 소프트웨어를 비활성화합니다. 예를 들면 다음과 같습니다.

* ReShade와 같은 후공정 인젝터
* 사용자 정의 십자선 또는 GPU 성능 측정 단위와 같은 오버레이
* 3D 그래픽을 실시간으로 기록, 스트리밍 또는 공유하기 위한 화면 캡처 소프트웨어
