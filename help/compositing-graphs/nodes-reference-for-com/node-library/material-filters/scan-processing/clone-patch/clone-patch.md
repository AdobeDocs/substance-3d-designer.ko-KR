---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/clone-patch.html"
breadcrumb-title: ''
description: Clone Patch 노드를 사용하여 스캔한 자료의 영역을 복제하고 패치하여 가공물 및 결함을 제거할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 복제 패치
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---


# 복제 패치

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch.png){width="128px"}

![](../../../../../../assets/clone-patch-grayscale.png){width="128px"}

## 복제 패치/복제 패치 회색 음영

**내부:** *재질 필터/스캔 처리*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

복제 패치는 절차적이며 파라메트릭 &quot;복제 도장&quot; 노드입니다. 이 기능은 입력의 한 영역을 다른 영역으로 복제하여 잠재적으로 원치 않는 세부 정보를 숨깁니다. 브러시 기반 응용 프로그램에서 익숙한 도구를 사용하는 것만큼 빠르고 쉽지는 않지만 비파괴적이며 노드 기반 작업 과정 내에서 작업할 수 있는 주요 장점을 제공합니다. 또한 이 노드는 대상 영역과 소스 영역을 스마트 분석하고 대비, 값 및 모양을 기반으로 항목을 최대한 혼합합니다.

이는 특정 영역에 원치 않는 세부 사항이 있는 경우 수동으로 수정하고 싶은 드문 순간을 위해 주로 사용됩니다.

이것은 표준적이고 단순한 &quot;스탬프&quot; 브러시처럼 작동하지 않는다는 점을 명심하십시오. 블렌딩된 영역의 모양은 작업 중인 영역의 모양과 값에 따라 달라집니다. 즉, 이는 인내심이 필요하지만 우수한 결과를 제공하는 두꺼운 노드입니다.

또한 알아야 할 사항은 gizmo로 대상 영역을 이동할 수 있지만 소스 영역은 &quot;소스 매트릭스&quot; 매개 변수를 변경하여 설정해야 한다는 사실입니다.

>[!NOTE]
>
> 전체 재질(대부분의 경우)에 대해 이 작업을 하려면 [재질 복제 패치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md)를 참조하십시오.
> 
> 재료가 되지 않고 동시에 여러 입력에 대해 이 작업을 수행하려는 경우 [다중 복제 패치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md)를 참조하십시오.

## 매개변수

* **일반(색상만 해당)**: *거짓/참*\
  입력이 정규맵인지 여부와 혼합을 정규맵으로 처리할지 여부를 설정합니다.
* **모양**: *정사각형, 디스크*&#x200B;스탬프 모양을 설정합니다. 기본으로만 사용됩니다.
* **가장자리**
  * **임계값**: *0.0 - 1.0*&#x200B;혼합 영역이 도달할 거리를 설정합니다. 이는 대상 영역의 모양을 따라 단계적으로 성장하며 균일한 배경*에는 거의 영향을 주지 않습니다.*
  * **흐림**: *0.0 - 2.0*&#x200B;더 부드러운 전환이 필요한 경우 스탬프 영역의 가장자리를 흐리게 합니다.
  * **Smoothness**: *0.0 - 2.0*&#x200B;스탬프 모양의 가장자리를 둥글게 하여 더 매끄럽게 흐르는 윤곽선을 만듭니다.
  * **격자 해상도**: *1 - 11*&#x200B;혼합 분석의 품질 해상도를 설정합니다. 값이 높을수록 더 정확한 혼합을 의미합니다.
* **변환**
  * **소스 행렬**: *(변환 행렬)*소스를 변환합니다(크기 조정 및 회전). 캔버스에서는 수행할 수 없으며 이러한 매개 변수만 변경하십시오.
  * **원본 오프셋**: *-0.5 - 0.5*&#x200B;원본 위치를 변환합니다. 캔버스에서는 수행할 수 없으며 이러한 매개 변수만 변경하십시오. *이 매개 변수는 아마도 변경할 기본 매개 변수입니다!*
  * **대상 행렬**: *(변환 행렬)*대상 위치를 변환합니다(크기 및 회전). 캔버스에서 gizmo를 통해 수행할 수도 있습니다.
  * **대상 오프셋**: *-0.5 - 0.5*&#x200B;대상 위치를 변환합니다. 캔버스에서 gizmo를 통해 수행할 수도 있습니다.

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
