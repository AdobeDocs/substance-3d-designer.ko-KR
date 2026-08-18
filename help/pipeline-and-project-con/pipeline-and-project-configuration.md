---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 파이프라인 및 프로젝트 설정을 구성하여 워크플로 및 출력을 최적화합니다.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 파이프라인 및 프로젝트 구성
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---


# 파이프라인 및 프로젝트 구성

Substance 3D Designer은 파이프라인 사용을 위해 애플리케이션을 구성하는 강력한 시스템을 갖추고 있습니다. 계층적 &quot;**프로젝트**&quot; 파일의 고급 시스템을 통해 모든 구성 및 라이브러리 콘텐츠가 버전 제어 하에 있는 상태에서 응용 프로그램을 Studio 또는 프로젝트 표준으로 즉시 구성할 수 있습니다. 이 시스템의 주요 목표는 모든 파이프라인 관련 설정을 중앙 집중화하면서도 여러 구성이 서로 오버라이드하고 확장할 수 있도록 하는 것입니다.

>[!WARNING]
>
> 이 시스템은 요구 사항이 더 단순한 단일 사용자를 위한 것이 아니라 *대형 프로젝트와 팀이 있는 스튜디오* 및 조직에 대한 더 높은 요구를 위한 것입니다. 이 시스템을 최대한 활용하기 위해서는 일정 정도의 자동화된 설정뿐만 아니라 계획 및 준비의 공정한 양이 권장됩니다!

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 구성 파일 계층 구조

Designer에는 각각 다른 목적을 가진 3개의 계층 또는 구성 파일이 있습니다. Windows의 경우 모든 파일은 *~User\AppData\Local\Adobe\Adobe Substance 3D Designer*&#x200B;에 있습니다.

이 이미지는 새로 설치한 후 Designer의 기본 설정에서 다른 파일 간의 관계를 보여줍니다.

</td>
<td style="border: 0;" valign="top">

![구성 파일 계층 구조](../assets/filestructureoverview.png "구성 파일 계층 구조")

</td>
</tr>
</table>

* <b>[User\_Preferences.XML](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md)</b>에는 프로젝트 파이프라인과 관련이 없는 일반 프로그램 설정이 포함되어 있습니다. 이 파일은 고유하며 스왑할 수 없습니다. Designer은 이 정확한 파일을 활용하도록 하드코딩되어 있습니다.\
  구성 파일에 대한 단일 참조가 하나 있습니다.
* <b>[Default\_Configuration.SBSCFG](../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md)</b>은(는) 이름이 다른 다른 SBSCFG 파일에 대해 스왑할 수 있지만 한 번에 하나의 SBSCFG 파일만 사용할 수 있습니다.\
  여기에는 프로젝트 파일에 대한 여러 참조가 포함됩니다. *기본 구성의 경우 이러한 파일은 명시적으로 정의되지 않지만 하드 코딩되어 있습니다.*
* <b>[Project.SBSPRJ](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)</b> 파일에 프로젝트/파이프라인 관련 설정이 있습니다. 여러 프로젝트는 계층 구조에서 정의할 수 있으며, 이전에 정의된 프로젝트를 재정의하거나 확장할 수 있습니다.

## Designer 파이프라인 설정

모든 유형의 파일은 이 페이지의 하위 페이지에 대해 자세히 설명되지만 Designer에 대한 사용자 정의 설정을 이상적으로 정의하는 방법에 대한 간단한 개요는 다음과 같습니다.

1. <b>프로젝트 파일에 추가할 설정을 식별하고 그룹화합니다.</b> 이는 모든 스튜디오마다 다르며 어느 정도의 계획이 필요합니다!\
   대부분의 경우 최소한 두 개의 프로젝트가 정의되어야 합니다. 하나는 기본 템플릿, 셰이더 파일, 베이킹 설정과 같은 전역 스튜디오 전체 기본값용이고 다른 하나는 라이브러리 콘텐츠와 같은 더 구체적인 콘텐츠용입니다. 동시에 실행되는 서로 다른 프로젝트가 있는 경우 각각에 대해 여러 프로젝트 구성(총 3개 이상)을 만들 수 있습니다.
1. <b>관련 [SBSPRJ 파일](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)을 만들고 해당 파일과 내용을 버전 제어 아래에 배치합니다.</b> *별도의 저장소*&#x200B;를 만들어 실제 프로젝트 콘텐츠 및 리소스(3D 모델, 텍스처, 코드)에서 Designer 파이프라인 및 라이브러리 콘텐츠를 분리하는 것이 좋습니다.
1. <b>모든 프로젝트 파일을 나열하는 [ SBSCFG configuration](../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md) 파일을 만들고 버전 제어 아래에 둡니다</b>. 프로젝트가 여러 개인 경우에는 모든 프로젝트에 대해 구성을 만들 수 있습니다.
1. <b>모든 사용자의 [User\_Preferences.xml](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md)을 관련 구성 파일을 참조하도록 설정합니다.</b>\
   모든 사용자가 이를 수동으로 수행하도록 하거나 XML 파일에 줄을 삽입하여 스크립트를 작성할 수 있습니다. [관련 페이지의 추가 정보](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md).
