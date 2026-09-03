---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/interface/preferences-window/version-control.html"
breadcrumb-title: ''
description: Substance 3D Designer 환경 설정에서 버전 제어 설정을 구성하여 Git 및 기타 시스템과 통합합니다.
helpx_creative_field: ""
helpx_description: Designer > Interface > Preferences window > Version control
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 버전 관리
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---


# 버전 관리

>[!IMPORTANT]
>
> Substance 3D Designer 버전 <b>14.0.0</b>은(는) Perforce 지원을 <b>Python 3</b>(으)로 업그레이드합니다.
> 
> 다른 스크립트 및 버전 제어 환경이 그에 따라 조정되었는지 확인합니다.

Designer은 [Perforce](https://www.perforce.com/)&#x200B;(P4) 버전 제어 시스템의 Python 통합을 제공합니다.

통합은 [탐색기](../../../interface/the-explorer-window/the-explorer-window.md)의 패키지 상황별 메뉴에 사용자 정의 &#39;버전 제어&#39; 하위 메뉴와 P4의 패키지 상태에 맞는 사용자 정의 아이콘을 추가합니다.

## P4 준비 중

[P4V](https://www.perforce.com/products/helix-core-apps/helix-visual-client-p4v)에서 아래와 같이 작업 영역 이름과 경로를 기록해 두십시오.

![P4V 작업 영역 정보](version-control.resources/version-control-01.jpg "P4V 작업 영역 정보"){zoomable="yes"}

텍스트 편집기 또는 IDE에서 Designer 설치 &#39;*tools/version\_control/perforce.py*&#39;에 있는 이 스크립트를 엽니다.

19행에서 시스템에서 <b>&#39;p4&#39; 실행 파일</b>의 위치에 대한 경로를 편집합니다.\
아래 예제에서 이 경로는 &#39;*c:/Program Files/Perforce/p4.exe*&#39;입니다.

```
## Editable variables

cPerforceP4AbsPath = os.path.abspath("c:/Program Files/Perforce/p4.exe")

cVerbose = False
```


## Designer에서 설정

Designer의 [환경 설정](../../../interface/preferences-window/preferences-window.md)에서 사용할 수 있는 [프로젝트 설정](../../../interface/preferences-window/project-settings/project-settings.md)에 버전 제어가 구성되어 있습니다.

프로젝트 설정의 ![&#39;버전 제어&#39; 탭](version-control.resources/version-control-02.jpg " 프로젝트 설정의 &#39;버전 제어&#39; 탭"){zoomable="yes"}

1. &#39;편집 > 환경 설정&#39;으로 이동
1. &#39;프로젝트&#39;로 이동하고 대상 [프로젝트 파일](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)을 선택한 다음 &#39;버전 제어&#39; 탭으로 이동합니다.
1. &#39;버전 제어 사용&#39; 확인
1. &#39;작업 영역&#39; 섹션에서 다음 정보를 입력합니다.

   * <b>이름:</b> P4V에서 이전에 검색한 &#39;작업 영역 이름&#39;을 입력하십시오.
   * <b>경로:</b> P4V에서 이전에 검색한 &#39;작업 영역 경로&#39;를 입력하십시오.

Designer에서 ![P4 설정: 작업 영역](version-control.resources/version-control-03.jpg "Designer에서 P4 설정: 작업 영역"){zoomable="yes"}

### 동작 설정

작업은 탐색기에 있는 패키지의 컨텍스트 메뉴에서 사용할 수 있습니다. 대부분의 버전 제어 도구 개념과 일치하는 미리 정의된 동작이 있습니다.

* 모든 작업 레이블은 필요에 따라 변경할 수 있습니다.
* 모든 액션을 사용하려면 스크립트가 필요합니다.

다음을 사용할 수 있습니다.

* 스크립트 *per* 작업 1개
* *모두* 작업에 대한 스크립트 1개

모든 액션에 대한 시작 스크립트는 Designer의 설치에서 사용할 수 있습니다. &#39;*tools/version\_control/perforce.py*&#39;.

>[!IMPORTANT]
>
> 사용할 수 있으려면 패키지를 &#39;작업 영역 경로&#39; 아래(예: &#39;*f:/Dev/perforce*&#39; 아래)에 저장해야 합니다.

1. <b>작업</b> 그룹에서 <b>추가</b> 작업의 &#39;...&#39; 단추를 클릭합니다.
1. Designer 설치에서 다음 스크립트를 선택합니다. &#39;*tools/version\_control/perforce.py*&#39;
1. 다른 모든 액션에 대해 스크립트가 자동으로 설정되어야 합니다.

Designer에서 ![P4 설정: 작업](version-control.resources/version-control-04.jpg "Designer에서 P4 설정: 작업"){zoomable="yes"}

### 사용자 정의 동작 설정

모든 버전 제어 도구는 서로 다르며 많은 기능을 포함하고 있으므로 사용자가 사용자 정의 동작을 추가할 수 있습니다.

1. &#39;항목 추가&#39; 클릭
1. 새 액션의 레이블을 채우고 스크립트 경로를 설정합니다

### 스크립트 인터프리터 설정

1. &#39;해석기&#39; 섹션에서 &#39;항목 추가&#39;를 클릭합니다.
1. 스크립트 파일 확장자 또는 접미어 및 인터프리터 실행 파일의 경로를 설정합니다
1. perforce.py 스크립트를 편집하여 &#39;p4&#39; 바이너리의 위치를 업데이트합니다.

Designer에서 ![P4 설정: 인터프리터](version-control.resources/version-control-05.jpg "Designer에서 P4 설정: 인터프리터"){zoomable="yes"}

## 버전 제어 사용 방법

1. 새 패키지 만들기
1. 패키지를 &#39;작업 영역 경로&#39; 디렉터리에 저장
1. 패키지의 RMB를 클릭합니다. 이제 &#39;버전 제어&#39; 하위 메뉴에 액세스할 수 있습니다.
1. 작업 영역에 있는 패키지 파일의 상태에 따라 다음과 같은 몇 가지 작업을 수행할 수 있습니다.

   * <b>추가:</b> 파일을 &#39;ToAdd&#39;로 표시
   * <b>제출:</b> 선택한 패키지를 제출합니다. 이 작업은 변경 메시지(아래 참조)를 지정하는 대화 상자를 표시합니다.
   * <b>되돌리기:</b> 수정 내용을 되돌립니다. 이 작업은 복구할 파일을 선택하는 대화 상자를 표시합니다(아래 참조).
   * <b>체크 아웃:</b> 저장소에서 파일을 확인하십시오.
   * <b>마지막 버전 가져오기:</b> 저장소에서 최신 버전 검색
   * <b>새로 고침 상태:</b> 패키지 파일 상태 새로 고침

   <table>
   <tr style="border: 0;">
   <td style="border: 0;" valign="top">

   ![&#39;Submit&#39; 대화 상자](version-control.resources/version-control-06.jpg "&#39;Submit&#39; 대화 상자"){zoomable="yes"}

   </td>
   <td style="border: 0;" valign="top">

   ![&#39;되돌리기&#39; 대화 상자](version-control.resources/version-control-07.jpg "&#39;되돌리기&#39; 대화 상자"){zoomable="yes"}

   </td>
   </tr>
   </table>

>[!NOTE]
>
> 모든 동작이 다중 선택을 지원합니다.
> 
> 읽기 전용 파일 권한을 사용하여 수정 사항을 제한하는 P4 및 기타 버전 제어 도구의 경우 사용자는 패키지를 수정하기 전에 먼저 체크아웃해야 합니다.
> 
> 읽기 전용 패키지 파일은 SD에서 수정할 수 없습니다.

패키지에는 상태에 따라 다음과 같은 아이콘이 있습니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![패키지 아이콘: 최신](version-control.resources/version-control-08.png "패키지 아이콘: 최신")

최신

</td>
<td style="border: 0;" valign="top">

![패키지 아이콘: 체크 아웃됨](version-control.resources/version-control-09.png "패키지 아이콘: 체크 아웃됨")

체크 아웃됨

</td>
<td style="border: 0;" valign="top">

![패키지 아이콘: 추가됨](version-control.resources/version-control-10.png "패키지 아이콘: 추가됨")

추가 대상으로 표시됨

</td>
<td style="border: 0;" valign="top">

![패키지 아이콘: 저장소에 없음](version-control.resources/version-control-11.png "패키지 아이콘: 저장소에 없음")

서비스 센터에 없음

</td>
</tr>
</table>

최신 상태가 아닌 패키지는 경고 표시로 표시됩니다.

## 액션 스크립트

각 액션에 의해 실행되는 명령은 다음과 같이 구성됩니다.

my\_script <b>*WorkspaceName WorkspacePath ActionName[ActionArgs]*</b>

<b>작업 영역 이름:</b> 작업 영역의 이름

<b>작업 영역 경로:</b> 작업 영역의 루트 디렉터리 경로

<b>ActionName:</b> 동작 이름:

* &quot;추가&quot; 작업에 대한 *추가:*
* &quot;체크 아웃&quot; 작업에 대한 *체크 아웃:*
* &quot;제출&quot; 작업에 대한 *제출:*
* &quot;되돌리기&quot; 작업에 대한 *되돌리기:*
* &quot;마지막 버전 가져오기&quot; 작업에 대한 *get\_last\_version:*
* &quot;상태 가져오기&quot; 작업에 대한 *가져오기\_상태:*

레이블은 프로젝트 설정에서 &#39; &#39; 문자가 &#39;\_&#39;로 대체되어 설정됩니다(예: &quot;My Action&quot; => &quot;My\_Action&quot;).

동작의 <b>ActionArgs:</b> 인수:

* *-desc*: &#39;Submit&#39; 작업에 사용되는 설명 문자열입니다.
* *-파일:* 파일 목록
* *-files\_list:* 줄당 파일 목록이 포함된 텍스트 파일입니다.

<b>get\_status</b>: 지정한 파일의 상태에 따라 값을 반환합니다.

* 0: 정의되지 않은 상태
* 1: 창고에 없음
* 2: 이전 버전(최신 버전 아님)
* 3: 최신 버전(최신)
* 4: 체크 아웃됨
* 5: 추가용으로 표시됨
* 기타 액션:
  * 0: 성공
  * 기타: 오류
