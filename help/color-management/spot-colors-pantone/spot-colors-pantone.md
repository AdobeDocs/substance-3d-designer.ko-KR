---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/color-management/spot-colors-pantone.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 Pantone 별색을 사용하여 인쇄 및 디자인 작업 과정에서 정확한 색상 일치를 하는 방법을 살펴보세요.
helpx_creative_field: ""
helpx_description: Designer > Color Management > Spot Colors (Pantone)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 별색 (Pantone)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---


# 별색 (Pantone)

별색 은 색상을 선택할 수 있는 대체 모드입니다. Substance 3D Designer에서는 표준 RGB 또는 HSV 색상 피커 대신 기존 색상 관리 및 재생 시스템과 일치하는 색상 책에서 색상을 선택할 수 있습니다. 이를 통해 Designer에서 사용되는 디지털 색상을 제조 제품의 색상과 거의 일치시킬 수 있습니다.

현재 [별색]에서는 Pantone 책 17권이 제공됩니다.

## 색상 관리

별색은 정확한 색상 재현과 일치를 위한 것이므로 작업을 시작하기 전에 Designer에 대해 [색상 관리](../../color-management/color-management.md)를 설정해야 합니다. 별색은 OCIO이 아닌 <b>Adobe Color Engine(ACE)</b> 색상 관리에서 가장 잘 작동합니다. 이 설정은 레거시 모드에서 작동하지만, 모니터가 sRGB로 보정되지 않은 경우에는 올바르게 표시되는지 확인할 수 없습니다.

즉, 별색에 대해 색상 관리를 설정하려면 다음과 같이 하십시오.

* 적절한 ICC 프로필을 생성하거나 획득하여 모니터를 보정합니다.
* Designer 환경 설정에서 Adobe Color Engine(ACE)로 색상 관리 를 활성화합니다.
* 2D 및 3D 보기를 설정하여 모니터의 적절한 프로필을 사용합니다.
* 변경 사항을 적용하려면 다시 시작하십시오.
* Designer과 다른 Adobe 응용 프로그램(예: Adobe Illustrator 또는 Photoshop) 간의 색상 일치 여부를 확인합니다. 첫 번째 Pantone 책인 Solid Coated의 색상 &quot;<b>Pantone Rhodamine Red C</b>&quot;은(는) 색상 관리가 올바르지 않으면 크게 달라질 수 있으므로 좋은 테스트 사례입니다.

>[!WARNING]
>
> **썸네일 색상**
> 
> 노드 축소판은 *기본적으로 색상이 관리되지 않음*&#x200B;이므로 올바른 프로필로 2D 보기의 색상만 신뢰합니다. 축소판 색상 관리는 프로젝트의 색상 관리 아래에 있는 환경 설정에서 활성화할 수 있지만 약간의 성능 비용이 소요됩니다.

## 별색 사용

### RGB에서 별색으로 전환

색상 관리를 설정한 경우에도 색상 피커는 기본적으로 RGB 또는 HSV 색상 피커로 설정됩니다. 이 색상을 별색으로 수동으로 전환해야 합니다. 이 설정은 매개 변수마다 저장되며 매개 변수를 노출할 때도 전달됩니다.

1. RGB 색상 견본 옆의 ![](spot-colors-pantone.resources/spot-colors-pantone-01.png) <b>색상 피커 유형</b> 버튼을 클릭합니다.
1. <b>RGB 색상</b> 대신 드롭다운 목록에서 <b>색상 책</b>을 선택합니다.
1. ![](spot-colors-pantone.resources/spot-colors-pantone-02.png) <b>색상 피커 유형</b>의 아이콘이 변경되고 해당 인터페이스가 <b>별색</b> 모드로 변경됩니다.

![별색 모드로 전환](spot-colors-pantone.resources/spot-colors-pantone-03.gif "별색 모드로 전환"){width="512px"}

### 별색 선택 및 찾기

색상 책에서 별색을 찾아 선택하는 몇 가지 방법이 있습니다.

* 책의 페이지 양쪽에서 ![](spot-colors-pantone.resources/spot-colors-pantone-04.png) ![](spot-colors-pantone.resources/spot-colors-pantone-05.png) <b>왼쪽 및 오른쪽 화살표</b>를 사용하여 페이지 사이를 이동할 수 있습니다. 페이지 표시를 클릭하고 드래그하여 페이지 간을 스크롤할 수도 있습니다.
* 현재 페이지에서 색상을 클릭하여 선택할 수 있습니다. 종종 더 많은 색상을 사용할 수 있으며 아래로 스크롤해야 합니다.
* 검색 막대를 사용하여 이름 또는 번호로 색상을 검색할 수 있습니다. 이 검색은 책의 색상 이름만 일치하며, 복잡한 논리는 진행되지 않습니다. &quot;회색&quot;을 검색하면 이름에 &quot;회색&quot;이라는 단어가 포함된 결과만 표시되고, 이름에 숫자만 포함된 회색 색상은 표시되지 않습니다.
* 색상 책의 더 크고 사용하기 쉬운 인터페이스를 얻으려면 ![](spot-colors-pantone.resources/spot-colors-pantone-06.png) <b>스포이드</b> 아이콘과 ![](spot-colors-pantone.resources/spot-colors-pantone-04.png) <b>왼쪽 화살표</b> 사이에 있는 색상 미리 보기 상자를 클릭하세요.

![별색 검색](spot-colors-pantone.resources/spot-colors-pantone-07.gif "별색 검색"){width="512px"}

### 별색 선택 및 변환

별색은 ![](spot-colors-pantone.resources/spot-colors-pantone-06.png) <b>스포이드</b> 도구를 사용하여 선택할 수 있습니다. [별색] 모드에 있는 경우 이 설정은 샘플링된 RGB 색상을 현재 선택한 책에서 가장 근접한 일치하는 별색으로 변환하는 것을 의미합니다.

Designer의 <b>스포이드</b> 도구는 제한 없이 화면의 아무 곳에서나 사용할 수 있으므로 Designer을 별색 변환 도구로 사용할 수 있습니다.

책을 전환하거나 별색 책에서 RGB으로 다시 전환해도 현재 색상이 가장 가깝게 변환됩니다. 즉, 책 간에 색상을 변환하고 다시 RGB으로 변환할 수 있습니다.

>[!WARNING]
>
> 책 간에 별색을 변환하면 손실이 발생합니다. 왕복 전환을 해도 처음에 사용했던 색상과 같은 색상이 나타나지 않는 경우가 많습니다.

![별색 선택 및 변환](spot-colors-pantone.resources/spot-colors-pantone-08.gif "별색 선택 및 변환"){width="512px"}
