---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/pipeline-and-project-configuration/configuration-list-sbscfg.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 SBSCFG 구성 목록을 사용하여 프로젝트 설정 및 사전 설정을 관리하는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Configuration List - SBSCFG
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 구성 목록 - SBSCFG
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# 구성 목록 - SBSCFG

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

구성 파일은 프로젝트 목록과 엔진 호환성 모드만 포함하므로 [프로젝트 구성 파일](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)보다 훨씬 간단합니다. 단일 프로젝트 파일보다 상위 수준의 프로젝트/환경 구성 목록으로 사용됩니다.

서로 다른 환경에 대해 여러 구성을 가질 수 있으며, 이러한 파일은 SBSPRJ 파일과 함께 버전 제어 하에 유지할 수 있습니다.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![SBSCFG 파일 아이콘](../../assets/sbscfg.png "SBSCFG 파일 아이콘")

</td>
</tr>
</table>

## 구성 파일 수정

이러한 파일은 간단하지만 SBSPRJ 파일과 마찬가지로 두 가지 방법으로 수정할 수 있습니다.

### 프로젝트 설정에서

강조 표시된 섹션은 구성 파일과 관련된 부분으로, 위에서 정의한 SBSCFG 파일에 저장된 목록에 더 많은 프로젝트를 추가하기만 하면 됩니다.

![프로젝트 설정](../../assets/config-ui.png "프로젝트 설정")

### XML로 외부 편집

Windows <b>Notepad++</b>의 경우 무료 옵션이며, macOS <b>Sublime Text</b>이(가) 대안입니다. 그러나 적절한 들여쓰기, 섹션 축소 및 일부 형식의 구문 강조 표시가 있는 모든 편집기는 사용자의 라이프를 훨씬 쉽게 만듭니다.

편집기에서 SBSCFG 파일을 열면 UI에 해당하는 섹션이 있는 매우 간단한 구조의 레이아웃이 표시됩니다.

```
<?xml version="1.0" encoding="UTF-8"?> 

<root> 

 <projects> 

  <projectfiles> 

   <size>1</size> 

   <_1 prefix="_"> 

    <path>custom_project.sbsprj</path> 

   </_1> 

  </projectfiles> 

 </projects> 

 <preferences> 

  <configuration> 

   <compatibilitymode>sbs_engine_v6</compatibilitymode> 

  </configuration> 

 </preferences> 

</root>
```


기본 프로젝트와 사용자 프로젝트는 명시적으로 나열되지 않으며 추가 프로젝트는 이러한 프로젝트 다음에 정의됩니다.

위의 예제에서는 [상대 경로](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)도 사용합니다. 상대 경로에 대한 논리는 CFG와 PRJ 파일 간에 약간 다릅니다. CFG 파일의 경우 위와 같이 **경로 앞에 &quot;file:/&quot;를 입력하면 안 됩니다**. 대신 경로는 CFG 파일이 정의된 위치에 추가됩니다.

## 기본 라이브러리 제거

지금은 기본 라이브러리를 제거할 수 없습니다. Designer의 기능이 많이 떨어지므로 이렇게 하는 것은 좋지 않을 수 있습니다.
