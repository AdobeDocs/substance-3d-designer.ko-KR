---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/working-with-3d-scenes/exporting-scenes.html"
breadcrumb-title: ''
description: '[3D 보기 장면] 메뉴의 [장면 내보내기] 동작을 사용하여 Designer에서 편집한 모든 내용을 포함한 3D 장면을 내보냅니다.'
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Exporting scenes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 장면 내보내기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---


# 장면 내보내기

Designer에서 편집한 모든 내용을 장면으로 내보내야 하는 경우 [3D 보기](../../interface/3d-view/3d-view.md)의 &#39;장면&#39; 메뉴에서 &#39;장면 내보내기...&#39; 동작을 사용하십시오.

USD 형식으로 내보낼 경우 장면의 콘텐츠는 [장면 브라우저](../../interface/3d-view/scene-browser/scene-browser.md)에 표시되는 트리와 일치합니다.

다른 포맷의 경우 장면의 내용과 해당 내부 구조는 선택한 파일 포맷에서 지원하는 기능에 따라 달라집니다.

>[!NOTE]
>
> Designer에서 장면에 추가한 모든 항목은 내보낸 장면에 포함됩니다(기본 카메라, 기본 환경, 모든 재질 복사).

![장면 내보내기 작업](exporting-scenes.resources/exportActions.png "장면 내보내기 작업"){zoomable="yes"}

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 장면 내보내기

</td>
<td style="border: 0;" valign="top">

### 장면을 레이어로 내보내기

</td>
<td style="border: 0;" valign="top">

### 텍스처

</td>
</tr>
</table>

## 장면 내보내기

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

&#39;장면&#39; 메뉴의 &#39;장면 내보내기...&#39; 동작은 편집된 3D 장면을 파괴적으로 내보냅니다. 장면이 *병합됨*&#x200B;이고 원본에 대한 참조가 모두 손실됩니다.

즉, 원본 장면에 대한 편집이 내보낸 장면에 전혀 영향을 주지 않습니다.

</td>
<td style="border: 0;" valign="top">

![내보낸 장면 파일 - 병합됨](exporting-scenes.resources/exportFlattened.png "내보낸 장면 파일 - 병합됨"){zoomable="yes"}

</td>
</tr>
</table>

## 장면을 레이어로 내보내기

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

&#39;장면을 레이어로 내보내기...&#39; 동작은 <b>USD</b> 형식(.usd, .usda, .usdc, .usdz)으로 내보내고 *비파괴*&#x200B;입니다. 기본 내보낸 파일은 새 장면의 편집된 모든 측면이 별도의 USD 파일에 저장되는 *참조 체인*&#x200B;에 도움이 됩니다.

즉, 원본 장면에 대한 편집이 내보낸 장면으로 이어집니다.

</td>
<td style="border: 0;" valign="top">

![내보낸 장면 파일 - 레이어드](exporting-scenes.resources/exportLayered.png "내보낸 장면 파일 - 레이어드"){zoomable="yes"}

</td>
</tr>
</table>

내보낸 파일은 다음 구조를 따릅니다.

* <b>기본 파일</b>
  * <b>.layers</b>: 아래의 하위 레이어를 참조하고 재질 재정의를 선언합니다. 이 재정의는 Designer에서 만든 재질 복사본에 기하학을 바인딩합니다.
    * <b>.assembly</b>: .scene# 파일을 참조하고 지오메트리 재정의를 선언합니다. 그러면 재정의된 재질에 의해 영향을 받는 지오메트리 중 Designer에서 다시 계산한 데이터가 표시됩니다.
      * <b>.장면#</b>: 원본 장면을 참조합니다.
    * <b>.camera</b>: Designer이 장면에 추가한 카메라를 선언합니다.
    * <b>.light</b>: Designer이 장면에 추가한 조명을 선언합니다.
    * <b>.material</b>: 내보낸 텍스처를 사용하는 장면에 Designer이 추가한 재질 복사본을 선언합니다.

## 텍스처

텍스처를 내보낸 파일 옆의 디렉터리로 내보내고 그 이름을 따서 &#39;<b>\_텍스처</b>&#39; 접미사와 함께 지정합니다.

<b>EXR</b> 형식을 사용하는 HDR 텍스처(부동 소수점)를 제외하고 <b>PNG</b> 형식을 사용합니다.
