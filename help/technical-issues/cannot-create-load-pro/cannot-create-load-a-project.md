---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/cannot-create-load-a-project.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 프로젝트를 만들거나 로드하는 데 발생하는 문제를 해결하고 해결 방법을 찾아보십시오.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Cannot createload a project
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 프로젝트를 만들 수 없습니다.
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 0%

---


# 프로젝트를 생성/로드할 수 없음

이 페이지에서는 Substance 3D Designer에서 프로젝트를 만들거나 로드하지 못하는 일반적인 원인을 나열하고 각각에 대한 문제 해결 단계를 제공합니다.

## 애플리케이션이 너무 오래되어 URL을 열 수 없습니다.

**![(오류)](../../assets/error.svg) 문제**

**Substance 3D 파일(SBS)**&#x200B;은 *해당 형식을 지원하지 않는* 버전의 Substance 3D Designer에서 로드되고 있습니다. Substance 3D 파일은 이러한 파일에 대해 업데이트된 형식을 사용하는 소프트웨어의 *최신 버전*&#x200B;에 저장되었을 수 있습니다.

**![(틱)](../../assets/check.svg) 권장 단계**

Substance 3D Designer이 발전함에 따라 Substance 3D 파일 형식(SBS)도 발전합니다. 새로운 버전의 소프트웨어가 최신 기능을 지원할 수 있도록 *파일을 업데이트*&#x200B;해야 하는 경우가 많습니다.

새 버전에서 *처음으로 파일을 로드*&#x200B;할 때 *이 업데이트를 수행하라는 메시지*&#x200B;가 표시됩니다.

>[!WARNING]
>
> 업데이트가 적용된 *후* 파일이 저장되면 형식 버전도 변경됩니다. 이 시점에서 Substance 3D Designer의 *이전 버전에서 더 이상 로드할 수 없습니다*.
> 
> 이 제한은 [Substance Player](https://helpx.adobe.com/substance-3d-player/home.html)에도 적용됩니다.

먼저 현재 라이선스에서 허용하는 최신 버전의 Substance 3D Designer을 사용하고 있는지 확인하십시오. 다음은 각 에디션의 업데이트에 대한 액세스 포인트입니다.

* <b>Substance 3D 구독 Adobe:</b> [Adobe Creative Cloud 데스크탑](https://creativecloud.adobe.com/en/apps/download/creative-cloud) 응용 프로그램의 앱 탭에 있는 업데이트 섹션으로 이동
* <b>[Substance3d.com](http://Substance3d.com) 구독:</b> Substance 3D Designer에 메시지가 표시되면 업데이트하거나, [Substance3d.com](http://substance3d.com) 웹 사이트의 [내 라이선스](https://store.substance3d.com/user) 섹션에서 최신 설치 관리자를 다운로드하십시오.
* <b>Steam:</b> 응용 프로그램이 기본적으로 자동 업데이트됩니다. Substance 3D Designer을 시작하거나 다운로드 화면으로 이동하여 업데이트를 수동으로 트리거할 수 있습니다

>[!WARNING]
>
> 업데이트된 파일을 저장하기 *전에*&#x200B;이전 버전의 Substance 3D Designer에서 파일을 로드할 필요가 없는지 확인합니다.
> 
> 또는 새 버전의 Substance 3D Designer에서 파일을 로드하기 *전에* 파일의 *복사본을 만들기*&#x200B;할 수 있으므로 이전 버전의 소프트웨어를 사용해야 하는 경우 언제든지 다시 돌아갈 수 있습니다.

## 프로젝트를 만들거나 로드할 때 충돌 발생

<b>![(오류)](../../assets/error.svg) 문제</b>

[3D 보기](../../interface/3d-view/3d-view.md)를 초기화하는 동안 오류가 발생하여 프로젝트를 만들거나 로드할 때 충돌이 발생하는 경우가 많습니다. 이 오류는 작업 영역을 설정할 때 발생합니다.

시스템이 랩톱인 경우 타사 응용 프로그램이 3D 보기에서 시스템 GPU를 사용하지 못하도록 하는 *전원 관리 계획*&#x200B;을 적용할 수 있습니다. 이로 인해 다른 GPU 장치가 그 자리에서 작업을 수행할 수 없는 경우 충돌이 발생할 수 있습니다.

세션 간에 *표시 구성 또는 크기 조정*&#x200B;이 변경되어 3D 보기 렌더링 프레임이 잘못된 좌표에서 만들어지는 경우에도 충돌이 발생할 수 있습니다.

<b>![(틱)](../../assets/check.svg) 권장 단계</b>

이 충돌의 가능한 여러 원인을 고려할 때 다음 문제 해결 단계를 순서대로 수행하는 것이 좋습니다.

그래픽 드라이버 업데이트

먼저 그래픽 드라이버가 최신 상태인지 확인하십시오. GPU의 최신 버전은 [여기](https://www.nvidia.com/Download/index.aspx?lang=en-us)&#x200B;(NVIDIA), [여기](https://www.amd.com/en/support)&#x200B;(AMD) 또는 [여기](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)&#x200B;(Intel)입니다.

최고 성능 강제 적용

특히 시스템이 노트북인 경우 시스템의 *전원 플랜*&#x200B;을 관리하는 소프트웨어(예: ASUS Armory Crate)를 찾습니다.

일부 전원 관리 애플리케이션은 시스템 GPU에 대한 다른 애플리케이션의 액세스를 제한하거나 GPU의 성능을 방해하여 충돌이 발생할 수 있습니다. 전원 관리 애플리케이션이 있고 활성 상태이면 최상의 성능을 제공하는 플랜으로 전환하십시오.

개별 GPU를 사용하여 강제 실행

시스템에 *전환 가능한 그래픽*&#x200B;이 있는 경우 Substance 3D 응용 프로그램에 추가 설치형 GPU(dGPU)를 사용하도록 하는 것이 좋습니다.

대부분의 경우 GPU 설정을 제어하는 전용 응용 프로그램에서 실행됩니다. 예를 들어 NVIDIA GPU의 경우 &#39;NVIDIA 제어판&#39; 응용 프로그램에서 이 작업을 수행할 수 있습니다.

레지스트리에 저장된 사용자 인터페이스 재설정

디스플레이 구성 또는 비율 변경으로 인해 충돌이 발생한 경우 Designer에서 사용자 인터페이스를 완전히 재설정하기 위해 기존 레지스트리 항목을 삭제할 수 있습니다. 다른 설정도 포함됩니다.

운영 체제별로 이 재설정을 수행하는 절차는 다음과 같습니다.

+++Windows
* Designer 닫기

Designer 닫기

* <b>명령 프롬프트</b> 응용 프로그램 열기

<b>명령 프롬프트</b> 응용 프로그램 열기

* 다음 명령을 입력하고 <b>Enter</b>를 누릅니다.

  <b>Creative Cloud 데스크톱</b>

  ```
  reg delete "HKEY_CURRENT_USER\Software\Adobe\Adobe Substance 3D Designer" /f
  ```


  <b>Steam/Substance 에디션</b>

  ```
  reg delete "HKEY_CURRENT_USER\Software\Allegorithmic\Substance Designer" /f
  ```


다음 명령을 입력하고 <b>Enter</b>를 누릅니다.

<b>Creative Cloud 데스크톱</b>

<b>Steam/Substance 에디션</b>

* 시스템에서 두 번째 모니터의 연결을 끊고 다시 연결합니다(*연결되지 않은* 경우 이 단계를 무시합니다).

시스템에서 두 번째 모니터의 연결을 끊고 다시 연결합니다(*연결되지 않은* 경우 이 단계를 무시합니다).

* Designer을 시작하되 프로젝트를 만들거나 열지 *마십시오*

Designer을 시작하되 프로젝트를 만들거나 열지 *마십시오*

* 상단 표시줄에서 <b>Windows</b> 메뉴를 열고 <b>새 3D 보기</b> 옵션을 선택합니다

상단 표시줄에서 <b>Windows</b> 메뉴를 열고 <b>새 3D 보기</b> 옵션을 선택합니다

* <b>3D 보기</b>가 올바르게 초기화되었는지 확인하고 패널 상단 표시줄의 <b>장면</b> 메뉴에서 다른 미리 보기 메시를 사용해 보세요.

<b>3D 보기</b>가 올바르게 초기화되었는지 확인하고 패널 상단 표시줄의 <b>장면</b> 메뉴에서 다른 미리 보기 메시를 사용해 보세요.

* 재질 만들기 또는 열기

재질 만들기 또는 열기

+++

+++macOS
* Designer 닫기

Designer 닫기

* <b>터미널</b> 응용 프로그램 열기

<b>터미널</b> 응용 프로그램 열기

* 다음 명령을 입력하고 <b>Enter</b>를 누릅니다.

  <b>Creative Cloud 데스크톱</b>

  ```
  rm ~/Library/Preferences/com.adobe.Adobe\ Substance\ 3D\ Designer.plist
  ```


  <b>Steam/Substance 에디션</b>

  ```
  rm ~/Library/Preferences/com.allegorithmic.Substance\ Designer.plist
  ```


다음 명령을 입력하고 <b>Enter</b>를 누릅니다.

<b>Creative Cloud 데스크톱</b>

<b>Steam/Substance 에디션</b>

* 시스템에서 두 번째 모니터의 연결을 끊고 다시 연결합니다(*연결되지 않은* 경우 이 단계를 무시합니다).

시스템에서 두 번째 모니터의 연결을 끊고 다시 연결합니다(*연결되지 않은* 경우 이 단계를 무시합니다).

* Designer을 시작하되 프로젝트를 만들거나 열지 *마십시오*

Designer을 시작하되 프로젝트를 만들거나 열지 *마십시오*

* 상단 표시줄에서 <b>Windows</b> 메뉴를 열고 <b>새 3D 보기</b> 옵션을 선택합니다

상단 표시줄에서 <b>Windows</b> 메뉴를 열고 <b>새 3D 보기</b> 옵션을 선택합니다

* <b>3D 보기</b>가 올바르게 초기화되었는지 확인하고 패널 상단 표시줄의 <b>장면</b> 메뉴에서 다른 미리 보기 메시를 사용해 보세요.

<b>3D 보기</b>가 올바르게 초기화되었는지 확인하고 패널 상단 표시줄의 <b>장면</b> 메뉴에서 다른 미리 보기 메시를 사용해 보세요.

* 재질 만들기 또는 열기

재질 만들기 또는 열기

+++
