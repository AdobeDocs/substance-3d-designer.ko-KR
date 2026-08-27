---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/pipeline-and-project-configuration/project-configuration-files-sbsprj.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 SBSPRJ 프로젝트 구성 파일을 사용하여 프로젝트 설정을 관리하는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Project Configuration Files - SBSPRJ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 프로젝트 구성 파일 - SBSPRJ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---


# 개요

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

<b>프로젝트 구성 파일</b>은(는) Substance 3D Designer 구성에 사용되는 가장 복잡하고 광범위한 파일입니다.

이러한 기능은 각 다음 &#39;자식&#39; 프로젝트가 이전 &#39;부모&#39;를 확장하거나 재정의하는 여러 프로젝트 구성 파일을 사용할 수 있다는 점에서 특별합니다. 특별히 필요하지 않은 경우에는 설정을 수정하거나 프로젝트 파일에 추가해서는 안 되므로 Designer의 부모 구성 또는 기본값을 그대로 사용할 수 있습니다.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![SBSPRJ 파일 아이콘](../../assets/sbsprj.png "SBSPRJ 파일 아이콘")

</td>
</tr>
</table>

기본적으로 Designer에는 두 개의 활성 프로젝트 구성이 있습니다.

<b>기본 프로젝트: </b>모든 기본 설정을 포함하며 라이브러리 Designer은 새로 설치할 때 함께 제공됩니다.*읽기 전용, 수정하거나 제거할 수 없습니다.*

<b>사용자 프로젝트: </b>기본값은 읽기 전용이므로 *사용자가 변경한 내용*&#x200B;은 기본적으로 이 프로젝트로 이동합니다. *제거할 수 없습니다.*

이 기본 설정은 기본 라이브러리 및 기타 설정을 손상하거나 수정할 수 없도록 하면서도 단일 아마추어 사용자가 복잡한 설정을 신경 쓰지 않고도 직접 수정할 수 있도록 합니다.

## 확장 또는 재정의

연속 프로젝트의 대부분의 설정은 이전 프로젝트의 설정을 <b>재정의</b>합니다. 예를 들어, 사용자 정의 프로젝트 파일에 있는 다른 탄젠트 공간 플러그인은 Default 또는 User 프로젝트에 정의된 TS 플러그인을 재정의합니다. 즉, 명시적으로 필요하지 않은 경우 하위 프로젝트의 설정을 재정의하거나 변경하지 않는 것이 좋습니다.

그러나 부모 설정을 재정의하는 대신 <b>확장</b>하는 일부 설정이 있습니다. 가장 눈에 띄는 것은 이러한 설정이 라이브러리 경로 및 필터이기 때문에 항상 라이브러리를 재정의하는 대신 라이브러리에 더 많은 콘텐츠를 추가합니다. 또한 확장되는 별칭(상대 파일 경로에 대한 경로 키워드)이 있으며 중복이 정의되면 재정의합니다. 이를 통해 컨텐트 파일 경로 및 참조를 효과적으로 제어할 수 있습니다.

## 프로젝트 파일 내용

프로젝트 파일에는 다음 설정이 포함될 수 있습니다.

<b>3D 보기: </b>기본 셰이더, HDR 및 장면 상태 정의.

<b>별칭: </b>상대 경로에 대한 키워드 별칭입니다.

<b>굽기: </b>굽기 명명 규칙에 대한 설정입니다.

<b>일반: </b>그래프 템플릿, 접선 공간 플러그인, 표준 및 이미지 형식 기본값.

<b>라이브러리: </b>라이브러리에 표시할 경로를 확인했습니다.

<b>스크립팅: </b>콜백 스크립트 및 해석기.

<b>버전 제어: </b>Designer에 버전 제어를 통합하기 위한 설정.

## 프로젝트 파일 수정

다른 모든 형식과 마찬가지로 프로젝트 구성은 Designer UI 또는 외부 텍스트 편집기를 통해 수정할 수 있는 구조화된 XML 파일(<b>.sbsprj</b> 확장명 사용)로 저장됩니다.

## Substance 3D Designer 내부

프로젝트 파일 관리 및 프로젝트 설정 변경에 대해 자세히 알아보려면 [프로젝트 설정](../../interface/preferences-window/project-settings/project-settings.md) 페이지를 참고하십시오.

프로젝트 파일에는 [라이브러리](../../interface/the-library/the-library.md)에 대한 사용자 지정 <b>범주</b> 및 <b>필터</b>도 포함되어 있습니다. 자세한 내용은 [사용자 지정 콘텐츠 및 필터 관리](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) 페이지를 참조하세요.

## 외부에서 XML 편집

Windows의 경우 [메모장++](https://notepad-plus-plus.org)을(를) 사용하는 것이 좋습니다. macOS에서는 [Sublime Text](https://www.sublimetext.com/)이(가) 대안입니다. 즉, 적절한 들여쓰기, 섹션 축소 및 일부 형식의 구문 강조 표시가 있는 모든 편집기는 귀하의 삶을 훨씬 더 쉽게 만들 것입니다.

편집기에서 SBSPRJ 파일을 열면 UI의 탭에 해당하는 섹션이 있는 매우 단순한 구조의 레이아웃이 표시됩니다. 모든 설정이 여기에 문서화되지는 않는데, 이는 상당히 자명하기 때문이다.

![XML 편집](../../assets/project-xml.png "XML 편집")

## 상대 경로 및 별칭

앨리어스와 결합된 상대 경로는 프로젝트 구성에서 더 복잡하지만 가장 중요한 부분 중 하나이므로 이 섹션에서 이러한 부분을 자세히 설명합니다. 특정 프로젝트 파일에 대한 사용자 지정 별칭을 추가하는 작업은 [프로젝트 설정](../../interface/preferences-window/project-settings/project-settings.md)에서 수행됩니다.

여러 사용자의 PC에서 시스템의 다른 파일을 참조하는 파일의 주요 문제 중 하나는 절대 파일 경로가 작동하지 않는다는 것입니다. 사용자는 완전히 다른 위치에 SVN 저장소를 정의할 수 있습니다(예: C:/John/Gamedev/SubstanceLibrary 또는 D:/Dev/SubstanceLibrary). 이 문제를 해결하기 위해 별칭과 상대 경로가 함께 사용됩니다. 그렇지 않으면 다른 사용자의 파일을 열고 사용자가 로컬에서 가지고 있는 특정 위치에 사용된 사용자 정의 노드를 찾으려고 할 수 있습니다. 이러한 노드는 정확히 같은 방법으로 정의하지 않았을 수 있습니다.

<b>별칭</b>은 경로를 바꾸는 키워드입니다. 이 변수는 %TEMP%와 같은 Windows 환경 변수와 비슷하며, 자주 사용하는 경로를 한 단어로 대체한 다음 중앙에서 정의됩니다. 이 장점은 모든 영역에 단순화된 경로를 사용할 수 있으며 이 경로를 재배치할 때 한 번에 모든 참조를 수정할 수 있다는 것입니다.

>[!NOTE]
>
> **별칭 예**
> 
> | 앨리어스 | 실제 경로 값 |
> | --- | --- |
> | <b>sbs</b> | *C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages* |
> | <b>사용자 지정</b> | *D:\Dev\CustomProject\Substance* |
> 
> 기본 라이브러리는 기본적으로 *C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages*&#x200B;에 있으며 기본 콘텐츠를 사용하는 모든 그래프는 이 디렉터리를 참조합니다. 전체 경로를 참조하는 대신 &#39;<b>SBS</b>&#39;의 별칭(따옴표 제외)이 정의됩니다. 기본 라이브러리의 경우 SBS 경로의 정확한 값은 설치 시 사용자가 Designer에서 선택한 디렉터리로 설정됩니다.
> 
> 내부적으로 참조가 별칭이 있는 경로를 포함하는 경우 다음과 같은 방법으로 수정됩니다.
> 
> **C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages\blur\_hq.sbs => <b>sbs://</b>blur\_hq.sbs**

<b>상대 경로</b>는 항상 상대 경로가 정의된 파일에 상대적입니다. 즉, 구성 파일의 현재 위치에 따라 대부분의 경로가 결정되고 별칭 경로는 이러한 경로를 기반으로 하며 대부분 하위 폴더를 추가하는 방식으로 이루어집니다. <b>보려는 폴더 옆에 sbsprj 파일을 배치하는 것이 좋습니다!</b>

예를 들어, *CustomProject.sbsprj*&#x200B;를 포함하는 *C:/Versioncontrol/Substance/*&#x200B;의 리포지토리와 노드를 포함하는 두 개의 폴더 */Base* 및 */Tools,*&#x200B;을(를) 사용합니다.

Base 및 Tools에 대한 두 개의 상대 앨리어스를 정의하려면 SBSPRJ 파일 내에서 다음과 같이 수행됩니다.

### C:/Versioncontrol/Substance/CustomProject.sbsprj

```
   <urlaliases> 

    <size>2</size> 

    <_2 prefix="_"> 

     <path>file:Base</path> 

     <name>BaseAlias</name> 

    </_2> 

    <_1 prefix="_"> 

     <path>file:Tools</path> 

     <name>ToolsAlias</name> 

    </_1> 

   </urlaliases>
```


이 구성 파일의 결과는 다음과 같습니다.

**BaseAlias://**&#x200B;은(는) *C:/Versioncontrol/Tool/Base/*&#x200B;이 되고 **ToolsAlias://**&#x200B;은(는) *C:/Versioncontrol/Substance/Tools/.*&#x200B;이 됩니다.

*C:/Versioncontrol/Substance/*&#x200B;만 정의하면 경로가 파일 자체의 위치를 나타내는 점인 **&quot;file:.&quot;**(으)로 나열됩니다.
