---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/pipeline-and-project-configuration/retrieving-the-installation-path.html"
breadcrumb-title: ''
description: 스크립팅 및 자동화를 위해 Substance 3D Designer 설치 경로를 검색하는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Retrieving the installation path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 설치 경로 검색
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 6%

---


# 설치 경로 검색

이 페이지에서는 버전 및 플랫폼에 따라 [Substance 3D Designer](https://www.adobe.com/kr/products/substance3d-designer.html)의 설치 경로를 검색하는 방법에 대한 정보를 다시 그룹화합니다.

## Windows

### Creative Cloud 데스크톱

1. <b>Windows 레지스트리 편집기</b> 열기(regedit)
1. 레지스트리 키로 이동합니다. <b>HKEY\_LOCAL\_MACHINE\Software\Microsoft\Windows\CurrentVersion\App 경로\&lt;/b>
1. 이름이 <b>Adobe Substance 3D Designer.exe</b>인 하위 키를 엽니다.
1. 키 값에는 키가 설치된 응용 프로그램 실행 파일의 경로가 포함됩니다

>[!NOTE]
>
> 이 레지스트리 키는 버전 11.2 이후에만 사용할 수 있습니다.\
> 이전 버전의 경우 HKEY\_CURRENT\_USER\Software\Microsoft\Windows\CurrentVersion\ Explorer\FileExts의 파일 연결에서 설치 경로를 검색할 수 있습니다.

### Substance 에디션(독립 실행형)

1. <b>Windows 레지스트리 편집기</b> 열기(regedit)
1. 레지스트리 키로 이동합니다. <b>HKEY\_LOCAL\_MACHINE\ SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall</b>
1. 응용 프로그램 버전의 <b>AppID</b>과(와) 일치하는 하위 키를 찾습니다(아래 표 참조)
1. 키 값에는 응용 프로그램 설치 위치에 대한 경로가 포함됩니다

| 버전 | AppId |
| --- | --- |
| **버전 5.x** | {25E7D16D-1FBA-49EA-BF36-E2D6B20A9206} |
| **버전 6.x** | {09a302b1-8da8-4f62-b0cb-a208faa210f9} |
| **버전 7.x(2017.x) - 11.1** | {e9e3d6d9-3023-41c7-b223-11d8fdd691b9} |
| **버전 11.2 이상** | {662bb79f-5616-44e6-a84d-b3d6abebe002} |

### Steam 에디션

어플리케이션은 Steam 설치 폴더의 stamp/common/sub-folder에 설치된다.

## macOS

Mac에서 애플리케이션은 다음 위치에 설치됩니다.

| 버전 | 경로 |
| --- | --- |
| **11.2 이상** | **/Applications/Adobe Substance 3D Designer.app** |
| **레거시** | **/Applications/Substance Designer.app** |

## 리눅스

Linux에서 rpm 패키지는 다음 경로에 설치됩니다.

| 버전 | 경로 |
| --- | --- |
| **11.2 이상** | **/opt/Adobe/Adobe\_Substance\_3D\_Designer** |
| **레거시** | **/opt/Allegorithmic/Substance\_Designer** |
