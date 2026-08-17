---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/packaging-plugins.html"
breadcrumb-title: ''
description: 배포 및 설치를 위해 Substance 3D Designer용 Python 플러그인을 패키징하는 방법에 대해 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Packaging plugins
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 플러그인 패키징
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 3%

---


# 플러그인 패키징

## 플러그인 패키지 콘텐츠

패키지는 단일 파일로, 내부적으로 zip 보관 파일이며, 플러그인에 대한 메타데이터가 포함된 **pluginInfo.json** 파일이 포함되어 있습니다.

플러그인 코드 및 플러그인이 작동하는 데 필요한 기타 파일 또는 리소스.

**PluginInfo.json 항목:**

| 항목 | 설명 | 기본값 | 메모 |
| --- | --- | --- | --- |
| metadata\_format\_version | 메타데이터 파일의 형식입니다. | 1 | Required.Current는 1로 설정해야 합니다. |
| 이름 | 플러그인 이름입니다. |  | Required.플러그인 코드가 포함된 Python 모듈의 이름과 일치해야 합니다. |
| 버전 | 플러그인 버전. |  | 선택 사항입니다. |
| 작성자 | 플러그인 작성자입니다. |  | 선택 사항입니다. |
| email | 플러그인 작성자 전자 메일. |  | 선택 사항입니다. |
| min\_designer\_version | 플러그인이 작동하는 데 필요한 애플리케이션의 최소 버전입니다. | 2019.2 | 선택 사항입니다. |
| 플랫폼 | 플러그인이 실행되는 플랫폼 | any | 선택 사항입니다.컴파일된 코드를 포함하는 플러그인의 경우 이 항목을 사용하여 지원되지 않는 플랫폼에서 플러그인을 비활성화할 수 있습니다.가능한 값: win, linux, osx, any. |

## 새 플러그인 패키지 프로젝트 만들기

플러그인 패키지 프로젝트 만들기를 단순화하기 위해 [Cookiecutter](https://cookiecutter.readthedocs.io/en/latest/) 템플릿 프로젝트를 제공합니다.

직접 사용하거나 필요에 따라 수정할 수 있습니다.

이 템플릿은 응용 프로그램 디렉터리의 <b>plugins/tools/pkgplugintemplate</b>에서 찾을 수 있습니다.

1. <b>Python이 시스템에 아직 설치되어 있지 않은 경우 설치</b>

   Cookiecutter는 Python 2 및 Python 3과 모두 호환됩니다
1. <b>쿠키 큐터가 없는 경우 설치</b>

   일반적으로 pip를 사용하여 수행할 수 있습니다.

   ```
   pip install cookiecutter
   ```


   Cookiecutter를 설치하는 다른 방법이나 Cookiecutter에 대한 자세한 내용은 <https://cookiecutter.readthedocs.io/en/latest/installation.html>에서 설명서를 확인할 수 있습니다.
1. <b>새 플러그인 패키지 프로젝트 만들기</b>

   터미널 창에서 다음을 실행합니다.

   ```
   cookiecutter path/to/pkgplugintemplate -o path/to/new/project
   ```


   필요한 정보를 입력합니다. 새 프로젝트가 지정된 디렉터리에 만들어집니다.
1. <b>개발 완료 후 플러그인 패키징</b>

   터미널 창에서 다음을 실행합니다.

   ```
   python makepackage.py
   ```

1. 플러그인 패키지가 빌드 디렉터리에 생성됩니다.
