---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-clone-patch.html"
breadcrumb-title: ''
description: 다중 복제 패치 노드 를 사용하여 스캔한 재료 가공물을 복구하기 위해 여러 텍스처 채널을 복제하고 패치합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 다중 복제 패치
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---


# 다중 복제 패치

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch-multi.png){width="128px"}

![](../../../../../../assets/clone-patch-multi-grayscale.png){width="128px"}

## 다중 복제 패치(회색 음영)

**내부:** *재질 필터/스캔 처리*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

이 노드는 [복제 패치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)의 다중 입력 버전입니다. 최대 8개의 입력을 서로 연결하고 모든 입력에 대해 정확히 동일한 클론 패치 작업을 수행합니다. 주로 다각 사진에 사용하기 위한 것으로, 다각 사진은 [알베도에 대한 다각](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) 또는 [보통 사진에 대한 다각](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)과 결합됩니다.

>[!NOTE]
>
> 자세한 내용은 [복제 패치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)를 참조하고 재질 버전에 대한 [재질 복제 패치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md)를 참조하십시오.

## 매개변수

### 매개변수

* **입력 수**: *1 - 8*&#x200B;동일한 패치 작업을 받을 입력 양을 설정합니다.
* **표준(색상에만 해당)**: **False/True**&#x200B;입력이 표준 맵인지 여부와 혼합을 표준으로 처리할지 여부를 설정합니다.
* **모양**: **정사각형, 디스크**&#x200B;스탬프 모양을 설정합니다. 기본으로만 사용됩니다.
* **가장자리**
  * **임계값**: *0.0 - 1.0*&#x200B;혼합 영역이 도달할 거리를 설정합니다. 이는 대상 영역의 모양에 따라 단계적으로 성장하며, 균일한 배경*에는 거의 효과가 없습니다.*
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
